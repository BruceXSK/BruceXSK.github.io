---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

## Reinforcement learning-based navigation for indoor service robots (2022.1-present)

<img src="/images/project_ugv.png" height="200x">

- The control commands of the robot is output directly by a network that encodes the features of laser, goal and speed.
- The network is trained based on reinforcement learning algorithms like PPO and Decision Transformer with simulators like Stage, Gazebo and Webots.
- Some security protection strategies and traditional path planning algorithms are combined to solve some corner cases that reinforcement learning cannot handle.
- The runtime code is written in C++ and deployed on Nvidia TX2 with ROS.

## Navigation of agricultural inspection/delivery robots  (2021.6-2022.9)

<img src="/images/project_agriculture.png" height="200x">

- The [Circular Accessible Depth](https://brucexsk.github.io/research/) is deployed as the perception module to predict the traversability.
- The UGV need to travel between the warehouse and the field. We built a point cloud map for indoor localization, which uses [fast_lio_localization](https://github.com/BruceXSK/fast_lio_localization), an open-source project that I maintained.
- However, due to the influence of tree growth on point cloud maps, we turn to fusing the odometry, IMU and GPS by Kalman filter for localization in the field.
- The navigation framework was deployed on Nvidia TX2 with ROS.

## Object detection-based people counting with edge computing (2020.9-2021.5)

<img src="/images/project_count.png" height="200x">

- YOLOv5 is taken as the detection network and trained to detect human body or head according to the characteristics of different application scenarios.
- The trajectories of bodies or heads are computed by some tracking algorithms like SORT.
- Then, the number of people who pass the line set by user could be counted by calculating the geometric relationship between the trajectories and the line.
- The YOLOv5 model accelerated by TensorRT and the tracking code were deployed on TX2 and can run at more than 10 frames per second.
