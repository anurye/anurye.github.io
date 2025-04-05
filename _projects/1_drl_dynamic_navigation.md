---
layout: page
title: Mobile Robot Navigation in Dynamic Environments
description: Deep Reinforcement Learning for dynamic robot navigation
img: assets/img/project_preview/msc_thesis/network-architecture.png
importance: 3
category: Navigation
giscus_comments: true
---

**Author:** Ahmed Yesuf Nurye  
**Advisor:** [Prof. Elżbieta Jarzębowska](https://www.meil.pw.edu.pl/daas/DAAS2/People/Elzbieta-Jarzebowska)

<div style="display: flex; justify-content: center; gap: 2rem; align-items: center; margin-bottom: 2rem;">

  <a href="/assets/pdf/Mobile_Robot_Navigation_in_Dynamic_Environments.pdf" target="_blank" style="text-decoration: none; text-align: center;">
    <i class="fas fa-file-pdf fa-3x"></i><br>
    <span>Read Thesis</span>
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

We present a framework for mobile robot navigation in dynamic environments using Deep Reinforcement Learning (DRL) and the Robot Operating System (ROS). Traditional navigation methods often lack the real-time adaptability required in highly dynamic settings. To address this, we leverage the [TD7](https://arxiv.org/abs/2306.02451) algorithm---an extension of the Twin Delayed Deep Deterministic Policy Gradient (TD3) algorithm incorporating state and state-action embeddings---to directly map raw sensor inputs to control actions. These embeddings, trained to minimize the mean squared error (MSE) between the encoded state-action representation and the transition-predicted next state, enhance the system's ability to model environment dynamics and improve navigation performance.

Extensive simulations were conducted in custom Gazebo environments of increasing complexity, ranging from open spaces to scenarios with static obstacles and moving actors. Performance was evaluated based on navigation success rate, time to goal, path efficiency, and collision rate. Results indicate that this approach consistently improves navigation performance, particularly in highly dynamic environments.

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
@mastersthesis{Nurye-2024,
  author = {Nurye, Ahmed Y.},
  title = {Mobile Robot Navigation in Dynamic Environments},
  year = {2024},
  month = oct,
  school = {Warsaw University of Technology},
  address = {Warsaw, Poland},
  number = {WUT4f18e5c2cd214a9cb555f730fa440901},
  keywords = {Mobile Robot Navigation, Deep Reinforcement Learning, ROS2, Gazebo},
}
```

{% endraw %}
