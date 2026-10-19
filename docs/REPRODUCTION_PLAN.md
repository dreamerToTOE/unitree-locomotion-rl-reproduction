# Reproduction Execution Plan / 分阶段复现计划

**Project:** Unitree Go2 PPO locomotion + MuJoCo Sim2Sim, optional G1
**Status:** PLANNED; no results have been executed or validated.

## Prior-learning checkpoint (required before coding)
Produce an explanation of (1) scientific/engineering problem; (2) main solution and why; (3) innovations vs baselines; (4) full published experiments; (5) which parts are reproducible from open source; (6) proposed numerical simulation scope. Do not silently omit experiments and do not claim original quantitative reproduction based on simulation visuals alone.

## Gates
- **U0** — dependencies: record setup and acceptance evidence in docs/PROGRESS.md; if incomplete mark BLOCKED with cause.
- **U1** — environment smoke: record setup and acceptance evidence in docs/PROGRESS.md; if incomplete mark BLOCKED with cause.
- **U2** — PPO: record setup and acceptance evidence in docs/PROGRESS.md; if incomplete mark BLOCKED with cause.
- **U3** — tracking: record setup and acceptance evidence in docs/PROGRESS.md; if incomplete mark BLOCKED with cause.
- **U4** — randomization: record setup and acceptance evidence in docs/PROGRESS.md; if incomplete mark BLOCKED with cause.
- **U5** — Sim2Sim: record setup and acceptance evidence in docs/PROGRESS.md; if incomplete mark BLOCKED with cause.
- **U6** — optional G1: record setup and acceptance evidence in docs/PROGRESS.md; if incomplete mark BLOCKED with cause.

## Project-specific actions
1. Check current pinned Unitree RL Lab build against Isaac Lab, Isaac Sim and RTX 4070 GPU/driver. Do not assume official README versions fit local hardware.
2. Inspect Go2 articulation, PD gains, action decimation, default joint poses, observation/history, randomization and termination conditions.
3. Train the documented PPO velocity command task. Record samples, elapsed wall-clock, episode statistics and seed-specific checkpoints.
4. Evaluate independent command regimes and perturbations; report velocity RMSE, fall/termination rate, torque/action smoothness.
5. Export the policy to MuJoCo and verify observation order, normalization, action scaling, policy timestep and PD loop semantics.
6. Only after Go2 success, study G1 floating-base dynamics and optionally reproduce the documented velocity task.

## Minimum acceptance
- Reproducible pinned source SHA, environment manifest and deterministic smoke test.
- Paper/baseline code map and honest difference log.
- A run manifest for **each** metric or figure; no fabricated results.
- At least 3 random seeds *if computationally feasible*; otherwise explicit budget and uncertainty.
- Held-out evaluation conditions separated from training, raw episodes and summary plots.
- Metrics: command tracking RMSE, episode survival/fall rate, torque proxy, energy, action smoothness.
- Completion report must distinguish validated claims, partial reproductions, extra extensions, and blocked claims.

## Stop/go rules
Stop after three distinct failed attempts on the same blocker; escalate cause and proposed alternatives. Do not silently lower model/environment complexity or invent synthetic 'paper-equivalent' evidence. Prefer numerical simulation verification where physical testing unavailable, clearly labeled. No unapproved long/high-cost runs.
