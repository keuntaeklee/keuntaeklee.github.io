---
layout: page
title: Controlling the Vision
description: PixelMPC with a Learned Optical Flow Dynamics
img: /assets/img/pixeltraj_plot.png
importance: 6
category: ML + Autonomous Drone
---

## Problem of the high-speed racing

In drone racing with a drone equipped with a camera, it is important to control the drone to see and collect more useful information, for example, by pitching up or rolling/yawing. 
However, this conflicts with the high-speed flying task for a drone because a quadrotor needs to pitch down to fly at a high speed and this results in losing more visual information.



## Controlling the Vision

We introduce deep optical flow (DOF) dynamics, which is a combination of optical flow and robot dynamics. With the DOF dynamics, we can predict the optical flow of the next image captured by the camera mounted on the drone. This prediction is coming from the control action the drone takes.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/dof.png' | relative_url }}" alt="" title="Pixel Trajectory"/>
    </div>
</div>
<div class="caption">
    *Left*: Legend of optical flow. *Middle*: The ground truth of optical flow, calculated from collected data. *Right*: The predicted optical flow from the learned model.
</div>

Using the DOF dynamics, PixelMPC explicitly incorporates the predicted movement of relevant pixels into the planned trajectory of a robot.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/pixeltraj.png' | relative_url }}" alt="" title="Pixel Trajectory"/>
    </div>
</div>
<div class="caption">
    The future movement of the target pixel (the center of a racing gate) predicted by propagating the learned pixel dynamics with MPC.
</div>

With the proposed MPC approach, the drone can achieve both a visual tracking task and the high speed racing task together.

## Publications:
1. **K. Lee**, J. Gibson, and E. A. Theodorou. "Aggressive Perception-Aware Navigation using Deep Optical Flow Dynamics and PixelMPC". IEEE Robotics and Automation Letters (RA-L), 2020. <a href="https://ieeexplore.ieee.org/document/8957291">[PDF]</a> <a href="https://drive.google.com/file/d/16E0-Ys0HDa6L_-fxsym4X6GkI89Fh6fM/view">[BibTeX]</a> <a href="https://www.youtube.com/watch?v=NzL2YRcOh_I"> [Video]</a>

