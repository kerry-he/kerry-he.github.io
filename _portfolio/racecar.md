---
title: "Optimal Control for Autonomous Racecar"
excerpt: "Trajectory optimization and model predictive control for a Formula Student autonomous racecar<br/><img src='/images/500x300.png'>"
collection: portfolio
---

Formula Student Driverless is a university engineering design competition which started in 2017 and is ran by [Formula Student](https://www.formulastudent.de/fsg/). The competition tasks student teams with designing, building, and programming a Formula-style race car which can autonomously navigate through known and unknown tracks as quickly as possible. Points are awarded for each mission based on the times taken to complete them, with time penalties if the car exits the track boundaries.

In autonomous driving, the motion planning subsystem is required to determine a feasible state and control trajectory to navigate the vehicle to perform a specific task. This project implements a model predictive controller (MPC) to perform motion planning for [Monash Motorsport](https://www.monashmotorsport.com/)’s autonomous racecar to compete in the Formula Student Driverless competition. Multiple modelling and discretisation methods were explored to determine the best performing MPC formulation. An extensive comparison of each formulation was conducted by prototyping each MPC in MATLAB, and performing simulated experiments in a simplified environment. The best performing MPC was then translated into C++ and validated in a full real time hardware-in-the-loop simulation.

Overall, a linear time-varying RHP formulation utilising a dynamic bicycle model is proposed, where the vehicle dynamics and path constraints are linearised at each time step, allowing the RHP to be formulated and solved as a quadratic program. An optimal racing line is precomputed offline by solving for a periodic time-optimal trajectory along the entire track, which the RHP then tracks in real time. Through simulated experiments, the proposed RHP is shown to be robust to noise, time delay and modelling error, and successfully outperforms Monash Motorsport’s previous motion planning and control implementations. The RHP is demonstrated to safely achieve speeds of up to 25 m/s while running in real time at 50 Hz.

[Thesis](/files/bachelor_thesis.pdf){: .btn--research}
[Paper](/files/bachelor_thesis_paper.pdf){: .btn--research}
