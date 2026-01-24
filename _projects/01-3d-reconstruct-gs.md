---
title: "3D Reconstruction using Gaussian Splatting and Simulation Integration"
excerpt: "A toy project using 3D Gaussian splatting (Free-SurGS) for 3D reconstruction from images; integrate the reconstructed mesh into AMBF simulator as a static object and enable teleoperation."
collection: projects
order: 1
year: 2025
venue: "Johns Hopkins University"
tags:
  - 3D Reconstruction
  - Surgical Scene Simulation
  - Computer Vision
  - Simulation Infrastructure
  
code_url: "coming_soon"
# Add your image or GIF here:
# header:
teaser: "projects/3d_reconstruct_demo.gif"
---

## Overview

A toy project using 3D Gaussian splatting (Free-SurGS) for 3D reconstruction from images; integrate the reconstructed mesh into AMBF simulator as a static object and enable teleoperation.

<figure>
  <img src="/images/projects/3d_reconstruct_demo.gif" alt="Description" style="width: 85%;">
  <figcaption>Integrated Simulation Scene using the Reconstructed 3D Mesh</figcaption>
</figure>

## Technical Details

- Train Free-SurGS on SCARED example dataset
- Reconstruct 3D Mesh (PLY and OBJ) from the 3D Gaussian
- Integrate the reconstructed mesh into AMBF simulator as a static object

## Reconstructed 3D Mesh

<figure>
  <div style="display: flex; gap: 1em;">
  <img src="/images/projects/ply_blender.png" alt="Before" style="width: 42%;">
  <img src="/images/projects/obj_blender.png" alt="After" style="width: 42%;">
</div>
  <figcaption>Reconstructed meshes in Blender. Left: PLY mesh; Right: OBJ mesh. Note that the color
differences of the two meshes are due to the color space differences (sRGB v.s. Linear)</figcaption>
</figure>

<!-- Add your media content below -->
<!-- ![VIO Demo](/images/projects/vio.gif) -->
