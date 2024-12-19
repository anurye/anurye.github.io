---
layout: page
title: Six Degree of Freedom Serial Manipulator
description: analytical inverse kinematics solution, trajectory planning, testing
img: assets/img/project_preview/six_dof_manipulator_matlab.png
importance: 2
category: Kinematics
giscus_comments: true
---

**Authors:** Ahmed Yesuf Nurye, Taye Tsehaye Alamrew, Dilge Vurmaz, Mete Ogulcan Ozduygu  
**Advisor:** Dr. Pawel Maciąg

<div style="display: flex; justify-content: center; gap: 2rem; align-items: center; margin-bottom: 2rem;">

  <a href="https://github.com/anurye/six-degree-of-freedom-serial-manipulator" target="_blank" style="text-decoration: none; text-align: center;">
    <i class="fab fa-github fa-3x"></i><br>
    <span>GitHub Repository</span>
  </a>

  <a href="https://petercorke.com/toolboxes/robotics-toolbox/" target="_blank" style="text-decoration: none; text-align: center;">
    <i class="fas fa-tools fa-3x"></i><br>
    <span>Robotics Toolbox</span>
  </a>

</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_preview/manipulator_kinematics/pick_and_place.gif" title="example simulation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example simulation.
</div>

---

## **Abstract**

This project presents the design and implementation of a six-degree-of-freedom serial manipulator with a spherical wrist configuration. An analytical solution to the inverse kinematics problem was developed to ensure precise and computationally efficient trajectory planning in both joint and task spaces. The manipulator's capabilities were validated through simulation and successful hardware demonstrations, including real-time pick-and-place tasks.

---

## **Introduction**

The aim was to:

1. Model the 6-DoF manipulator kinematics analytically.
2. Implement trajectory planning in joint and task space.
3. Test and validate the kinematic model in both simulated and real environments.

Key challenges:

- **Managing singularities during inverse kinematics:** Singularities were addressed by analyzing the Jacobian and excluding configurations leading to rank deficiency.
- **Synchronizing multi-joint trajectories for smooth motion:** This was critical for ensuring the manipulator's accuracy and efficiency during real-time tasks.

---

## **Methods**

### **Kinematic Analysis**

- **Modified DH Parameters:** Used for frame assignments and transformations.
- **Singularities:** Identified via Jacobian analysis; configurations causing rank deficiency were excluded.

The manipulator’s kinematic configuration and workspace are visualized below:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_preview/six_dof_manipulator_matlab.png" title="Manipulator Home Configuration" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Manipulator in Home Configuration (MATLAB Visualization using Peter Corke’s Robotics Toolbox).
</div>

### **Trajectory Planning**

- **Joint Space (LSPB):** Smooth transitions with synchronized joint movements.
- **Task Space:** Linear interpolation was used to achieve precise straight-line end-effector motion during the approach and retraction phases of the pick-and-place task.

---

## **Results**

### **Simulation**

- **Accuracy:** Both forward and inverse kinematics passed MATLAB validation against the Robotics Toolbox with a tolerance of MATLAB’s single-precision floating-point limit (`eps('single')`).
- **Trajectory Planning:** Pick-and-place tasks were executed using synchronized joint trajectories.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/task_joint_traj.png" title="Comparison of Joint and Task Space Trajectories." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Comparison of Joint and Task Space Trajectories.
</div>

### **Hardware Implementation**

- **Setup:** Dynamixel servos were configured using MATLAB scripts to ensure precise communication and control of joint motions.
- **Outcome:** The hardware implementation successfully replicated the pick-and-place task.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <iframe width="100%" height="315" src="https://www.youtube.com/embed/mdQygfjbZLo?mute=1" 
                frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                allowfullscreen></iframe>
    </div>
</div>
<div class="caption">
    Video: Pick-and-place task execution.
</div>

---

## **Further Reading**

For foundational concepts in robotics, refer to the following textbook:

- John J. Craig. _Introduction to Robotics: Mechanics and Control_. 4th Edition, Pearson, 2018.
