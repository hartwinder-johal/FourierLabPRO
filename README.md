# Fourier Lab PRO — Release Candidate 1

This is a stabilization milestone based on the existing Fourier Lab PRO v24 prototype.
It preserves the current feature set while separating markup, styles and application logic.

## Run
Open `index.html` in a modern desktop browser. For local hosting, run:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

The current package loads Three.js 0.160.0 and fft.js 4.0.4 from CDNs, so internet
access is needed for those dependencies. If Three.js/WebGL is unavailable, the
existing 2D Fourier renderer and projected 3D fallback remain available.

## Layout
- `index.html` — application markup and dependency loading
- `assets/app.css` — main styles
- `src/app.js` — application logic
- `tests/static_audit.py` — static integrity checks
- `FourierLabPRO_RC1_standalone.html` — portable single-file edition

## RC1 changes
- 3D epicycle wheels are spatial ellipses, not flat circles overlaid on a 2D path.
- The selected depth profile is decomposed into signed-frequency Fourier components.
- Each wheel contributes an XYZ vector to the next wheel.
- The original 2D canvas renderer and epicycle display remain intact.
- WebGL context-loss fallback returns to the projected/2D renderer.
- Uncaught errors and rejected background tasks report in the application status line.
- App source is split into HTML, CSS and JavaScript modules.
- Fractal, generative, parametric, drawing, image, audio, equation and export features
  from the v24 baseline are retained.

## Validation performed
- `node --check src/app.js` passes.
- Static ID audit: no duplicate IDs.
- All literal `$('<id>')` DOM references resolve.
- Three.js, 3D depth coefficients, 3D wheel geometry and fallback code are present.

## Not release-certified yet
A headless Chromium launch in the build environment did not complete within the
20-second test window. Therefore browser interaction tests were not completed.
Before a stable release, test:
1. WebGL startup, orbit/pinch/zoom and context-loss fallback.
2. 2D/3D Fourier reconstruction against known reference curves.
3. Sample sizes 16–4096 and harmonic counts up to 4096 under load.
4. Drawing, skeletonization, image import and text extraction.
5. Audio synchronization and long-duration playback.
6. GIF, video, standalone HTML and equation exports (including expected 3D behavior).
7. Project/settings persistence.
8. Windows packaging and installation.

RC1 is a QA candidate, not a certified final release.