# Navigating the Physical World: A Survey of Embodied Navigation
[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
<img src="https://img.shields.io/badge/Contributions-Welcome-278ea5" alt="Contrib"/>

This is a repository of embodied navigation survey **led by MSP group from Shanghai Jiao Tong University**. 

In this repository, you can learn the concept of embodied navigation and find the state-of-the-arts works related to this topic. 

If you find this repository helpful, please consider Stars ⭐ or Sharing ⬆️.
## Call for Cooperators: Join Us in Advancing Embodied Navigation Research
We are excited to invite researchers and experts in the field of embodied navigation to collaborate on an innovative paper aimed at pushing the boundaries of autonomous navigation systems. Our goal is to explore the intersection of interactive perception, neuromorphic cognition, and evolutionary motion capabilities in the development of cutting-edge embodied navigation systems.(Contact: sjtu4742986@sjtu.edu.cn)

## 1. Embodied Navigation Paradigm and Elements

### 1.1 Definition
The **Embodied Navigation System** is a fully autonomous navigation system with **Interactive Perception**, **Neuromorphic Cognition**, and **Motion Execution** capabilities.
![image](images/Definition.png)
### 1.2 Embodied Navigation Paradigm
Given an intelligent agent with a certain degree of freedom, which follows specific motion rules and has hardware parameters, equipped with sensors capable of acquiring extensive environmental observations, we aim to establish a differentiable objective function. This function is designed for joint optimization of the state space and motion space, providing outputs for environment state, motion execution, and agent state.
![image](images/Paradigm.png)

The primary characteristic of this paradigm lies in the **joint optimization and solving of the agent's state, environmental state, and agent motion**. In contrast to prior navigation methods that may have focused solely on optimizing the agent's state, or SLAM problems which crucially consider the agent and environment, embodied navigation **additionally optimizes its own motion execution**.
### 1.3 Key Elements of Embodied Navigation

|Embodied Navigation|Traditional Navigation|
|-------------------|----------------------|
|Ego-centric|Global Axis|
|Multi Nodes, n-DoF|Single Node, <=6DoF|
|Evolved Motion Skills|Fixed Movement|
|Autonomous Task Decomposition and Multi-Task Joint Optimization|Manual Task Decomposition for Individual Optimization|
|First Principles|Engineering-Oriented Approach|
|Weak Metricity|Precise Metricity|
|Active Interaction Between Agent and Environment|Passive Perception|



## 2. Interactive Perception

### Surrunding Environment -Task

#### Object Detection

| Algorithm | Modality | Object Type | Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |

#### Place Recognization

| Algorithm | Modality | Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- |
| R2former | Cam | 2023 | CVPR | [Link](https://openaccess.thecvf.com/content/CVPR2023/papers/Zhu_R2Former_Unified_Retrieval_and_Reranking_Transformer_for_Place_Recognition_CVPR_2023_paper.pdf) | [Code](https://github.com/Jeff-Zilence/R2Former) |
| Eigenplaces | Cam | 2023 | ICCV | [Link](https://openaccess.thecvf.com/content/ICCV2023/papers/Berton_EigenPlaces_Training_Viewpoint_Robust_Models_for_Visual_Place_Recognition_ICCV_2023_paper.pdf) | [Code](https://github.com/gmberton/EigenPlaces) |
| Anyloc | Cam | 2023 | RAL | [Link](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10361537) | [Code](https://anyloc.github.io/) |
| Optimal transport aggregation for visual place recognition | Cam | 2023 | ArXiv | [Link](https://arxiv.org/pdf/2311.15937) | [Code](https://github.com/serizba/salad) |
| Seqot | LiDAR | 2022 | TIE | [Link](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9994714) | [Code](https://github.com/BIT-MJY/SeqOT) |
| Lpd-net | LiDAR | 2019 | ICCV | [Link](https://openaccess.thecvf.com/content_ICCV_2019/papers/Liu_LPD-Net_3D_Point_Cloud_Learning_for_Large-Scale_Place_Recognition_and_ICCV_2019_paper.pdf) | |
| Bevplace | LiDAR | 2023 | ICCV | [Link](https://openaccess.thecvf.com/content/ICCV2023/papers/Luo_BEVPlace_Learning_LiDAR-based_Place_Recognition_using_Birds_Eye_View_Images_ICCV_2023_paper.pdf) | [Code](https://github.com/zjuluolun/BEVPlace) |
| Adafusion | Cam-LiDAR | 2022 | RAL | [Link](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9905898) | |
| Mff-pr | Cam-LiDAR | 2022 | ISMAR | [Link](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9995604) | |
| Lcpr | Cam-LiDAR | 2023 | RAL | [Link](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10373064) | |
| Explicit Interaction for Fusion-Based Place Recognition | Cam-LiDAR | 2024 | ArXiv | [Link](https://arxiv.org/pdf/2402.17264) | |


#### Semantic Classification

| Algorithm | Modality | Semantic Type | Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |






### Ego State -Body

#### Wheeled Vehicle

| Algorithm | Modality | Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- |
| Doppler-only Single-scan 3D Vehicle Odometry | Radar | 2023 | ArXiv | [Link](https://arxiv.org/abs/2310.04113) |  |
| PhaRaO | Radar | 2020 | ICRA | [Link](https://ieeexplore.ieee.org/document/9197231/) |  |
| RadarSLAM | Radar | 2020 | IROS | [Link](https://ieeexplore.ieee.org/abstract/document/9341287?casa_token=4_fyBqP1zNMAAAAA:HSNPEsdToMbn01O6omMm5OadK2fAS9Gq__dcFqXpxvIppWtZU-ERASPj-5fgAhotDYvaCOrf5A) |  |
| 4DRadarSLAM | Radar | 2023 | ICRA | [Link](https://ieeexplore.ieee.org/document/10160670/) | [Code](https://github.com/zhuge2333/4DRadarSLAM) |
| LIC-Fusion | Lidar-IMU-Cam | 2019 | IROS | [Link](https://ieeexplore.ieee.org/document/8967746/) |  |
| LIC-Fusion 2.0 | Lidar-IMU-Cam | 2020 | IROS | [Link](https://ieeexplore.ieee.org/abstract/document/9340704) |  |
| Faster-LIO | Lidar-IMU | 2022 | RAL | [Link](https://ieeexplore.ieee.org/abstract/document/9718203) | [Code](http://github.com/gaoxiang12/faster-lio) |
| LOAM | Lidar | 2014 | RSS | [Link](https://www.ri.cmu.edu/pub_files/2014/7/Ji_LidarMapping_RSS2014_v8.pdf) |  |
| LeGO-LOAM | Lidar | 2018 | IROS | [Link](https://ieeexplore.ieee.org/document/8594299) |  |


#### Drone

| Algorithm | Modality | Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- |
| Fast-LIO | Lidar-IMU | 2021 | RAL | https://ieeexplore.ieee.org/abstract/document/9372856 | https://github.com/hku-mars/FAST_LIO |
|  |  |  |  |  |  |

#### Legged Robot

| Algorithm | Modality | Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- |
| Direct LiDAR Odometry | LiDAR | 2022 | RAL | https://ieeexplore.ieee.org/document/9681177 |  |
|  |  |  |  |  |  |

#### Humanoid/Human

| Algorithm | Modality | Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |
|  |  |  |  |  |  |


### Collabrative Sensing -View

#### Sky-Ground

| Algorithm | Modality | Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |
|  |  |  |  |  |  |

#### Sky-Sky

| Algorithm | Modality | Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |
|  |  |  |  |  |  |

#### Ground-Ground

| Algorithm | Modality | Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |
|  |  |  |  |  |  |

## 3. Advanced Cognition

### Global/Local Space -Representation

#### Point

| Algorithm | Based Structure | Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- |
| Point Cloud Library (PCL)  | Point cloud | 2011 | ICRA | [link](https://doi.org/10.1109/ICRA.2011.5980567) |  |
| PointNet | Point cloud | 2017 | CVPR | [link](https://openaccess.thecvf.com/content_cvpr_2017/html/Qi_PointNet_Deep_Learning_CVPR_2017_paper.html) |  |

#### Voxel

| Algorithm | Based Structure | Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- |
| Direct Voxel Grid Optimization | voxel grid  | 2022 | CVPR | [link](https://openaccess.thecvf.com/content/CVPR2022/html/Sun_Direct_Voxel_Grid_Optimization_Super-Fast_Convergence_for_Radiance_Fields_Reconstruction_CVPR_2022_paper.html) |  |
| NICE-SLAM | multireslutional voxel grid | 2022 | CVPR | [link](https://openaccess.thecvf.com/content/CVPR2022/html/Zhu_NICE-SLAM_Neural_Implicit_Scalable_Encoding_for_SLAM_CVPR_2022_paper.html) |  |
| Instant neural graphics primitives with a multiresolution hash encoding  | voxel grid hash encoding  | 2022 | ACM Transactions on Graphics | [link](https://doi.org/10.1145/3528223.3530127) |  |
| Vox-Fusion | voxel grid with octree | 2022 | ISMAR | [link](https://doi.org/10.1109/ISMAR55827.2022.00066) |  |
| Occupancy Networks | occupancy grid | 2019 | CVPR | [link](https://openaccess.thecvf.com/content_CVPR_2019/html/Mescheder_Occupancy_Networks_Learning_3D_Reconstruction_in_Function_Space_CVPR_2019_paper.html) |  |

#### Neural Weights

| Algorithm | Based Structure | Date | Publication | Paper Link | Code |
| --- | --- | --- | --- | --- | --- |
| NeRF  | MLP | 2022 | ACM Transactions on Graphics | [link](https://dl.acm.org/doi/10.1145/3528223.3530127) |  |
| 3D-GS  | 3D-GS  | 2023 | ACM Transactions on Graphics | [link](https://doi.org/10.48550/arXiv.2308.04079) |  |
| NerF-LOAM | Neural-SDF | 2023 | ICCV | [link](https://openaccess.thecvf.com/content/ICCV2023/papers/Deng_NeRF-LOAM_Neural_Implicit_Representation_for_Large-Scale_Incremental_LiDAR_Odometry_and_ICCV_2023_paper.pdf) |  |
| DeepSDF | MLP-SDF/TSDF | 2019 | CVPR | [link](https://openaccess.thecvf.com/content_CVPR_2019/html/Park_DeepSDF_Learning_Continuous_Signed_Distance_Functions_for_Shape_Representation_CVPR_2019_paper.html) |  |


## 4. Motion Execution

### 4.1 Ontological Skills

#### Meta-Skills (Meaning, Definition, Classification in Multi-Carrier)

- Traditional Platforms: Drone, Unmanned Vehicle, Quadruped Platform
- Skill Types: Fly, Run, Walk...
- Relationship between Skills and Terrain Passability

#### Multi-Skill Learning

- Transfer
- Reinforcement

### 4.2 Planning and Control

#### Path Planning

- Classic Path Planning
    - Graph Search Based
    - Interpolating Curve Based
    - Sampling Based
    - Numerical Optimization Based
- Learning-Based Path Planning
    - Supervised Learning
    - Self-Supervised Learning
    - Reinforcement Learning

#### Motion Control

- Single-Body Control 
- Cluster Control


### 4.3 Morphological Coordination

#### Morphological Transformation

#### Agile Coordination

## 5. Platforms and Data

### 5.1 Hardware Platforms

### 5.2 Simulation Platforms

### 5.3 Open Datasets

## 6. Challenges in Embodied Navigation

## 7. Conclusion and Outlook
