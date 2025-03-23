<a id="readme-top"></a>

<br />
<div align="left">
  <a href="https://github.com/alexdrumi/Autonomous-Vehicle-Internship">
    <img src="assets/mne_eeg.jpg" alt="MNE EEG Logo" width="550" height="300">
  </a>
<h1 align="center">AUTONOMOUS-VEHICLE-INTERNSHIP</h1>


---

## Introduction

**TELEANN** works on an **Autonomous Forklift** — a cutting-edge solution designed to revolutionize the warehouse environment by automating the movement of items between various points. This system enhances efficiency, reduces costs, and minimizes human error. The forklifts are retrofitted with our hardware and software kit, making it compatible with all types of existing forklifts.

In the context of this internship project, my focus was on **real-time object detection and navigation** using **ROS** (Robot Operating System). The internship involves integrating **software, hardware, and AI** components to create a robust autonomous forklift prototype. **Notably, TELEANN has recently raised over €200,000 to continue developing this solution using the same core software stack.**

<p align="right">(<a href="#top">back to top</a>)</p>

---
## Core Objective
Eliminate manual item transport in warehouses by automating forklifts. This boosts efficiency, cuts costs, and frees human labor for more advanced tasks.

## Target Market
Designed for medium- to large-scale warehouses, distribution centers, and manufacturing facilities aiming to automate internal logistics and enhance operations.

## Key Features
1. **Autonomous Navigation** – AI-driven, handling complex warehouse terrains  
2. **Load Handling** – Comparable lifting capacity to traditional forklifts  
3. **Safety** – Multiple sensors ensure safe coexistence with human operators  
4. **Integration** – Real-time updates via existing WMS  
5. **Energy Efficiency** – Eco-friendly motors for reduced power consumption

## Technology Stack Overview
1. **Operating System** – Ubuntu 20.04 LTS (Jetson Linux with kernel 5.10)  
2. **Robotics Framework** – ROS1 Noetic 
3. **Libraries** - ORB_SLAM3 (ROS fork), Anybotics packages, Camera & IMU Calibration  
4. **Hardware** – PiRacer (initial experiments), Jetson AGX Orin (higher compute for AI tasks), Intel Realsense D435i (main camera for ORB_SLAM3 and point clouds) 


## Demonstration and Media

We keep all demonstration materials—images, GIFs, and videos—in the **`assets/`** folder.

1. **ROS Environment & Outside View**  
   ![ROS/Outside View](assets/ros_outside_view.png)  
   *A screenshot showing real-time object detection in ROS (rviz) plus an external camera feed.*

2. **Video Demo (45 seconds)**  
   [![Autonomous Forklift Demo](assets/Teleann_demo_compressed.mp4)](assets/forklift_demo.mp4)  
   - **Sound**: Commentary on forklift’s real-time object detection.  
   - **Split-screen**: Top/left is ROS view; bottom/right is the forklift moving in a warehouse setting.  
   - **Delay Notice**: The visible lag is strictly a **display refresh** artifact, not a ROS system delay.


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
