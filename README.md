# ContinousControl
## My solution for Udacity course "Deep Reinforced Learning"

This is a solution for Project 2 in Udacity course "Deep Reinforced Learning". It is using materials from course, particulary it is based on DDPG solution from course:
https://github.com/udacity/deep-reinforcement-learning/tree/master/ddpg-pendulum

### The Environment

This project is for  [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment.

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

### Solving the Environment

I have selected option 1 (from two avaliable) to solve:

Option 1: Solve the First Version
The task is episodic, and in order to solve the environment, your agent must get an average score of +30 over 100 consecutive episodes.


### Getting Started

This solution is designed and tested in Workspace evrinoment provided by Udacity. You need to 
