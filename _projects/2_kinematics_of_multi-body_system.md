---
layout: page
title: Kinematics of Multi-body System
description: kinematic analysis of a general case planar multi-body system using absolute coordinates
img: assets/img/project_preview/multibody_kinematics/mechanism.png
importance: 3
category: Kinematics
giscus_comments: true
---

**Authors:** Ahmed Yesuf Nurye  
**Advisor:** [Prof. Janusz Frączek](https://ztmir.meil.pw.edu.pl/web/eng/People/prof.-Janusz-Fraczek)

<div style="display: flex; justify-content: center; gap: 2rem; align-items: center; margin-bottom: 2rem;">

  <a href="https://github.com/anurye/kinematics-of-multi-body-system" target="_blank" style="text-decoration: none; text-align: center;">
    <i class="fab fa-github fa-3x"></i><br>
    <span>GitHub Repository</span>
  </a>

  <a href="/assets/pdf/Dynamics_of_Multi_body_Systems.pdf" target="_blank" style="text-decoration: none; text-align: center;">
    <i class="fas fa-file-pdf fa-3x"></i><br>
    <span>Read Report</span>
  </a>

</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="/assets/img/project_preview/multibody_kinematics/mechanism.png" title="example mechanism" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example mechanism.
</div>

---

## **Abstract**

To address scalability challenges in joint-coordinate methods for complex mechanisms, we developed an alternative approach based on absolute coordinates. Absolute coordinates localize the constraint equations to individual joints, resulting in inherently sparse constraint and Jacobian matrices that are computationally efficient to solve. The solver employs the Newton-Raphson method to solve the nonlinear constraint equations for position and uses the Jacobian matrix to compute the velocities and accelerations of any point on the bodies of the mechanism.

---
