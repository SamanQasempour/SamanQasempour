<div align="center">

<!-- ANIMATED SPACE HEADER -->
<svg width="860" height="220" viewBox="0 0 860 220" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Deep space background gradient -->
    <radialGradient id="spaceBg" cx="50%" cy="50%" r="70%">
      <stop offset="0%" stop-color="#0d1b2e"/>
      <stop offset="60%" stop-color="#060d18"/>
      <stop offset="100%" stop-color="#020609"/>
    </radialGradient>
    <!-- Planet glow -->
    <radialGradient id="planetGlow" cx="50%" cy="40%" r="60%">
      <stop offset="0%" stop-color="#00d4ff" stop-opacity="0.9"/>
      <stop offset="50%" stop-color="#0077cc" stop-opacity="0.7"/>
      <stop offset="100%" stop-color="#003366" stop-opacity="0.4"/>
    </radialGradient>
    <!-- Ring gradient -->
    <linearGradient id="ringGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#00d4ff" stop-opacity="0.1"/>
      <stop offset="30%" stop-color="#00d4ff" stop-opacity="0.8"/>
      <stop offset="50%" stop-color="#ffd700" stop-opacity="0.9"/>
      <stop offset="70%" stop-color="#00d4ff" stop-opacity="0.8"/>
      <stop offset="100%" stop-color="#00d4ff" stop-opacity="0.1"/>
    </linearGradient>
    <!-- Nebula glow filter -->
    <filter id="glow" x="-30%" y="-30%" width="160%" height="160%">
      <feGaussianBlur stdDeviation="4" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="softGlow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="8" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="textGlow">
      <feGaussianBlur stdDeviation="3" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <!-- Moon gradient -->
    <radialGradient id="moonGrad" cx="35%" cy="35%" r="65%">
      <stop offset="0%" stop-color="#c8e8ff"/>
      <stop offset="100%" stop-color="#1a4a6e"/>
    </radialGradient>
    <!-- Clip for ring behind planet -->
    <clipPath id="ringBackClip">
      <rect x="0" y="0" width="860" height="106"/>
    </clipPath>
    <clipPath id="ringFrontClip">
      <rect x="0" y="106" width="860" height="114"/>
    </clipPath>
  </defs>

  <!-- Background -->
  <rect width="860" height="220" fill="url(#spaceBg)" rx="16"/>

  <!-- Nebula blobs -->
  <ellipse cx="120" cy="80" rx="90" ry="55" fill="#0033aa" opacity="0.12"/>
  <ellipse cx="720" cy="150" rx="100" ry="60" fill="#002299" opacity="0.10"/>
  <ellipse cx="430" cy="30" rx="140" ry="40" fill="#00aacc" opacity="0.06"/>

  <!-- Stars — static small dots -->
  <g fill="#ffffff">
    <circle cx="30" cy="15" r="0.8" opacity="0.9"/><circle cx="85" cy="42" r="0.6" opacity="0.7"/>
    <circle cx="140" cy="8" r="1" opacity="0.8"/><circle cx="200" cy="55" r="0.7" opacity="0.6"/>
    <circle cx="260" cy="20" r="0.9" opacity="0.9"/><circle cx="310" cy="68" r="0.6" opacity="0.7"/>
    <circle cx="370" cy="12" r="0.8" opacity="0.8"/><circle cx="450" cy="40" r="0.5" opacity="0.6"/>
    <circle cx="510" cy="18" r="1" opacity="0.9"/><circle cx="560" cy="62" r="0.7" opacity="0.7"/>
    <circle cx="620" cy="9" r="0.8" opacity="0.8"/><circle cx="680" cy="48" r="0.6" opacity="0.6"/>
    <circle cx="750" cy="22" r="0.9" opacity="0.9"/><circle cx="800" cy="70" r="0.7" opacity="0.7"/>
    <circle cx="840" cy="15" r="0.8" opacity="0.8"/><circle cx="50" cy="170" r="0.7" opacity="0.6"/>
    <circle cx="110" cy="195" r="0.9" opacity="0.8"/><circle cx="170" cy="180" r="0.6" opacity="0.7"/>
    <circle cx="240" cy="210" r="0.8" opacity="0.6"/><circle cx="340" cy="185" r="0.7" opacity="0.8"/>
    <circle cx="480" cy="200" r="0.6" opacity="0.7"/><circle cx="590" cy="175" r="0.9" opacity="0.9"/>
    <circle cx="700" cy="205" r="0.7" opacity="0.6"/><circle cx="820" cy="190" r="0.8" opacity="0.8"/>
    <circle cx="15" cy="110" r="0.9" opacity="0.7"/><circle cx="855" cy="130" r="0.7" opacity="0.8"/>
  </g>

  <!-- Twinkling stars with animation -->
  <circle cx="65" cy="100" r="1.2" fill="#00d4ff" opacity="0.8">
    <animate attributeName="opacity" values="0.8;0.2;0.8" dur="2.3s" repeatCount="indefinite"/>
  </circle>
  <circle cx="790" cy="55" r="1" fill="#ffd700" opacity="0.7">
    <animate attributeName="opacity" values="0.7;0.15;0.7" dur="3.1s" repeatCount="indefinite"/>
  </circle>
  <circle cx="400" cy="195" r="1.1" fill="#00d4ff" opacity="0.6">
    <animate attributeName="opacity" values="0.6;0.1;0.6" dur="1.8s" repeatCount="indefinite"/>
  </circle>
  <circle cx="650" cy="130" r="0.9" fill="#ffffff" opacity="0.9">
    <animate attributeName="opacity" values="0.9;0.2;0.9" dur="2.7s" repeatCount="indefinite"/>
  </circle>

  <!-- PLANET - ring BEHIND (clipped to upper half) -->
  <g clip-path="url(#ringBackClip)">
    <ellipse cx="108" cy="108" rx="74" ry="14" fill="none" stroke="url(#ringGrad)" stroke-width="9" opacity="0.75"/>
  </g>

  <!-- PLANET body -->
  <circle cx="108" cy="108" r="52" fill="url(#planetGlow)" filter="url(#softGlow)"/>
  <!-- Planet surface detail -->
  <ellipse cx="100" cy="95" rx="30" ry="8" fill="#0099dd" opacity="0.25" transform="rotate(-15,100,95)"/>
  <ellipse cx="118" cy="118" rx="22" ry="5" fill="#00ccff" opacity="0.15" transform="rotate(10,118,118)"/>
  <!-- Planet shimmer -->
  <circle cx="90" cy="88" r="14" fill="#ffffff" opacity="0.07"/>

  <!-- PLANET - ring FRONT (clipped to lower half) -->
  <g clip-path="url(#ringFrontClip)">
    <ellipse cx="108" cy="108" rx="74" ry="14" fill="none" stroke="url(#ringGrad)" stroke-width="9" opacity="0.75"/>
  </g>

  <!-- Orbiting moon -->
  <g>
    <animateTransform attributeName="transform" type="rotate" from="0 108 108" to="360 108 108" dur="8s" repeatCount="indefinite"/>
    <circle cx="182" cy="108" r="8" fill="url(#moonGrad)" filter="url(#glow)"/>
    <circle cx="182" cy="108" r="12" fill="#00d4ff" opacity="0.12"/>
  </g>

  <!-- Second smaller moon, opposite orbit -->
  <g opacity="0.7">
    <animateTransform attributeName="transform" type="rotate" from="180 108 108" to="540 108 108" dur="13s" repeatCount="indefinite"/>
    <circle cx="176" cy="108" r="5" fill="#ffd700" opacity="0.85" filter="url(#glow)"/>
  </g>

  <!-- TEXT SECTION -->
  <!-- Name / Title -->
  <text x="235" y="72" font-family="'Courier New', monospace" font-size="11" fill="#00d4ff" opacity="0.7" letter-spacing="4">
    ◈ DEVELOPER · BUILDER · CREATOR ◈
  </text>

  <text x="232" y="115" font-family="'Courier New', monospace" font-size="38" font-weight="bold"
        fill="#00d4ff" filter="url(#textGlow)" letter-spacing="2">
    Sam
    <animate attributeName="fill" values="#00d4ff;#ffffff;#ffd700;#00d4ff" dur="5s" repeatCount="indefinite"/>
  </text>

  <!-- Typing cursor effect line -->
  <text x="232" y="148" font-family="'Courier New', monospace" font-size="14" fill="#7dd4f0" letter-spacing="1" opacity="0.85">
    &gt; Building the future, one commit at a time_
    <animate attributeName="opacity" values="0.85;0.4;0.85" dur="2s" repeatCount="indefinite"/>
  </text>

  <!-- Divider line -->
  <line x1="232" y1="162" x2="840" y2="162" stroke="#00d4ff" stroke-width="0.5" opacity="0.3"/>

  <!-- Stats row -->
  <text x="235" y="185" font-family="'Courier New', monospace" font-size="12" fill="#ffd700" opacity="0.9">
    ✦ Nibero  ·  Programming &amp; Mobile Tech  ·  Open Source Enthusiast
  </text>

  <!-- Corner accents -->
  <g stroke="#00d4ff" stroke-width="1.5" fill="none" opacity="0.4">
    <path d="M10,10 L10,25 M10,10 L25,10"/>
    <path d="M850,10 L835,10 M850,10 L850,25"/>
    <path d="M10,210 L10,195 M10,210 L25,210"/>
    <path d="M850,210 L835,210 M850,210 L850,195"/>
  </g>
