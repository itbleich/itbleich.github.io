---
layout: page
title: Metadata- The Most Important Thing You'll Ever Save
published: false
---

# How to make sure no experimental data point is lost #



** 1. Embedding - Make your metadata inseparable from your data. **

** 2. Redundant Metadata Collection - The more, the merrier. **
              

Information about your experimental data, your metadata, can be more valuable than the data themselves. 
This page presents the workflow I use to make my experiments as metadata-proof as possible.

## What is metadata? ##
Metadata are everything required to transform a single experimental trial into a meaningful data point in a figure or statistical analysis. One of the most frustrating reasons preventing from trials to become real data points is when everything works perfectly, but during analysis you discover that you can't related the data to a specific experimental setting. The single experimental data is there but it has lost the context that gives it meaning. 
After dealing with numerous metadata-related issues throughout my research, these are the principles I follow to metadata-proof my experiments.


1.	Embedding - Whenever possible, incorporate essential experimental metadata directly into the raw data itself.
2.	Redundancy - Record metadata in multiple independent formats and locations. 

## Embedding ##

**The best metadata are impossible to get rid of**

The best metadata are always attached to the data themselves. Whenever possible, metadata should be embedded directly into the experiment instead of being stored alongside it. The harder it is to separate metadata from the data, the more likely both will remain together throughout the lifetime of the dataset.

One example of this principle is a workflow I use for embedding experimental metadata directly into neurophysiological recordings through the photodiode trigger signal of the experiment. The trigger signal is saved along with the recording signals and thus, in addition to using the trigger channel  for stimulus synchronization, the same signal also encodes key experimental metadata using pulse-duration modulation and an 8-bit binary representation. As a result, the metadata become an integral part of the recorded data stream and remain permanently attached to every neurophysiological recording I make.

The raw data file effectively becomes its own experiment log. As a result, it can be interpreted and analyzed without relying on separate log files. While this implementation was developed for visual stimulation using PsychoPy and a photodiode, the underlying principle is much broader: whenever possible, make your metadata inseparable from your data.

This is how it looks when the signal is visualized:

<img src="/assets/photodiode_1.jpg"
     alt="photodiode trigger and metadata saver 1"
     style="width:500px; max-width:100%; height:auto;">



<img src="/assets/photodiode_2.jpg"
     alt="photodiode trigger and metadata saver 2"
     style="width:500px; max-width:100%; height:auto;">


This approach can, of course, be extended to more sophisticated forms of data embedding and adapted to other experimental systems that do not rely on a photodiode.

**Code and implementation:**  
[View the PsychoPy photodiode metadata encoding repository on GitHub](https://github.com/itbleich/experimental-metadata-trigger-encoding)


## Redundancy ##

**There is no such thing as metadata over-registration.**

The more independent ways your metadata are recorded, the better. No logging method is completely failure-proof, so critical information should never rely on a single source. Redundancy not only protects against data loss but also allows cross-checking, and synchronization between different systems (i.e. different devices involved in the same experiment).

For example, in a behavioral experiment involving visual stimulation, I record metadata through every device participating in the experiment. My stimulus script  generates log files containing all relevant experimental parameters. At the same time, whenever possible, I position the behavioral camera so that it captures at least part of the stimulus display. In addition, at the beginning of every recording I verbally state the date, time, stimulus, and experimental group. Because this information becomes part of the video itself, it remains attached to the raw data wherever the file is copied, moved, or shared. These simple redundancies have repeatedly saved me from losing valuable experimental context.

Does this make the system failure-proof? 

No. But it greatly improves the chances that every experimental trial will remain interpretable and ultimately become analyzable.
Build your experiments so that every critical piece of metadata exists in multiple independent forms.

**All metadata fail. They rarely fail all at once.**


<img src="/assets/metadata_final_3_recursive_loop.png"
     alt="Metadata recursive endless loop"
     style="width:500px; max-width:100%; height:auto;">

**There is no such thing as metadata over-registration.**






