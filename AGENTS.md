# AGENTS.md

Single-file static game. No build step, no dependencies, no tests.

## Repo layout

- `index.html` — the entire game (HTML + CSS + vanilla JS canvas). Edit this file only.
- `.juno_task/` — MCP server logs, not source. Do not edit or commit.

## Deploy

Live site is GitHub Pages, served from `main` branch root. Any push to `main` auto-deploys (legacy Pages build type).

- URL: https://enricjake.github.io/Neon-Dasher/
- Repo: https://github.com/enricjake/Neon-Dasher

The file MUST stay named `index.html` at repo root — Pages serves that path as the site root.

## Verification

Open `index.html` directly in a browser, or push to `main` and load the Pages URL. No commands to run.

## Game architecture (non-obvious from the single file)

- Game runs entirely in-browser via `requestAnimationFrame` loop; no server, no assets, no imports.
- Player is fixed at left (`x=50`); obstacles scroll left. Vertical movement only (touch drag / tap / Space / click).
- Difficulty scales with `speed` (increments every frame); spawn rate derives from `speed`.
- Canvas resizes to full viewport; player Y recenters only when game is stopped.
