# Dual-Process Theory of Reinforcement Learning

* * *

### Overview

The following paper describes an AI system that adaptively switches how it thinks, reasons, and acts in order to maximize cumulative reward. 



### Thought Processes

The system switches between two different processing types, called Automatic and Controlled processing, which are functional opposites (The weaknesses of one is likely a strength in the other, and vice-versa). If one process is struggling in a given situation, the other process takes over. The interactions between them effectively increase their net strengths and suppress their net weaknesses. 

* * *

### Automatic Process

The default method of action selection calculates the expected utility of each neighboring state in order to select actions that maximize the cumulative reward. The agent learns to apply this method through reinforcement, such that the agent is driven to make incremental changes over time, which ultimately improves the accuracy of beliefs, along with the agent’s ability to select actions effectively.
 
 This method of action selection is efficient in both speed and use of resources, but it is only effective once the agent has collected an adequate amount of knowledge, which takes time. 



### Controlled Process

If the default method fails, the agent switches to controlled action selection. This secondary method calculates the distance between each neighboring state and the goal state, compares it to the current distance, and selects the action that best minimizes the distance. 

Not only is the controlled method effective in dealing with uncertainty, but it also provides an opportunity for the agent to enhance its performance using the automatic method, thereby decreasing the need for manual selection, which relatively slow and inefficient relative to the automatic method.

* * *

### Learning

The automatic method assigns fitness to each neighboring state, which equals the sum of utilities of their neighboring states, thus providing an expected potential utility for each possible path. This mechanism is reminiscent of Q-learning, an algorithm that discovers optimal paths through backward-chaining of rewards. However, this algorithm was designed with an emphasis on being robust, which is perhaps the weakest attribute of Q-Learning. 

States have weighted connections to neighboring states, such that each connection is associated with an action that leads to the neighboring state. Weights are adjusted when the agent selects an action and receives a reward in the new state.

![](https://github.com/CarsonScott/Dual-Process-Action-Selection/blob/master/img/Capture.PNG)
