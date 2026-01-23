---
title: "FaceSwap Implementation using PRNet"
excerpt: "Implementation of FaceSwap algorithms and Neural Radiance Fields for 3D scene reconstruction"
collection: projects
order: 3
year: 2022
venue: "Worcester Polytechnic Institute"
tags:
  - Deep Learning
  - Computer Vision
  - FaceSwap
  - PyTorch
code_url: "coming_soon"
# Add your image or GIF here:
# header:
teaser: "projects/face_swap_demo.jpg"
---

## Overview

Course project implementing FaceSwap deep learning algorithms using Position Map Regression Network (PRNet) for 3D face reconstruction and alignment.

<figure>
  <img src="/images/projects/face_swap_demo.jpg" alt="Description" style="width: 85%;">
  <figcaption>3D Head Mesh using normal map preview when faceswap</figcaption>
</figure>

**Note:** Most images are not shown due to privacy concerns.

<figure>
  <div style="display: flex; gap: 1em;">
  <img src="/images/projects/face_swap_depth_example.jpg" alt="Before" style="width: 42%;">
  <img src="/images/projects/face_mesh_no_texture.png" alt="After" style="width: 42%;">
</div>
  <figcaption>Left: Face Mesh Mask with Depth based on video input. Right: Textureless Face Mesh</figcaption>
</figure>

## Technical Details

- Implemented FaceSwap using deep neural networks for face detection and replacement using PRNet
- Collected custom dataset of faces and used it for training the FaceSwap model
- Built FaceSwap script from scratch using PyTorch

<!-- Add your media content below -->
<!-- ![NeRF Demo](/images/projects/nerf.gif) -->
