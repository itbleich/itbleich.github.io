---
layout: page
title: Metadata- The Most Important Thing You'll Ever Save
published: false
---

### my approch for making sure no experimental data point is lost: ###
### 1. Redundant Metadata Collection - The more, the merrier. ###
### 2. Embedding - Make your metadata inseparable from your data. ###
              

 **All metadata fail. They rarely fail all at once.**

Build your experiments so that every critical piece of metadata exists in multiple independent forms.

Information about your experimental data, your metadata, can be more valuable than the data themselves. 
This page presents the workflow I use to make my experiments as metadata-proof as possible.

What is metadata?
From my perspective, metadata are everything required to transform a single experimental trial into a meaningful data point in a figure or statistical analysis. One of the most frustrating reasons preventing from trials to become real data points is when everything works perfectly, but during analysis you discover that you can't related the data to a specific experimental setting. The single experimental data is there but it has lost the context that gives it meaning. 
After dealing with numerous metadata-related issues throughout my research, these are the principles I follow to metadata-proof my experiments.

1.	Redundancy - Record metadata in multiple independent formats and locations. 
2.	Embedding - Whenever possible, incorporate essential experimental metadata directly into the raw data itself. 


**Redundancy**
The more independent ways your metadata are recorded, the better. No logging method is completely failure-proof, so critical information should never rely on a single source. Redundancy not only protects against data loss but also allows cross-checking, and synchronization between different systems (i.e. different devices involved in the same experiment).

For example, in a behavioral experiment involving visual stimulation, I record metadata through every device participating in the experiment. My stimulus script automatically generates log files containing all relevant experimental parameters. At the same time, whenever possible, I position the behavioral camera so that it captures at least part of the stimulus display. In addition, at the beginning of every recording I verbally state the date, time, stimulus, and experimental group. Because this information becomes part of the video itself, it remains attached to the raw data wherever the file is copied, moved, or shared. These simple redundancies have repeatedly saved me from losing valuable experimental context.

Does this make the system failure-proof? 

No. But it greatly improves the chances that every experimental trial will remain interpretable and ultimately become analyzable.

The following principles summarize my approach:

**Every metadata source can fail. They rarely all fail at once.**

**There is no such thing as metadata over-registration.**
