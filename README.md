# Fourier Lab PRO

Fourier Lab PRO turns drawn paths, images and text into animated Fourier reconstructions. It brings together 2D and 3D visualization, curve generators, equation tools and pattern-driven audio in one browser-based studio.

## Get started

Open `index.html` in a current desktop browser. To serve it locally, run:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

Three.js 0.160.0 and fft.js 4.0.4 are loaded from public CDNs. An internet connection is needed for those libraries. The 2D renderer and built-in radix-2 FFT fallback remain available if the external libraries cannot be loaded.

## Features

- Fourier epicycle animation with adjustable harmonics, speed and orientation
- 2D and 3D curve views with orbit controls
- Classic curves, fractals, generative art and parametric designs
- Freehand drawing, image tracing and text-to-path conversion
- Fourier equations, coefficient data and Desmos parametric export
- Pattern-based audio synthesis and sound controls
- Procedural animated backgrounds
- GIF, video and standalone HTML export

## Project files

- `index.html` — browser edition and site entry point
- `FourierLabPRO_RC1_standalone.html` — portable single-file build
- `assets/app.css` — interface styles
- `src/app.js` — application logic
- `tests/static_audit.py` — static integrity checks
- `QA_REPORT.md` — test results and outstanding checks

## Publish with GitHub Pages

The repository includes a Pages deployment workflow. To enable it, open **Settings → Pages** and set **Build and deployment → Source** to **GitHub Actions**. The workflow will then publish the site on pushes to `main`.

## Current status

This is Release Candidate 1. Tested by Hartwinder Singh. Review [QA_REPORT.md](QA_REPORT.md) for the QA snapshot.
