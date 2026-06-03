# 5-DOF Robotic Manipulator

A 3.5-foot tall, five-degree-of-freedom robotic arm built from the ground up, including a custom PCB, inverse kinematics solver, and motion control firmware.

---

## Overview

The manipulator combines mechanical design, embedded electronics, and machine learning into a single system. Each joint is driven by a servo or stepper motor controlled via a custom PCB designed in Altium Designer. The software stack runs inverse kinematics in Python using PyTorch, then dispatches motion commands over serial to C++ firmware on the microcontroller.

---

## Technical Breakdown

### Mechanical Design
- 5 degrees of freedom: base rotation, shoulder, elbow, wrist pitch, wrist roll
- 3D-printed arm segments designed in Autodesk Inventor
- ~3.5 ft reach at full extension
- Counterbalanced base for stability under load

### Electronics
- Custom PCB designed in Altium Designer
- Dedicated motor driver ICs per joint
- Encoder feedback for position sensing
- USB-to-serial bridge for host communication

### Software
- Inverse kinematics solver in Python with PyTorch — given a target (x, y, z) position and orientation, computes joint angles via gradient descent optimization
- Motion planning handles joint limits and singularity avoidance
- C++ firmware on the microcontroller receives joint angle targets and executes smooth interpolated motion

---

WILL ADD MORE CONTENT SOON

---