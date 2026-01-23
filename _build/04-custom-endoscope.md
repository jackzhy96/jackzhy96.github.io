---
title: "Modern Endoscope Integration with the da Vinci Research Kit"
excerpt: "Integrate a modern endoscope with the dVRK-Si for surgical robotics research."
collection: build
order: 4
year: 2025
venue: "Johns Hopkins University"
tags:
  - System Integration
  - Video Pipeline Construction
  - Surgical Robotics
# Add your image or GIF here:
# header:

teaser: "build/custom_endoscope_dvrk.jpg"

publications:
  - title: "SurgSync: Time-Synchronized Multi-modal Data Collection Framework and Dataset for Surgical Robotics"
    authors: "Zhou, H.*, Liu, C.*, Wu, Y., ..., & Kazanzides, P."
    venue: "IEEE Intl. Conf. on Robotics and Automation (ICRA)"
    year: 2026
    submit_year: 2025
    under_review: true
---

## Overview

Integrate a modern endoscope seamlessly with the da Vinci Research Kit for surgical robotics research.

<figure>
  <img src="/images/build/custom_endoscope_dvrk.jpg" alt="Description" style="width: 85%;">
  <figcaption>dVRK-Si using the Modern Endoscope Integration</figcaption>
</figure>

## Technical Details

- Figured HDMI-to-USB frame capture devices for endoscope video signal capture and reading
- Designed and manufactured adapters to install the endoscope on the dVRK-Si
- Deployed a customized video streaming pipeline using v4l2 and gscam to read the endoscope video signal and publish to ROS/ROS2 image topics
- Implemented customized kinematic models for the endoscope
- Developed customized configuration files for seamless integration with the dVRK-Si

## Custom Mechanical Adapters

<figure>
  <div style="display: flex; gap: 1em;">
  <img src="/images/build/endo_adapter.png" alt="Before" style="width: 42%;">
  <img src="/images/build/endo_holder.png" alt="After" style="width: 42%;">
</div>
  <figcaption>Custom Endoscope Adapters. Light: Custom Holder for the endoscope. Right: Custom Trocar.</figcaption>
</figure>

## Image Quality Comparison

<figure>
  <div style="display: flex; gap: 1em;">
  <img src="/images/build/dVRKSi_ref_img.png" alt="Before" style="width: 42%;">
  <img src="/images/build/csr_ref_img.png" alt="After" style="width: 42%;">
</div>
  <figcaption>Representative frames from the dVRK-Si endoscope (left) and our modern endoscope (right). Brightness settings: dVRK-Si CCU at 100%, ours at 30%. Both frames are captured with similar camera-phantom distances.</figcaption>
</figure>


**More details will be added later. Stay tuned!**

<!-- Add your media content below -->
<!-- ![Capacitive Sensor](/images/build/capacitive-sensor.jpg) -->
