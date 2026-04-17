<script lang="ts">
  import "./layout.css";

  let { children } = $props();
</script>

<div class="min-h-screen bg-[#050505] text-slate-200 selection:bg-cyan-500/30">
  
  <nav class="sticky top-0 z-50 border-b border-white/5 bg-[#050505]/80 backdrop-blur-md">
    <div class="mx-auto flex h-16 max-w-7xl items-center justify-between px-4">
      <div class="flex items-center gap-2">
        <div class="flex h-8 w-8 items-center justify-center rounded bg-gradient-to-br from-cyan-400 to-blue-600 font-bold text-white">
          C
        </div>
        <span class="text-xl font-semibold tracking-tight">ClawFish<span class="text-cyan-400">.ai</span></span>
      </div>

      <div class="hidden gap-8 text-sm font-medium text-slate-400 md:flex">
        <a href="/" class="hover:text-white transition-colors">Home</a>
        <a href="/platform" class="hover:text-white transition-colors">Platform</a>
        <a href="https://github.com/ClawFish-Labs" class="hover:text-white transition-colors">GitHub</a>
      </div>

      <button class="rounded-full bg-white px-5 py-2 text-sm font-semibold text-black hover:bg-slate-200 transition-all active:scale-95">
        Launch App
      </button>
    </div>
  </nav>

  <main>
    {@render children()} 
    </main>

</div>