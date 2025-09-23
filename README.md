# MountainCar - QLearning Agent

> **This project implements a Q-learning agent to solve the MountainCar problem.**

## Overview

The Mountain Car MDP is a deterministic MDP that consists of a car placed stochastically at the bottom of a sinusoidal valley, with the only possible actions being the accelerations that can be applied to the car in either direction. The goal of the MDP is to strategically accelerate the car to reach the goal state on top of the right hill.


![mountain_car](https://github.com/user-attachments/assets/e2516b4d-2cb0-4b09-96f9-290c5eba1da8)

## Observation Space

The observation is a ndarray with shape (2,) where the elements correspond to the following:



## Action Space

There are 3 discrete deterministic actions:  
- 0: Accelerate to the left
- 1: Don’t accelerate
- 2: Accelerate to the right
