---
layout: page
title: Experience
site_title: Experience
nav_bar: false
permalink: /experience/
image:
---

## <u>Work</u>

### TinyGrid
**New York**  
Building next-gen energy infrastructure for a scalable civilization. Stay tuned.

### DARPA AI Research
**New York**
[LINC](https://www.darpa.mil/program/learning-introspective-control):

Worked with the [Safe Robotics Lab](https://www.imperial.ac.uk/adaptive-intelligent-robotics/) at Princeton and [Adaptive and Intelligent Robotics Lab](https://www.imperial.ac.uk/adaptive-intelligent-robotics/) at Imperial College London to design robust controllers that can augment human drivers in unsafe and unseen environments. Used Hamilton Jacobi Isaacs formulation with game theoretic reinforcement learning for safety and Gaussian Processes with Quality Diversity for adaptation. Evaluated product on DoD site.

[SDCPS](https://www.darpa.mil/program/symbiotic-design-for-cyber-physical-systems):

Worked with the [Jha Lab](https://engineering.princeton.edu/faculty/niraj-jha) at Princeton and [Proof Lab](https://prooflab.stevens.edu) and [Robust Field Autonomy Lab](https://robustfieldautonomylab.github.io) at Stevens Institute of Technology to optimize the design of drones and submarines using sample efficient active learning, graph neural networks, and fitness surrogates.

### Cleveland Clinic AI Research
**Cleveland**

Working with the [Artificial Intelligence and Informatics in Imaging and Healthcare Lab](https://my.clevelandclinic.org/departments/pathology/depts/artificial-intelligence-data-science) to design models that understand patient data and can assist with real-time clinical decision makking. Using knowledge graph sampling with contrastive pre-training and conformal probability to develop SoTA models. 

### NASA
**Langley**

Worked on the next-gen [RAMPT project](https://www.nasa.gov/rapid-analysis-and-manufacturing-propulsion-technology/) to completely redesign the combustion chamber and nozzle of rockets. Optimized the adhesion between GrCop84 and Carbon Fiber pre-pregs using simulated and experimental techniques to potentially reduce total rocket mass by over 50%. Collaborated with NASA Glenn and NASA Huntsville on this multi-site project.

## <u>Education</u>

### Princeton University
**Bachelor of Science in Engineering '22**
**Major**: Mechanical and Aerospace Engineering <br>
**Minors**: Computer Science, Engineering Biology, Optimization and Quantitative Data Science

## <u>Projects</u>

### Design and Control of a Synthetic Bio-Organ
Used CAD software and 3D Stereolithography printing to design, fabricate, and test both pediatric and adult Bladder-Urethra models. Subsequently used C++ and TI software in combination with sensing hardware to design a stable, closed loop control system to maintain sphincter pressure during various stages of catheterization. Built a 3D Finite Element Model in Abaqus to model electrosurgery of the organ, including mechanical, thermal, and electrical fields to help inform power decisions during excision.

### Autonomous Cruise Control
Developed autonomous cruise control for mini toy-cars within a model city. Applied computer vision techniques with an onboard ZED2 Camera and used iLQR for control, with constraint costs ascertained from the road boundaries and SLAM. Used Partially Observable Markov Decision Processes to navigate car-car interactions within the model city, and developed algorithms for stop sign intersections. Gained extensive experience with Robotic Operation System (ROS) and sensing hardware.

### Meal Segmentation
Majority of America's rising health issues are related to lifestyle. And since corporate interests spend trillions per year on hijacking our biocircuits, we believe a strong solution is to counterbalance this with a health coach that lives in your pocket. That knows you and can tailor the recommendations better than any doctor can. To this end, we built a food detection, segmentation, and calorie estimation pipeline using the Dino and Segment Anything Models. We coupled this with an AI nutritionist and health coach using GPT4 and retrieval augmented generation. In the limit, we believe cheap, accessible, and highly tailored healthcare will be available for all.

### Sample Efficient Defect Detection
Built a full-stack implementation of real-time defect detection in manufacturing assemblies using various machine learning techniques and a robotic arm. Used Generative Adversarial Networks to augment a sparse dataset, then used a Convolutional Neural Network to classify images as either defective or non-defective and subsequent image processing and epipolar geometry to locate the defect in the world-frame. Implemented a new technique called synaptic metaplasticity so that networks trained on sequential tasks do not exhibit “catastrophic forgetting”. This method enables faster re-training during drift and reduces costs of retraining while preserving high performance. Trained a Franka robotic arm using Proximal Policy Optimization and Trust Region Policy Optimization to grasp and remove defective objects from assembly lines. Was able to achieve 84% system effectiveness with minimal data, and in real-time.