# Universal Download Link — demo

A **standalone, dependency-free** demo of GoBrain's one-link / one-QR app download.

The live feature: a single URL — `https://gobrain.fighttech.vn/get/` — and a single QR
code that auto-detect the visitor's platform and forward them to the right store
(App Store on iOS, Google Play on Android; desktop gets a chooser).

## Run it

It's a single self-contained `index.html` — no build, no `npm install`, no external
CSS/JS/fonts, no network requests. Either:

- **Double-click `index.html`** to open it in any browser, or
- Serve the folder: `python3 -m http.server 5601` then open <http://localhost:5601/>
  (also available as the `demo-universal-download` launch config).

## What it shows

- An interactive **platform simulator** (iPhone / Android / Desktop) showing exactly
  where `/get/` would send each device.
- Live detection of **your** current device using the same logic as production.
- The **shared QR code** (encodes `gobrain.fighttech.vn/get/`).
- The detection snippet, for reference.

## Source of truth

This demo is a self-contained copy for showcasing. The real implementation lives in
the landing site: `landing/get/index.html` (redirect page) and the QR on
`landing/download/index.html`.
