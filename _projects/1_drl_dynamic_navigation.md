---
layout: page
title: Mobile Robot Navigation in Dynamic Environments
img: assets/img/project_preview/msc_thesis/network-architecture.png
importance: 1
category: Navigation
giscus_comments: true
---

<div style="text-align: center; margin-bottom: 1.5rem;">
  <a href="https://anurye.github.io/" target="_blank">Ahmed Yesuf Nurye</a><sup>1</sup>, <a href="https://www.meil.pw.edu.pl/daas/DAAS2/People/Elzbieta-Jarzebowska" target="_blank">Elżbieta Jarzębowska</a><sup>1</sup><br>
  
  <small><sup>1</sup> Warsaw University of Technology</small>
</div>

<div style="display: flex; justify-content: center; gap: 2rem; align-items: center; margin-bottom: 2rem;">

  <a href="/assets/pdf/MMAR_2025.pdf" target="_blank" style="text-decoration: none; text-align: center;">
    <i class="fas fa-file-pdf fa-3x"></i><br>
    <span>Read Paper</span>
  </a>

  <a href="https://github.com/anurye/Mobile-Robot-Navigation-Using-Deep-Reinforcement-Learning-and-ROS" target="_blank" style="text-decoration: none; text-align: center;">
    <i class="fab fa-github fa-3x"></i><br>
    <span>GitHub Repository</span>
  </a>

</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_preview/msc_thesis/simulation.gif" title="example simulation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example simulation.
</div>

---

## **Abstract**

This paper presents a framework for mobile robot navigation in dynamic environments using
deep reinforcement learning (DRL) and the Robot Operating System (ROS).
The framework enables proactive adaptation to environmental changes.
Traditional navigation methods typically assume a static environment and treat moving obstacles as
outliers during mapping and localization. This assumption severely limits the robustness of these
methods in highly dynamic settings such as homes, hospitals, and other public spaces. To overcome
this limitation, we employ encoder networks that jointly learns state and state–action
representations by minimizing the mean squared error (MSE) between predicted and actual next-state embeddings.
This approach explicitly captures the environment’s transition dynamics, enabling the robot to
anticipate and effectively navigate around moving obstacles.

We evaluate the proposed framework through extensive simulations in custom Gazebo worlds of
increasing complexity,ranging from open spaces to scenarios with densely populated static obstacles
and moving actors. We assess performance in terms of success rate, time to goal, path efficiency, and
collision rate. Results demonstrate that our approach consistently improves navigation performance,
particularly in highly dynamic environments.

---

## **Network Architecture**

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_preview/msc_thesis/network-architecture.png" title="network archtecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    To effectively capture dynamic actors in the environment, enabling the policy to make more informed actions, it is essential to predict the next state of the environment accurately. For this purpose, a pair of encoders (state and state-action encoders) are used. 
</div>

---

## **Simulation Environment**

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_preview/msc_thesis/reset_0.png" title="initial state" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_preview/msc_thesis/reset_1.png" title="state after first reset" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_preview/msc_thesis/reset_2.png" title="state after second reset" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Upon reset, the positions of the obstacles are randomly altered to enhance generalization, and new starting and target positions are generated randomly.
</div>

The framework was tested in Gazebo simulation environments with increasing level of complexity.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_preview/msc_thesis/test_env_0.png" title="test environment 1" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_preview/msc_thesis/test_env_1.png" title="test environment 2" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_preview/msc_thesis/test_env_2.png" title="test environment 3" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    We have tested our system in a range of environments that vary in complexity to assess its robustness and effectiveness.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_preview/msc_thesis/slam.gif" title="usage with SLAM toolbox" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    One of the potential application of this framework is exploration. We can use this framework to autonomously navigate in unknown environment and use SLAM frameworks to generate a map of that environment for further application.
</div>

{% raw %}

```bibtex
@INPROCEEDINGS{nurye2025,
author={Nurye, Ahmed Yesuf and Jarzebowska, Elzbieta},
booktitle={2025 29th International Conference on Methods and Models in Automation and Robotics (MMAR)},
title={Deep Reinforcement Learning for Mobile Robot Navigation in Dynamic Environments},
year={2025}
}
```

{% endraw %}
