---
layout: default
title: Homework 1
---

# Overall

My homework 1 is done under the Optix API.

# Acceleration 

Since using optix, I implemented the bounding box function and then activate the "Trbvh". With the acceleration structure, the rendering of a single frame of the scene 7 costs 0.0723 seconds. Without that, it costs 0.0887 seconds.

# Special Implementation

I add a simple implementation to achieve the depth of view effect. Shown below:
<div style="text-align:center"><img src="figures/hw1/fig1.png" width="897" height="501"  /></div>

You can see the balls in the front and black are out of focus and have been blurred.

My implementation is using multiple sample rays. Instead of sending one ray from the "eye" position, I make the eye position as a center of a ball with radian $r$, and sample different starting points on that ball to make sample rays. The sampling method is rejection sampling. Then, I send 200 rays for each pixels and average the color.

<div style="text-align:center"><img src="figures/hw1/fig2.png" width="594" height="295"  /></div>