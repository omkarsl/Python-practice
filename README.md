# Animated & Interactive README for `Python-practice`

> A lively, animated README template you can drop into your repo. Includes an SVG hero animation (copy into `assets/hero.svg`), interactive sections, badges, and usage instructions to preview locally.

---

<p align="center">
  <img src="assets/hero.svg" alt="hero animation" width="720" />
</p>

<p align="center">
  <a href="#about"><img alt="readme" src="https://img.shields.io/badge/README-Interactive-brightgreen"/></a>
  <img alt="license" src="https://img.shields.io/badge/License-MIT-blue"/>
  <img alt="python" src="https://img.shields.io/badge/Python-3.10+-blueviolet"/>
</p>

---

## About

Welcome to **Python-practice** — a curated collection of Python practice problems, solutions, and small projects. This README is animated and interactive to make browsing more fun.

## Features

* 🎨 Animated SVG hero (see `assets/hero.svg`)
* 🧭 Collapsible sections for quick navigation
* 🧪 Badges and quick status
* 🖥️ Local preview instructions (live reload)

---

## How to use this README

1. Create a folder called `assets` in the repository root.
2. Save the SVG contents provided below into `assets/hero.svg`.
3. Commit `README.md` (this file) and the `assets/hero.svg` file to your repo.
4. View the README on GitHub — GitHub will render the SVG animation.

> **Why an SVG?** GitHub allows SVG images in READMEs and they can include CSS animations. We avoid JavaScript for security/sanitization reasons; CSS + SMIL in SVG gives smooth animation.

---

## assets/hero.svg (copy this into `assets/hero.svg`)

```svg
<!-- Save this exact text into assets/hero.svg -->
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 300">
  <style>
    .bg { fill: #0f172a }
    .title { fill: #e6edf3; font-family: Inter, Roboto, sans-serif; font-weight: 700 }
    .mono { font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, "Roboto Mono", "Courier New", monospace }

    .wave { animation: moveWave 6s linear infinite }
    @keyframes moveWave {
      0% { transform: translateX(0) }
      50% { transform: translateX(-30px) }
      100% { transform: translateX(0) }
    }

    .fade-in { animation: fade 1.2s ease forwards; opacity: 0 }
    .delay-1 { animation-delay: 0.6s }
    .delay-2 { animation-delay: 1.1s }
    @keyframes fade { to { opacity: 1 } }

    .pulse { transform-origin: center; animation: pulse 2.4s infinite }
    @keyframes pulse { 0% { transform: scale(1) } 50% { transform: scale(1.06) } 100% { transform: scale(1) } }
  </style>

  <rect width="100%" height="100%" class="bg" rx="12"/>

  <!-- moving waves -->
  <g transform="translate(0,220)" class="wave" opacity="0.18">
    <path d="M0 30 Q150 0 300 30 T600 30 T900 30 V60 H0 Z" fill="#38bdf8"/>
  </g>

  <!-- Title -->
  <text x="48" y="110" font-size="36" class="title fade-in delay-1">Python-practice</text>
  <text x="50" y="150" font-size="18" fill="#cfe9ff" class="fade-in delay-2">Practice problems • Algorithms • Small projects</text>

  <!-- typing bar (simulated) -->
  <g transform="translate(48,175)" class="mono">
    <rect x="0" y="-20" width="760" height="36" rx="8" fill="#061025" opacity="0.9"/>
    <text id="typed" x="12" y="6" font-size="16" fill="#bfe6ff">
      <!-- we will create a type-like animation using multiple tspan elements fading in -->
      <tspan class="fade-in delay-1"># solve_two_sum(nums, target) ➜ indices</tspan>
      <tspan x="12" dy="20" class="fade-in delay-2"># complexity: O(n) using hash map</tspan>
    </text>

    <!-- blinking cursor -->
    <rect x="730" y="-14" width="6" height="20" fill="#7dd3fc" class="pulse"/>
  </g>

  <!-- small icons / quick links -->
  <g transform="translate(640,40)">
    <a href="https://github.com/omkarsl/Python-practice">
      <rect x="0" y="0" width="200" height="44" rx="8" fill="#0ea5a4" opacity="0.14"/>
      <text x="16" y="28" font-size="14" fill="#ccfbf1">Open on GitHub →</text>
    </a>
  </g>
</svg>
```

---

## Interactive (no JS) sections

Use collapsible details to make long READMEs feel interactive. Example:

<details>
  <summary>🚀 Quick start</summary>

**Clone & preview locally**

```bash
# clone
git clone https://github.com/omkarsl/Python-practice.git
cd Python-practice

# preview README (simple):
# open README.md in your browser using an editor, or install a local markdown preview extension

# or use a local static server to preview assets:
python -m http.server 8000
# then open http://127.0.0.1:8000 in your browser
```

</details>

---

## Suggestions & extensions

* Add small GIFs for demos of tricky solutions (place in `assets/` and embed as `![demo](assets/demo.gif)`).
* Add GitHub Action badges for test/CI to show repository health.
* Create an `examples/` folder with short Jupyter notebooks; embed preview links.

---

## License

This README template is MIT licensed. Feel free to adapt for your repository.

---

*If you want, I can also generate a second SVG (a compact animated "tech stack" badge), or create a small demo GIF. Tell me which you'd prefer and I'll add it.*
