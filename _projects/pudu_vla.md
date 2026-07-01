---
layout: page
title: Pudu Robotics — VLA Foundation Models
description: reproduction, embodiment adaptation, inference acceleration, and RL post-training
img: assets/img/1.jpg # TODO: replace with a real teaser screenshot/photo of the robot
importance: 1
category: work
related_publications: false
---

Internship at **Pudu Robotics** (Mar 2026 – Jun 2026) as a **VLA Algorithm Intern**, working on vision-language-action foundation models for a self-developed wheeled dual-arm robot across four threads.

## Model reproduction & embodiment adaptation
Reproduced **GR00T-N1** and **DM0**, and performed SFT on box-moving and production-task data for a self-developed wheeled dual-arm body. Adapted the action representation and inference config, and recorded training pitfalls with effect attribution.

## RoboChallenge evaluation for in-house foundation model
Stood up the official **RoboChallenge** evaluation pipeline: deployed an in-house foundation-model HTTP inference service, ClientAPI integration, and a local mock closed-loop. Implemented a **20-dim model-action → Franka control-interface** action mapping and fine-tuned on Table 30 tasks.

## Inference acceleration
Following **Realtime-VLA**, optimized end-to-end online inference:
- **CUDA Graph** to eliminate CPU scheduling overhead
- Client-side pre-resize; image codec **WebP95 → JPEG90**
- Communication **WebSocket → ZMQ**

Result: ~**50 ms** reduction in per-step end-to-end inference latency.

## RL post-training
Applied **ConRFT** reinforcement-learning fine-tuning on FlowerVLA SFT weights. Designed a human-in-the-loop pipeline (**SFT → offline RL → online RL**) combining BC and Q-learning dual loss, human intervention, and sparse rewards. Built a reward model and real-robot rollout evaluation loop, substantially improving grasp and push task success rates and error-recovery ability.

<!-- TODO: add a demo video. Local file example:
{% include video.liquid path="assets/video/pudu_demo.mp4" controls="true" %} -->
<!-- Or a YouTube embed: replace VIDEO_ID below -->
<div class="row mt-3">
  <div class="col-sm mt-3 mt-md-0">
    <div class="ratio ratio-16x9">
      <iframe src="https://www.youtube-nocookie.com/embed/VIDEO_ID" allow="autoplay; encrypted-media" allowfullscreen></iframe>
    </div>
  </div>
</div>
<div class="caption">
  TODO: replace VIDEO_ID with a YouTube demo of the robot, or use a local video file via the video include above.
</div>
