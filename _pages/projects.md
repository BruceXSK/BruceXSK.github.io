---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

## Reinforcement learning-based navigation for indoor service robots

<img src="/images/project_ugv.png" height="200x">

- Time: 2022-present
- The network output control comand by encoding the features of laser, goal and speed.
- We trained the network based on the online reinforcement learning algorithms PPO/Decision Transformer with robot simulators like Stage, Gazebo and Webots.
- The runtime code is written in C++ and deployed on Nvidia TX2 with ROS.
- Some security protection strategies and traditional path planning algorithms are combined to solve some corner cases that reinforcement learning cannot handle.

## Navigation of agricultural inspection/delivery robots

<img src="/images/project_agriculture.png" height="200x">

- Time: 2021-present
- The [https://brucexsk.github.io/research/](Circular Accessible Depth) is depolyed as the perception module to predict the traversability.
- The UGV need to travel between the warehouse and the field. We built a point cloud map for indoor localization, which uses [fast_lio_localization
](https://github.com/BruceXSK/fast_lio_localization), an open-source project that I maintained.
- However, due to the influence of tree growth on point cloud maps, we turn to fusing the odometry, IMU and GPS by Kalman filter for localization in the trees.

## Object detection-based people counting with edge computing

<img src="/images/project_count.png" height="200x">
