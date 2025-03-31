# Mobile-Robot-Simulation

A simulation environment for mobile robot navigation, path planning, and control algorithms.

## Overview

This project provides a platform for simulating mobile robot behavior in various environments. It allows for testing and visualization of algorithms for robot navigation, obstacle avoidance, and path planning.

![Robot Simulation Demo](demo.gif)

## Features

- Real-time 2D/3D robot simulation
- Multiple environment configurations
- Sensors simulation (lidar, cameras, etc.)
- Path planning algorithms implementation
- Obstacle avoidance capabilities
- Customizable robot parameters

## Prerequisites

- Python 3.6+
- ROS (Robot Operating System) - optional, for advanced features
- Required Python packages (see Installation)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/Mobile-Robot-Simulation.git
   cd Mobile-Robot-Simulation
   ```

2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## How to Run

1. Start the simulation environment:

   ```bash
   python src/main.py
   ```

2. To run with specific parameters:

   ```bash
   python src/main.py --map-file maps/example.yaml --robot-model models/differential_drive.json
   ```

3. For visualization mode:
   ```bash
   python src/main.py --visualize
   ```

## Configuration

You can customize various parameters in the `config.yaml` file:

- Robot physical parameters
- Sensor configurations
- Environment settings
- Simulation parameters

## Project Structure

```
Mobile-Robot-Simulation/
├── catkin_ws/             # ROS workspace
│   ├── src/               # ROS packages source code
│   ├── build/             # Build directory
│   └── devel/             # Development space
├── scripts/               # Utility scripts
├── launch/                # Launch files
├── config/                # Configuration files
├── worlds/                # Simulation world definitions
├── maps/                  # Environment maps
├── urdf/                  # Robot model definitions
├── meshes/                # 3D models for visualization
├── demo.gif               # Simulation demonstration
└── README.md              # Project documentation
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

