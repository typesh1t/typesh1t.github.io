---
layout: page
title: Anker Innovations — Embodied Closed-Loop
description: VLA deployment on quadruped, multimodal data pipelines, teleop collection, VLM auto-labeling
img: assets/img/2.jpg # TODO: replace with a real teaser of Go2 / manipulator setup
importance: 2
category: work
related_publications: false
---

Internship at **Anker Innovations** (Oct 2025 – Mar 2026) as an **Embodied Closed-Loop Algorithm Intern**, working on VLA deployment, multimodal robot-data pipelines, teleoperation data collection, and VLM auto-labeling.

## VLA reproduction & validation
Reproduced **ACT**, **pi0.5**, and **Diffusion Policy**, completing end-to-end **Franka block-insertion** validation. Deployed **InternVLA-N1** in a client/server split on the **Unitree Go2**:
- **RTX 4090** side: HTTP inference server
- **Jetson Orin** side: D435i capture + ROS2/UDP control bridge + client execution
- Trajectories streamed over LAN HTTP for language-guided navigation

## Quadruped multimodal data pipeline
Built an **8-sensor spatiotemporal alignment** chain:
- 3-LiDAR extrinsic calibration, coordinate transforms, and point-cloud fusion
- 5 fisheye-camera calibration & undistortion
- MCAP slicing / unpacking / alignment services on **Kubernetes** with task-queue async scheduling

Processed **tens of TB** of raw robot data.

## Manipulator data collection
Built **UMI + teleop** collection pipelines: LAN networking, NTP clock sync, station ingest, **rerun** playback, multimodal alignment, and **WebDataset / lerobot** format conversion. Surveyed data-quality eval literature and industry methods, then designed a **5-dimension on-device quality rule check** plus a cloud data-lake scoring algorithm.

## VLM auto-labeling & toolchain
Built a **Qwen-VL + GroundingDINO** video-understanding data-production line (scene description, object grounding, region annotation). Via **vLLM** high-concurrency inference, multi-machine parallelism, and queue load balancing, lifted end-to-end throughput by **~30%**.

<!-- TODO: add a demo video of Go2 navigation or the manipulator data collection.
{% include video.liquid path="assets/video/anker_demo.mp4" controls="true" %} -->
<div class="row mt-3">
  <div class="col-sm mt-3 mt-md-0">
    <div class="ratio ratio-16x9">
      <iframe src="https://www.youtube-nocookie.com/embed/VIDEO_ID" allow="autoplay; encrypted-media" allowfullscreen></iframe>
    </div>
  </div>
</div>
<div class="caption">
  TODO: replace with a demo video of the Go2 language-guided navigation or manipulator collection setup.
</div>
