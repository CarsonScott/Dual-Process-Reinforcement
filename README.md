# Dual-Process Theory of Reinforcement Learning



## Overview

This paper describes an algorithm for an intelligent agent that adaptively changes its thought processes to maximize cumulative reward. It has two different "styles" of thought, which are both useful at achieving certain tasks. 

---

## Thought Processes

The system switches between two types of thought processes, called Automatic and Controlled processes, which are basically opposite of one another, in terms of their functions (i.e. the strenghts of one process make up for the weakenesses of the other). The interaction between them increases their net-strength while suppressing their net-weakness. 

This is due to the fact that if a process is doing well it is less likely to be replaced, and if its doing poorly it is more likely to be replaced. This causes a scheduling-like mechanism where the processes are more likely to be active in sitations where they perform well, and less likely to be active in situations where the do not.

---

## Automatic Process

The automatic process the default method of "thinking". It calculates the expected utility of each neighboring state in order to select actions that maximize the cumulative reward. The agent learns to apply this process through reinforcement, where the agent make incremental changes each time a reward is received, which ultimately improves the accuracy of beliefs, along with the agent’s ability to successfully use the automatic thought process.

---

## Controlled Process

If the automatic process fails, the agent switches secondary method, which is the controlled process. It calculates the distance between each neighboring state and the goal state, compares it to the current distance, and selects the action that best minimizes the distance. 

The constrolled process allows the agent to accumulate knowledge for the automatic process. This allows prepration of knowledge before the real appliacation. In other words, the agent uses the controlled process to "study" for the automatic process.

This period of preperation has the additional effect of improving efficiency of the agent. The controlled proccess has a large relative cost, Thus, decreasing the reliace on the secondary memthod is a form of optimization. In an ideal world, the automatic process is an air-tight, self-contained system that performs optimally in every situation all the time.

In a real, complex environment, the agent mostly uses the automatic process but occasionally swithces the the controlled process to deal with uncertainty. Too much uncertainty can hinder the performance of the automatic process, either because the agent lack the knowledge/experience, or because the oserved information contradicts the believed knowledge.

---

## Learning

The automatic method assigns fitness to each neighboring state, which equals the sum of utilities of their neighboring states, thus providing an expected potential utility for each possible path. This mechanism is reminiscent of Q-learning, an algorithm that discovers optimal paths through backward-chaining of rewards. However, this algorithm was designed with an emphasis on being robust, which is perhaps the weakest attribute of Q-Learning. 

States have weighted connections to neighboring states, such that each connection is associated with an action that leads to the neighboring state. Weights are adjusted when the agent selects an action and receives a reward in the new state.

![](https://github.com/CarsonScott/Dual-Process-Action-Selection/blob/master/img/Capture.PNG)
