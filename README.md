# Unitree Locomotion RL Reproduction | 足式机器人强化学习运控

> Status: **PLANNED / 未开始复现** · Secondary job target: legged/humanoid RL

## Goal
从机械臂控制跨入浮动基座足式机器人：基于 **Unitree RL Lab + Isaac Lab + RSL-RL** 复现 Go2 速度跟踪策略，验证 MuJoCo Sim2Sim；完成后再评估 G1 的课程学习与动作模仿扩展。

Upstream: https://github.com/unitreerobotics/unitree_rl_lab
PPO library: https://github.com/leggedrobotics/rsl_rl
Docs: https://isaac-sim.github.io/IsaacLab/

## What counts as reproduced
A trained policy that is independently evaluated on random velocity commands and perturbations; training parameters, random seeds, env step counts, evaluation protocol, control/action frequency, deployment model, video and raw results must all be recorded. **A pretrained-policy demo is not training reproduction.**

## Milestones
| Gate | Task | Exit criterion |
|---|---|---|
| U0 | License/dependencies/version audit | Pin Unitree/IsaacLab/RSL-RL SHA, GPU compatibility and model asset usage |
| U1 | Go2 environment smoke | Reset/step and inspect observation, action, rewards, terminations, PD interface |
| U2 | Official PPO training | >=3 fixed seeds or explicit compute-limited justification; tensorboard metrics |
| U3 | Go2 velocity tracking evaluation | Track vx/vy/yaw, fall rate, tracking error, energy/proxy, action smoothness |
| U4 | Domain randomization | Friction, mass, motor strength, control latency sensitivity |
| U5 | Sim2Sim MuJoCo | Same exported policy, observation ordering, action scaling and PD dynamics checked |
| U6 | G1 optional | Reproduce a pinned supported G1 velocity task only after Go2 report complete |

## Interview evidence
Explain floating-base vs fixed-base dynamics, contact constraints, action decimation, command-conditioned observations, PPO rollout and GAE, termination bias, domain gap and policy deployment.

## Current state
No training executed, no performance or Sim2Real verified. The upstream README has referenced Isaac Sim 5.1.0 / Isaac Lab 2.3.0 at inspection time; pin a compatible release rather than assuming those versions work on the existing RTX 4070 machine.

## Working documents
- [AGENTS.md](AGENTS.md)
- [docs/REPRODUCTION_PLAN.md](docs/REPRODUCTION_PLAN.md)
- [docs/EXPERIMENT_MATRIX.md](docs/EXPERIMENT_MATRIX.md)
- [docs/PAPER_CODE_ALIGNMENT.md](docs/PAPER_CODE_ALIGNMENT.md)
- [docs/FAILURE_LOG.md](docs/FAILURE_LOG.md)
- [docs/RESUME_EVIDENCE.md](docs/RESUME_EVIDENCE.md)
