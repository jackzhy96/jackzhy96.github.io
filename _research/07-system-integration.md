---
title: "Surgical Robotics System Integration and Teleoperation"
excerpt: "Integration of photo-acoustic probes, advanced teleoperation with sEMG biofeedback, and etc."
collection: research
order: 7
year: 2022
venue: "Worcester Polytechnic Institute"
location: "Worcester, MA"
tags:
  - System Integration
  - Teleoperation
  - Photoacoustics
  - Augmented Reality
# Add your image or GIF here:
# header:
#   teaser: "research/system-integration.gif"

publications:
  - title: "Intraoperative laparoscopic photoacoustic image guidance system in the da Vinci surgical system"
    authors: "Gao, S., Wang, Y., Ma, X., Zhou, H., Jiang, Y., Yang, K., ..., & Zhang, H. K."
    venue: "Biomedical Optics Express"
    year: 2023
    paper_url: "https://doi.org/10.1364/BOE.498052"
    teaser: "research/PA_overview.png"
    
  - title: "Laparoscopic photoacoustic imaging system integrated with the da Vinci surgical system"
    authors: "Gao, S., Wang, Y., Zhou, H., Yang, K., Jiang, Y., Lu, L., ..., & Zhang, H. K."
    venue: "Medical Imaging: Image-Guided Procedures, Robotic Interventions, and Modeling, SPIE"
    year: 2023
    paper_url: "https://doi.org/10.1117/12.2653967"
    teaser: "research/PA_tool.png"
    
  - title: "A sEMG Proportional Control for the Gripper of Patient Side Manipulator in da Vinci Surgical System"
    authors: "Yang, K., Meier, T. B., Zhou, H., Fischer, G. S., & Nycz, C. J."
    venue: "Intl. Conf. of the IEEE Engineering in Medicine & Biology Society (EMBC)"
    year: 2022
    paper_url: "https://doi.org/10.1109/EMBC48229.2022.9871664"
    teaser: "research/sEMG_teleop.jpg"
---

## Overview

Research on integrating various sensing modalities and control interfaces with the da Vinci Research Kit.
- photo-acoustic probes integration with dVRK PSM:
<figure>
  <img src="/images/research/PA_overview.png" alt="Description" style="width: 85%;">
  <figcaption>Overall Photo-Acoustic System</figcaption>
</figure>
<figure>
  <img src="/images/research/PA_tool.png" alt="Description" style="width: 85%;">
  <figcaption>Instrument Integration Overview</figcaption>
</figure>
- sEMG biofeedback for teleoperation
<figure>
  <img src="/images/research/sEMG_teleop.jpg" alt="Description" style="width: 85%;">
  <figcaption>sEMG-based Teleoperation Overview</figcaption>
</figure>

## Key Contributions

- Developed a novel teleoperation approach using sEMG biofeedback signals
- Integrated a photo-acoustic probe with a dVRK instrument and installed on the dVRK Patient Side Manipulator (PSM)
- Constructed the kinematic model for the custom instrument to enable teleoperation and script-based control
- Developed the synchronized autonomous scanning system using ROS communication for image overlay
- Enabled teleoperation for dVRK PSMs with multiple common haptic devices, such as Phantom Omni and Razer Hydra controller, subsequently utilized in a dVRK-based AR measurement system
- Developed the <a href="https://github.com/jackzhy96/Touch_Tomorrow" target="_blank">teleoperation pipeline</a> that enabled participants to remotely operate the dVRK PSM during WPI’s 2022 <a href="https://wp.wpi.edu/touchtomorrow/" target="_blank">TouchTomorrow</a> event.

<!-- Add your media content below -->
<!-- ![System Integration Demo](/images/research/system-integration.gif) -->
