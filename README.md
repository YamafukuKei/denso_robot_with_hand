# denso_robot_with_hand

## Description

This project do easy robot arm & hand simulation on Gazebo & MoveIt! 

##  Installation
The project uses ROS Kinetic Kame running on Ubuntu 16.04 LTS

Gazebo :7.14.0

### 1. Clone repositories

        $ cd ~/your_ws/src
        $ git clone https://github.com/YamafukuKei/denso_robot_with_hand.git
        $ git clone https://github.com/ros-industrial/robotiq.git
        $ git clone https://github.com/YamafukuKei/denso_robot_ros.git
        $ git clone https://github.com/ros-planning/moveit.git
        $ git clone https://github.com/ros-industrial/industrial_moveit.git

### 2. Setup

- denso_robot_ros setup

        $ cd ~/your_ws
        $ rosdep install -i --from-paths src
        $ cd ~/your_ws/src/industrial_moveit
        $ rm -rf industrial_collision_detection/ constrained_ik/ industrial_moveit_benchmarking/

- robotiq setup

        $ cd ~/your_ws/src/robotiq
        $ git checkout kinetic-devel

- catkin_make

        $ cd ~/your_ws
        $ catkin_make

    **Note:** Maybe you will fail catkin_make because [ros-industrial/robotiq](https://github.com/ros-industrial/robotiq) require packages. Please check   catkin_make error and install required packages by useing under command:

        $ sudo apt install ros-kinetic-[required package name]

### 3. Simulation

- Simulate vs087 with robotiq-3f-gripper on Gazebo & MoveIt!

        $ roslaunch vs087_with_robotiq_3f_gripper_bringup vs087_with_robotiq_3f_gripper.launch
