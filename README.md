# Characterizing the performance of a deep reinforcement learning framework for skid-steered visual navigation
Curated code repository for training and evaluation of visual navigation framework for skid-steerd robots with deep reinforcement learning. 
Paper Link : [Arxiv Paper link]

<p float="left">
  <img src="https://github.com/ARMLabCUICAR/SkidSteerVisualNavigation/assets/54649022/c4286a95-fe7a-4517-a852-0c6eb4a71c56" width="250" height="350" />
  <img src="https://github.com/ARMLabCUICAR/SkidSteerVisualNavigation/assets/54649022/2cb3169a-839e-42e6-95af-81a98515e7fa" width="250" height="350" /> 
</p>



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


<p float="left">
  <img src="https://github.com/ARMLabCUICAR/SkidSteerVisualNavigation/assets/54649022/f43000c6-a4c4-477c-800f-1e446f3538c6" width="250" height="350" />
  <img src="https://github.com/ARMLabCUICAR/SkidSteerVisualNavigation/assets/54649022/12b81ab0-8fc3-42c9-bae9-b31f347fa77f" width="250" height="350" /> 
</p>


