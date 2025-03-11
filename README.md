# AUTONOMOUS-VEHICLE-INTERNSHIP #

## Introduction ##

TELEANN is proud to introduce its Autonomous Forklift, a solution that is designed to revolutionize the warehouse environment. This cutting-edge product aims to completely automate the task of moving items between various points within a warehouse setting, thereby enhancing efficiency, reducing costs, and minimizing human error.

### Core objective ###

The core objective of the product is to eliminate the mundane and often labor-intensive job of manually transporting items from one location to another. By automating this critical function we could focus more on workflow efficiency and more human-oriented tasks while reducing operational costs.

### Target Market ###

Our Autonomous Forklift is aimed at medium to large-scale warehouses, distribution centers, and manufacturing facilities that are looking to automate their internal logistics and improve operational efficiencies.

### Features ###

- _Autonomous Navigation_

    Leveraging state-of-the-art robotics and AI algorithms, our Autonomous Forklift is capable of navigating complex warehouse terrains without human intervention.

- _Load Handling_

    Designed to match the capacity and functionality of a traditional forklift,  our product can lift and transport a wide range of items, from small parcels to heavy industrial equipment.

- _Safety_

    Equipped with an array of sensors and safety mechanisms, the Autonomous Forklift is designed to work seamlessly alongside human operators, ensuring a safe and accident-free environment.

- _Integration_

    Our forklift can be integrated with existing Warehouse Management Systems (WMS) to provide real-time updates on inventory movement, thereby optimizing stock management.

- _Energy Efficient_

    Built with sustainability in mind, our forklift uses energy-efficient motors and offers an eco-friendly alternative to traditional, fossil fuel-powered forklifts.

* * *

## TECHNOLOGY STACK OVERVIEW ##

### Operating system ###

- Name: Ubuntu 20.04 LTS
- Website: [link](https://releases.ubuntu.com/20.04.6/)
- Description: Ubuntu 20.04 LTS (Long-Term Support) is the chosen operating system for our startup. It provides a stable and well-supported environment for our robotics and AI applications.
- For the Jetson AGX Orin system we use Jetson Linux which is based on ubuntu 20.04 LTS. For more information see [here](https://developer.nvidia.com/embedded/jetson-linux)
- Kernel: 5.10

### Robotics framework/middleware ###

- Name: ROS1 Noetic
- Website: [link](http://wiki.ros.org/noetic)
- Description:
    ROS1 Noetic is a powerful middleware designed for building   robotics applications. It enables us to efficiently develop, simulate, and deploy complex robotic systems.

### Libraries/Frameworks ###

- ORB SLAM3
  - Github Repository: [link](https://github.com/thien94/orb_slam3_ros)
  - Description:
      ORB_SLAM3 (Oriented FAST and Rotated BRIEF Simultaneous Localization and Mapping) is a cutting-edge SLAM algorithm that we're using for real-time mapping and localization. It leverages oriented FAST keypoints and rotated BRIEF descriptors for accurate tracking and mapping. This version is a fork for a ros implementation of the algorithm.

- Anybotics
  - Github Repository: [link](https://github.com/ANYbotics)
  - Description:
    ANYbotics is a repository that we use for multiple purposes. Used packages are grid_map and elevation_mapping.

- Camera Calibration
  - Website: [link](http://wiki.ros.org/camera_calibration/Tutorials/MonocularCalibration)
  - Trello: [link](https://trello.com/c/bcNHNTJ2/97-configure-webcam-see-steps-in-the-description)
  - Description:
    This is used to calibrate the camera and make a config file that ORB_SLAM3 uses. On the Trello page there is more step-by-step information, although it is made for the CoolerMaster (server-desktop).

- IMU Calibration
  - Website: [link1](htps://github.com/ori-drs/allan_variance_ros) and [link2](https://github.com/ethz-asl/kalibr/wiki/IMU-Noise-Model)
  - Description:
    This is used to calibrate the imu sensor for the camera and should be in the config file that ORB_SLAM3 (Inertial) uses. It uses a rosbag file of the imu sensor data of mininumum length of 3 hours (intel suggests 15-24 hours). This sensor data should be from an imu sensor that is fully at rest and on a dampened foam.

### Hardware Platforms ###

- PiRacer
  - Product Page: [link](https://www.waveshare.com/piracer-ai-kit.htm)
  - Description: We are currently using the PiRacer robotics kit for our AI-based applications. The PiRacer kit provides a foundation for our robotics projects, and we plan to transition to using the car with Jetson AGX Orin instead of the RaspberryPi platform as we continue to develop our startup's technology.

- Jetson AGX Orin
  - Product Page: [link](https://developer.nvidia.com/embedded/learn/get-started-jetson-agx-orin-devkit)
  - Description:
    The Jetson AGX Orin developer kit is a small AI computer for makers, learners, and developers. It can work on more resource-intensive tasks than the Raspberry Pi or Nvidia Jetson Nano.

- Intel Realsense D435i
  - Product Page: [link](https://www.intelrealsense.com/depth-camera-d435i/)
  - Description:
    This is the camera that we are using to run the orb_slam3 algorithm on. We also use the pointcloud data it generates for object detection.

* * *

