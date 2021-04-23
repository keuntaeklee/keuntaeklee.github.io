---
layout: page
title: Objective Learning
description: Learning an implicit objective function with Deep Neural Networks to generalize to new environments
img: /assets/img/shadow.jpg
importance: 4
category: ML + Autonomous Driving
---

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/shadow.jpg' | relative_url }}" alt="" title="Shadow"/>
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/dayandnight.jpg' | relative_url }}" alt="" title="Day and Night"/>
    </div>
</div>
<div class="caption">
    Various lighting conditions autonomous cars see in the real world.
</div>

Data-driven approaches in safety-critical systems are easy to fail.

Now only due to the change of lighting conditions shown above, there are numerous cases that could fail the deep learned moels.

One big challenge of deel models are the generalizability to new environments. Imagine a deep learning model of your self-driving car was trained in U.S., and you're testing them in Korea.

Especially, when the learned mapping via ML/DL is to the final decision (control action), the DL model tends to fail more.

To solve this issue, instead of learning the control policy of the expert from data, we propose to learn, from the same data, an objective function of an expert when the data was collected. In this way, the predicted objective function will be less vulnerable to new inputs (environments).

Some examples of Objective Learning includes Inverse Reinforcement Learning and Inverse Optimal Control. Both learns the implicit reward/cost function from the observed data (expert's demonstration).

In this project, we learned the implicit cost function (costmap) from data and showed a better generalizability compared to the other end-to-end learning approach and the supervised costmap learning approach.

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/Marietta_input_img_000348.png' | relative_url }}" alt="" title="new input"/>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/Marietta_output_img_000348.png' | relative_url }}" alt="" title="airl"/>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/Marietta_paul_output000348.png' | relative_url }}" alt="" title="supervised"/>
    </div>
</div>
<div class="caption">
*Left*: A new input image to the trained model. *Middle*: Our approach of predicting a costmap. *Right*: The state-of-the-art supervised learning approach.
</div>

## Publications:
1. **K. Lee**, B. Vlahov, J. Gibson, J. M. Rehg, and E. A. Theodorou. "Approximate Inverse Reinforcement Learning from Vision-based Imitation Learning." 2021 IEEE International Conference on Robotics and Automation (ICRA). <a href="https://arxiv.org/abs/2004.08051">[PDF]</a> <a href="https://drive.google.com/file/d/14XbceV8czvdwh0T-K9U8sHTaBxtjYOh1/view">[BibTeX]</a> <a href="https://www.youtube.com/watch?v=WyJfT5lc0aQ"> [Video]</a>

