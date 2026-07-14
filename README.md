# Unit Circle → Sine Wave (Offline)

Fully self-contained, offline-capable visualization. No internet, no build step, no dependencies.

## Contents
- `index.html` — single-file app (HTML+CSS+JS, Canvas). ~58KB.

## Features
- Unit circle (black, turns light gray when sine off) with rotating radius (light blue) and dark blue dot
- Sine wave 0 → 6π (3 cycles) synced to dot height
- Rate slider: 0 → 1 Hz (0 = frozen, 0.5 Hz = 2s period default)
- Buttons (stacked vertically):
  - **Sine On/Off** — hides wave, grays circle (circle always visible)
  - **Square** — inscribed square (green) + dark green intersection dot + green clipped wave, with rotation slider -180° → +180° (clockwise right)
  - **Triangle** — inscribed equilateral triangle (orange) + dark orange dot + orange wave, with rotation slider
- Play/Pause, dark/light mode toggle (hamburger menu), Print/Save as PDF

## How to run
Just open `index.html` in any modern browser:
```bash
open index.html
# or double-click in Finder
```

## GitHub Pages
1. Create repo, push this folder's contents to `main`
2. Settings → Pages → Deploy from branch → `main` / root
3. `index.html` will be served at `https://<user>.github.io/<repo>/`

## Email / Zip
Zip the folder:
```bash
zip -r unit-circle-offline.zip unit-circle-offline
```
Send the zip — recipient just unzips and opens `index.html`. No install needed.

## Offline note
This build has **no CDN**: Google Fonts replaced by system fonts (`system-ui`, `ui-monospace`), `html2canvas` removed (Save as Image falls back to Print). Works air-gapped.

Generated 2026-07-14