</svg>

<!-- ABOUT ME -->
<br/>

```
┌─────────────────────────────────────────────────────────────┐
│  > whoami                                                   │
│  Developer @ Nibero  |  Programming & Mobile Phone Parts   │
│  Passionate about clean code, space, and pushing limits    │
└─────────────────────────────────────────────────────────────┘
```

</div>

---

## 🪐 About Me

```yaml
name: "Sam"
company: "Nibero"
focus:
  - "Software Development"
  - "Mobile Technology"
  - "Building scalable systems"
currently_learning: "Always exploring new frontiers"
motto: "The universe is big — so are the possibilities in code"
```

---

## ⚡ Tech Stack & Skills

<!-- ANIMATED SKILLS SVG -->
<div align="center">
<svg width="760" height="280" viewBox="0 0 760 280" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <radialGradient id="skillBg" cx="50%" cy="50%" r="70%">
      <stop offset="0%" stop-color="#0d1b2e"/>
      <stop offset="100%" stop-color="#040c18"/>
    </radialGradient>
    <filter id="skillGlow">
      <feGaussianBlur stdDeviation="2.5" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <linearGradient id="barBase" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#00d4ff"/>
      <stop offset="100%" stop-color="#0055aa"/>
    </linearGradient>
    <linearGradient id="barGold" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#ffd700"/>
      <stop offset="100%" stop-color="#aa7700"/>
    </linearGradient>
    <linearGradient id="barCyan" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#00ffcc"/>
      <stop offset="100%" stop-color="#007755"/>
    </linearGradient>
  </defs>

  <rect width="760" height="280" fill="url(#skillBg)" rx="12"/>

  <!-- Corner brackets -->
  <g stroke="#00d4ff" stroke-width="1" fill="none" opacity="0.35">
    <path d="M8,8 L8,20 M8,8 L20,8"/>
    <path d="M752,8 L740,8 M752,8 L752,20"/>
    <path d="M8,272 L8,260 M8,272 L20,272"/>
    <path d="M752,272 L740,272 M752,272 L752,260"/>
  </g>

  <!-- Title -->
  <text x="380" y="35" text-anchor="middle" font-family="'Courier New',monospace"
        font-size="13" fill="#00d4ff" letter-spacing="5" opacity="0.8">◈ SKILL MATRIX ◈</text>

  <!-- Left column skills -->
  <!-- Python -->
  <text x="30" y="72" font-family="'Courier New',monospace" font-size="12" fill="#7dd4f0">Python</text>
  <rect x="30" y="78" width="280" height="7" rx="3" fill="#0a1a2e"/>
  <rect x="30" y="78" width="0" height="7" rx="3" fill="url(#barBase)" filter="url(#skillGlow)">
    <animate attributeName="width" from="0" to="252" dur="1.4s" fill="freeze" begin="0.3s"/>
  </rect>
  <text x="320" y="87" font-family="'Courier New',monospace" font-size="10" fill="#00d4ff">90%</text>

  <!-- JavaScript -->
  <text x="30" y="112" font-family="'Courier New',monospace" font-size="12" fill="#7dd4f0">JavaScript</text>
  <rect x="30" y="118" width="280" height="7" rx="3" fill="#0a1a2e"/>
  <rect x="30" y="118" width="0" height="7" rx="3" fill="url(#barBase)" filter="url(#skillGlow)">
    <animate attributeName="width" from="0" to="238" dur="1.4s" fill="freeze" begin="0.5s"/>
  </rect>
  <text x="320" y="127" font-family="'Courier New',monospace" font-size="10" fill="#00d4ff">85%</text>

  <!-- React -->
  <text x="30" y="152" font-family="'Courier New',monospace" font-size="12" fill="#7dd4f0">React / Next.js</text>
  <rect x="30" y="158" width="280" height="7" rx="3" fill="#0a1a2e"/>
  <rect x="30" y="158" width="0" height="7" rx="3" fill="url(#barCyan)" filter="url(#skillGlow)">
    <animate attributeName="width" from="0" to="224" dur="1.4s" fill="freeze" begin="0.7s"/>
  </rect>
  <text x="320" y="167" font-family="'Courier New',monospace" font-size="10" fill="#00ffcc">80%</text>

  <!-- Git -->
  <text x="30" y="192" font-family="'Courier New',monospace" font-size="12" fill="#7dd4f0">Git / DevOps</text>
  <rect x="30" y="198" width="280" height="7" rx="3" fill="#0a1a2e"/>
  <rect x="30" y="198" width="0" height="7" rx="3" fill="url(#barGold)" filter="url(#skillGlow)">
    <animate attributeName="width" from="0" to="238" dur="1.4s" fill="freeze" begin="0.9s"/>
  </rect>
  <text x="320" y="207" font-family="'Courier New',monospace" font-size="10" fill="#ffd700">85%</text>

  <!-- Mobile Dev -->
  <text x="30" y="232" font-family="'Courier New',monospace" font-size="12" fill="#7dd4f0">Mobile Dev</text>
  <rect x="30" y="238" width="280" height="7" rx="3" fill="#0a1a2e"/>
  <rect x="30" y="238" width="0" height="7" rx="3" fill="url(#barBase)" filter="url(#skillGlow)">
    <animate attributeName="width" from="0" to="210" dur="1.4s" fill="freeze" begin="1.1s"/>
  </rect>
  <text x="320" y="247" font-family="'Courier New',monospace" font-size="10" fill="#00d4ff">75%</text>

  <!-- Vertical divider -->
  <line x1="380" y1="55" x2="380" y2="265" stroke="#00d4ff" stroke-width="0.5" opacity="0.2"/>

  <!-- Right column: Tech badges -->
  <text x="410" y="72" font-family="'Courier New',monospace" font-size="11" fill="#ffd700" letter-spacing="2">TECHNOLOGIES</text>

  <!-- Badge grid -->
  <g font-family="'Courier New',monospace" font-size="11" filter="url(#skillGlow)">
    <!-- Row 1 -->
    <rect x="410" y="82" width="80" height="22" rx="4" fill="#001a33" stroke="#00d4ff" stroke-width="0.8" opacity="0.9"/>
    <text x="450" y="97" text-anchor="middle" fill="#00d4ff">Python</text>

    <rect x="500" y="82" width="80" height="22" rx="4" fill="#001a33" stroke="#00d4ff" stroke-width="0.8" opacity="0.9"/>
    <text x="540" y="97" text-anchor="middle" fill="#00d4ff">Node.js</text>

    <rect x="590" y="82" width="80" height="22" rx="4" fill="#001a33" stroke="#ffd700" stroke-width="0.8" opacity="0.9"/>
    <text x="630" y="97" text-anchor="middle" fill="#ffd700">React</text>

    <!-- Row 2 -->
    <rect x="410" y="114" width="80" height="22" rx="4" fill="#001a33" stroke="#00ffcc" stroke-width="0.8" opacity="0.9"/>
    <text x="450" y="129" text-anchor="middle" fill="#00ffcc">Docker</text>

    <rect x="500" y="114" width="80" height="22" rx="4" fill="#001a33" stroke="#00d4ff" stroke-width="0.8" opacity="0.9"/>
    <text x="540" y="129" text-anchor="middle" fill="#00d4ff">Linux</text>

    <rect x="590" y="114" width="80" height="22" rx="4" fill="#001a33" stroke="#ffd700" stroke-width="0.8" opacity="0.9"/>
    <text x="630" y="129" text-anchor="middle" fill="#ffd700">Android</text>

    <!-- Row 3 -->
    <rect x="410" y="146" width="80" height="22" rx="4" fill="#001a33" stroke="#00d4ff" stroke-width="0.8" opacity="0.9"/>
    <text x="450" y="161" text-anchor="middle" fill="#00d4ff">SQL</text>

    <rect x="500" y="146" width="80" height="22" rx="4" fill="#001a33" stroke="#00ffcc" stroke-width="0.8" opacity="0.9"/>
    <text x="540" y="161" text-anchor="middle" fill="#00ffcc">Git</text>

    <rect x="590" y="146" width="80" height="22" rx="4" fill="#001a33" stroke="#00d4ff" stroke-width="0.8" opacity="0.9"/>
    <text x="630" y="161" text-anchor="middle" fill="#00d4ff">TypeScript</text>

    <!-- Row 4 -->
    <rect x="410" y="178" width="80" height="22" rx="4" fill="#001a33" stroke="#ffd700" stroke-width="0.8" opacity="0.9"/>
    <text x="450" y="193" text-anchor="middle" fill="#ffd700">Firebase</text>

    <rect x="500" y="178" width="80" height="22" rx="4" fill="#001a33" stroke="#00d4ff" stroke-width="0.8" opacity="0.9"/>
    <text x="540" y="193" text-anchor="middle" fill="#00d4ff">AWS</text>

    <rect x="590" y="178" width="80" height="22" rx="4" fill="#001a33" stroke="#00ffcc" stroke-width="0.8" opacity="0.9"/>
    <text x="630" y="193" text-anchor="middle" fill="#00ffcc">REST API</text>
  </g>

  <!-- Floating particles -->
  <circle cx="700" cy="230" r="2" fill="#00d4ff" opacity="0.5">
    <animate attributeName="cy" values="230;220;230" dur="3s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.5;1;0.5" dur="3s" repeatCount="indefinite"/>
  </circle>
  <circle cx="720" cy="245" r="1.5" fill="#ffd700" opacity="0.4">
    <animate attributeName="cy" values="245;235;245" dur="4s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.4;0.9;0.4" dur="4s" repeatCount="indefinite"/>
  </circle>
  <circle cx="740" cy="225" r="1" fill="#00ffcc" opacity="0.6">
    <animate attributeName="cy" values="225;215;225" dur="2.5s" repeatCount="indefinite"/>
  </circle>
