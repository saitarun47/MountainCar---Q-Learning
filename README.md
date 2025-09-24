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


https://github.com/user-attachments/assets/e43f8aed-4194-467c-9a19-3e76870ea8d1


## Scores per episode

<img width="1807" height="376" alt="image" src="https://github.com/user-attachments/assets/0dd2beb5-be79-4f91-b158-9c24516d01a2" />


## Last few lines from the logs

```
Episode: 20000, Score:  -156, Avg.Score: -129.05, Epsilon: 0.010, Time: 00:03:07
Episode: 21000, Score:  -168, Avg.Score: -160.15, Epsilon: 0.010, Time: 00:03:16
Episode: 22000, Score:  -142, Avg.Score: -142.00, Epsilon: 0.010, Time: 00:03:24
Episode: 23000, Score:  -132, Avg.Score: -143.52, Epsilon: 0.010, Time: 00:03:31
Episode: 24000, Score:  -132, Avg.Score: -140.20, Epsilon: 0.010, Time: 00:03:39
Episode: 25000, Score:  -200, Avg.Score: -145.36, Epsilon: 0.010, Time: 00:03:47
Episode: 26000, Score:  -166, Avg.Score: -161.04, Epsilon: 0.010, Time: 00:03:55
Episode: 27000, Score:  -141, Avg.Score: -139.03, Epsilon: 0.010, Time: 00:04:04
Episode: 28000, Score:  -139, Avg.Score: -134.10, Epsilon: 0.010, Time: 00:04:12
Episode: 29000, Score:  -200, Avg.Score: -153.55, Epsilon: 0.010, Time: 00:04:20
Episode: 30000, Score:  -139, Avg.Score: -140.18, Epsilon: 0.010, Time: 00:04:28
Episode: 31000, Score:  -107, Avg.Score: -126.63, Epsilon: 0.010, Time: 00:04:36

Environment solved in 31062 episodes!	Average Score: -109.78
```
