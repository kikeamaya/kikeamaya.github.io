---
title: "Predictive Target Pursuit for Autonomous UAVs using RF-DETR with Depth-Aware State Estimation and Physics-Informed Trajectory Prediction"
collection: publications
category: manuscripts
permalink: /publications/spie-conference-paper/
authors: '<a href="https://www.linkedin.com/in/rylan-malarchick/" target="_blank" rel="noopener noreferrer">Rylan Malarchick </a>, <a href="https://www.linkedin.com/in/carmen-dimario/" target="_blank" rel="noopener noreferrer"> Carmen DiMario </a>, Enrique Amaya, <a href="https://www.linkedin.com/in/graysen-brinkman/" target="_blank" rel="noopener noreferrer"> Graysen Brinkman </a>, et al.'
date: 2026-06-11
excerpt: "aa"
abstract: > 
  Autonomous UAV target pursuit requires robust detection, state estimation, and control under conditions where visual input degrades or disappears entirely. We present AIRHOUND, an onboard perception-to-control pipeline for single-target drone tracking that runs entirely on an NVIDIA Jetson Orin. The system integrates two detection architectures, RF-DETR (transformer-based) and YOLOv8n (CNN-based), with Intel RealSense D455 stereo depth for 3D state estimation, a 6-state Kalman filter for temporal smoothing, and a physics-informed neural network (PINN) for trajectory prediction during detection dropout. We evaluate both detectors under four synthetic degradation types (Gaussian noise, low light, motion blur, partial occlusion) at five severity levels. RF-DETR retains 75% of its clean-baseline mAP at maximum noise severity, compared to 33% for YOLOv8n, a +39.8 percentage point advantage attributable to the transformer attention mechanism’s ability to aggregate global context from uncorrupted image regions. RF-DETR achieves 15 FPS end-to-end on the Jetson Orin after TensorRT FP16 conversion, sufficient for the 10 Hz control loop. The PINN enforces a velocity magnitude constraint (∥v∥ ≤ 10 m/s) during training, preventing physically implausible extrapolation during multi-second dropouts. The complete pipeline is validated in PX4 hardware-in-the-loop configuration with closed-loop yaw tracking, achieving 58.8 ms mean end-to-end detection latency on the Jetson Orin with TensorRT. All perception and tracking components are modular, configurable at runtime via a single YAML file, and communicate over standard ROS 2 interfaces.
paperurl: "https://doi.org/10.1117/12.3094732"
projecturl: "/projects/airhound/"
---

## Abstract

{{ page.abstract }}