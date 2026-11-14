# Fourier Lab PRO — Release Candidate 1

A browser-based Fourier drawing, tracing, visualization and sound-synthesis studio.

## Run

Open **[index.html](index.html)** or **[FourierLabPRO_RC1_standalone.html](FourierLabPRO_RC1_standalone.html)** in a modern desktop browser. The root `index.html` is the self-contained build, so GitHub Pages can serve it directly.

Three.js 0.160.0 and fft.js 4.0.4 are loaded from CDNs. Internet access is required for the enhanced WebGL 3D renderer and optimized FFT library; the app retains its 2D renderer and radix-2 FFT fallback.

## Included features

- Fourier epicycle tracing and harmonic controls
- 2D and Three.js-based 3D views
- Fractal, generative-art and parametric curve families
- Freehand drawing, image tracing and text-to-path workflows
- Fourier equation and Desmos parametric export
- Pattern-driven audio synthesis
- Procedural wallpaper backgrounds
- GIF, video and standalone HTML export

## Files in this repository

- `index.html` — self-contained GitHub Pages entry point
- `FourierLabPRO_RC1_standalone.html` — portable standalone build
- `QA_REPORT.md` — validation snapshot and known test gaps

## QA status

RC1 is a QA candidate, not a certified final release. Static checks passed, but full browser interaction, numerical FFT validation, audio, export and Windows packaging tests have not been completed. See [QA_REPORT.md](QA_REPORT.md) before relying on it as a production release.
