---
layout: post
title: "Developing an LC Sinker Electrical Discharge Machine (WIP)"
header: false
---

<span class="tag">Circuit Design</span> ·
<span class="tag">CAD</span> ·
<span class="tag">Power System Design</span> ·
<span class="tag">C++</span> ·
<span class="tag">High Voltage Protection</span> ·
<span class="tag">Arduino</span> 
<span class="tag">LC Circuits</span> ·
<span class="tag">Control System</span> ·
<span class="tag">Mechanical System</span> ·


## Overview
I am currently in the process of developing a sinker Electrical Discharge Machine (EDM), which is a device that is able to shape metal parts using controlled electrical sparks. A sinker EDM pushes a conductive electrode into a metal piece in order to shape it.
The purpose of this personal project is to gain experience in building and developing a complex electro-mechanical system.

## Mechanical Design
With the mechanical design I aimed to design a simple single-axis movement mechanism, it's important for it to stay aligned along it's axis. The platform would be driven by a lead screw driven by a stepper motor. 
![EDM Mechanical](/blog/images/uni_projects/edm_machine/edm_mechanical.JPG)


## Electrical Design
For the electrical design I opted to go with an LC type spark generator, essentially it works similarly to a conventional boost converter by using an inductor and capacitor to increase the voltage to around 200V, enough to generate a spark between the electrodes.
The circuit also uses electrical isolation to separate the high and low voltage components. As well it controls a water pump, the stepper motor and an lcd screen for the user iterface. 
![EDM Schematic](/blog/images/uni_projects/edm_machine/schematic.JPG)

## Assembled Project

![EDM Electrical Demonstration](/blog/images/uni_projects/edm_machine/electrical_demonstration.JPG)
