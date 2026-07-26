# Neon Dasher

A fast-paced, single-file browser game built with vanilla JavaScript and HTML5 Canvas.

## 🎮 Play

[Live Demo](https://enricjake.github.io/Neon-Dasher/)

## 🚀 Quick Start

No build step, no dependencies, no installation required.

1. Clone the repo
2. Open `index.html` in your browser
3. Play!

## 📁 Project Structure

```
Neon-Dasher/
├── index.html    # Entire game (HTML + CSS + vanilla JS canvas)
└── README.md     # This file
```

**Note:** Edit only `index.html` — the entire game lives in this single file.

## 🎯 How to Play

- **Controls:** Touch drag, tap, Space bar, or click to move vertically
- **Goal:** Dodge obstacles scrolling from the right
- **Difficulty:** Speed increases progressively as you score
- **Game Over:** Collision with any obstacle ends the run

## 🛠️ Development

### Local Testing
Simply open `index.html` directly in a browser — no server needed.

### Deployment
The site is hosted on GitHub Pages from the `main` branch. Any push to `main` auto-deploys (legacy Pages build type).

**Important:** The file MUST stay named `index.html` at repo root — Pages serves that path as the site root.

## 🏗️ Game Architecture

- **Rendering:** HTML5 Canvas with `requestAnimationFrame` loop
- **No server:** Runs entirely in-browser; no assets, no imports
- **Player:** Fixed at left (`x=50`); obstacles scroll left
- **Movement:** Vertical only (touch drag / tap / Space / click)
- **Difficulty:** Scales with `speed` (increments every frame); spawn rate derives from `speed`
- **Responsive:** Canvas resizes to full viewport; player Y recenters when game stops

## 📝 License

MIT
