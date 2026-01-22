---
title: "Surgical Robot Dynamic Model Identification and Control"
excerpt: "Dynamic model identification and gravity compensation (shown) for dVRK-Si PSM using convex optimization; upcoming journal paper is on the way, stay tuned! Develop a novel force estimation method using modal-based and learning-based hybrid approach for trocar interaction."
collection: research
order: 3
year: 2022
year_end: 2026
venue: "Johns Hopkins University"
location: "Baltimore, MD"
tags:
  - Robot Dynamics
  - Robot Kinematics
  - Control
  - Convex Optimization
  - dVRK
# Add your image or GIF here:
# header:
teaser: "research/enable_gc.gif"

publications:
  - title: "Gravity Compensation of the dVRK-Si Patient Side Manipulator based on Dynamic Model Identification"
    authors: "Zhou, H., Yang, H., Deguet, A., ..., & Kazanzides, P."
    venue: "Hamlyn Symp. on Medical Robotics"
    year: 2025
    paper_url: "https://doi.org/10.31256/HSMR25.46"
    arxiv_url: "https://arxiv.org/abs/2501.19058"
    code_url: "https://github.com/jackzhy96/dVRK_Si_PSM_gravity_compensation"
    award: "oral presentation"
    
  - title: "A Hybrid Model and Learning-Based Force Estimation Framework for Surgical Robots"
    authors: "Yang, H., Zhou, H., Fischer, G. S., & Wu, J. Y."
    venue: "IEEE/RSJ Intl. Conf. on Intelligent Robots and Systems (IROS)"
    year: 2024
    paper_url: "https://doi.org/10.1109/IROS58592.2024.10802648"
    arxiv_url: "https://arxiv.org/abs/2409.19970"
---

## Overview

This research develops novel 
- Dynamic model identification and gravity compensation (shown) for dVRK-Si (the next-generation da Vinci Research Kit) Patient Side Manipulator (PSM) using convex optimization
<figure>
  <div style="display: flex; gap: 1em;">
  <img src="/images/research/no_gc.gif" alt="Before" style="width: 42%;">
  <img src="/images/research/enable_gc.gif" alt="After" style="width: 42%;">
</div>
  <figcaption>Left: Without gravity compensation (free fall). Right: Enable gravity compensation. Both 6x speed</figcaption>
</figure>
- a novel force estimation method using a model-based and learning-based hybrid approach for trocar interaction.
<figure>
  <img src="/images/research/hybrid_fe_overview.png" alt="Description" style="width: 85%;">
  <figcaption>Hybrid Force Estimation Overview</figcaption>
</figure>

## Key Contributions

- Develop a novel force estimation approach for the robot under trocar interaction using a hybrid model combined the model-based approach and the learning-based approach, **reducing the estimation errors by 30%**
- Implement the dynamic model identification and gravity compensation of dVRK Classic/Si Patient Side Manipulator using convex optimization approaches, **reducing the static control errors by 73%**

<!-- Add your media content below -->
<!-- ![Dynamic Model](/images/research/dynamic-model.png) -->
