# 🎳👑 Trevor's Bowling (3D)

A 3D bowling game designed by Trevor, where Trevor always wins.

**Play:** https://leelim81.github.io/trevor-bowling/

## How to play
- Type your name, then **slide up the screen to bowl** — aim a little **left/right** to curve it.
- Play as **Trevor** (any capitalization) for **magic strike powers** 👑 — easy strikes,
  combo bonuses, huge scores, and a permanent #1 spot.
- **Everyone else plays real ten-pin bowling**: proper strike/spare scoring, 10th-frame
  fill balls, **max 300**. Flush throws strike; off-aim throws leave pins or gutter.
- Climb the ranks 🥉 Bronze → 🥈 Silver → 🥇 Gold → 💎 Diamond, then check the leaderboard.

## Tech
- **Three.js** (WebGL 3D) + **cannon-es** (physics) — vendored in [`lib/`](lib/) so it's self-hosted.
- A chase camera follows the ball down the lane to the pins, which scatter with real 3D physics.
- Everything else is one `index.html` (HTML + CSS + a module script). No build step.
- Leaderboard is device-local by default; drop a Firebase config into `index.html`
  (`FIREBASE_CONFIG`) to make it worldwide.
- The original 2D version is preserved at [`classic-2d.html`](classic-2d.html).

Made for Trevor 💛
