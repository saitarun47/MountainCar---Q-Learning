# MountainCar - QLearning Agent

> **This project implements a Q-learning agent to solve the MountainCar problem.**

## Overview

The Mountain Car MDP is a deterministic MDP that consists of a car placed stochastically at the bottom of a sinusoidal valley, with the only possible actions being the accelerations that can be applied to the car in either direction. The goal of the MDP is to strategically accelerate the car to reach the goal state on top of the right hill.


![mountain_car](https://github.com/user-attachments/assets/e2516b4d-2cb0-4b09-96f9-290c5eba1da8)

## Observation Space

The observation is a ndarray with shape (2,) where the elements correspond to the following:
| Num | Observation | Min | Max | Unit |
| :--- | :--- | :--- | :--- | :--- |
| 0 | position of the car along the x-axis | -1.2 | 0.6 | position (m) |
| 1 | velocity of the car | -0.07 | 0.07 | velocity (v) |


## Action Space

There are 3 discrete deterministic actions:  
- 0: Accelerate to the left
- 1: Don’t accelerate
- 2: Accelerate to the right

## Rewards

The goal is to reach the flag placed on top of the right hill as quickly as possible, as such the agent is penalised with a reward of -1 for each timestep.

## Start State

The position of the car is assigned a uniform random value in [-0.6 , -0.4]. The starting velocity of the car is always assigned to 0.

## Episode End

The episode ends if either of the following happens:

- 1.Termination: The position of the car is greater than or equal to 0.5 (the goal position on top of the right hill)

- 2.Truncation: The length of the episode is 200.

## Trained Agent


## Some Graphs

## Last few lines from the logs
