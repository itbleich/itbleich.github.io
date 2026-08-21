---
layout: page
title: "Trackball Analysis of Motion"
permalink: /research/trackball/
published: true
---

Trackball-based assays are a practical way to quantify locomotion and steering behavior in tethered animals while preserving precise control of sensory stimuli.
This page outlines the workflow I use to extract behavioral kinematics from trackball recordings with FicTrac.

## Why use a trackball setup?

In many experiments, I need both:

- controlled visual stimulation, and
- high-resolution measurements of movement dynamics.

A trackball setup makes this possible by allowing continuous readout of forward, lateral, and rotational motion while the animal remains in a stable recording configuration.

## Core workflow

1. **Acquisition and synchronization**  
   Record trackball motion alongside stimulus timing and experimental metadata.

2. **Preprocessing**  
   Organize trials, verify synchronization, and remove unusable segments.

3. **FicTrac-based extraction**  
   Convert raw trackball motion into velocity and turning time series.

4. **Trial-level quantification**  
   Compute behavioral features such as response latency, steering bias, pause structure, and movement amplitude.

5. **Condition-level comparison**  
   Compare kinematic features across stimulus conditions and experimental groups.

## Kinematic outputs I typically analyze

- Forward walking velocity
- Angular turning velocity
- Lateral displacement components
- Pause/move structure (duration and frequency)
- Stimulus-locked response timing

## Quality-control principles

- Keep metadata tightly linked to every trial.
- Validate temporal alignment between stimulus and behavior before analysis.
- Track exclusion criteria explicitly and reproducibly.
- Preserve both processed outputs and intermediate analysis states.

## Practical note

The exact implementation details (hardware geometry, calibration values, and parameter settings) can vary between preparations and experimental aims.
The key principle is to keep the pipeline transparent, reproducible, and robust to re-analysis over time.

<p class="back-link">← <a href="{{ '/Research_and_Insights/' | relative_url }}">Back to Research &amp; Insights</a></p>
