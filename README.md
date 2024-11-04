# Navigating the Physical World: A Survey of Embodied Navigation
[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
<img src="https://img.shields.io/badge/Contributions-Welcome-278ea5" alt="Contrib"/>

This is a repository of embodied navigation survey **led by MSP group from Shanghai Jiao Tong University**. 

In this repository, you can learn the concept of embodied navigation and find the state-of-the-arts works related to this topic. 

If you find this repository helpful, please consider Stars ⭐ or Sharing ⬆️.


## 1. Embodied Navigation Paradigm and Elements

Embodied navigation (EN) is a novel problem of conducting advanced egocentric navigation tasks through state estimation, task cognition and motion execution for an autonomous robot. Compared with traditional navigation, EN is stressed with the key features of **1) egocentric sensing, 2) interactive engagement with the environment through high degrees of freedom in actions and 3) high-level cognition for complex tasks.**
![image](images/Framework.png)

Recently, an increasing number of works are proposed to solve the problems within the EN system. However, existing studies tend to focus on specific sub-issues, lacking a coherent and unified framework. Consequently, the systematic level and real-world application of EN now remain constrained due to the absence of a comprehensive problem formulation. **To this end, we propose a unified formulation for EN, structured into five stages: transition, observation, fusion, task reward construction and action skills optimization (TOFRA).**


|Embodied Navigation|Traditional Navigation|
|-------------------|----------------------|
|Ego-centric|Global Axis|
|Multi Nodes, n-DoF|Single Node, <=6DoF|
|Evolved Motion Skills|Fixed Movement|
|Autonomous Task Decomposition and Multi-Task Joint Optimization|Manual Task Decomposition for Individual Optimization|
|First Principles|Engineering-Oriented Approach|
|Weak Metricity|Precise Metricity|
|Active Interaction Between Agent and Environment|Passive Perception|

## 2. Summary and Integration of current works into TOFRA

### Space Configuration

