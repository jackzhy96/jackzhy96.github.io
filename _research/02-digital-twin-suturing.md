---
title: "Digital Twin for Suturing Scenes"
excerpt: "High-fidelity simulation environments for suturing execution on AMBF and NVIDIA Isaac Sim"
collection: research
order: 2
year: 2022
year_end: 2026
venue: "Johns Hopkins University"
location: "Baltimore, MD"
tags:
  - Simulation
  - Digital Twin
  - AMBF
  - NVIDIA Isaac Sim

# Add your image or GIF here:
teaser: "research/digital_twin_suture_sim.png"

# Publications associated with this research
publications:
  - title: "Robot-Assisted Suturing in Surgical Simulation: A Comparative Analysis between NVIDIA's Simulator and an Open Platform"
    authors: "Kim, T. W., Zhou, H., Barragan, J. A., ..., Munawar, A."
    venue: "Journal of Medical Robotics Research"
    year: 2026
    paper_url: "https://doi.org/10.1142/S2424905X26400052"
    
  - title: "Surgical Robotics Environment in NVIDIA Isaac Sim for Robot-Assisted Suturing"
    authors: "Kim, T. W., Zhou, H., Barragan, J. A., ..., Munawar, A."
    venue: "Intl. Symp. on Medical Robotics (ISMR), IEEE"
    year: 2025
    paper_url: "https://doi.org/10.1109/ISMR67322.2025.11025977"
    code_url: "https://github.com/surgical-robotics-ai/isaac-sim-surgical-robotics-challenge"
    
  - title: "SurgicAI: A Hierarchical Platform for Fine-Grained Surgical Policy Learning and Benchmarking"
    authors: "Wu, J., Zhou, H., Kazanzides, P., Munawar, A., Liu, A."
    venue: "NeurIPS Datasets and Benchmarks Track"
    year: 2024
    paper_url: "https://doi.org/10.52202/079017-2037"
    arxiv_url: "https://arxiv.org/abs/2406.13865"
    code_url: "https://github.com/surgical-robotics-ai/SurgicAI"

  - title: "Realistic Data Generation for 6D Pose Estimation of Surgical Instruments"
    authors: "Barragan, J. A., Zhang, J., Zhou, H., Munawar, A., Kazanzides, P."
    venue: "IEEE Intl. Conf. on Robotics and Automation (ICRA)"
    year: 2024
    paper_url: "https://doi.org/10.1109/ICRA57147.2024.10611638"
    arxiv_url: "https://arxiv.org/abs/2406.07328"
    website_url: "https://github.com/surgical-robotics-ai/realistic-6dof-data-generation"
    code_url: "https://github.com/jabarragann/6d_pose_collection_scripts"
    dataset_url: "https://www.kaggle.com/datasets/juanantoniobarragan/6-dof-pose-estimation-of-surgical-instruments"
---

## Overview

Development of high-fidelity digital twin environments for surgical suturing scenes, utilized for NSF <a href="https://github.com/surgical-robotics-ai/surgical_robotics_challenge" target="_blank">AccelNet Surgical Robotics Challenges</a>.

## Key Contributions

- Develop high-fidelity environments with realistic dynamic feedback for suturing execution on an open-source 3D simulation platform (<a href="https://github.com/WPI-AIM/ambf" target="_blank">AMBF</a>), utilized for NSF AccelNet Surgical Robotics Challenges
- Scan the real-world suturing training phantoms using MRI and import the segmented 3D models into the simulation environment
- Build photorealistic dVRK surgical instrument simulation models, sharing the models with the dVRK community
- Construct high-fidelity digital twin for suturing scenes in NVIDIA Omniverse Isaac Sim

## Simulation Scene Examples

<figure>
  <img src="/images/research/amf_suture_sim.png" alt="Description" style="width: 85%;">
  <figcaption>AMBF Simulation Scene</figcaption>
</figure>

<figure>
  <img src="/images/research/digital_twin_suture_sim.png" alt="Description" style="width: 85%;">
  <figcaption>NVIDIA Omniverse Isaac Sim Simulation Scene</figcaption>
</figure>

<!-- Add your media content below -->
<!-- ![Digital Twin Demo](/images/research/digital-twin.gif) -->
