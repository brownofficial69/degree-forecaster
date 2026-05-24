# Degree Forecaster

A single-file pastel pixel-art academic forecaster. BSc, MSc, and PhD modes — slide your module grades, tick your milestones, see your projected classification update live.

![v0.9](https://img.shields.io/badge/version-0.9-fcf6bd?style=for-the-badge) ![License](https://img.shields.io/badge/license-MIT-b5e48c?style=for-the-badge)

## Features

- **Three degree modes** with the right calculation engine for each:
  - **BSc/BA** — runs both UK methods (100% Year 3 vs 30% Year 2 + 70% Year 3) and awards the higher result automatically.
  - **MSc/MA** — flat average across modules with Distinction / Merit / Pass / Fail bands.
  - **PhD** — milestone checklist with a completion bar instead of a numeric grade.
- **Universal control bar** — add / remove modules, reset the current mode, or wipe all data, from any tab.
- **Live UK university autocomplete** via `universities.hipolabs.com` with an offline fallback list.
- **Auto-save** to `localStorage` on every keystroke and slider drag.
- **Animated pixel cats** on the Forecast tab that swap based on your degree:
  - BSc → graduate cat with mortarboard and diploma
  - MSc → scholar cat with glasses and an open book
  - PhD → doctor cat with a four-corner tam and a thesis stack
  - Failing band → sad rainy cat under a pastel umbrella with a flickering lightning flash
- **Print-to-PDF** export styled for clean monochrome output.
- **8-bit audio synth** built on `AudioContext` — no sample files, all tones generated in-browser.
- **Confetti** on first-class / distinction / completed-doctorate results.

## Run it

Open `index.html` directly in any modern browser. No build step, no server required — Tailwind, the Press Start 2P / VT323 fonts, and `canvas-confetti` all load from CDN.

```bash
# Or serve it if you want a local dev URL
python -m http.server 5500
# then visit http://localhost:5500
```

## GitHub Pages

This repo is set up to deploy as-is: enable **Settings → Pages → Deploy from branch → `main` / root** and the live forecaster will be served at the repo's Pages URL.

## Stack

- HTML5 + vanilla JavaScript (no framework)
- [Tailwind CSS](https://tailwindcss.com/) (CDN)
- [canvas-confetti](https://github.com/catdad/canvas-confetti)
- Google Fonts: Press Start 2P, VT323
- Inline SVG pixel art (`shape-rendering="crispEdges"`)

## Storage

State persists under the `localStorage` key `academicForecasterStateV9`. The **Wipe All** button clears it. Bumping the version suffix in the source is the migration story — old data won't collide with a new schema.

## License

MIT — see [LICENSE](LICENSE).

---

v0.9 | Made by [@brownofficial69](https://github.com/brownofficial69)
