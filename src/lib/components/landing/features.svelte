<script lang="ts">
  const features = [
    {
      title: 'Clear positioning',
      text: 'Your product message lands fast with a headline, subtext, and direct CTA.'
    },
    {
      title: 'Professional layout',
      text: 'Navbar, hero, features, and footer are separated cleanly for a polished flow.'
    },
    {
      title: 'SVG-only visuals',
      text: 'No emoji, no icon packs, just custom SVG shapes that look intentional.'
    },
    {
      title: 'Conversion focused',
      text: 'Every section keeps attention on ClawFish.ai and the launch path.'
    }
  ];
</script>

<section id="features" class="bg-linear-to-b from-black to-slate-950 px-6 md:px-10 py-24 md:py-32">
  <div class="mx-auto max-w-7xl">
    <div class="max-w-2xl">
      <p class="text-sm font-semibold uppercase tracking-[0.35em] text-orange-300/80">Features</p>
      <h2 class="mt-4 text-4xl font-black tracking-tight text-white md:text-5xl">
        Built for a sharper first impression.
      </h2>
      <p class="mt-5 text-base leading-7 text-slate-300 md:text-lg">
        The page stays dark, premium, and direct, so the message feels deliberate instead of noisy.
      </p>
    </div>

    <div class="mt-14 grid gap-6 md:grid-cols-2 xl:grid-cols-4">
      {#each features as feature}
        <article class="group rounded-3xl border border-white/8 bg-white/5 p-7 backdrop-blur-sm transition duration-300 hover:-translate-y-1 hover:border-orange-500/30 hover:bg-orange-500/8">
          <svg class="h-12 w-12 text-orange-400" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
            <circle cx="24" cy="24" r="19" stroke="currentColor" stroke-width="2.5" opacity="0.35"/>
            <path d="M14 25L21 32L35 17" stroke="currentColor" stroke-width="3.2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>

          <h3 class="mt-6 text-2xl font-bold text-white">{feature.title}</h3>
          <p class="mt-4 text-base leading-7 text-slate-300">{feature.text}</p>
        </article>
      {/each}
    </div>
  </div>
</section>