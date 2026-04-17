<script lang="ts">
  const links = [
    { href: '#pricing', label: 'Pricing' },
    { href: '#platform', label: 'Platform' },
    { href: '#meet', label: 'Meet Clawfish' }
  ];
</script>

<nav class="sticky top-0 z-50 border-b border-white/5 bg-black/80 backdrop-blur-md">
  <div class="mx-auto flex h-16 max-w-7xl items-center justify-between px-4">
    <a href="/" class="flex items-center gap-3">
      <div class="logo-mark">C</div>
      <div class="leading-tight">
        <div class="text-sm font-semibold tracking-[0.24em] text-white">CLAWFISH</div>
        <div class="text-[11px] text-white/40">AI AGENT SYSTEM</div>
      </div>
    </a>

    <div class="hidden items-center gap-6 sm:flex sm:gap-8 text-sm text-white/60">
      {#each links as link}
        <a href={link.href} class="transition-colors hover:text-white">{link.label}</a>
      {/each}

      <a
        href="/app"
        class="rounded-full border border-orange-500/30 bg-orange-500/10 px-4 py-2 font-medium text-orange-300 transition hover:bg-orange-500/20 hover:text-white"
      >
        Try Clawfish
      </a>
    </div>
  </div>
</nav>