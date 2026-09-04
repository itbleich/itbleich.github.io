---
layout: page
title: Metadata- The Most Important Thing You'll Ever Save
permalink: /research/metadata/
---

Information about your experimental data, your metadata, can be more valuable than the data themselves. 
This page presents the workflow I use to make my experiments as metadata-proof as possible.

<div style="display:flex; align-items:center; gap:30px; flex-wrap:wrap;">

  <div style="flex:1; min-width:280px;">
    <p><strong>The short version:</strong></p>

    <p><strong>1. Embedding — Make your metadata inseparable from your data.</strong></p>

    <p><strong>2. Redundant Metadata Collection — The more, the merrier.</strong></p>
  </div>

  <div style="flex:0 0 320px; text-align:center;">
    <img src="{{ '/assets/Metadata_proofed_no_background.png' | relative_url }}"
         width="320"
         alt="Metadata proofed"
         style="max-width:100%;
                height:auto;
                transform:rotate(-15deg);">
  </div>

</div>

## What is metadata? ##

Metadata are everything required to transform a single experimental trial into a meaningful data point in a figure or statistical analysis. When metadata are lost, corrupted, or lose their meaning, the data may ultimately lose their value altogether.

After dealing with numerous metadata-related issues throughout my research, I developed a set of principles that I now follow to make my experiments as metadata-proof as possible.

1.	Embedding - Whenever possible, incorporate essential experimental metadata directly into the raw data itself.
2.	Redundancy - Record metadata in multiple independent formats and locations. 

## Embedding ##

**The best metadata are impossible to get rid of**

Whenever possible, metadata should be embedded directly into the experiment rather than stored alongside it. The harder it is to separate the metadata from the data, the more likely they are to remain together throughout the lifetime of the dataset.

One example of this principle is a workflow I use to embed experimental metadata directly into neurophysiological recordings through the experiment’s photodiode trigger signal. The trigger signal is recorded alongside the neurophysiological signals and serves two purposes: in addition to providing stimulus synchronization, it encodes key experimental metadata using pulse-duration modulation and an 8-bit binary representation. In this way, the raw data file effectively becomes its own experiment log, reducing the risk of losing the information needed to interpret it.

While this implementation was developed for visual stimulation using PsychoPy and a photodiode, the underlying principle is much broader: whenever possible, make your metadata inseparable from your data.
This is how it looks when the signal is visualized:

<img src="/assets/photodiode_1.jpg"
     alt="photodiode trigger and metadata saver 1"
     style="width:500px; max-width:100%; height:auto;">



<img src="/assets/photodiode_2.jpg"
     alt="photodiode trigger and metadata saver 2"
     style="width:500px; max-width:100%; height:auto;">


This approach can be extended to more sophisticated forms of data embedding and adapted to other experimental systems that do not rely on a photodiode.

**Code and implementation:**  
[View the PsychoPy photodiode metadata encoding repository on GitHub](https://github.com/itbleich/experimental-metadata-trigger-encoding)


## Redundancy ##

**There is no such thing as metadata over-registration.**

The more independent ways your metadata are recorded, the better. No logging method is completely failure-proof, so critical information should never rely on a single source. Redundancy not only protects against data loss but also enables cross-checking and synchronization between different systems (i.e., different devices involved in the same experiment).

For example, this is my workflow for behavioral experiments involving visual stimuli:

A. My stimulus script generates log files containing all relevant experimental parameters.<br>
B. The behavioral camera is positioned so that it captures at least part of the stimulus display.<br>
C. At the beginning of every recording, I verbally state the date, time, stimulus, and experimental group, embedding this information directly in the video itself.

These simple redundancies have repeatedly saved me from losing valuable experimental context.

Does this make the system failure-proof? No. But it greatly improves the chances that every experimental trial will remain interpretable and, ultimately, analyzable.
Build your experiments so that every critical piece of metadata exists in multiple independent forms.

**All metadata fail. They rarely fail all at once.**


<img src="/assets/metadata_final_3_recursive_loop.png"
     alt="Metadata recursive endless loop"
     style="width:500px; max-width:100%; height:auto;">

**There is no such thing as metadata over-registration.**


← [Back to Research & Insights]({{ "/Research_and_Insights/" | relative_url }})






