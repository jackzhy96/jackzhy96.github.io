---
title: "Point Cloud Completion"
excerpt: "Novel chamfer distance loss function achieving state-of-the-art results on benchmark datasets"
collection: research
order: 8
year: 2023
year_end: 2024
venue: "Worcester Polytechnic Institute"
location: "Worcester, MA"
publication_only: True
tags:
  - Deep Learning
  - Point Cloud Completion
  - 3D Vision
# Add your image or GIF here:
# header:
teaser: "research/point_cloud_complete.png"

publications:
  - title: "Loss Distillation via Gradient Matching for Point Cloud Completion with Weighted Chamfer Distance"
    authors: "Lin, F.*, Liu, H.*, Zhou, H.*, Hou, S.*, Yamada, K. D., ... & Zhang, Z."
    venue: "IEEE/RSJ Intl. Conf. on Intelligent Robots and Systems (IROS)"
    year: 2024
    paper_url: "https://doi.org/10.1109/IROS58592.2024.10801828"
    arxiv_url: "https://arxiv.org/abs/2409.06171"
    code_url: "https://github.com/ark1234/IROS2024-LossDistillationWeightedCD"
---

## Overview

Research on improving point cloud completion tasks through novel loss function design.

<figure>
  <img src="/images/research/point_cloud_complete.png" alt="Description" style="width: 85%;">
  <figcaption>Visualization of ShapeNet-55 benchmark. Gray represents the partial
input. Yellow represents HyperCD. Green represents Landau CD (our novel approach) </figcaption>
</figure>

## Key Contributions

- Proposed a novel chamfer distance loss function (based on Landau distribution) for point cloud completion task
- Achieved new state-of-the-art results on some benchmark datasets

<!-- Add your media content below -->
<!-- ![Point Cloud Completion](/images/research/point-cloud.gif) -->
