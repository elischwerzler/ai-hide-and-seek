# AI Hide & Seek 3D

A 3D browser game where you watch AI bots play hide-and-seek — or jump in and play yourself.

**▶ Play it:** https://elischwerzler.github.io/ai-hide-and-seek/

Single self-contained HTML file. No build step, no install — just open it.

## What it does

- **Seekers** (red) hunt with a 160° vision cone, **pathfind** around walls, sweep the arena in patrol lanes, split up so they don't dogpile, sense hiders right next to them, and pounce to tag.
- **Hiders** (green) have their own short-range vision cone, **flee and re-hide** when they spot a seeker, and tuck into cover (behind walls and ramps) when it's safe.
- **Obstacles:** push movable **crates**, break line-of-sight behind **ramps**.
- Each bot has a **name and a win/loss record** that persists in your browser.

## Play it yourself (desktop)

Click **Play Hider** or **Play Seeker** to drop into first-person:

- **W / S** — walk forward / back
- **A / D** — turn
- **Right-click** — lock the mouse to look around (right-click again to unlock)

You only see your own vision cone. Hider: survive the round using cover. Seeker: tag every hider.

> Best on desktop (keyboard + mouse). On phones you can watch the AI, but not play first-person.

## Watch & tune

- **1× / 4× / ⚡ Train** — playback speed.
- **+ / −** — change how many hiders and seekers are on the field. **4 hiders vs 1 seeker** is the balanced default; add seekers for a tougher hunt.
- Click any bot to inspect it.

## Tech

Pure HTML/JS + [Three.js](https://threejs.org/) (loaded from a CDN) for the 2.5D isometric 3D rendering. The bots run on hand-coded "instinct" AI: BFS pathfinding, vision/line-of-sight raycasting, systematic search memory, and flee/cover logic.

Built with [Claude Code](https://claude.com/claude-code).
