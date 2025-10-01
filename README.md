# K.A.R.L. is my sandbox for exploring robotics and autonomy.

![ROS2](https://img.shields.io/badge/ROS2-Humble-blue?logo=ros)
![Python](https://img.shields.io/badge/Python-3.10-green?logo=python)
![C++](https://img.shields.io/badge/C++-17-00599C?logo=cplusplus)
![Raspberry Pi Pico](https://img.shields.io/badge/Raspberry%20Pi-Pico-red?logo=raspberrypi)
![MicroPython](https://img.shields.io/badge/MicroPython-✓-lightgrey)
![Maker](https://img.shields.io/badge/Maker-Project-orange)

K.A.R.L. (**Kinetic Autonomous Rover for Learning**) is a personal robotics project designed to explore **ROS2, embedded firmware, real-time control, and autonomy**.  
It combines microcontroller-based motor control with a ROS2 stack for sensing, decision-making, and simulation.

---

## Table of Contents
- [Overview](#overview)
- [Hardware](#hardware)
- [Software](#software)
- [Repository Structure](#repository-structure)
- [Setup](#setup)
- [Roadmap](#roadmap)
- [Contributions](#contributions)

---

## Overview

The goal of this project is to build a **field-ready rover platform** for experimenting with:
- ROS2 nodes and topic communication
- Real-time motor control with PWM
- Hardware-in-the-loop (HIL) testing
- Sensor fusion and autonomy experiments
- Firmware/hardware co-design for robotics

---

## Hardware

- **Raspberry Pi Pico (RP2040)** running MicroPython  
- **L298N dual H-bridge motor driver** (driving 4 motors — 2 per channel)  
- **Four TT-style DC motors** (4-wheel drive system)  
- **Neopixel LED on GP15** for status/debug feedback  
- Power: Li-ion battery pack (2S recommended)  
- Additional planned sensors: IMU, ultrasonic, and camera module  

---

## Software

- **MicroPython** drivers for motor control and LEDs  
- **ROS2 Humble** nodes for high-level control, simulation, and visualization  
- **Python / C++** code for ROS2 interfaces  
- Test scripts for SPI, I²C, and UART comms integration  

---

## Repository Structure

---

## Setup

### Firmware (MicroPython on Pico)
1. Flash MicroPython firmware to your Raspberry Pi Pico  
2. Copy files from `/firmware` using [Thonny](https://thonny.org/) or `rshell`  
3. Power on — the Pico should control the motors and LED  

### ROS2 (Control Layer)
1. Source ROS2 Humble environment  
2. Build workspace:  
   ```bash
   cd ros2_ws
   colcon build
   source install/setup.bash
