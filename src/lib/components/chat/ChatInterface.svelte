'<script lang="ts">
  import { onMount } from 'svelte';
  import { messages } from '$lib/stores/appStore.js';
  import Sidebar from './sidebar.svelte';
  import MessageBubble from './MessageBubble.svelte';
  import Icons from './ui/icons.svelte';
  import { createMessage } from '$lib/logic/clawLibrary';
  import { normalizeMessage } from '$lib/logic/clawCore';

  let textarea: HTMLTextAreaElement;
  let composing = false;
  let pending = false;

  async function sendMessage() {
    const text = textarea.value.trim();
    if (!text || pending) return;

    const userMsg = createMessage('user', text);
    textarea.value = '';
    composing = false;
    pending = true;

    messages.update(msgs => [...msgs, userMsg]);

    try {
      const response = await fetch('/api/chat', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ text })
      });

      const data = await response.json();
      if (data.reply) {
        const assistantMsg = createMessage('assistant', data.reply);
        messages.update(msgs => [...msgs, assistantMsg]);
      }
    } catch (error) {
      console.error('Chat error:', error);
      messages.update(msgs => [...msgs, createMessage('assistant', 'Sorry, something went wrong. Try again.')]);
    }

    pending = false;
  }

  function handleKeydown(e: KeyboardEvent) {
    if (e.key === 'Enter' && !e.shiftKey && !pending) {
      e.preventDefault();
      sendMessage();
    }
  }

  $: if (textarea && !composing) {
    textarea.style.height = 'auto';
    textarea.style.height = Math.min(Math.max(textarea.scrollHeight, 48), 160) + 'px';
  }
</script>

<div class="flex min-h-screen bg-black text-slate-200">
  <Sidebar />

  <main class="flex min-w-0 flex-1 flex-col">
    <header class="flex h-16 items-center justify-between border-b border-white/10 px-4 sm:px-6">
      <div>
        <div class="text-sm font-semibold text-white">ClawFish Chat</div>
        <div class="text-xs text-white/40">Shell interface</div>
      </div>

      <div class="flex items-center gap-3">
        <div class="rounded-full border border-orange-500/20 bg-orange-500/10 px-3 py-1 text-xs text-orange-200">Beta</div>
        <button class="rounded-full border border-white/10 px-4 py-2 text-sm text-white transition hover:bg-white/5">
          <Icons name="settings" />
        </button>
      </div>
    </header>

    <section class="flex-1 overflow-y-auto px-4 py-6 sm:px-6">
      <div class="mx-auto flex w-full max-w-4xl flex-col gap-6">
        <div class="rounded-3xl border border-white/10 bg-white/3 p-6">
          <h1 class="text-3xl font-semibold tracking-tight text-white sm:text-4xl">Chat with ClawFish.</h1>
          <p class="mt-3 max-w-2xl text-sm leading-6 text-white/55">
            Send a message to get started.
          </p>
        </div>

        <div class="flex flex-wrap gap-3">
          <button class="rounded-full border border-white/10 bg-black/40 px-4 py-2 text-sm text-white/70 transition hover:border-orange-500/30 hover:bg-orange-500/10 hover:text-orange-200">
            Plan a feature
          </button>
          <button class="rounded-full border border-white/10 bg-black/40 px-4 py-2 text-sm text-white/70 transition hover:border-orange-500/30 hover:bg-orange-500/10 hover:text-orange-200">
            Write code
          </button>
          <button class="rounded-full border border-white/10 bg-black/40 px-4 py-2 text-sm text-white/70 transition hover:border-orange-500/30 hover:bg-orange-500/10 hover:text-orange-200">
            Debug issue
          </button>
        </div>

        <div class="space-y-4">
          {#each $messages as message}
            <MessageBubble role={message.role} text={message.text} />
          {/each}
        </div>
      </div>
    </section>

    <footer class="border-t border-white/10 bg-[#050505] px-4 py-4 sm:px-6">
      <div class="mx-auto flex max-w-4xl items-end gap-3 rounded-3xl border border-white/10 bg-white/3 p-3">
        <textarea
          bind:this={textarea}
          bind:value={textarea}
          rows="1"
          placeholder="Message ClawFish..."
          class="max-h-40 min-h-[48px] flex-1 resize-none bg-transparent px-2 py-3 text-sm text-white placeholder:text-white/35 outline-none"
          on:input={() => composing = true}
          on:keydown={handleKeydown}
        ></textarea>
        <button
          disabled={pending}
          on:click={sendMessage}
          class="rounded-2xl bg-orange-500 px-5 py-3 text-sm font-semibold text-black transition hover:bg-orange-400 disabled:opacity-50"
          class:cursor-not-allowed={pending}
        >
          <Icons name="send" />
        </button>
      </div>
    </footer>
  </main>
</div>