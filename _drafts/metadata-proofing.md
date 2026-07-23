---
layout: page
title: Metadata: The Most Important Thing You'll Ever Save
published: false
---

# Metadata: The Most Important Thing You'll Ever Save

...


Why Experiments Become Uninterpretable

We've all experienced it.

You open a dataset collected six months—or six years—ago, convinced you'll be able to continue where you left off. The files are all there. Nothing is missing.

And yet, the experiment is effectively lost.

Was the stimulus moving left or right? Which version of the analysis script generated these results? Was this animal excluded for a reason? Why are there only 18 trials instead of the expected 20? Was the camera running at 100 or 200 fps? At some point, you knew the answer to all of these questions. Now you don't.

Most datasets don't become unusable because the data disappear. They become unusable because the context disappears.

Data are easy to preserve. Context is not.

Modern research laboratories are remarkably good at backing up raw data. Hard drives fail less often than they used to, cloud storage is inexpensive, and data can be copied indefinitely.

The real challenge is preserving everything that gives those data meaning:

Experimental parameters
Hardware configurations
Software versions
Stimulus settings
Calibration values
Exclusion criteria
Notes made during the experiment
Unexpected events that never made it into the methods section

Without this information, interpreting the data becomes increasingly difficult over time.

Your future self is your most important collaborator

One realization has changed the way I design experiments: the person most likely to use today's data in the future is me.

By the time I return to a dataset, I may have forgotten details that once seemed too obvious to record. What feels impossible to forget today often becomes impossible to remember months later.

I now try to build experiments that explain themselves. Whenever possible, metadata are generated automatically, embedded directly into the recorded data, or stored in a way that makes them difficult to separate from the experiment they describe.

Building experiments that survive time

The goal isn't to collect more metadata. It's to ensure that the essential context remains attached to the data throughout their lifetime.

The ideas in this section reflect workflows and practices that I've found useful for making experiments more robust, reproducible, and resilient to the inevitable loss of human memory.

If even one future dataset is saved from becoming an unsolved mystery, they'll have been worth sharing.

My philosophy

Embed your metadata in every way and on every medium possible.

If a parameter is important enough to record once, it's important enough to record multiple times. Store it in trigger channels, log files, filenames, analysis outputs, configuration files, and anywhere else it naturally belongs.

In most areas of engineering, redundancy is something to minimize. With experimental metadata, I believe the opposite is true: redundancy is a blessing. You never know which storage method will fail, which file will become separated from the dataset, or which piece of information you'll wish you had recorded. By preserving the same metadata across multiple media, you greatly increase the chances that your experiments will remain interpretable years into the future.

The goal is simple: no single lost file should make an experiment impossible to interpret.

