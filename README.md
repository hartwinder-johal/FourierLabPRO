# Fourier Lab PRO

Fourier Lab PRO turns drawn paths, images and text into animated Fourier reconstructions. It includes 2D and 3D views, a collection of curve generators, equation tools and pattern-driven audio.

## Get started

Open `index.html` in a current desktop browser. For local hosting, run:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

The application loads Three.js 0.160.0 and fft.js 4.0.4 from public CDNs. An internet connection is needed for those libraries. The 2D renderer and built-in radix-2 FFT fallback remain available if the external libraries cannot be loaded.

## Features

- Fourier epicycle animation with adjustable harmonic count, speed and orientation
- 2D and 3D curve views, including orbit controls
- Classic curves, fractals, generative art and parametric designs
- Freehand drawing, image tracing and text-to-path conversion
- Fourier equations, coefficient data and Desmos parametric export
- Pattern-based audio synthesis with sound controls
- Procedural animated backgrounds
- GIF, video and standalone HTML export

## Project files

- `index.html` — self-contained browser edition and site entry point
- `FourierLabPRO_RC1_standalone.html` — portable single-file build
- `assets/app.css` — interface styles
- `src/app.js` — application logic
- `tests/static_audit.py` — static integrity checks
- `QA_REPORT.md` — current test results and items still requiring hands-on testing

## Current status

This is Release Candidate 1. Static checks pass, but a full browser test pass has not yet been completed. WebGL interaction, numerical FFT accuracy, audio playback, media exports and Windows packaging still need hands-on verification. Review [QA_REPORT.md](QA_REPORT.md) before using this build as a production release.
