# Dual-Process Theory of Reinforcement Learning

## Overview
This paper describes an algorithm for an intelligent agent that adaptively changes its thought processes to maximize cumulative reward. 

There are two methods of thought- automatic and controlled- where exactly one is active at any given time. Each process contains a utility function, which assigns expected rewards to possible actions in order to select an action. 

The automatic and controlled processes cooperate in order to achieve a common goal- Maximize cumulative reward. Each process has specific strengths and weaknesses, where the strong aspects of one process tend to make up for the weak aspects of the other.

---

## Automatic Process
The automatic process, or the default method of thinking, calculates the expected utility of each neighboring state in order to select actions that maximize cumulative reward. The agent learns to apply this process through reinforcement, where the agent makes incremental changes to the beliefs to better fit the observed rewards.

## Controlled Process
If the automatic process fails, the agent switches to the controlled process which calculates the distance from the goal state to each neighboring state, and selects actions according to the current distance. Simply put, the agent uses hill climbing to select actions when it experiences high uncertainty.

The controlled process allows the agent to accumulate knowledge for the automatic process. This allows preparation of knowledge before the real application. In other words, the agent uses the controlled process to "study" for the automatic process.

This period of preparation has the additional effect of improving efficiency of the agent. The controlled process has a large relative cost, Thus, decreasing the reliance on the secondary method is a form of optimization. In an ideal world, the automatic process is an air-tight, self-contained system that performs optimally in every situation all the time.

In real-world applications, exclusive application of the automatic process is a naïve idea, as it lacks the adequate skills required to navigate complex environments. In contrast the controlled process is a self-reliant system by nature, in that it makes decisions according to a built-in utility function as opposed to reinforcement from an external source.

--

## Learning

The automatic method assigns fitness to each neighboring state, which equals the sum of utilities of their neighboring states, thus providing an expected potential utility for each possible path. This mechanism is reminiscent of Q-learning, an algorithm that discovers optimal paths through backward-chaining of rewards. However, this algorithm was designed with an emphasis on being robust, which is perhaps the weakest attribute of Q-Learning.

States have weighted connections to neighboring states, such that each connection is associated with an action that leads to the neighboring state. Weights are adjusted when the agent selects an action and receives a reward in the new state.

![](https://github.com/CarsonScott/Dual-Process-Action-Selection/blob/master/img/Capture.PNG)
