# Skyrift City Flight Simulator (Web)

Browser-based 3D city flight game built as a single `index.html` with Three.js.

## Overview

Fly an aircraft over a procedurally rendered city, steer through rings, and avoid crashing into buildings. Everything (HTML, CSS, game logic) lives in `index.html`; Three.js r183 and its addons are loaded from the jsDelivr CDN via an import map.

## Features (from code)

- Three.js WebGL renderer with shadows, ACES tone mapping, sky (`Sky`), post-processing (bloom, FXAA)
- Main menu with difficulty selection: Normal, Hard, Realistic
- Ring targets, crash detection ("You hit a building"), pull-up warning
- Local high-score leaderboard stored in `localStorage`
- Switchable camera, reset

## Controls

| Input | Action |
|---|---|
| Mouse / Arrow keys | Pitch / roll |
| Shift / Ctrl | Throttle up / down |
| Space or B | Airbrake |
| Z / X (or Q / E) | Yaw |
| C | Change camera |
| R | Reset |

## Running

ES module imports require serving over HTTP (not `file://`):

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

An internet connection is needed to load Three.js and Google Fonts from CDNs.

## Tech Stack

HTML, CSS, JavaScript (ES modules), Three.js 0.183.2.
