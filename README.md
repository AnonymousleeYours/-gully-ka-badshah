# Gully Ka Badshah

A mobile-first Three.js endless runner with procedural street scenery, an articulated player, three lanes, hazards, coins, timed power-ups, touch and keyboard input, persistent best score, and pause/restart/game-over flows. The PWA manifest and icon are retained from the existing GitHub project.

## Run locally

Serve this folder over HTTP so the browser can load the JavaScript module and Three.js import map:

```sh
python -m http.server 8000
```

Then open `http://localhost:8000`. Three.js 0.170.0 is pinned in the import map and loaded from jsDelivr; Google Fonts are also loaded by the stylesheet. Gameplay models and effects are generated locally in code, so no model or texture download is required. The game needs an internet connection on first load because Three.js is hosted by the CDN.

## Controls

- Swipe left/right or use **←/→** and **A/D** to change lanes.
- Swipe up or use **↑**, **W**, or **Space** to jump.
- Swipe down or use **↓** or **S** to slide.
- Use **P** or **Escape** to pause.

The game stores the best score in browser local storage. Use the in-game sound toggle to enable or mute synthesized effects. The service worker caches the local app shell for repeat visits; Three.js itself is not bundled locally, so offline startup is not guaranteed.

