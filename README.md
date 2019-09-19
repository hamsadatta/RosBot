# RosBot (An Autonomous Navigation Ambition Project)

As autonomous driving is rapidly becoming the next major challenge in the automotive industry, the problem of Simultaneous Localization and Mapping (SLAM) has never been more relevant than it is today. This project presents the idea of examining SLAM algorithms by implementing such an algorithm on a custom bot which has been fitted with sensors and microcontrollers. The software architecture of this small-scale vehicle is based on the Robot Operating System (ROS), an open-source framework designed to be used in robotic applications.

This Project covers, the examining of these algorithms in both simulations, and real-world experiments. The method used in this project is more related to v-development cycle, meaning that a near model of the vehicle is first implemented in simulations using each algorithm and followed by real world experiment. The comparative analysis is performed next.

This project has resulted in a dynamic model of a small-scale vehicle which can be used for simulation of any ROS-compliant SLAM-algorithm, and this model has been simulated extensively in order to provide empirical evidence to define which SLAM algorithm is most suitable for this application.

```diff
- This Repo contains launch files for Gmapping, Hector Map and Rtab Map.
- Please navigate through the readme files to know more about simulation and real-time implementation in respective folders

```
 
## Compatability mode

Hardware and software used for this project:


Software

    ROS: Kinetic Kame
    
    OS:  Ubuntu 16.04
    
    SIM: Gazebo 7.0.0

Hardware

MASTER PC

    RAM: 8GB DDR4
    
    SSD: Samsung EVO
    
    CPU: Intel i5 (8th Gen)
    
    GPU: Nvidia MX150-4GB 
    
 REMOTE PC
 
    Raspberry pi3 B+
 
 OTHERS
 
    RP LIDAR A1M8
    
    Microsoft Kinect Sensor
    
    SPG30E-200K DC Geared Motor with Encoder 17RPM 80N.cm 12V
    
    L298N 2A Based Motor Driver Module









