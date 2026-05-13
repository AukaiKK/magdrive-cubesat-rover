# MagDrive — Magnetically Controlled Rover System

A four-wheeled rover controlled by a non-contact magnetic joystick, 
developed as a final project for ME 375 (Machine System Dynamics) at the 
University of Hawaiʻi at Mānoa. The system demonstrates full closed-loop 
sensor-actuator integration using embedded C++ on Arduino.

## System Architecture
- Input: MLX90393 3-axis magnetometer (magnetic joystick)
- Controller: Arduino Uno (C++)
- Output: TB6612FNG motor driver → dual rear DC motors (propulsion)
- Steering: front servo motor via PWM

## Control System Features
- Automatic zero calibration on startup (100-sample average)
- Exponential moving average drift correction (α = 0.02)
- Deadzone filtering on both steering and propulsion axes
- Minimum PWM threshold to ensure reliable motor startup
- 50 Hz control loop update rate (~20 ms cycle)
- X-axis → steering angle (±30° from center)
- Y-axis → motor speed and direction (forward/reverse)

## Hardware
- Arduino Uno microcontroller
- MLX90393 magnetometer (I2C, address 0x18)
- TB6612FNG dual motor driver
- 2× DC motors (rear drive)
- 1× servo motor (front steering)
- Custom Onshape CAD chassis — 3D printed (FDM) steering and 
  differential assemblies
- Dimensions: 35 × 22 × 9 cm

## Files
- `magdrive_main.ino` — main control loop with calibration, 
  deadzone filtering, and motor/servo control
- `CAD/` — Onshape export files for custom mechanical components

## Tools
- Arduino IDE 2.0
- Onshape (CAD)
- Bambu FDM 3D printer

## Author
Aukai Kaai — University of Hawaiʻi at Mānoa, ME 375 Spring 2026
