# Interview Skills from This Reproduction / 项目关联面试技术栈

**Focus:** 足式运控 + RL / Locomotion
**Target job families:** 足式、人形机器人 RL 运控岗位

## Core required skills
- Floating-base dynamics, contact friction, support constraints
- commanded velocity and observation history
- PPO, domain randomization, actor/critic privileged information
- policy/control rate
- Sim2Sim
- WBC/MPC at concept level

## Portfolio / interview drill
Derive floating-base vs fixed-base equations; explain tracking reward and termination; train Go2 to follow velocity commands and report fall rate; audit observation/action mapping from Isaac Lab to MuJoCo.

## Evidence policy
- Knowledge != implemented code != verified experiment. Demonstrate the exact level using code links and logs.
- Prepare one 3-minute overview and one 15-minute whiteboard walkthrough.
- Be ready to answer: Why this algorithm? Which baselines? What are training and evaluation metrics? How do you debug failures? What is your independent contribution?
- If this remains a numerical simulation, **do not** advertise physical robot experience, Sim2Real transfer or field deployment.

## Links
See [plan](REPRODUCTION_PLAN.md), [experiment matrix](EXPERIMENT_MATRIX.md), [resume evidence](RESUME_EVIDENCE.md).
