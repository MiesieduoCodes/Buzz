<!--
  README.md — BUZZ (Animated GitHub README)
  Paste this whole file into your repo's README.md (UTF-8).
-->

<!-- ===== Animated SVG Header ===== -->
<!-- GitHub renders inline SVG in Markdown; this SVG contains self-contained animations -->
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 260" width="100%" preserveAspectRatio="xMidYMid meet" role="img" aria-labelledby="title desc" style="background: linear-gradient(90deg,#071226,#081223 40%, #061018); border-radius:12px;">
  <title id="title">BUZZ — Messaging Reimagined</title>
  <desc id="desc">Animated header with flying bee, honey meter, and glowing title for BUZZ app</desc>

  <!-- defs: gradients, drop shadows -->
  <defs>
    <linearGradient id="goldGrad" x1="0" x2="1">
      <stop offset="0" stop-color="#FFD97D"/>
      <stop offset="1" stop-color="#F4B400"/>
    </linearGradient>

    <filter id="softShadow" x="-50%" y="-50%" width="200%" height="200%">
      <feOffset dx="0" dy="6" result="off"/>
      <feGaussianBlur in="off" stdDeviation="18" result="blur"/>
      <feBlend in="SourceGraphic" in2="blur"/>
    </filter>

    <!-- hexagon shape -->
    <polygon id="hex" points="0,30 25,0 75,0 100,30 75,60 25,60" />
  </defs>

  <!-- background subtle glow -->
  <rect x="0" y="0" width="1200" height="260" fill="url(#bgGrad)" opacity="0"/>
  <g transform="translate(40,30)" opacity="0.95">

    <!-- Title block -->
    <g transform="translate(120,22)">
      <!-- Title text -->
      <text x="0" y="28" font-family="Inter, system-ui, -apple-system, 'Segoe UI', Roboto, Arial" font-weight="700" font-size="36" fill="#F8C948">BUZZ</text>
      <text x="0" y="60" font-family="Inter, system-ui, -apple-system, 'Segoe UI', Roboto, Arial" font-size="14" fill="#9AA6B2">Messaging Reimagined — vibes, hives & golden moments</text>

      <!-- HoneyScore label -->
      <g transform="translate(0,84)">
        <rect x="0" y="0" rx="12" ry="12" width="380" height="48" fill="#071126" fill-opacity="0.4" stroke="#0f2330" stroke-width="1"/>
        <text x="14" y="30" font-family="Inter, Arial" font-size="12" fill="#FFD97D" font-weight="700">HoneyScore</text>

        <!-- honey meter background -->
        <rect x="120" y="12" width="230" height="12" rx="8" fill="#0b1220" stroke="#0f1a25" />
        <!-- animated honey fill -->
        <rect id="honeyFill" x="120" y="12" width="0" height="12" rx="8" fill="url(#goldGrad)" filter="url(#softShadow)">
          <animate attributeName="width" from="0" to="165" dur="2.0s" begin="0.4s" fill="freeze" />
        </rect>

        <text x="360" y="22" font-family="Inter, Arial" font-size="12" fill="#fff" fill-opacity="0.85">72%</text>
      </g>
    </g>

    <!-- Animated bee group -->
    <g transform="translate(18,22) scale(1.22)">
      <!-- flight path animation -->
      <g id="beeGroup">
        <!-- body -->
        <ellipse cx="72" cy="66" rx="34" ry="22" fill="#FFD97D" />
        <path d="M50 54c-10-12-10-27 2-37 12-11 40-8 52 2 10 9 10 25 2 37-9 12-32 16-56-2z" fill="#101827"/>
        <!-- wings -->
        <g>
          <path id="wingL" d="M41 30c-18-8-36 7-30 23 6 16 30 14 44 4 17-12 10-28-14-27z" fill="#fff" opacity="0.92">
            <animateTransform attributeName="transform" type="rotate" from="0 20 38" to="22 20 38" dur="0.9s" begin="0s" repeatCount="indefinite" additive="sum" />
            <animateTransform attributeName="transform" type="rotate" from="22 20 38" to="0 20 38" dur="0.9s" begin="0.45s" repeatCount="indefinite" additive="sum" />
          </path>
          <path id="wingR" d="M110 30c18-8 36 7 30 23-6 16-30 14-44 4-17-12-10-28 14-27z" fill="#fff" opacity="0.92">
            <animateTransform attributeName="transform" type="rotate" from="0 92 38" to="-22 92 38" dur="0.9s" begin="0.12s" repeatCount="indefinite" additive="sum" />
            <animateTransform attributeName="transform" type="rotate" from="-22 92 38" to="0 92 38" dur="0.9s" begin="0.57s" repeatCount="indefinite" additive="sum" />
          </path>
        </g>

        <!-- eye and tail -->
        <circle cx="74" cy="52" r="4" fill="#fff" />
        <rect x="56" y="86" width="36" height="8" rx="4" fill="#FFD97D" />
      </g>

      <!-- bee flight bob (translate) -->
      <animateTransform xlink:href="#beeGroup" attributeName="transform" type="translate" values="0 0; 6 -8; 0 0; -4 6; 0 0" dur="6s" repeatCount="indefinite" />
    </g>

    <!-- small animated hex tiles on right for style -->
    <g transform="translate(940,20)" opacity="0.9">
      <g transform="translate(0,0) scale(1.6)">
        <g transform="translate(0,0)">
          <use xlink:href="#hex" fill="rgba(244,180,0,0.06)"/>
        </g>
        <g transform="translate(56,6)">
          <use xlink:href="#hex" fill="rgba(244,180,0,0.04)">
            <animate attributeName="opacity" values="0.04;0.12;0.04" dur="4s" repeatCount="indefinite" />
          </use>
        </g>
        <g transform="translate(28,48)">
          <use xlink:href="#hex" fill="rgba(244,180,0,0.03)">
            <animate attributeName="opacity" values="0.03;0.09;0.03" dur="3s" repeatCount="indefinite" />
          </use>
        </g>
      </g>
    </g>

  </g>
</svg>

<!-- ===== Markdown Content ===== -->

# BUZZ — Messaging Reimagined

**BUZZ** is a living, emotional messaging experience built with vibes, hives, and golden moments.  
Built with **React Native + Expo + Firebase**, Buzz focuses on *emotional presence*, *playful interactions*, and *community energy*.

---

## 🚀 Quick Links
- **Demo / Design**: `design/` (link to Figma or design kit)
- **Docs**: `docs/`
- **Issues**: Please open issues for bugs or feature requests.

---

## ✨ Core Concepts (Short)
- **Vibes** — send emotion pulses: color + haptics + sound  
- **Pollination Chains** — daily streaks that earn Nectar & glow visually  
- **Buzz Moments** — mood-reactive ephemeral posts that morph over time  
- **Audio Realms** — drop-in audio with reactive visuals  
- **Hives** — small groups with shared energy, leaderboards & rewards

---

## 📦 Features (detailed)
- 1:1 and group messaging (text, media, voice notes)  
- Vibes: micro-emotional signals (color + haptic + audio)  
- HoneyScore: user engagement score (bee-themed, like Snap Score)  
- Pollination Chains: streaks between friends (visual honey trails)  
- Buzz Moments: ephemeral mood posts (24h by default)  
- Hive System: create & manage hives, hive leaderboards  
- Audio Realms: live group audio with voice filters  
- Privacy: ephemeral whispers, biometric lock, E2E options  
- Offline-first support with local caching & sync  
- Gamification: Nectar currency, badges, Hive events

---

## 🎨 UX & Visual Language
- Hexagon grid motifs (subtle, not literal UI)  
- Golden/amber palette with warm dark backgrounds  
- Micro-interactions: send animation, honey drips, vibe pulses  
- Accessible: reduced motion, high-contrast mode, screen reader labels

---

## 🧱 Backend Architecture (overview)
- **Auth**: Firebase Auth (Email, Google, Apple, Phone)  
- **Database**: Firestore for chats & metadata; RTDB for presence (optional)  
- **Storage**: Firebase Storage for media assets  
- **Functions**: Cloud Functions for HoneyScore calculation, notification triggers, scheduled cleanup  
- **Notifications**: FCM (push notifications)  
- **Monitoring**: Crashlytics + Firebase Analytics

---

## 🛠 Getting Started (Local)
```bash
# clone
git clone https://github.com/your-org/buzz.git
cd buzz

# install
yarn install
# or
npm install

# start expo
expo start
