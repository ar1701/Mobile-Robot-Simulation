# 🤖 TurtleBot3 Navigation with ROS2 Nav2

<img src="https://github.com/ROBOTIS-GIT/emanual/blob/master/assets/images/platform/turtlebot3/logo_turtlebot3.png" width="300">

## 📋 Project Description

This project demonstrates autonomous navigation using the TurtleBot3 robot platform with ROS2 and Navigation2 (Nav2). It provides a complete setup for simulating and testing navigation capabilities, including SLAM (Simultaneous Localization and Mapping), path planning, obstacle avoidance, and autonomous navigation in various environments.

The TurtleBot3 is a small, affordable, programmable, ROS-based mobile robot for education, research, and product development. This project leverages its capabilities combined with the powerful Nav2 stack to implement robust navigation solutions.

## 🧭 Navigation2 (Nav2)

Navigation2 is the next generation ROS navigation stack designed specifically for ROS2. It provides a set of modules for robot navigation, including:

- 🗺️ Map building and localization
- 🛣️ Path planning and following
- 🚧 Obstacle avoidance
- 🔄 Recovery behaviors

## 🚀 How to Run

### Prerequisites

- Ubuntu 20.04 or later
- ROS2 (Foxy, Galactic, or Humble)
- Gazebo simulation environment
- TurtleBot3 packages

### Step 1: Setup Environment

```bash
# Set TurtleBot3 model (choose one: burger, waffle, waffle_pi)
export TURTLEBOT3_MODEL=burger
export GAZEBO_MODEL_PATH=$GAZEBO_MODEL_PATH:/opt/ros/humble/share/turtlebot3_gazebo/models
```

### Step 2: Launch Simulation Environment

```bash
# Launch Gazebo with a world map
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py
```

### Step 3: Start Navigation2

```bash
# Launch Nav2 with a pre-built map
ros2 launch turtlebot3_navigation2 navigation2.launch.py use_sim_time:=True map:=/path/to/your/map.yaml
```

### Step 4: Set Navigation Goal

- In RViz, click on the "2D Pose Estimate" button and set the initial pose of the robot
- Click on the "2D Goal Pose" button and set a navigation goal
- The robot will autonomously plan a path and navigate to the goal while avoiding obstacles

### Step 5: SLAM Mapping (Optional)

If you need to create a new map:

```bash
# Launch SLAM toolbox
ros2 launch turtlebot3_cartographer cartographer.launch.py use_sim_time:=True
# Save map when complete
ros2 run nav2_map_server map_saver_cli -f ~/map
```

## 📊 Performance Metrics

- **Localization Accuracy**: Typically within 5cm in simulation
- **Path Planning**: Optimal paths with dynamic obstacle avoidance
- **Navigation Speed**: Configurable based on safety requirements

