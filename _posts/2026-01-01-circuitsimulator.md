---
layout: post
title: "Power Flow Solver"
header: false
---

<span class="tag">Power Flow Simulator</span> ·
<span class="tag">Power Systems</span> ·
<span class="tag">Newton-Raphson Solver</span> ·
<span class="tag">Rust</span> ·
<span class="tag">Steady State Analysis</span> ·
<span class="tag">Programming</span>

*Power Flow Simulator · Steady State Analysis · Newton-Raphson · Power Systems · Rust · Numerical Methods · Programming*

#### Overview

I developed an AC Newton–Raphson power-flow solver in Rust to analyse electrical power networks. The simulator calculates bus voltage magnitudes and phase angles, power flows, and network losses under different operating conditions.

The project was an opportunity to deepen my understanding of power-system analysis and numerical methods by implementing the solver from first principles rather than relying on existing power-system simulation software.

![Basic Window Demonstration](/blog/images/uni_projects/rust_power_flow/basic_window.JPG)


#### Why?

Power-flow analysis is fundamental to understanding how electrical networks behave under different generation and loading conditions. While studying power systems, I wanted to build a simulator that would allow me to explore these concepts computationally and gain a deeper understanding of what happens inside a power-flow solver.

Rather than using an existing library to perform the calculations, I implemented the Newton–Raphson power-flow algorithm from first principles. This required developing the underlying mathematical models for the network and understanding how the different components of a power system interact.

#### How?

The simulator represents an electrical network using an admittance matrix (Y-bus) and solves the nonlinear power-flow equations using the Newton–Raphson method.

At each iteration, the solver:

Calculates the power produced or consumed at each bus.
Determines the mismatch between the calculated and specified power.
Constructs the Newton–Raphson Jacobian matrix.
Solves for corrections to the bus voltage magnitudes and phase angles.
Updates the system state and repeats until the power mismatches converge within a specified tolerance.

The solver supports different bus types, including Slack, PV, and PQ buses, as well as transformers, shunt elements, and networks operating across multiple voltage levels.

The project was implemented in Rust, using nalgebra for numerical linear algebra and egui to provide an interactive interface for constructing and analysing power systems.

![Code Base](/blog/images/uni_projects/rust_power_flow/code_base.JPG)


#### Features
- AC Newton–Raphson power-flow analysis
- Slack, PV and PQ buses
- Generators and loads
- Transformers
- Shunt elements
- Per-unit (p.u.) system support
- Multiple voltage levels
- Bus voltage magnitude and phase-angle calculations
- Power-flow calculations
- Network loss calculations
- Interactive graphical interface
- Built using Rust, nalgebra and egui
![Component Demonstration](/blog/images/uni_projects/rust_power_flow/component_demonstration.JPG)


#### Key Takeaways

This project strengthened my understanding of both power-system analysis and numerical methods. Implementing the Newton–Raphson algorithm from scratch required me to work through the mathematical formulation of the power-flow equations, Jacobian matrix, bus types, and network modelling rather than treating the solver as a black box.

It also gave me experience applying Rust and numerical linear-algebra tools to a problem involving a relatively complex mathematical model.

![Complex Project](/blog/images/uni_projects/rust_power_flow/complex_window.JPG)






