---
layout: page
title: When does ML-based driving fail?
description: Failure detection with Bayesian Neural Networks and MPC
img: /assets/img/stop.jpg
importance: 3
category: ML + Autonomous Driving
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/foolstop.png' | relative_url }}" alt="" title="foolstop"/>
    </div>
</div>
<div class="caption">
    An example of a fooled ML-based model. Source: Eykholt, K. et al. CVPR 2018.
</div>

Data-driven approaches in safety-critical systems are easy to fail. It is necessary to detect when they will fail, before it happens.

We propose the use of Bayesian networks, which provide both a mean value and an uncertainty estimate (variance) as output, to enhance the safety of end-to-end learned deep control policies trained for autonomous driving.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/lee2019earlyfig1b.png' | relative_url }}" alt="" title="lee2019earlyfig1b"/>
    </div>
</div>
<div class="caption">
    Increased output variance from the Bayesian neural network due to a novel test-time input.
</div>


Especially the failure of vision-based deep models (e.g. camera-based end-to-end controllers) can be detected much earlier if we combine the model predictive control (MPC) with them.

MPC can guide the vision system *where to focus* and embed an attention mechanism into the vision pipeline. We train Bayesian convolutional neural networks to predict regions of interest in the input visual information and perform early failure detection of end-to-end trained controllers.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/lee2019papcfig2c.png' | relative_url }}" alt="" title="lee2019papcfig2c"/>
    </div>
</div>
<div class="caption">
    MPC embeds attention mechanisms on the input vision information for the Bayesian CNN.
</div>


## Publications:
1. **K. Lee**, G. N. An, V. Zakharov, and E. A. Theodorou. "Perceptual Attention-based Predictive Control." 3rd Conference on Robot Learning (CoRL), 2019. (Acceptance rate: 27%) <a href="http://proceedings.mlr.press/v100/lee20b.html">[PDF]</a> <a href="https://drive.google.com/file/d/1zhzlFdBdhkpy0UEXwQshJoYTdQ7KgGig/view">[BibTeX]</a> <a href="https://www.youtube.com/watch?v=-Zmi0HCvM9I"> [Video]</a>
2. **K. Lee**, Z. Wang, B. Vlahov, H. Brar, and E. A. Theodorou. "Ensemble Bayesian Decision Making with Redundant Deep Perceptual Control Policies." The 18th IEEE International Conference on Machine Learning and Applications (ICMLA), 2019. (Acceptance rate, Long paper : 28%) <a href="https://ieeexplore.ieee.org/abstract/document/8999215">[PDF]</a> <a href="https://drive.google.com/file/d/1VwP9cD5If7W-PKhZ1oTT36X7ZG5yBtjc/view">[BibTeX]</a> <a href="https://www.youtube.com/watch?v=poRbH__kB2M">[Video]</a> 
3. **K. Lee**, K. Saigol, and E. A. Theodorou. "Early Failure Detection of Deep End-to-End Control Policy by Reinforcement Learning." 2019 IEEE International Conference on Robotics and Automation (ICRA). <a href="https://ieeexplore.ieee.org/abstract/document/8794189">[PDF]</a> <a href="https://drive.google.com/file/d/1S2cR0UrAyt-IIDHkFL7O5g-zz4_RfxSC/view">[BibTeX]</a> <a href="https://www.youtube.com/watch?v=UQwhVuMJK7E">[Video]</a>
4. **K. Lee**, K. Saigol, and E. A. Theodorou. "Safe Imitation Learning for End-to-End Control."  Robotics: Science and Systems(RSS) Workshop on Adversarial Robotics, 2018. <a href="https://www.semanticscholar.org/paper/Safe-Imitation-Learning-for-End-to-End-Control-Lee-Saigol/59bd8cf6cb618d056d7bdb477909f08f4d77e641?p2df">[PDF]</a> <a href="https://drive.google.com/file/d/1Sr6wzUg8-hPbjKOk9K0tYASnl1mKOEYA/view">[BibTeX]</a> <a href="https://www.youtube.com/watch?v=UQwhVuMJK7E">[Video]</a>

