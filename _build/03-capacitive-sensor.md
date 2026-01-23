---
title: "Custom Capacitive Contact Sensor"
excerpt: "Design and implementation of custom capacitive sensor for tool-tissue contact detection. More details will be shared later, stay tuned!"
collection: build
order: 3
year: 2025
venue: "Johns Hopkins University"
tags:
  - Sensor Design
  - Capacitive Sensing
  - Arduino
  - System Integration
# Add your image or GIF here:
# header:
teaser: "build/contact_sensor.jpeg"
code_url: "coming_soon"

publications:
  - title: "SurgSync: Time-Synchronized Multi-modal Data Collection Framework and Dataset for Surgical Robotics"
    authors: "Zhou, H.*, Liu, C.*, Wu, Y., ..., & Kazanzides, P."
    venue: "IEEE Intl. Conf. on Robotics and Automation (ICRA)"
    year: 2026
    submit_year: 2025
    under_review: true
---

## Overview

Design and implementation of a custom capacitive contact sensor to acquire ground truth data for tool-tissue contact detection in surgical robotics research. More details will be shared later, stay tuned!

<figure>
  <div style="display: flex; gap: 1em;">
  <img src="/images/build/contact_sensor.jpeg" alt="Before" style="width: 42%;">
  <img src="/images/build/sensor_connection.jpeg" alt="After" style="width: 42%;">
</div>
  <figcaption>Custom Capacitive Contact Sensor. Left: Contact sensor for 3 dVRK PSMs. Right: Contact Sensor Connect to the dVRK controller</figcaption>
</figure>

## Technical Details

- Leverage Arduino microcontroller to implement the capacitive sensor
- Seamlessly integrated the sensor with the dVRK controller
- Implemented signal processing for contact detection
- Validated sensor performance with tissue phantoms

## Integration with dVRK tools

This sensor is used to provide ground truth labels for tool-tissue contact detection.

**More details will be added later. Stay tuned!**

<figure>
  <img src="/images/build/sensor_tool_integration.png" alt="Description" style="width: 85%;">
  <figcaption>Instrument wire connection. Non-polar instrument on the left, monopolar in the center, and bipolar on the right. For non-polar instrument, the tool housing is opened and the wire insulation layer is removed for better visualization.</figcaption>
</figure>

<!-- Add your media content below -->
<!-- ![Capacitive Sensor](/images/build/capacitive-sensor.jpg) -->
