<svg width="800" height="400" viewBox="0 0 800 400" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <radialGradient id="bg" cx="50%" cy="43%" r="75%">
      <stop offset="0%" stop-color="#1a0f0a"/>
      <stop offset="45%" stop-color="#090610"/>
      <stop offset="100%" stop-color="#010104"/>
    </radialGradient>
    <radialGradient id="halo">
      <stop offset="30%" stop-color="#ff9a3c" stop-opacity="0.55"/>
      <stop offset="55%" stop-color="#d4501a" stop-opacity="0.22"/>
      <stop offset="100%" stop-color="#7a2a10" stop-opacity="0"/>
    </radialGradient>
    <radialGradient id="vig" cx="50%" cy="45%" r="70%">
      <stop offset="55%" stop-color="#000" stop-opacity="0"/>
      <stop offset="100%" stop-color="#000" stop-opacity="0.75"/>
    </radialGradient>
    <linearGradient id="diskG" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#6b2208" stop-opacity="0"/>
      <stop offset="12%" stop-color="#9a3a10" stop-opacity="0.65"/>
      <stop offset="30%" stop-color="#ffb860" stop-opacity="0.95"/>
      <stop offset="44%" stop-color="#fff4dc"/>
      <stop offset="58%" stop-color="#ffa24a" stop-opacity="0.9"/>
      <stop offset="84%" stop-color="#8f2c0c" stop-opacity="0.5"/>
      <stop offset="100%" stop-color="#5a1a06" stop-opacity="0"/>
    </linearGradient>
    <linearGradient id="arcG" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#c8501a" stop-opacity="0"/>
      <stop offset="25%" stop-color="#ffb860"/>
      <stop offset="45%" stop-color="#fff2d6"/>
      <stop offset="75%" stop-color="#ff9a3c"/>
      <stop offset="100%" stop-color="#a83a10" stop-opacity="0"/>
    </linearGradient>
    <linearGradient id="flareG" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#ffd9a0" stop-opacity="0"/>
      <stop offset="50%" stop-color="#fff" stop-opacity="0.9"/>
      <stop offset="100%" stop-color="#ffd9a0" stop-opacity="0"/>
    </linearGradient>
    <linearGradient id="nameG" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#ffd9a0"/>
      <stop offset="50%" stop-color="#fff"/>
      <stop offset="100%" stop-color="#ffb060"/>
    </linearGradient>

    <filter id="b1" x="-20%" y="-300%" width="140%" height="700%"><feGaussianBlur stdDeviation="1.2"/></filter>
    <filter id="b3" x="-20%" y="-300%" width="140%" height="700%"><feGaussianBlur stdDeviation="3"/></filter>
    <filter id="b8" x="-30%" y="-100%" width="160%" height="300%"><feGaussianBlur stdDeviation="8"/></filter>
    <filter id="b20" x="-50%" y="-50%" width="200%" height="200%"><feGaussianBlur stdDeviation="20"/></filter>

    <!-- streaky, evolving gas texture for the accretion disk -->
    <filter id="gas" x="0" y="-100%" width="100%" height="300%" color-interpolation-filters="sRGB">
      <feTurbulence type="fractalNoise" baseFrequency="0.006 0.09" numOctaves="3" seed="4" result="n">
        <animate attributeName="baseFrequency" dur="14s" repeatCount="indefinite"
                 values="0.006 0.09;0.009 0.12;0.006 0.09"/>
      </feTurbulence>
      <feColorMatrix in="n" type="matrix" result="m"
        values="0 0 0 0 1  0 0 0 0 1  0 0 0 0 1  1.9 0 0 0 -0.35"/>
      <feComposite in="SourceGraphic" in2="m" operator="in" result="t"/>
      <feGaussianBlur in="t" stdDeviation="0.8 0.6"/>
    </filter>
  </defs>

  <!-- space -->
  <rect width="800" height="400" fill="url(#bg)"/>
  <ellipse cx="120" cy="90" rx="170" ry="70" fill="#3b2a8f" opacity="0.18" filter="url(#b20)" transform="rotate(-20 120 90)"/>
  <ellipse cx="690" cy="310" rx="150" ry="60" fill="#8f2a4a" opacity="0.14" filter="url(#b20)" transform="rotate(25 690 310)"/>
  <ellipse cx="650" cy="70" rx="130" ry="50" fill="#1f5f8f" opacity="0.12" filter="url(#b20)"/>

  <!-- stars -->
  <g>
    <circle cx="40" cy="35" r="1.2" fill="#cfe0ff" opacity=".3"><animate attributeName="opacity" values=".3;1;.3" dur="3.2s" repeatCount="indefinite"/></circle>
    <circle cx="95" cy="210" r="0.9" fill="#fff" opacity=".4"><animate attributeName="opacity" values=".4;1;.4" dur="4.1s" begin="-1s" repeatCount="indefinite"/></circle>
    <circle cx="150" cy="330" r="1.4" fill="#ffe6c8" opacity=".3"><animate attributeName="opacity" values=".3;1;.3" dur="5s" begin="-2s" repeatCount="indefinite"/></circle>
    <circle cx="205" cy="120" r="0.8" fill="#fff" opacity=".5"><animate attributeName="opacity" values=".5;1;.5" dur="2.8s" begin="-.5s" repeatCount="indefinite"/></circle>
    <circle cx="240" cy="260" r="1.1" fill="#cfe0ff" opacity=".3"><animate attributeName="opacity" values=".3;1;.3" dur="3.7s" begin="-3s" repeatCount="indefinite"/></circle>
    <circle cx="300" cy="30" r="1.5" fill="#fff" opacity=".3"><animate attributeName="opacity" values=".3;1;.3" dur="4.6s" begin="-1.5s" repeatCount="indefinite"/></circle>
    <circle cx="330" cy="365" r="0.9" fill="#ffe6c8" opacity=".4"><animate attributeName="opacity" values=".4;1;.4" dur="3.4s" begin="-2.2s" repeatCount="indefinite"/></circle>
    <circle cx="480" cy="25" r="1" fill="#fff" opacity=".4"><animate attributeName="opacity" values=".4;1;.4" dur="5.2s" begin="-.8s" repeatCount="indefinite"/></circle>
    <circle cx="560" cy="355" r="1.3" fill="#cfe0ff" opacity=".3"><animate attributeName="opacity" values=".3;1;.3" dur="3s" begin="-1.8s" repeatCount="indefinite"/></circle>
    <circle cx="600" cy="130" r="0.8" fill="#fff" opacity=".5"><animate attributeName="opacity" values=".5;1;.5" dur="4.4s" begin="-2.6s" repeatCount="indefinite"/></circle>
    <circle cx="660" cy="240" r="1.2" fill="#ffe6c8" opacity=".3"><animate attributeName="opacity" values=".3;1;.3" dur="3.9s" begin="-.2s" repeatCount="indefinite"/></circle>
    <circle cx="720" cy="45" r="1.6" fill="#fff" opacity=".3"><animate attributeName="opacity" values=".3;1;.3" dur="5.5s" begin="-3.4s" repeatCount="indefinite"/></circle>
    <circle cx="765" cy="170" r="0.9" fill="#cfe0ff" opacity=".4"><animate attributeName="opacity" values=".4;1;.4" dur="3.3s" begin="-1.1s" repeatCount="indefinite"/></circle>
    <circle cx="775" cy="375" r="1.1" fill="#fff" opacity=".3"><animate attributeName="opacity" values=".3;1;.3" dur="4.8s" begin="-2.9s" repeatCount="indefinite"/></circle>
    <circle cx="20" cy="150" r="1" fill="#fff" opacity=".4"><animate attributeName="opacity" values=".4;1;.4" dur="3.6s" begin="-.9s" repeatCount="indefinite"/></circle>
    <circle cx="420" cy="385" r="1.2" fill="#fff" opacity=".3"><animate attributeName="opacity" values=".3;1;.3" dur="4.2s" begin="-1.3s" repeatCount="indefinite"/></circle>
  </g>

  <!-- outer glow -->
  <circle cx="400" cy="170" r="175" fill="url(#halo)" filter="url(#b20)">
    <animate attributeName="opacity" values="0.75;1;0.75" dur="6s" repeatCount="indefinite"/>
  </circle>

  <!-- lensed far side of the disk (bent over top and under bottom) -->
  <g fill="none" stroke="url(#arcG)" stroke-linecap="round">
    <path d="M 262 172 C 285 95, 515 95, 538 172" stroke-width="18" filter="url(#b8)" opacity="0.8"/>
    <path d="M 262 172 C 285 95, 515 95, 538 172" stroke-width="7" filter="url(#b3)"/>
    <path d="M 262 172 C 285 95, 515 95, 538 172" stroke-width="2" filter="url(#b1)"/>
    <path d="M 290 172 C 310 232, 490 232, 510 172" stroke-width="10" filter="url(#b3)" opacity="0.55"/>
    <path d="M 290 172 C 310 232, 490 232, 510 172" stroke-width="1.5" filter="url(#b1)" opacity="0.7"/>
  </g>

  <!-- event horizon -->
  <circle cx="400" cy="170" r="60" fill="#000"/>
  <circle cx="400" cy="170" r="66" fill="none" stroke="#7ab8ff" stroke-width="1" opacity="0.25" filter="url(#b1)"/>
  <circle cx="400" cy="170" r="63" fill="none" stroke="#ff9a3c" stroke-width="4" filter="url(#b3)" opacity="0.6"/>
  <circle cx="400" cy="170" r="61" fill="none" stroke="#ffe2b0" stroke-width="1.6" filter="url(#b1)">
    <animate attributeName="opacity" values="0.7;1;0.7" dur="4s" repeatCount="indefinite"/>
  </circle>

  <!-- accretion disk (front) -->
  <ellipse cx="400" cy="171" rx="285" ry="24" fill="url(#diskG)" filter="url(#b8)" opacity="0.55"/>
  <ellipse cx="400" cy="171" rx="270" ry="15" fill="url(#diskG)" filter="url(#b3)" opacity="0.8"/>
  <ellipse cx="400" cy="171" rx="268" ry="13" fill="url(#diskG)" filter="url(#gas)"/>
  <ellipse cx="400" cy="171" rx="150" ry="2.2" fill="#fff6e4" opacity="0.85" filter="url(#b1)"/>

  <!-- swirling streaks -->
  <g fill="none" stroke="#fff3d8" stroke-linecap="round" filter="url(#b1)">
    <ellipse cx="400" cy="171" rx="235" ry="9" stroke-width="1.4" opacity="0.35" stroke-dasharray="40 70 12 90">
      <animate attributeName="stroke-dashoffset" from="0" to="-424" dur="7s" repeatCount="indefinite"/>
    </ellipse>
    <ellipse cx="400" cy="171" rx="185" ry="6" stroke-width="1.2" opacity="0.4" stroke-dasharray="25 55 8 70">
      <animate attributeName="stroke-dashoffset" from="0" to="-316" dur="4.5s" repeatCount="indefinite"/>
    </ellipse>
    <ellipse cx="400" cy="171" rx="130" ry="3.5" stroke-width="1" opacity="0.5" stroke-dasharray="18 40 6 50">
      <animate attributeName="stroke-dashoffset" from="0" to="-228" dur="3s" repeatCount="indefinite"/>
    </ellipse>
  </g>

  <!-- orbiting sparks -->
  <g fill="#fff" filter="url(#b1)">
    <circle r="1.8"><animateMotion dur="5s" repeatCount="indefinite" path="M 200 171 a 200 8 0 1 1 400 0 a 200 8 0 1 1 -400 0"/></circle>
    <circle r="1.4"><animateMotion dur="5s" begin="-2.5s" repeatCount="indefinite" path="M 200 171 a 200 8 0 1 1 400 0 a 200 8 0 1 1 -400 0"/></circle>
    <circle r="1.6"><animateMotion dur="3.4s" repeatCount="indefinite" path="M 260 171 a 140 5 0 1 1 280 0 a 140 5 0 1 1 -280 0"/></circle>
    <circle r="1.2"><animateMotion dur="3.4s" begin="-1.7s" repeatCount="indefinite" path="M 260 171 a 140 5 0 1 1 280 0 a 140 5 0 1 1 -280 0"/></circle>
  </g>

  <!-- anamorphic lens flare -->
  <ellipse cx="400" cy="171" rx="390" ry="1.3" fill="url(#flareG)" filter="url(#b1)">
    <animate attributeName="opacity" values="0.35;0.7;0.35" dur="5s" repeatCount="indefinite"/>
  </ellipse>

  <!-- vignette -->
  <rect width="800" height="400" fill="url(#vig)"/>

  <!-- name -->
  <text x="400" y="334" text-anchor="middle" font-family="Segoe UI, Helvetica, Arial, sans-serif"
        font-size="36" font-weight="300" letter-spacing="16" fill="#ff9a3c" filter="url(#b8)" opacity="0.7">ABIJITH</text>
  <text x="400" y="334" text-anchor="middle" font-family="Segoe UI, Helvetica, Arial, sans-serif"
        font-size="36" font-weight="300" letter-spacing="16" fill="url(#nameG)">ABIJITH
    <animate attributeName="opacity" values="0.85;1;0.85" dur="5s" repeatCount="indefinite"/>
  </text>
</svg>
