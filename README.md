# Space Worm 3D

A browser-based Three.js snake-growth arena set in a cosmic battlefield. Steer a glossy jelly worm, collect energy, bite smaller rivals and swallow celestial bodies that become glowing segments with stackable permanent powers.

## Modes and features

- **Free-for-all** with 12 worms, and **Team Battle** 6 v 6 (Nova vs Ember), 3-minute rounds
- Smart AI rivals with three skill levels
- Hazards: asteroids, gravity wells, and energy gates that flash yellow before going live
- Pickups: magnet, shield, free boost
- Crown bounties, bite combos and callouts
- Stardust cosmetics (skins and boost trails), local records
- Minimap, edible and hazard indicators
- English and Simplified Chinese UI, reduced-motion option
- Mouse, keyboard, gamepad and dual-touch controls
- Synthesized music and sound effects, staged loading

## Controls

| Input | Steer | Boost | Pause |
| --- | --- | --- | --- |
| Mouse | Point | Hold left button | Esc / P |
| Keyboard | A / D or ← / → | Space, W, ↑ or Shift | Esc / P |
| Gamepad | Left stick | A, RB or RT | Start |
| Touch | Drag on left half | Hold BOOST button | Pause button |

## Project layout

```
index.html    The whole game (HTML, CSS and JavaScript in one file)
favicon.svg   Site icon
vercel.json   Vercel headers and URL settings
```

There is no build step. Three.js r149 and the Google Fonts load from CDNs at runtime.

## Deploy on Vercel

1. In Vercel, choose **Add New → Project** and import `Conexantz/spaceworm`.
2. Set **Framework Preset** to **Other**. Leave **Build Command** and **Install Command** empty and **Output Directory** as the default (the repository root).
3. Click **Deploy**. Every push to `main` redeploys automatically.

Or from a terminal with the Vercel CLI:

```bash
npm i -g vercel
vercel        # preview deployment
vercel --prod # production deployment
```

## Run locally

Any static file server works, for example:

```bash
npx serve .
# or
python3 -m http.server 8080
```

## Notes

- Records, stardust, owned cosmetics and settings are saved in the browser's localStorage, per device.
- The opt-in global leaderboard uses claude.ai's shared artifact storage, so it only works when the game is opened on claude.ai. On Vercel the Leaderboard panel says it is unavailable; everything else works.
- Graphics quality (High / Battery) applies after a page reload.