</svg>
</div>

---

## 🌌 GitHub Stats

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=tokyonight&bg_color=060d18&border_color=00d4ff&title_color=00d4ff&icon_color=ffd700&text_color=7dd4f0&hide_border=false" height="160"/>
  &nbsp;
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=tokyonight&bg_color=060d18&border_color=00d4ff&title_color=00d4ff&text_color=7dd4f0" height="160"/>
</div>

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=YOUR_USERNAME&theme=tokyonight&background=060d18&ring=00d4ff&fire=ffd700&currStreakLabel=00d4ff&border=00d4ff" height="160"/>
</div>

---

<!-- FOOTER -->
<div align="center">

<svg width="760" height="55" viewBox="0 0 760 55" xmlns="http://www.w3.org/2000/svg">
  <rect width="760" height="55" fill="#060d18" rx="8"/>
  <text x="380" y="22" text-anchor="middle" font-family="'Courier New',monospace"
        font-size="11" fill="#00d4ff" letter-spacing="3" opacity="0.7">◈ NIBERO ◈</text>
  <text x="380" y="42" text-anchor="middle" font-family="'Courier New',monospace"
        font-size="10" fill="#7dd4f0" opacity="0.5">
    The cosmos is our canvas — and code is our language
  </text>
  <!-- Subtle line top -->
  <line x1="60" y1="5" x2="700" y2="5" stroke="#00d4ff" stroke-width="0.5" opacity="0.2"/>
</svg>

</div>
