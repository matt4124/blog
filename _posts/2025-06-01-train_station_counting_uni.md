---
layout: post
title: "Train Station Counting"
header: false
---

*Python · Machine Learning · Computer Vision · CNNs · CSRNet · Crowd Counting*

## Overview

As part of the ENG30002 Engineering Technology Sustainability Project in Semester 1, 2025, our group investigated ways to improve the efficiency and sustainability of Melbourne's metropolitan train network.

The broader objective was to encourage greater use of public transport by improving the efficiency of the network and reducing reliance on private vehicles. We proposed a system that could dynamically optimise train schedules and carriage allocations based on predicted passenger demand at individual train stations.

## The Problem

Train passenger demand varies significantly throughout the day and across different stations. Fixed timetables and carriage allocations may therefore result in trains that are overcrowded in some situations while operating with excess capacity in others.

Our proposed solution was a data-driven workflow that would:

Collect passenger numbers from individual train platforms.
Use historical and real-time data to predict future passenger demand.
Optimise train schedules based on predicted demand.
Adjust the number of carriages allocated to different services.

This approach aimed to improve the efficiency of the network while providing a better experience for passengers.

## My Role

I was responsible for developing the passenger counting component of the proposed system.

The objective was to estimate the number of people present on each train platform and provide this information as an input to the demand prediction system.

I investigated several potential approaches, including:

Pressure sensors installed on platforms
Infrared sensors
Wi-Fi-based device detection
Camera-based computer vision

I ultimately selected a camera-based computer vision approach, using an AI model to estimate the number of people visible in a platform image or video.

This approach offered the potential for high accuracy while also making use of existing security camera infrastructure at train stations.

## Developing the People Counting System

I initially investigated developing a custom convolutional neural network (CNN) using publicly available people-counting datasets.

However, the initial model experienced difficulties generalising to new images and handling different image dimensions. The performance was also affected by differences between the training datasets and the target environment of train station platforms.

I therefore investigated alternative approaches and implemented CSRNet, a deep-learning architecture designed specifically for crowd counting.

Using pretrained weights and further training on relevant datasets, I investigated how the model could be adapted to better generalise to crowded train station environments.

The resulting system was demonstrated using live footage from a public camera in Rome, Italy, providing an example of how the proposed passenger-counting component could operate on real-world video footage.

## System Workflow

The proposed system connected passenger counting with the broader train network optimisation workflow.

Platform Cameras → Passenger Counting → Demand Prediction → Train Scheduling → Carriage Allocation

The passenger-counting system provided the initial data required to predict future passenger demand. This information could then be used to inform decisions about train frequency and the number of carriages required on different routes.

![Project Plan](/blog/images/uni_projects/sustainability_project_plan.png)

## Key Takeaways

This project provided experience in applying machine learning and computer vision to a real-world sustainability problem.

A key part of the project was adapting the technical approach when the initial CNN model did not perform as expected. Investigating CSRNet and pretrained models provided an opportunity to explore how specialised machine-learning architectures could better address the challenges of crowd counting.

The project demonstrated how computer vision, predictive modelling, and transport data could potentially be combined to improve public transport efficiency and support more sustainable urban transportation.

![Project Explanation](/blog/images/uni_projects/sustainability_project_explanation.JPG)

![Project Demonstration](/blog/images/uni_projects/sustainability_project_demonstration.gif)

