# 🤖 INARS — Autonomous Indoor Service Robot

<p align="center">
  <strong>Intelligent Navigation and Autonomous Robotic System</strong>
</p>

<p align="center">
  An autonomous indoor service robot combining LiDAR navigation, 
  computer vision, Mecanum-wheel mobility, and robotic manipulation.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/ROS_2-Humble-blue?logo=ros" />
  <img src="https://img.shields.io/badge/Python-3.x-yellow?logo=python" />
  <img src="https://img.shields.io/badge/Raspberry%20Pi-4-red?logo=raspberrypi" />
  <img src="https://img.shields.io/badge/Linux-Ubuntu-orange?logo=ubuntu" />
  <img src="https://img.shields.io/badge/Computer%20Vision-OpenCV-green?logo=opencv" />
  <img src="https://img.shields.io/badge/Robotics-Autonomous-purple" />
</p>

---

## 📌 Overview

**INARS** is an autonomous indoor service robot designed to navigate
indoor environments, avoid obstacles, understand its surroundings,
and perform physical interaction tasks.

The robot combines **LiDAR-based navigation, SLAM, computer vision,
Mecanum-wheel movement, and a robotic manipulator** to perform
service-oriented tasks such as navigating through indoor environments
and interacting with elevator buttons.

The system is built around a **Raspberry Pi** and uses **ROS 2 Humble**
to connect and coordinate the different robotic subsystems.

---

## ✨ Key Features

- 🛞 **4-Wheel Mecanum Drive**
  - Forward and backward movement
  - Sideways movement
  - Diagonal movement
  - Holonomic motion

- 📡 **LiDAR Navigation**
  - Real-time environment sensing
  - Mapping
  - Localization
  - Obstacle detection

- 🗺️ **SLAM**
  - Simultaneous Localization and Mapping
  - Indoor environment mapping
  - Robot localization

- 👁️ **Computer Vision**
  - Camera-based environment perception
  - Elevator-button detection
  - Visual interaction support

- 🦾 **Robotic Manipulator**
  - Servo-controlled robotic arm
  - Physical interaction with elevator buttons

- 🧠 **ROS 2 Architecture**
  - Modular ROS 2 nodes
  - Topic-based communication
  - Sensor and actuator integration

- 🎮 **Teleoperation**
  - Manual robot control
  - Testing and debugging support

---

## 🏗️ System Architecture

```text
                         ┌─────────────────────┐
                         │    Raspberry Pi 4   │
                         │   Main Controller   │
                         └──────────┬──────────┘
                                    │
                 ┌──────────────────┼──────────────────┐
                 │                  │                  │
                 ▼                  ▼                  ▼
          ┌────────────┐     ┌────────────┐     ┌────────────┐
          │   LiDAR    │     │   Camera   │     │ Controller │
          │  RPLIDAR   │     │  Vision    │     │ Teleop     │
          └─────┬──────┘     └─────┬──────┘     └─────┬──────┘
                │                  │                  │
                ▼                  ▼                  ▼
          ┌────────────┐     ┌────────────┐     ┌────────────┐
          │    SLAM    │     │ Elevator   │     │   Motor    │
          │ Navigation │     │  Detection │     │  Control   │
          └─────┬──────┘     └─────┬──────┘     └─────┬──────┘
                │                  │                  │
                └──────────────────┼──────────────────┘
                                   │
                                   ▼
                         ┌────────────────────┐
                         │   Robot Platform  │
                         │                    │
                         │  Mecanum Wheels   │
                         │  Robotic Arm      │
                         │  Servo Motors     │
                         └────────────────────┘
