# Gully Ka Badshah 🛺

A desi endless runner game with a behind-the-player pseudo-3D perspective. Runs on Android and Windows browsers, supports touch and keyboard, and saves the best score locally.

## Features
- Three-lane endless runner
- Auto-rickshaws, cows, potholes, barriers, bicycles and wedding banners
- Coins and chai boost
- Keyboard and touchscreen controls
- Local high-score saving
- PWA manifest and service worker for offline caching after the first visit
- No external game libraries, fonts, image CDNs, or APIs

## Run locally
Open `index.html` in a modern browser. The game works as a local HTML file. Service-worker/PWA installation requires HTTPS or localhost.

## Publish as a website
This repository includes a GitHub Actions workflow at `.github/workflows/pages.yml`.

1. Create a new **public** GitHub repository named `gully-ka-badshah`.
2. Upload all files from this folder, including the hidden `.github` folder, to the repository's `main` branch.
3. In GitHub, open **Settings → Pages** and ensure publishing via **GitHub Actions** is selected if prompted.
4. Wait for the Actions workflow to finish. Your game will be available at:
   `https://YOUR-GITHUB-USERNAME.github.io/gully-ka-badshah/`

## Embed the game in Framer
After GitHub Pages is live:
1. Add an **Embed** component to your Framer page.
2. Use an iframe with the published URL. Example:

```html
<iframe
  src="https://YOUR-GITHUB-USERNAME.github.io/gully-ka-badshah/"
  title="Gully Ka Badshah"
  width="100%"
  height="720"
  style="border:0;border-radius:16px;overflow:hidden"
  allow="fullscreen"
></iframe>
```

Use your actual published GitHub Pages URL. Set the Framer embed to a responsive width and a height suitable for mobile and desktop.

## Offline note
The game code itself is self-contained. The PWA service worker caches the game shell when the player first opens it over HTTPS. Offline play works on the same browser/device after that successful first visit; an embedded Framer page itself may still need internet, while a separately installed PWA can launch from its cached files.
