# Characterizing the performance of a deep reinforcement learning framework for skid-steered visual navigation
Curated code repository for training and evaluation of visual navigation framework for skid-steerd robots with deep reinforcement learning. 
Paper Link : [Arxiv Paper link]


![HuskyVSOverview](https://github.com/ARMLabCUICAR/SkidSteerVisualNavigation/assets/54649022/a7831e5e-df6f-416b-8f5d-d3fe02486c00) ![2024-02-17 23-45-53](https://github.com/ARMLabCUICAR/SkidSteerVisualNavigation/assets/54649022/b84a4ed1-c5dc-445d-92d0-661c2839920e)


## Pre-requisites :
The deep reinforcement learning (DRL) training requires following pre-requistes to be installed:
1. CoppeliaSim robotics simulator - A multibody robot dynamics simulator used as a gym environment for DRL training. (https://www.coppeliarobotics.com/)
2. StableBaselines3 reinforcement learning libraries for training with proximal policy opimization (PPO agent) (SB3 and associated libraries have be enlisted as a conda environment file in the repo as Husky_CS_SB3.yml . Users may choose to directly install this environment to install all the necessary python libraries)
3. Konsole terminal emulator to spawn multiple environments simultaneously for parallelized training.

## File discriptions :
### HuskyCP-gym
Learning gym environment setup as a python package. Installing and sourcing this package will register the learning environment as a gym environment.

### HuskyInfinityGym.ttt
CoppeliaSim scene file containing Clearpath Husky Robot with a visually rederable path.

### exec_parallel.sh
A shell script to spawn multiple instances of the same training environments for parallelized training. Users may choose to spawn as many environments as the total logical cores on their computers. This code has been tested on upto 32 parallel environments on academic compute cluster. Note : All environments are intialized on distinct ports which all for correct connection between the training algorithm and the environment.

### train_parallel.py
Python file that starts the training and saves the agent as a '.zip' folder that can be evaluated as well as deployed on actual robot by installing the SB3 library.

## Parallel training instance :
(For visual appeal shown only 16 parallel instances by actual training can be scaled for as many logical cores on the computer)

https://github.com/ARMLabCUICAR/SkidSteerVisualNavigation/assets/54649022/a3664bfe-cb15-4805-bf3c-aadc22e0c910


## Simulation evaluation of the trained DRL agent 

https://github.com/ARMLabCUICAR/SkidSteerVisualNavigation/assets/54649022/3abb0a2b-a269-46b9-b523-b87bcb417fe2


## Deployment of the trained agent on actual robot


