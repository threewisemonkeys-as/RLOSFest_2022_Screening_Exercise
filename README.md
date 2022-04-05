# RLOSFest 2022 Screening Exercise


## What compiler optimization tasks do you want to tackle and why?


As part of the project, I want to build agents to tackle the [`LLVM`](https://compilergym.com/llvm/index.html) optimisation environment in `CompilerGym`. 
This environment essentially encapsulates a sequential decision making problem in which the agent has to generate a sequence of optimisation transforms for a given input program that optimises for some objective.
Useful objectives could include 
- Minimising IR Instruction Count (cheap to evaluate)
- Minimising Memory used during runtime (expensive to evaluate)
- Minimising runtime (expensive to evaluate)
- A learned metric that takes as input some program representation and outputs estimated runtime (cheap to evaluate during test time)

The main reasons for tackling this particular task are
- It can be naturally modelled as a sequential decision making problem which allows us to use a large range of tools from _search_ to _reinforcement learning_
- Preliminary results from the `CompilerGym` leaderboard show that significant gains over the default `-O3` flag are possible even using random search (e.g. 1.5x for `sha`). This shows promise for a learning based method which understands input program semantics to give significant gains over default confguration. Such a tool could have a massive impact even if it gives consisitent fractional improvemnent since LLVM is used across the industry.

## Links to past coding project in Python or C++

### Open Source - 

1. [GenRL](https://github.com/SforAiDl/genrl): PyTorch Reinforcement Learning Library
   - Contributed implementations of various Deep Contextual Bandits
   - Core Maintainer and worked on implementation of [distributed RL](https://github.com/threewisemonkeys-as/genrl/tree/distributed/genrl) using RPC
2. [Trotbot](https://github.com/ERC-BPGC/Trotbot): Autonomous Delivery Robot
   - Built obstacle detection and path planning stack using Robot Operating System (ROS) in Python
   - Implemented Rapidly Exploring Random Trees (RRT) for path planning in complex indoor environments
3. [GenNav](https://github.com/ERC-BPGC/gennav): Python library for Robotics Navigation
   - Co-author and Lead Maintainer working with a team of 10+ student contributors
   - Modular collection of navigation algorithms and utilities commonly used in Robotics with a ROS wrapper


### Personal Projects (also open source) -

1. [Causal Reasoning from Meta-Reinforcement Learning Exploration](https://github.com/threewisemonkeys-as/causal-meta-rl/)
   - Devised, performed and documented additional experiments to futher evaluate the central claim that Meta RL
agents can performs Causal Inference
2. [Torched Impala](https://github.com/threewisemonkeys-as/torched_impala): Attempt at implemented distributed deep RL in PyTorch
3. [Drone Controller Wrapper using MAVROS and PX4](https://github.com/threewisemonkeys-as/drone_automation)
