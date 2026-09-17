---
layout: page
title: "Trackball Analysis of Motion"
permalink: /research/trackball/
published: false
---

Behavioral analysis using a trackball

A trackball is a useful tool for behavioral tracking, allowing an animal to perform relatively natural walking behavior while remaining stationary relative to the experimental setup. At the same time, the rotation of the ball provides continuous quantitative information about the animal’s locomotion.

This page provides a basic introduction to extracting motion parameters from trackball recordings.

I analyze trackball motion using FicTrac, although other tracking methods can also be used. FicTrac uses visual markings on the trackball to estimate its rotation by comparing its position between consecutive video frames. The resulting data are saved in a CSV file containing several parameters describing the ball’s motion. FicTrac analysis is based on the rotation of the ball around three axes.

For this example, I will focus on three raw parameters representing the relative rotation around each of these axes between consecutive frames. These parameters form the basis for calculating other motion parameters.

First, let’s look at the raw output. It is quite noisy, even when the locust and the ball are motionless. We therefore apply a sliding median window to reduce this noise and make the underlying motion patterns easier to interpret.

Let’s look at three short videos illustrating different types of movement to understand how these parameters work. The videos show three distinct behaviors: pausing, forward motion, and sideways motion. We can examine how each of the three parameters changes across these different behaviors.
