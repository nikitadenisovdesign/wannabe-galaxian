# WANNABE — Galaxian 👾

A polished, single-file arcade clone of the classic **Galaxian** — but instead of alien ships, you're blasting stylized **WANNABE** logo marks out of the sky. Built with vanilla HTML5 Canvas + Web Audio. No build step, no dependencies.

## Play

Just open `index.html` in any modern browser, or serve the folder:

```bash
python3 -m http.server 8753
# then open http://localhost:8753
```

## Controls

| Action | Key | Touch |
| --- | --- | --- |
| Move | ◀ / ▶ arrows | on-screen pad |
| Fire | `Space` | ✦ button |
| Pause | `P` | — |
| Sound on/off | `M` | 🔊 button (top-right) |
| Start / Restart | `Space` / tap | tap |

## Features

- 🛸 **Authentic Galaxian formation + dive attacks** — enemies swoop down in bézier-curve arcs and fire at you. Shooting a diver scores **double**.
- 🌊 **Endless escalating waves** — clear the screen and a fresh wave *flies in* in formation, with the yellow flagship row growing each time (2 → 4 → 6 … up to a full row).
- 🏆 **Local leaderboard** — beat a top-8 score and enter your name; high scores persist in `localStorage` and show on the splash + game-over screens.
- 🌈 **WANNABE wordmark splash** styled like the Galaxian title screen (rainbow arc + starburst).
- 👾 **Enemies are the WANNABE logo mark** (the real SVG), color-tiered like the original arcade: gold flagships, red, purple, and three teal rows.
- 🔊 **Fully synthesized sound** via Web Audio — shooting, explosions, dive sirens, the bouncy bass loop, extra-life and stage-clear jingles.
- ✨ Particle explosions, screen shake, hit flash, scrolling starfield, floating score popups.
- 💯 Hi-score saved to `localStorage`, extra life at 5,000 pts, escalating difficulty per stage.
- 🖥️ **True fullscreen** — the playfield adapts to any aspect ratio edge-to-edge (no letterboxing, no distortion); the logo is the splash hero, then docks to the top-left corner in-game.
- 📱 Responsive on desktop and mobile, with on-screen touch controls.

## Scoring

| Enemy | Points |
| --- | --- |
| 🟡 Flagship | 200 |
| 🔴 Red | 150 |
| 🟣 Purple | 80 |
| 🟦 Teal | 60 |

*Divers are worth 2×.*

## Tech

Everything lives in **`index.html`** — markup, CSS, and the game engine. The enemy sprite is drawn straight from the `wannabe-logo.svg` path data via `Path2D`. The title wordmark is inline SVG. ~600 lines, zero dependencies.

---

🤖 Built with [Claude Code](https://claude.com/claude-code)
