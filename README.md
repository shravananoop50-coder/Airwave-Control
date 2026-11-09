# Airwave Control — iPhone PWA starter

## What this build does
- Responsive iPhone-first interface.
- Five-band EQ for audio files played inside this app.
- EQ presets: Flat, Bass Boost, Balanced, Vocal, Treble.
- Demo ANC and Gaming mode controls (visual only).
- PWA manifest and service worker for Home Screen installation/offline shell.

## Important limitations
- iOS Safari does not support Web Bluetooth, so this web app cannot scan/connect to or send commands to the Noise Airwave Max 6.
- ANC, Transparency, Adaptive ANC and Gaming controls are display-only.
- EQ applies only to local audio played inside this app. It cannot change system-wide audio or EQ in Spotify/YouTube/Apple Music.
- The first visit and PWA installation require hosting over HTTPS (localhost is fine for development).

## Run locally on Linux
From this folder:
```bash
python3 -m http.server 8000
```
Open `http://localhost:8000` on the same computer. For iPhone testing, deploy the folder to an HTTPS static host (for example GitHub Pages, Netlify, or Cloudflare Pages).

## Add to iPhone Home Screen
1. Open the deployed HTTPS URL in Safari.
2. Tap Share.
3. Choose Add to Home Screen.
4. Tap Add.

## Project files
- `index.html` — app UI, EQ and player logic
- `manifest.webmanifest` — PWA metadata
- `sw.js` — offline app shell
- `icon-192.png`, `icon-512.png` — app icons
