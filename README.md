# Graph Animation — Unit Circle → Waves

Fully self-contained, offline-capable visualization. Works on GitHub Pages, local file open, or as email zip.

## Features
- **Unit circle** (black, turns light gray when sine off) with rotating radius (light blue) and dark blue dot
- **Waves 0 → 6π** (3 cycles) synced to dot height, scrolling procedurally
- **Rate slider**: 0 → 1 Hz (0 = frozen, 0.5 Hz = 2s period default), 220px long for easy control, double-click to reset
- **Controls stacked vertically**:
  - **Sine On/Off** — hides blue sine wave, grays circle (circle always visible)
  - **Square** — axis-aligned inscribed square (green) + green intersection dot + green clipped wave, rotation slider -180°→+180° (clockwise right, 160px long)
  - **Triangle** — equilateral triangle (orange) + orange dot + wave, rotation slider
  - **Square Wave** (purple) — `y = A·sign(sinθ)`, shape = two horizontal lines `y=±A`, dot jumps top/bottom
  - **Sawtooth** (red) — `y = A·(θ mod 2π / π -1)`, diagonal hint shape
  - **Ellipse** (teal) — inscribed ellipse `a=R`, `b=R·√(1-e²)` with sliders for **eccentricity** `0→0.95` and **rotation** `-180°→+180°`, intersection `t = 1/√(cos²(θ-φ)/a² + sin²(θ-φ)/b²)`

All sliders are longer (rate 220px, rotation/eccentricity 160px) for easier control. Double-click any slider control to reset.

## Run locally
```bash
open index.html
```

## GitHub Pages
Push `index.html` to repo root:
```bash
cd graph_animation
git add index.html README.md
git commit -m "Update viz"
git push
```
Enable Pages: Settings → Pages → Deploy from branch → `main` / root.

## Offline / Zip
No CDN: system fonts only, `html2canvas` removed. Zip folder and email:
```bash
zip -r graph_animation.zip graph_animation
```

Generated 2026-07-15 — offline build, no external deps.
