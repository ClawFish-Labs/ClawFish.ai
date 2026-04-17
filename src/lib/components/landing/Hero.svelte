<section class="mx-auto grid min-h-[85vh] max-w-7xl gap-12 px-4 py-24 lg:grid-cols-[1.05fr_0.95fr] lg:items-center">
  <div class="max-w-3xl">
    <div class="reveal-pill mb-6 inline-flex items-center gap-2 rounded-full border border-orange-500/20 bg-orange-500/5 px-4 py-2 text-xs text-orange-300">
      Lightweight web frame for Clawfish Labs
    </div>

    <h1 class="reveal-title text-5xl font-semibold tracking-tight text-white sm:text-6xl lg:text-7xl">
      Meet
      <span class="text-orange-400">ClawFish</span>.
    </h1>

    <p class="reveal-copy mt-6 max-w-2xl text-base leading-7 text-white/60 sm:text-lg">
      A minimal AI agent shell with a dark interface, orange energy, and room to grow without bloating the stack.
    </p>

    <div class="reveal-actions mt-10 flex flex-wrap gap-4">
      <a href="/platform" class="rounded-full bg-orange-500 px-6 py-3 text-sm font-semibold text-black transition hover:bg-orange-400">
        Open Platform
      </a>
      <a href="#features" class="rounded-full border border-white/10 px-6 py-3 text-sm font-semibold text-white transition hover:border-white/20 hover:bg-white/5">
        View Features
      </a>
    </div>
  </div>

  <div class="relative flex justify-center lg:justify-end">
    <div class="globe-hologram">
      <div class="globe-halo"></div>
      <div class="globe-scanlines"></div>

      <div class="globe-shell">
        <svg viewBox="0 0 820 820" class="globe-svg" aria-hidden="true">
          <defs>
            <radialGradient id="earthFill" cx="38%" cy="30%" r="62%">
              <stop offset="0%" stop-color="#241609" stop-opacity="0.95" />
              <stop offset="38%" stop-color="#111111" stop-opacity="0.96" />
              <stop offset="100%" stop-color="#050505" stop-opacity="1" />
            </radialGradient>

            <radialGradient id="shine" cx="32%" cy="24%" r="58%">
              <stop offset="0%" stop-color="#ffffff" stop-opacity="0.24" />
              <stop offset="45%" stop-color="#ffffff" stop-opacity="0.08" />
              <stop offset="100%" stop-color="#ffffff" stop-opacity="0" />
            </radialGradient>

            <linearGradient id="land" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" stop-color="#ffd3a8" />
              <stop offset="100%" stop-color="#f97316" />
            </linearGradient>

            <clipPath id="sphereClip">
              <circle cx="410" cy="410" r="275" />
            </clipPath>
          </defs>

          <circle cx="410" cy="410" r="275" fill="url(#earthFill)" />
          <circle cx="410" cy="410" r="275" fill="url(#shine)" opacity="0.8" />
          <circle cx="410" cy="410" r="275" fill="none" stroke="rgba(255,255,255,0.10)" stroke-width="2" />

          <g clip-path="url(#sphereClip)">
            <g class="globe-spin">
              <g fill="none" stroke="rgba(255,255,255,0.12)" stroke-width="1.25">
                <ellipse cx="410" cy="410" rx="245" ry="92" />
                <ellipse cx="410" cy="410" rx="245" ry="144" />
                <ellipse cx="410" cy="410" rx="245" ry="196" />
                <path d="M140 410h540" />
                <path d="M410 140v540" />
                <path d="M166 268c74-50 414-50 488 0" />
                <path d="M166 552c74 50 414 50 488 0" />
              </g>

              <g fill="url(#land)" opacity="0.94">
                <path d="M190 274c22-18 51-31 87-38 34-6 65 0 86 15 14 11 21 28 18 43-4 19-22 31-43 37-22 7-40 9-53 20-15 13-17 31-29 45-15 18-39 28-68 27-31-1-61-13-73-34-11-20-8-43 6-60 11-12 15-38 69-55Z" />
                <path d="M338 196c24-18 60-29 95-24 30 4 58 20 73 43 12 19 13 41 2 57-10 15-29 23-50 26-24 4-40 0-54 12-15 13-18 32-30 48-13 17-36 26-61 25-24-2-46-13-55-31-9-18-7-38 4-54 10-14 13-34 10-53-3-19 12-39 66-69Z" />
                <path d="M518 238c27-14 57-19 86-14 26 5 49 18 62 38 11 16 13 35 6 50-8 18-28 31-51 35-21 4-35 12-45 26-13 18-34 28-57 28-24 0-44-10-53-28-8-16-6-34 4-49 10-14 15-31 15-48 1-17 9-29 33-38Z" />
                <path d="M214 408c16-12 34-16 52-12 16 4 29 14 35 27 6 13 4 28-4 39-9 12-23 19-39 21-18 2-34-2-46-12-12-10-16-24-13-37 2-12 5-19 15-26Z" />
                <path d="M370 402c19-13 42-17 64-13 20 4 35 14 42 29 7 14 7 30-2 42-9 14-26 23-46 26-23 3-43-2-56-15-12-11-16-26-13-41 3-15 2-21 11-28Z" />
                <path d="M548 396c17-10 38-14 57-10 17 3 31 14 38 27 8 14 8 31 1 44-9 16-25 26-44 29-21 4-40 0-54-13-12-11-17-25-13-40 3-14 3-26 15-37Z" />
              </g>

              <g fill="none" stroke="rgba(249,115,22,0.20)" stroke-width="2">
                <path d="M150 315c82 34 438 34 520 0" />
                <path d="M138 410c90 26 454 26 544 0" />
                <path d="M150 505c82 18 438 18 520 0" />
              </g>
            </g>
          </g>

          <circle cx="410" cy="410" r="275" fill="none" stroke="rgba(255,255,255,0.08)" stroke-width="2" />
        </svg>
      </div>
    </div>
  </div>
</section>