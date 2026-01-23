---
title: "Open-source da Vinci Instrument CAD"
excerpt: "Open-source photorealistic CAD models for da Vinci instruments. More instruments will be added in the future. Stay tuned!"
collection: build
order: 1
year: 2024
year_end: 2026
venue: "Johns Hopkins University"
tags:
  - dVRK
  - Surgical Instrument
  - Simulation
  - Blender
# Add your image or GIF here:
# header:
code_url: "https://github.com/jhu-dvrk/instrument-cad"
teaser: "build/blender_LND420006.gif"
---

## Overview

Open-source photorealistic CAD models for da Vinci instruments. More instruments will be added in the future. Stay tuned!

Current available models:
- Large Needle Driver, 420006

<figure>
  <img src="/images/build/blender_LND420006.gif" alt="Description" style="width: 85%;">
  <figcaption>Large Needle Driver Overview</figcaption>
</figure>

## Technical Details

- Detached and reassembled CAD from Intuitive Surgical Inc. using Blender.
- Refined model parameters/components (e.g. adding cables) for optimal photorealistic rendering.
- Modified the center of rigid bodies for better alignment.
- Defined the joints for control and actuation in simulation.
- Used <a href="https://github.com/WPI-AIM/ambf_addon" target="_blank">AMBF Blender Add-on</a> to export OBJ meshes.

## Community Impact

This work contributes to the broader dVRK community and facilitates research in the field of surgical robotics, especially in the context of photorealistic simulation and rendering.

The models have been used in the following publications:
- Instrument-Splatting: Controllable Photorealistic Reconstruction of Surgical Instruments Using Gaussian Splatting (Yang et al., MICCAI 2025)
- Robot-Assisted Suturing in Surgical Simulation: A Comparative Analysis between NVIDIA's Simulator and an Open Platform (Kim et al., Journal of Medical Robotics Research 2026)
- Surgical Robotics Environment in NVIDIA Isaac Sim for Robot-Assisted Suturing (Kim et al., ISMR 2025)
- FIRE-3DV: Framework-Independent Rendering Engine for 3D Graphics Using Vulkan (Allison et al., IEEE International Conference on Robotic Computing (IRC) 2024)
- ...

**More details will be added later. Stay tuned!**

<!-- Add your media content below -->
<!-- ![dVRK Reactivation](/images/build/dvrk-reactivation.jpg) -->
