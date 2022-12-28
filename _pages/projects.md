---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

---

## Reinforcement learning-based navigation for indoor service robots (2022.1-present)

<img src="/images/project_ugv.png" height="200x">

- The network output control comand by encoding the features of laser, goal and speed.
- We trained the network based on the online reinforcement learning algorithms PPO/Decision Transformer with robot simulators like Stage, Gazebo and Webots.
- The runtime code is written in C++ and deployed on Nvidia TX2 with ROS.
- Some security protection strategies and traditional path planning algorithms are combined to solve some corner cases that reinforcement learning cannot handle.

---

## Navigation of agricultural inspection/delivery robots  (2021.6-2022.9)

<img src="/images/project_agriculture.png" height="200x">

- The [Circular Accessible Depth](https://brucexsk.github.io/research/) is depolyed as the perception module to predict the traversability.
- The UGV need to travel between the warehouse and the field. We built a point cloud map for indoor localization, which uses [fast_lio_localization](https://github.com/BruceXSK/fast_lio_localization), an open-source project that I maintained.
- However, due to the influence of tree growth on point cloud maps, we turn to fusing the odometry, IMU and GPS by Kalman filter for localization in the trees.
- The navigation framework was deployed on Nvidia TX2 with ROS.

---

## Object detection-based people counting with edge computing (2020.9-2021.5)

<img src="/images/project_count.png" height="200x">

- We trained YOLOv5 to detect the heads people.
- The heads are assigned different IDs by tracking algorithm like SORT. 
- Then, the number of people who pass the scribed line could be counted by calculating the geometric relationship between the trajectories of heads and the line.
- The YOLOv5 model accelerated by TensorRT and the tracking code are deployed on TX2.
