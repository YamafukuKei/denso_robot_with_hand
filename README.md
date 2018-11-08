# denso_robot_with_hand

## Description

This project do easy robot arm & hand simulation on Gazebo & MoveIt!

<img src="/picture/vs087_with_robotiq_3f_gripper_bringup.png">

##  Installation
The project uses ROS Kinetic Kame running on Ubuntu 16.04 LTS

Gazebo :7.14.0

### 1. Clone repositories

        $ cd ~/your_ws/src
        $ git clone https://github.com/YamafukuKei/denso_robot_with_hand.git
        $ git clone https://github.com/YamafukuKei/robotiq.git
        $ git clone https://github.com/YamafukuKei/denso_robot_ros.git
        $ git clone https://github.com/YamafukuKei/moveit.git
        $ git clone https://github.com/YamafukuKei/industrial_moveit.git

### 2. Setup

- Run commands

        $ cd ~/your_ws
        $ rosdep install -iry --from-paths src
        $ catkin_make

### 3. Simulation

- Simulate vs087 with robotiq-3f-gripper on Gazebo & MoveIt!

        $ roslaunch vs087_with_robotiq_3f_gripper_bringup vs087_with_robotiq_3f_gripper_bringup.launch


  <!-- <img src="/gif/robot_arm&hand-2018-09-21_21.27.09.gif" width="900" height="450"> -->