[![kinetic-devel Status](https://github.com/ROBOTIS-GIT/turtlebot3_simulations/workflows/kinetic-devel/badge.svg)](https://github.com/ROBOTIS-GIT/turtlebot3_simulations/tree/kinetic-devel)
[![melodic-devel Status](https://github.com/ROBOTIS-GIT/turtlebot3_simulations/workflows/melodic-devel/badge.svg)](https://github.com/ROBOTIS-GIT/turtlebot3_simulations/tree/melodic-devel)
[![noetic-devel Status](https://github.com/ROBOTIS-GIT/turtlebot3_simulations/workflows/noetic-devel/badge.svg)](https://github.com/ROBOTIS-GIT/turtlebot3_simulations/tree/noetic-devel)

[![dashing-devel Status](https://github.com/ROBOTIS-GIT/turtlebot3_simulations/workflows/dashing-devel/badge.svg)](https://github.com/ROBOTIS-GIT/turtlebot3_simulations/tree/dashing-devel)
[![foxy-devel Status](https://github.com/ROBOTIS-GIT/turtlebot3_simulations/workflows/foxy-devel/badge.svg)](https://github.com/ROBOTIS-GIT/turtlebot3_simulations/tree/foxy-devel)
[![galactic-devel Status](https://github.com/ROBOTIS-GIT/turtlebot3_simulations/workflows/galactic-devel/badge.svg)](https://github.com/ROBOTIS-GIT/turtlebot3_simulations/tree/galactic-devel)
[![humble-devel Status](https://github.com/ROBOTIS-GIT/turtlebot3_simulations/workflows/humble-devel/badge.svg)](https://github.com/ROBOTIS-GIT/turtlebot3_simulations/tree/humble-devel)

## ROBOTIS e-Manual for TurtleBot3

- [ROBOTIS e-Manual for TurtleBot3](http://turtlebot3.robotis.com/)

## Wiki for turtlebot3_simulations Packages

- http://wiki.ros.org/turtlebot3_simulations (metapackage)
- http://wiki.ros.org/turtlebot3_fake
- http://wiki.ros.org/turtlebot3_gazebo

## Open Source related to TurtleBot3

- [turtlebot3](https://github.com/ROBOTIS-GIT/turtlebot3)
- [turtlebot3_msgs](https://github.com/ROBOTIS-GIT/turtlebot3_msgs)
- [turtlebot3_simulations](https://github.com/ROBOTIS-GIT/turtlebot3_simulations)
- [turtlebot3_applications_msgs](https://github.com/ROBOTIS-GIT/turtlebot3_applications_msgs)
- [turtlebot3_applications](https://github.com/ROBOTIS-GIT/turtlebot3_applications)
- [turtlebot3_autorace](https://github.com/ROBOTIS-GIT/turtlebot3_autorace)
- [turtlebot3_deliver](https://github.com/ROBOTIS-GIT/turtlebot3_deliver)
- [hls_lfcd_lds_driver](https://github.com/ROBOTIS-GIT/hls_lfcd_lds_driver)
- [ld08_driver](https://github.com/ROBOTIS-GIT/ld08_driver)
- [open_manipulator_msgs](https://github.com/ROBOTIS-GIT/open_manipulator_msgs)
- [open_manipulator](https://github.com/ROBOTIS-GIT/open_manipulator)
- [open_manipulator_simulations](https://github.com/ROBOTIS-GIT/open_manipulator_simulations)
- [open_manipulator_perceptions](https://github.com/ROBOTIS-GIT/open_manipulator_perceptions)
- [open_manipulator_with_tb3_msgs](https://github.com/ROBOTIS-GIT/open_manipulator_with_tb3_msgs)
- [open_manipulator_with_tb3](https://github.com/ROBOTIS-GIT/open_manipulator_with_tb3)
- [open_manipulator_with_tb3_simulations](https://github.com/ROBOTIS-GIT/open_manipulator_with_tb3_simulations)
- [dynamixel_sdk](https://github.com/ROBOTIS-GIT/DynamixelSDK)
- [OpenCR-Hardware](https://github.com/ROBOTIS-GIT/OpenCR-Hardware)
- [OpenCR](https://github.com/ROBOTIS-GIT/OpenCR)

## Documents and Videos related to TurtleBot3

- [ROBOTIS e-Manual for TurtleBot3](http://turtlebot3.robotis.com/)
- [ROBOTIS e-Manual for OpenManipulator](http://emanual.robotis.com/docs/en/platform/openmanipulator/)
- [ROBOTIS e-Manual for Dynamixel SDK](http://emanual.robotis.com/docs/en/software/dynamixel/dynamixel_sdk/overview/)
- [Website for TurtleBot Series](http://www.turtlebot.com/)
- [e-Book for TurtleBot3](https://community.robotsource.org/t/download-the-ros-robot-programming-book-for-free/51/)
- [Videos for TurtleBot3 ](https://www.youtube.com/playlist?list=PLRG6WP3c31_XI3wlvHlx2Mp8BYqgqDURU)