| EN Space | Modules | Categories | Algorithm| Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- | --- | --- |
| State Space | Body | Vector | OpenVINS | 2020 | ICRA | [Link](https://ieeexplore.ieee.org/document/9196524) | [Link](https://github.com/rpng/open_vins) |
| State Space | Body | Vector | VINS-Mono | 2018 | TRO | [Link](https://ieeexplore.ieee.org/document/8421746) | [Link](https://github.com/HKUST-Aerial-Robotics/VINS-Mono) |
| State Space | Body | Lie Group | IEKF as a Stable Observer | 2017 | TAC | [Link](https://ieeexplore.ieee.org/document/7523335/authors#authors) | --- |
| State Space | Body | Lie Group | PIEKF-VIWO | 2023 | ICRA | [Link](https://ieeexplore.ieee.org/document/10160380) | --- |
| State Space | Body | Lie Group | Convergence and Consistency Analysis for a 3-D Invariant-EKF SLAM | 2017 | RA-L | [Link](https://ieeexplore.ieee.org/abstract/document/7812660) | --- |
| State Space | Body | Quaternion-Based | A Trident Quaternion Framework for Inertial-Based Navigation Part I: Rigid Motion Representation and Computation | 2022 | TAES | [Link](https://ieeexplore.ieee.org/document/9640520) | --- |
| State Space | Body | Implicit | Towards Versatile Embodied Navigation | 2022 | TAES | [Link](https://ieeexplore.ieee.org/document/9640520) | [Link](https://github.com/hanqingwangai/VXN) |
| State Space | Body | Implicit | Scene Memory Transformer for Embodied Agents in Long Time Horizon Tasks | 2019 | CVPR | [Link](https://openaccess.thecvf.com/content_CVPR_2019/html/Fang_Scene_Memory_Transformer_for_Embodied_Agents_in_Long-Horizon_Tasks_CVPR_2019_paper.html) | --- |
| State Space | Body | Implicit | Zero Experience Required | 2022 | CVPR | [Link](https://ieeexplore.ieee.org/abstract/document/9878587) | [Link](https://github.com/ziadalh/zero_experience_required) |
| State Space | Body | Neuromophic | - | - | - | - | - |
| State Space | Environment | Point Cloud | 3D is here | 2011 | ICRA | [Links](https://ieeexplore.ieee.org/document/5980567) | [Link](https://github.com/PointCloudLibrary/pcl) |
| State Space | Environment | Voxel | Occupancy Networks | 2019 | CVPR | [Links](https://ieeexplore.ieee.org/document/8953655) | [Link](https://github.com/autonomousvision/occupancy_networks) |
| State Space | Environment | Implicit | NeRF-LOAM | 2023 | ICCV | [Links](https://ieeexplore.ieee.org/document/10377635) | [Link](https://github.com/JunyuanDeng/NeRF-LOAM) |
| State Space | Environment | Neuromophic | - | - | - | - | - |
| Action Space | Low-level Control | Ground Wheel Vehicles | Are we ready for autonomous driving | 2012 | CVPR | [Link](https://ieeexplore.ieee.org/document/6248074) | --- |
| Action Space | Low-level Control | Ground Wheel Vehicles | CARLA | 2017 | CARLA | [Link](https://proceedings.mlr.press/v78/dosovitskiy17a/dosovitskiy17a.pdf) | [Link](https://github.com/carla-simulator/carla) |
| Action Space | Low-level Control | UAVs/AUVs | Unmanned Aerial Vehicles (UAVs) | 2019 | IEEE Access | [Link](https://ieeexplore.ieee.org/document/8682048) | - |
| Action Space | Low-level Control | UAVs/AUVs | AUV Navigation and Localization | 2014 | JOE | [Link](https://ieeexplore.ieee.org/document/6678293) | - |
| Action Space | Low-level Control | Legged Robots | ANYmal | 2016 | IROS | [Link](https://ieeexplore.ieee.org/document/7758092) | [Link](https://github.com/ANYbotics) |
| Action Space | Low-level Control | Legged Robots | MIT Cheetah 3 | 2018 | IROS | [Link](https://ieeexplore.ieee.org/document/8593885) | --- |
| Action Space | Low-level Control | Legged Robots | Learning to walk in confined spaces using 3D representation | 2024 | ICRA | [Link](https://arxiv.org/abs/2403.00187) | --- |
| Action Space | Low-level Control | Legged Robots | Learning agile and dynamic motor skills for legged robots | 2019 | Science Robotics | [Link](https://www.science.org/doi/10.1126/scirobotics.aau5872) | --- |
| Action Space | Low-level Control | Legged Robots | Whole-body Humanoid Robot Locomotion with Human Reference | 2024 | arXiv | [Link](https://arxiv.org/abs/2402.18294) | --- |
| Action Space | Low-level Control | Wheel-Legged Robots | Dynamic Hybrid Locomotion and Jumping for Wheeled-Legged Quadrupeds | 2023 | IROS | [Link](https://ieeexplore.ieee.org/document/10341824) | --- |
| Action Space | Low-level Control | Wheel-Legged Robots | Learning robust autonomous navigation and locomotion for wheeled-legged robots | 2024 | Science Robotics | [Link](https://www.science.org/doi/10.1126/scirobotics.adi9641) | --- |
| Action Space | High-level Command Control | Legged Robots | QUAR-VLA | 2024 | arXiv | [Link](https://arxiv.org/abs/2312.14457) | --- |
| Action Space | High-level Command Control | Wheel-Legged Robots | Learning robust autonomous navigation and locomotion for wheeled-legged robots | 2024 | Science Robotics | [Link](https://www.science.org/doi/10.1126/scirobotics.adi9641) | --- |

### Transition (T)

| Transition Levels | Modules | Categories | Algorithm| Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Dynamics | Pre-integration | Trapezoidal | VINS-Mono | 2018 | TRO | [Link](https://ieeexplore.ieee.org/document/8421746) | [Link](https://github.com/HKUST-Aerial-Robotics/VINS-Mono) |
| Dynamics | Pre-integration | Runge-Kutta | OpenVINS | 2020 | ICRA | [Link](https://ieeexplore.ieee.org/document/9196524) | [Link](https://github.com/rpng/open_vins) |
| Dynamics | Pre-integration | Polynomials | iNavFIter | 2020 | TAES | [Link](https://ieeexplore.ieee.org/document/8844820) | [Link](https://github.com/iNavFlight/inav) |
| Dynamics | Dynamics | Wheel Vehicles | --- | 2010 | Ground Vehicle Dynamics | [Link](https://link.springer.com/book/10.1007/978-3-540-68553-1) | --- |
| Dynamics | Dynamics | UAV/AUVs | Modelling, simulation and implementation of a quadrotor UAV | 2013 | ICIIS | [Link](https://ieeexplore.ieee.org/document/6731982) | --- |
| Dynamics | Dynamics | UAV/AUVs | AUV Trajectory Tracking Models and Control Strategies | 2021 | JMSE | [Link](https://www.mdpi.com/2077-1312/9/9/1020) | --- |
| Dynamics | Dynamics | Legged Robots | 56 | --- | --- | --- | --- |
| Dynamics | Dynamics | Wheel-Legged | --- | --- | --- | --- | --- |
| Dynamics | Mult-node | Pedestrian | --- | --- | --- | --- | --- |
| Dynamics | Mult-node | Pedestrian | --- | --- | --- | --- | --- |
| Dynamics | Mult-node | Pedestrian | --- | --- | --- | --- | --- |
| Dynamics | Mult-node | Ground Vehicles | --- | --- | --- | --- | --- |
| Dynamics | Mult-node | Legged Robots | --- | --- | --- | --- | --- |
| Motion Cognition | Stationary Detection | Classic Model | --- | --- | --- | --- | --- |
| Motion Cognition | Stationary Detection | Classic Model | --- | --- | --- | --- | --- |
| Motion Cognition | Stationary Detection | Deep Learning | --- | --- | --- | --- | --- |
| Motion Cognition | Activity Recognition | IMUs Only | --- | --- | --- | --- | --- |
| Motion Cognition | Activity Recognition | IMUs Only | --- | --- | --- | --- | --- |
| Motion Cognition | Activity Recognition | Multi Modalities | --- | --- | --- | --- | --- |
| Motion Cognition | Activity Recognition | Multi Modalities | --- | --- | --- | --- | --- |
| Motion Cognition | Activity Recognition | Multi Modalities | --- | --- | --- | --- | --- |
| Motion Cognition | Activity Recognition | Multi Modalities | --- | --- | --- | --- | --- |
| Motion Cognition | Activity Recognition | Multi Modalities | --- | --- | --- | --- | --- |
| End-to-end | Neural Networks | IMU Denoising | --- | --- | --- | --- | --- |
| End-to-end | Neural Networks | IMU Denoising | --- | --- | --- | --- | --- |
| End-to-end | Neural Networks | IMU Denoising | --- | --- | --- | --- | --- |
| End-to-end | Neural Networks | IMU Denoising | --- | --- | --- | --- | --- |
| End-to-end | Neural Networks | Direct End-to-end | --- | --- | --- | --- | --- |
| End-to-end | Neural Networks | Direct End-to-end | --- | --- | --- | --- | --- |
| End-to-end | Neural Networks | Direct End-to-end | --- | --- | --- | --- | --- |

### Observation (O)

### Fusion (F)

### Task Reward Construction (R)

### Action Skills Optimization (A)

## 3. Fundamental Platforms

## Call for Cooperators: Join Us in Advancing Embodied Navigation Research
We are excited to invite researchers and experts in the field of embodied navigation to collaborate on an innovative paper aimed at pushing the boundaries of autonomous navigation systems. Our goal is to explore the intersection of interactive perception, neuromorphic cognition, and evolutionary motion capabilities in the development of cutting-edge embodied navigation systems.(Contact: sjtu4742986@sjtu.edu.cn)

