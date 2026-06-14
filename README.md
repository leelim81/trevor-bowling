# 🎳👑 Trevor's Bowling (3D)

A 3D bowling game designed by Trevor.

**Play:** https://leelim81.github.io/trevor-bowling/

## How to play
- Type your name, then **slide up the screen to bowl** — aim a little **left/right** to curve it.
- **Real ten-pin bowling for everyone**: proper strike/spare scoring, 10th-frame fill balls,
  **max 300**. Flush throws strike; off-aim throws leave pins or gutter. Best score wins.
- Climb the ranks 🥉 Bronze → 🥈 Silver → 🥇 Gold → 💎 Diamond, then check the leaderboard.
- **Modes:** Solo, vs a CPU (Easy/Medium/Hard, random meme names), or **🌐 online multiplayer**
  (create a session, share the link, take turns with up to 4 friends).
- *(Trevor still gets a cosmetic gold ball + 👑 — but no gameplay advantage; everyone's fair.)*

## Tech
- **Three.js** (WebGL 3D) + **cannon-es** (physics) — vendored in [`lib/`](lib/) so it's self-hosted.
- A chase camera follows the ball down the lane to the pins, which scatter with real 3D physics.
- Everything else is one `index.html` (HTML + CSS + a module script). No build step.
- **Worldwide leaderboard** via Firebase Firestore (`FIREBASE_CONFIG` in `index.html`),
  cumulative per player and case-insensitive, with a `SEASON_START` reset cutoff.
  Online multiplayer uses Firestore realtime sessions (a `sessions` collection).
- The original 2D version is preserved at [`classic-2d.html`](classic-2d.html).

Made for Trevor 💛
