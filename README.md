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
| Dynamics | Dynamics | Legged Robots | Legged Robots | 208 | Springer Handbook of Robotics | [Link](https://link.springer.com/referenceworkentry/10.1007/978-3-540-30301-5_17) | --- |
| Dynamics | Dynamics | Wheel-Legged | Whole-Body MPC and Online Gait Sequence Generation for Wheeled-Legged Robots | 2021 | IROS | [Link](https://ieeexplore.ieee.org/abstract/document/9636371) | --- |
| Dynamics | Mult-node | Pedestrian | Estimating Lower Limb Kinematics Using a Reduced Wearable Sensor Count | 2021 | TBME | [Link](https://ieeexplore.ieee.org/document/9205648) | --- |
| Dynamics | Mult-node | Pedestrian | Estimating Lower Limb Kinematics using Distance Measurements with a Reduced Wearable Inertial Sensor Count | 2020 | EMBC | [Link](https://ieeexplore.ieee.org/document/9175684) | --- |
| Dynamics | Mult-node | Pedestrian | Sensor network oriented human motion capture via
wearable intelligent system | 2021 | IJIS | [Link](https://onlinelibrary.wiley.com/doi/10.1002/int.22689?msockid=21f27229bd326658052c6731bc716797) | --- |
| Dynamics | Mult-node | Ground Vehicles | Multi-aided Inertial Navigation for Ground Vehicles in Outdoor Uneven Environments | 2005 | ICRA | [Link](https://ieeexplore.ieee.org/document/1570846) | --- |
| Dynamics | Mult-node | Legged Robots | MIPO | 2023 | IROS | [Link](https://ieeexplore.ieee.org/document/10342061) | [Link](https://github.com/ShuoYangRobotics/Multi-IMU-Proprioceptive-Odometry) |
| Motion Cognition | Stationary Detection | Classic Model | A Novel Position and Orientation System for Pedestrian Indoor Mobile Mapping System | 2021 | IEEE Sensors Journal | [Link](https://ieeexplore.ieee.org/document/9169888) | --- |
| Motion Cognition | Stationary Detection | Classic Model | A Novel Minimum Distance Constraint Method Enhanced Dual-Foot-Mounted Inertial Navigation System for Pedestrian Positioning | 2023 | IoT-J | [Link](https://ieeexplore.ieee.org/document/10110972) | --- |
| Motion Cognition | Stationary Detection | Deep Learning | AI-IMU Dead-Reckoning | 2020 | TIV | [Link](https://ieeexplore.ieee.org/document/9035481) | [Link](https://github.com/mbrossar/ai-imu-dr) |
| Motion Cognition | Activity Recognition | IMUs Only | MARS | 2021 | IoT-J | [Link](https://ieeexplore.ieee.org/document/9343342) | --- |
| Motion Cognition | Activity Recognition | IMUs Only | Multi-level Contrast Network for Wearables-based Joint Activity Segmentation and Recognition | 2022 | Global Communications | [Link](https://www.semanticscholar.org/paper/Multi-level-Contrast-Network-for-Wearables-based-Xia-Chu/347be659764ae7444330c541508aff1f9e03d2c9) | --- |
| Motion Cognition | Activity Recognition | Multi Modalities | Egocentric Action Recognition by Automatic Relation Modeling | 2023 | TPAMI | [Link](https://ieeexplore.ieee.org/document/9706375) | --- |
| Motion Cognition | Activity Recognition | Multi Modalities | Egocentric Human Activities Recognition With Multimodal Interaction Sensing | 2024 | IEEE Sensors Journal | [Link](https://ieeexplore.ieee.org/document/10387162) | --- |
| Motion Cognition | Activity Recognition | Multi Modalities | EgoHumans | 2023 | ICCV | [Link](https://ieeexplore.ieee.org/document/10377933) | [Link](https://github.com/rawalkhirodkar/egohumans) |
| Motion Cognition | Activity Recognition | Multi Modalities | E2(GO)MOTION | 2022 | CVPR | [Link](https://ieeexplore.ieee.org/document/9879783) | --- |
| Motion Cognition | Activity Recognition | Multi Modalities | Towards Continual Egocentric Activity Recognition | 2023 | TMM | [Link](https://ieeexplore.ieee.org/document/10184468) | --- |
| End-to-end | Neural Networks | IMU Denoising | Denoising IMU Gyroscopes With Deep Learning for Open-Loop Attitude Estimation | 2020 | RA-L | [Link](https://ieeexplore.ieee.org/document/9119813) | --- |
| End-to-end | Neural Networks | IMU Denoising | Deep IMU Bias Inference for Robust Visual-Inertial Odometry With Factor Graphs | 2022 | RA-L | [Link](https://ieeexplore.ieee.org/document/9954167) | [Link](https://github.com/ori-drs/allan_variance_ros) |
| End-to-end | Neural Networks | IMU Denoising | DUET | 2023 | TIM | [Link](https://ieeexplore.ieee.org/document/10225410) | [Link](https://github.com/kk9six/duet) |
| End-to-end | Neural Networks | IMU Denoising | A MEMS IMU Gyroscope Calibration Method Based on Deep Learning | 2022 | TIM | [Link](https://ieeexplore.ieee.org/document/9739788) | --- |
| End-to-end | Neural Networks | Direct End-to-end | A Learning-Based Multi-Node Fusion Positioning Method Using Wearable Inertial Sensors | 2024 | ICASSP | [Link](https://ieeexplore.ieee.org/document/10447298) | --- |
| End-to-end | Neural Networks | Direct End-to-end | IMUPoser | 2023 | CHI | [Link](https://dl.acm.org/doi/10.1145/3544548.3581392) | [Link](https://github.com/FIGLAB/IMUPoser) |
| End-to-end | Neural Networks | Direct End-to-end | Robust Inertial Motion Tracking through Deep Sensor Fusion across Smart Earbuds and Smartphone | 2021 | IMWUT | [Link](https://dl.acm.org/doi/10.1145/3463517) | --- |

### Observation (O)

### Fusion (F)

### Task Reward Construction (R)

### Action Skills Optimization (A)

## 3. Fundamental Platforms

## Call for Cooperators: Join Us in Advancing Embodied Navigation Research
We are excited to invite researchers and experts in the field of embodied navigation to collaborate on an innovative paper aimed at pushing the boundaries of autonomous navigation systems. Our goal is to explore the intersection of interactive perception, neuromorphic cognition, and evolutionary motion capabilities in the development of cutting-edge embodied navigation systems.(Contact: sjtu4742986@sjtu.edu.cn)

