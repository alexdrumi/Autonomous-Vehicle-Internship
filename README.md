<a id="readme-top"></a>

<br />
<div align="center">
  <a href="https://github.com/alexdrumi/Autonomous-Vehicle-Internship">
    <img src="assets/mne_eeg.jpg" alt="MNE EEG Logo" width="550" height="300">
  </a>
<h1 align="center">AUTONOMOUS-VEHICLE-INTERNSHIP</h1>


---

## Introduction

**TELEANN** proudly introduces its **Autonomous Forklift**—a cutting-edge solution designed to revolutionize the warehouse environment by automating the movement of items between various points. This system enhances efficiency, reduces costs, and minimizes human error.

In the context of this internship project, our focus is on **real-time object detection and navigation** using **ROS** (Robot Operating System). The internship involves integrating **software, hardware, and AI** components to create a robust autonomous forklift prototype. **Notably, TELEANN has recently raised over €200,000 to continue developing this solution using the same core software stack.**

<p align="right">(<a href="#top">back to top</a>)</p>

---

## Core Objective

Our goal is to **eliminate the mundane and labor-intensive task** of manually transporting items in a warehouse. By automating this function, we can optimize workflow efficiency and shift human labor toward higher-level tasks, reducing operational costs in the process.

<p align="right">(<a href="#top">back to top</a>)</p>

---

## Target Market

This autonomous forklift targets **medium to large-scale warehouses**, distribution centers, and manufacturing facilities seeking to automate **internal logistics** and bolster operational efficiency.

<p align="right">(<a href="#top">back to top</a>)</p>

---

## Key Features

1. **Autonomous Navigation**  
   Utilizes advanced robotics and AI algorithms to move through complex warehouse terrains.

2. **Load Handling**  
   Matches the capacity of a traditional forklift; capable of lifting and transporting items ranging from small parcels to heavy industrial equipment.

3. **Safety**  
   Multiple sensors and safety mechanisms ensure safe interaction alongside human operators.

4. **Integration**  
   Seamless connectivity with existing Warehouse Management Systems (WMS) for real-time inventory movement updates.

5. **Energy Efficiency**  
   Designed with sustainability in mind, featuring energy-efficient motors and an eco-friendly approach.

<p align="right">(<a href="#top">back to top</a>)</p>

---

## Technology Stack Overview

### Operating System
- **Ubuntu 20.04 LTS**  
  - Provides a stable foundation for robotics and AI applications.  
  - For **Jetson AGX Orin**, we use **Jetson Linux** (based on Ubuntu 20.04 LTS).  
  - **Kernel**: 5.10

### Robotics Framework
- **ROS1 Noetic**  
  - A powerful middleware for building robotics applications.  
  - Enables efficient development, simulation, and deployment of complex robotic systems.

### Libraries & Frameworks

1. **ORB SLAM3**  
   - [GitHub Repository](#)  
   - Real-time **Simultaneous Localization and Mapping (SLAM)** algorithm using oriented FAST keypoints and rotated BRIEF descriptors.  
   - We employ a ROS implementation fork for specialized usage.

2. **Anybotics**  
   - [GitHub Repository](#)  
   - Contains packages like **grid_map** and **elevation_mapping** which we leverage for mapping and environmental understanding.

3. **Camera Calibration**  
   - [Website](#), [Trello](#)  
   - Calibrates the camera and generates configuration files needed by ORB_SLAM3. More details are on our internal Trello board.

4. **IMU Calibration**  
   - [Reference 1](#), [Reference 2](#)  
   - Calibrates the IMU sensor data for ORB_SLAM3 (Inertial). Requires a ROS bag file of IMU sensor data recorded for several hours while the sensor remains at rest.

### Hardware Platforms
1. **PiRacer**  
   - [Product Page](#)  
   - A robotics kit used for initial AI-based experiments. Our plan is to move from a Raspberry Pi platform to the **Jetson AGX Orin**.

2. **Jetson AGX Orin**  
   - [Product Page](#)  
   - Compact AI computer enabling more resource-intensive tasks than smaller boards like Raspberry Pi or Jetson Nano.

3. **Intel Realsense D435i**  
   - [Product Page](#)  
   - The primary camera for running ORB_SLAM3, with additional **point cloud** data for object detection.

<p align="right">(<a href="#top">back to top</a>)</p>

---

## Demonstration and Media

We keep all demonstration materials—images, GIFs, and videos—in the **`assets/`** folder.

1. **ROS Environment & Outside View**  
   ![ROS/Outside View](assets/ros_outside_view.png)  
   *A screenshot showing real-time object detection in ROS (rviz) plus an external camera feed.*

2. **Video Demo (45 seconds)**  
   [![Autonomous Forklift Demo](assets/forklift_demo_thumbnail.png)](assets/forklift_demo.mp4)  
   - **Sound**: Commentary on forklift’s real-time object detection.  
   - **Split-screen**: Top/left is ROS view; bottom/right is the forklift moving in a warehouse setting.  
   - **Delay Notice**: The visible lag is strictly a **display refresh** artifact, not a ROS system delay.

3. **Additional Clip**  
   [![Extra Demo](assets/forklift_demo2_thumbnail.png)](assets/forklift_demo2.mp4)  
   - *Another short demo focusing on obstacle avoidance and object recognition.*

<p align="right">(<a href="#top">back to top</a>)</p>

---

## Repository Structure

```plaintext
.
├── assets
│   ├── forklift_demo.mp4
│   ├── forklift_demo_thumbnail.png
│   ├── forklift_demo2.mp4
│   ├── forklift_demo2_thumbnail.png
│   ├── ros_outside_view.png
│   └── ... other images/GIFs
├── README.md
└── ... (other private or internal code not shared publicly)
