---
layout: page
title: Deep Inverse Reinforcement Learning
description: Learning a reward/cost function with Deep Neural Networks
img: /assets/img/carla.png
importance: 4
category: ML + Autonomous Driving
---

<div class="row justify-content-sm-center">
    <div class="col-sm-22 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/carla.png' | relative_url }}" alt="" title="CARLA simulator"/>
    </div>
</div>
<div class="caption">
    Lane changing in a dense traffic scenario in CARLA simulator.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-22 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/rviz_occupancy.png' | relative_url }}" alt="" title="Learned high reward region in Red"/>
    </div>
</div>
<div class="caption">
    The learned high reward region from human driving data (Red: high reward).
</div>


It can be difficult to autonomously produce driver behavior so that it appears natural to other traffic participants. Through Inverse Reinforcement Learning (IRL), we can automate this process by learning the underlying reward function from human demonstrations.

We propose a new IRL algorithm that learns costmaps that can be used by Model Predictive Controllers (MPCs) to perform a task without any hand-designing or hand-tuning of the cost function.


## Publications:
1. **K. Lee**, B. Vlahov, J. Gibson, J. M. Rehg, and E. A. Theodorou. "Approximate Inverse Reinforcement Learning from Vision-based Imitation Learning." 2021 IEEE International Conference on Robotics and Automation (ICRA). <a href="https://arxiv.org/abs/2004.08051">[PDF]</a> <a href="https://drive.google.com/file/d/14XbceV8czvdwh0T-K9U8sHTaBxtjYOh1/view">[BibTeX]</a> <a href="https://www.youtube.com/watch?v=WyJfT5lc0aQ"> [Video]</a>

2. **K. Lee**, D. Isele, E. A. Theodorou, S. Bae. "Spatiotemporal Costmap Inference for MPC via Deep Inverse Reinforcement Learning." IEEE Robotics and Automation Letters (RA-L), 2022. <a href="https://arxiv.org/abs/2201.06539">[PDF]</a> <a href="https://drive.google.com/file/d/1L0gGurBnsY4zoTuNWOgovwx2KJjfFBVu/view">[BibTeX]</a> <a href="https://youtu.be/Ft4u5AclSLA"> [Video]</a>

3. **K. Lee**, D. Isele, E. A. Theodorou, S. Bae. "Risk-sensitive MPCs with Deep Distributional Inverse RL for Autonomous Driving." IEEE/RSJ International Conference on Intelligent Robots and Systems
(IROS), 2022.
