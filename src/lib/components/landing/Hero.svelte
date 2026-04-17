<section class="mx-auto grid min-h-[85vh] max-w-7xl gap-12 px-4 py-24 lg:grid-cols-[1.1fr_0.9fr] lg:items-center">
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
      <a href="/app" class="rounded-full bg-orange-500 px-6 py-3 text-sm font-semibold text-black transition hover:bg-orange-400">
        Open Platform
      </a>
      <a href="#features" class="rounded-full border border-white/10 px-6 py-3 text-sm font-semibold text-white transition hover:border-white/20 hover:bg-white/5">
        View Features
      </a>
    </div>
  </div>

  <div class="relative flex justify-center lg:justify-end">
    <div class="globe-shell">
      <div class="globe-halo"></div>

      <div class="globe">
        <svg viewBox="0 0 720 720" class="globe-svg" aria-hidden="true">
          <defs>
            <radialGradient id="globeShade" cx="50%" cy="42%" r="60%">
              <stop offset="0%" stop-color="#1b120a" />
              <stop offset="52%" stop-color="#0b0b0b" />
              <stop offset="100%" stop-color="#030303" />
            </radialGradient>

            <linearGradient id="continent" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" stop-color="#ffb36c" />
              <stop offset="100%" stop-color="#f97316" />
            </linearGradient>

            <clipPath id="sphereClip">
              <circle cx="360" cy="360" r="248" />
            </clipPath>
          </defs>

          <circle cx="360" cy="360" r="248" fill="url(#globeShade)" />
          <circle cx="360" cy="360" r="248" fill="none" stroke="rgba(255,255,255,0.08)" stroke-width="2" />

          <g clip-path="url(#sphereClip)" opacity="0.98">
            <g class="globe-rotate">
              <g fill="none" stroke="rgba(255,255,255,0.1)" stroke-width="1.2">
                <ellipse cx="360" cy="360" rx="220" ry="92" />
                <ellipse cx="360" cy="360" rx="220" ry="142" />
                <ellipse cx="360" cy="360" rx="220" ry="190" />
                <path d="M120 360h480" />
                <path d="M360 120v480" />
                <path d="M160 250c65-36 335-36 400 0" />
                <path d="M160 470c65 36 335 36 400 0" />
              </g>

              <g fill="url(#continent)">
                <path d="M182 250c16-22 42-37 74-43 30-6 59 5 74 23 10 12 14 31 8 44-8 18-31 29-54 30-28 1-40 13-53 31-16 22-46 33-76 26-28-7-51-24-56-46-6-27 10-53 37-65 11-5 33-3 46 0Z" />
                <path d="M307 188c23-14 54-20 84-14 24 5 46 17 58 33 11 14 11 33 2 46-9 13-25 21-41 25-18 4-35 0-47 9-17 13-20 34-31 49-11 15-31 22-51 20-22-2-41-15-45-34-4-16 1-33 14-45 12-11 23-27 20-47-2-17 11-34 37-42Z" />
                <path d="M452 255c21-11 48-14 72-7 21 6 39 20 49 37 9 15 10 33 3 48-10 20-32 33-56 36-20 3-32 12-44 25-16 17-41 24-65 18-21-5-37-18-42-35-5-18 1-35 13-48 12-13 22-28 22-45 0-17 15-28 48-29Z" />
                <path d="M210 392c16-10 34-13 52-7 15 5 26 15 30 28 4 13 1 27-8 37-10 12-24 17-38 21-17 4-32 0-44-9-14-11-18-27-14-42 3-11 9-21 22-28Z" />
                <path d="M353 390c17-11 38-15 58-11 18 4 32 14 39 28 7 14 6 30-2 42-10 15-28 23-47 26-21 4-39-1-51-13-11-11-14-24-11-39 3-14 2-24 14-33Z" />
                <path d="M510 402c18-10 39-13 58-8 17 5 31 15 38 29 7 13 7 29 1 42-8 15-24 25-42 28-20 4-39 0-52-12-12-11-16-24-12-40 4-14 3-29 9-39Z" />
              </g>

              <g opacity="0.7" fill="none" stroke="rgba(249,115,22,0.15)" stroke-width="2">
                <path d="M145 295c70 34 360 34 430 0" />
                <path d="M137 365c75 26 371 26 446 0" />
                <path d="M150 435c68 18 352 18 420 0" />
              </g>
            </g>

            <circle cx="360" cy="360" r="248" fill="none" stroke="rgba(255,255,255,0.08)" stroke-width="2" />
            <circle cx="360" cy="360" r="248" fill="url(#shine)" opacity="0.06" />
          </g>

          <defs>
            <radialGradient id="shine" cx="38%" cy="30%" r="55%">
              <stop offset="0%" stop-color="#ffffff" stop-opacity="0.35" />
              <stop offset="45%" stop-color="#ffffff" stop-opacity="0.08" />
              <stop offset="100%" stop-color="#ffffff" stop-opacity="0" />
            </radialGradient>
          </defs>
        </svg>
      </div>
    </div>
  </div>
</section>