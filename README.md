Project Overview
Goal: Develop an autonomous RC system capable of real-time obstacle detection and navigation using a combination of thermal imaging and LIDAR data.
Platform: The microcontroller is programmed using Arduino language (C/C++), allowing direct control of the hardware.
Operating Systems:
FreeRTOS: Enables multi-threaded task execution, prioritization, and scheduling, making it more responsive to sensor inputs.
No-OS (Bare Metal): Uses direct control over microcontroller resources, optimizing speed and reducing overhead.
Key Components
Microcontroller:

Arduino-based (e.g., ESP32-S3 Mini or STM32 if needed for advanced real-time tasks).
Handles sensor data processing and decision-making.
Sensors for Environmental Awareness:

AMG8833 Thermal Sensor: Detects heat signatures, useful for navigating in low visibility conditions and identifying living obstacles.
TF-Luna LIDAR Sensor: Measures distance to objects in real-time, enabling precise obstacle detection and mapping.
Motor Control & Actuation:

Uses PWM-based motor drivers to control speed and direction.
Can implement PID control for smoother navigation.
Software Architecture:

Sensor Data Fusion: Combines LIDAR and thermal data for improved object classification.
Path Planning Algorithm: Uses decision-making logic based on sensor feedback.
RTOS Implementation (if used): Manages tasks for real-time response to sensor inputs.
System Operation
Sensor Data Acquisition:

LIDAR scans the environment for obstacles.
The thermal sensor detects heat-based obstacles.
Processing & Decision-Making:

If running No-OS, uses direct polling or interrupts.
If running FreeRTOS, uses tasks for sensor reading, motor control, and decision logic.
Navigation & Control:

The vehicle adjusts its route dynamically based on sensor feedback.
Can be enhanced with machine learning models for improved path planning.
