# Upstream & Dependency Audit / 依赖与原始版本锁定

Source: https://github.com/unitreerobotics/unitree_rl_lab
Status: **UNPINNED / 未锁定**, install and experiments not yet executed.

## Setup checklist
- [ ] Read source paper & full README, inspect upstream LICENSE and assets' usage rights.
- [ ] Record exact Git commit SHA (not just branch name) and release/tag.
- [ ] Verify simulator/Python/PyTorch/CUDA/GPU driver compatibility.
- [ ] Verify task names, supported controller/action/observation modes at the selected SHA.
- [ ] Lock all datasets and models with licenses, source URLs, hashes and download policy.
- [ ] Execute the smallest no-training smoke test and record command/log.

## Observed upstream references (not an installed lock)
Isaac Sim 5.1.0 / Isaac Lab 2.3.0 cited by inspected upstream README; verify pinned matching versions, RSL-RL, model assets.

## Risk
RTX 4070 VRAM, driver and CUDA compatibility must be checked before installing.

## Environment lock table
| Component | Version | SHA/hash | License | Evidence/log | Verified |
|---|---|---|---|---|---|
| Upstream | TBD | TBD | TBD | — | No |
| Simulator | TBD | TBD | TBD | — | No |
| RL library | TBD | TBD | TBD | — | No |
| Python/Torch/CUDA | TBD | TBD | — | — | No |
| Model/asset/data | TBD | TBD | TBD | — | No |

Never alter the user's existing dual FR3 Isaac Sim / ROS2 environment to install an incompatible upstream.
