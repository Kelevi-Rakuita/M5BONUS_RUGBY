# M5BONUS — Rugby Sevens MVP (v2, Encabulation-First)

**Date:** 2025-11-07  
**Author:** Kel (Kelevi Rakuita)

This re-do delivers a cleaner UI and deeper rugby logic while staying single-file and submission-ready.

---

## 0) Encabulation (Plan → Build → Iterate)

### Problem & User Story
- **Problem:** The first MVP worked, but gameplay depth and clarity could be better.
- **User Story:** *As a player,* I want meaningful choices (risk/reward), readable state (stamina, momentum, territory), and rugby-feeling outcomes (penalties, turnovers, conversions).

### Constraints
- One HTML file, vanilla JS/CSS.
- ~300–450 lines core logic, well-commented.
- 2 x 7 “turn-minutes” halves (abstracted time).

### Acceptance Criteria
- Runs locally; obvious controls.  
- Actions with distinct tradeoffs: **Crash, Switch Pass, Chip & Chase, Box Kick to Touch, Offload**.  
- Stats surfaced: **Stamina**, **Momentum**, **Territory**.  
- Realistic outcomes: knock-on, forward pass, **penalties** (offside/holding on), **lineout from touch**, **sin-bin** chance on repeated penalties.  
- Opponent AI adapts to score/time.  
- **Conversion** timing mini-game.  
- Clear match log + halftime + full time.

### Risks & Mitigations
- Complexity overload → tooltips + log detail.  
- Balance issues → momentum caps, stamina effects kept mild.  
- Random feel → show meters and cause text every play.

### Milestones
1. **M1 — UI & State** (scoreboard, options, log).  
2. **M2 — Core Loop** (actions, AI, scoring, penalties, lineout).  
3. **M3 — Polish** (conversion UX, tooltips, balance tweaks).

---

## Iterations (Commit Notes)

### ✅ Iteration 1 — New UI + Options
- Theme refresh, added **Team Select** and **Difficulty** (Casual / Standard / Elite).  
- Stamina and Momentum surfaced with badges.

### ✅ Iteration 2 — Deeper Rugby Logic
- Actions: **Crash**, **Switch Pass**, **Chip & Chase**, **Box Kick (to touch)**, **Offload** (contextual).  
- **Penalties** (holding on, offside) and **lineout** from touch; small **sin-bin** on repeat infringements.  
- AI adapts: chases game when behind, plays territory when ahead.

### ✅ Iteration 3 — Polish & Balance
- Conversion timing bar improved; disabled inputs during AI/animation.  
- Stamina influences meters and error rate; momentum capped (−2..+2).  
- Copy tweaks for clarity; responsive styling.

---

## How to Run
1. Open `rugby_sevens_v2.html` in a modern browser.  
2. Choose **team** and **difficulty**, then **Kickoff**.  
3. Use actions on your possession; AI attacks on theirs.  
4. Score tries (+5) and nail conversions (+2). Highest score at full time wins.

---

## Suggested Git (3+ commits today)
```bash
git init
git add .
git commit -m "M5BONUS: Iteration 1 — v2 UI + options"
git commit -m "M5BONUS: Iteration 2 — actions, AI, penalties, lineout"
git commit -m "M5BONUS: Iteration 3 — balance + polish + conversion UX"
git branch -M main
git remote add origin YOUR_GITHUB_REPO_URL
git push -u origin main
```

---

## Files
```
M5BONUS_RUGBY_V2/
├─ README.md
└─ rugby_sevens_v2.html
```
