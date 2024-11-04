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

| Reference | EN Space | Modules | Categories | Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- | --- | --- |
| OpenVINS | State Space | Body | Vector | 2020 | ICRA | [Link](https://ieeexplore.ieee.org/document/9196524) | [Link](https://github.com/rpng/open_vins) |
| VINS-Mono | State Space | Body | Vector | 2018 | TRO | [Link](https://ieeexplore.ieee.org/document/8421746) | [Link](https://github.com/HKUST-Aerial-Robotics/VINS-Mono) |
| IEKF as a Stable Observer | State Space | Body | Lie Group | 2017 | TAC | [Link](https://ieeexplore.ieee.org/document/7523335/authors#authors) | --- |
| PIEKF-VIWO | State Space | Body | Lie Group | 2023 | ICRA | [Link](https://ieeexplore.ieee.org/document/10160380) | --- |
| Convergence and Consistency Analysis for a 3-D Invariant-EKF SLAM | State Space | Body | Lie Group | 2017 | RA-L | [Link](https://ieeexplore.ieee.org/abstract/document/7812660) | --- |
| A Trident Quaternion Framework for Inertial-Based Navigation Part I: Rigid Motion Representation and Computation | State Space | Body | Quaternion-Based | 2022 | TAES | [Link](https://ieeexplore.ieee.org/document/9640520) | --- |
| Towards Versatile Embodied Navigation | State Space | Body | Implicit | 2022 | TAES | [Link](https://ieeexplore.ieee.org/document/9640520) | [Link](https://github.com/hanqingwangai/VXN) |
| Scene Memory Transformer for Embodied Agents in Long Time Horizon Tasks
 | State Space | Body | Implicit | 2019 | CVPR | [Link](https://openaccess.thecvf.com/content_CVPR_2019/html/Fang_Scene_Memory_Transformer_for_Embodied_Agents_in_Long-Horizon_Tasks_CVPR_2019_paper.html) | --- |

| EN Space | Modules | Categories | Reference | Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- | --- | --- |
| State Space | Body | Vector | OpenVINS | 2020 | ICRA | [Link](https://ieeexplore.ieee.org/document/9196524) | [Link](https://github.com/rpng/open_vins) |
| State Space | Body | Vector | VINS-Mono | 2018 | TRO | [Link](https://ieeexplore.ieee.org/document/8421746) | [Link](https://github.com/HKUST-Aerial-Robotics/VINS-Mono) |
| State Space | Body | Lie Group | IEKF as a Stable Observer | 2017 | TAC | [Link](https://ieeexplore.ieee.org/document/7523335/authors#authors) | --- |
| State Space | Body | Lie Group | PIEKF-VIWO | 2023 | ICRA | [Link](https://ieeexplore.ieee.org/document/10160380) | --- |
| State Space | Body | Lie Group | Convergence and Consistency Analysis for a 3-D Invariant-EKF SLAM | 2017 | RA-L | [Link](https://ieeexplore.ieee.org/abstract/document/7812660) | --- |
| State Space | Body | Quaternion-Based | A Trident Quaternion Framework for Inertial-Based Navigation Part I: Rigid Motion Representation and Computation | 2022 | TAES | [Link](https://ieeexplore.ieee.org/document/9640520) | --- |
| State Space | Body | Implicit | Towards Versatile Embodied Navigation | 2022 | TAES | [Link](https://ieeexplore.ieee.org/document/9640520) | [Link](https://github.com/hanqingwangai/VXN) |
| State Space | Body | Implicit | Scene Memory Transformer for Embodied Agents in Long Time Horizon Tasks | 2019 | CVPR | [Link](https://openaccess.thecvf.com/content_CVPR_2019/html/Fang_Scene_Memory_Transformer_for_Embodied_Agents_in_Long-Horizon_Tasks_CVPR_2019_paper.html) | --- |

### Transition (T)

### Observation (O)

### Fusion (F)

### Task Reward Construction (R)

### Action Skills Optimization (A)

## 3. Fundamental Platforms

## Call for Cooperators: Join Us in Advancing Embodied Navigation Research
We are excited to invite researchers and experts in the field of embodied navigation to collaborate on an innovative paper aimed at pushing the boundaries of autonomous navigation systems. Our goal is to explore the intersection of interactive perception, neuromorphic cognition, and evolutionary motion capabilities in the development of cutting-edge embodied navigation systems.(Contact: sjtu4742986@sjtu.edu.cn)

