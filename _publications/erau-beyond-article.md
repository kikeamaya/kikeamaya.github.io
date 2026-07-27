---
title: "Robust Real-Time UAV Target Tracking with Onboard Vision-Based Yaw Control"
collection: publications
category: manuscripts
permalink: /publications/erau-beyond-article/
authors: "Rylan Malarchick, Jose Castelblanco, Enrique Amaya, Carmen DiMario, Graysen Brinkman, et al."
excerpt: "aa"
date: 2026-06-15
abstract: >
  The proliferation of small, agile unmanned aerial vehicles (UAVs) has created a growing need for platforms that can autonomously detect and maintain visual contact with moving aerial targets. Achieving this on resource-constrained airborne hardware is difficult: modern detection networks are computationally demanding, and purely reactive controllers fail during momentary detection dropouts. This study investigates whether a modular ROS2-based software architecture can achieve reliable real-time yaw tracking using onboard computer vision, validated for sustained operation. We present AIRHOUND (Autonomous Intelligent Rotorcraft for Hostile Object Unified Navigation and Detection), a UAV platform implementing vision-based “yaw-to-target” control. AIRHOUND employs a three-node ROS2 architecture (perception, tracking, offboard control). YOLOv8 object detection is optimized with NVIDIA TensorRT for an embedded NVIDIA Jetson Orin; a geometric tracking module converts pixel coordinates to angular yaw errors using a pinhole camera model, and a proportional controller streams rate-limited yaw commands to a PX4 flight controller through the Micro XRCE-DDS bridge. The architecture was validated with a 600-second end-to-end integration test in the PX4 Software-In-The-Loop (SITL) simulation environment using a 30 Hz detector. The pipeline sustained 30 Hz message throughput across all stages with zero dropped messages, exceeding the 15 Hz minimum requirement by a factor of two and maintaining a 0.000 Hz steady-state standard deviation, and seven integration bugs were identified and resolved before validation succeeded. This work contributes a validated, reusable software foundation for vision-based UAV tracking whose modular structure decouples perception, tracking, and control. Future work moves from simulation to physical validation on the assembled hardware, transitions to a transformer-based detector (RF-DETR), and adds Kalman filtering for occlusion-robust tracking
paperurl: "https://commons.erau.edu/beyond/vol9/iss1/6/"
projecturl: "/projects/airhound/"
---
# {{ page.title }}
Published: {{ page.date | date: "%B %-d, %Y" }}

## Abstract

{{ page.abstract }}