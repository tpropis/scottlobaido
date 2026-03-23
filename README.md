# Scott LoBaido — Cinematic Hero Page

An unsolicited redesign gift for [scottlobaido.com](https://scottlobaido.com) — hero section only.

## Setup

Place the following files in `assets/` before opening in a browser:

| File | Description |
|---|---|
| `assets/scott.png` | Portrait photo (transparent background) |
| `assets/logo.png` | "American Artist Scott LoBaido" logo (white on transparent) |

Then open `index.html` directly in any modern browser — no server required.

## What It Does

On page load, the hero runs a cinematic opening-title sequence:

1. **Page starts pure black**
2. **13 stripes paint themselves** left-to-right using SVG `clip-path` animation — each stripe staggers slightly after the previous, simulating a brush moving across canvas. Red stripes carry a fractal-noise displacement filter for a painted, textured edge.
3. **Blue canton fades in** after stripes complete
4. **50 stars stagger in** inside the canton using official US flag proportions
5. **Scott's portrait fades in** center-right, layered above the flag
6. **Logo fades in** bottom-left, last

Total sequence: ~8 seconds.

## Technical

- Single `index.html` — fully self-contained
- Vanilla HTML, CSS, and JS — zero frameworks, zero CDN, zero dependencies
- SVG flag with `feTurbulence` + `feDisplacementMap` filter for brushstroke texture
- Animated film-grain overlay generated via `<canvas>` at runtime
- Cinematic radial vignette (dark edges, open toward Scott)
- Flag slightly scaled and rotated for dramatic composition
- Mobile responsive — portrait and logo reflow to centered stack on narrow screens

## Colors

| Element | Hex |
|---|---|
| Red stripes | `#B22234` |
| Blue canton | `#3C3B6E` |
| Cream stripes | `#EDE5CC` |
| Stars | `#FFFFFF` |
