# Representation-of-a-Real-World-Problem-as-a-Markov-Decision-Process


## Aim

To represent a real-world warehouse delivery robot problem as a Markov Decision Process (MDP) by defining its states, actions, transition probabilities, reward function, and objective for optimal decision-making.

## Problem Statement
A warehouse robot is responsible for picking up packages from storage locations and delivering them to the correct loading area. The robot operates in a grid-based warehouse where it must avoid obstacles, navigate efficiently, and conserve battery power. At every step, the robot decides whether to move up, down, left, or right. It receives a positive reward for successfully delivering a package, a small negative reward for each movement (to encourage shorter paths), and a large negative reward if it collides with an obstacle. The robot continues making decisions until it successfully completes the delivery or its battery is exhausted.
### Problem Description

Write your answer here.

Describe the real-world application that you selected.


---

## MDP Components

A Markov Decision Process is represented as:

$$
MDP = (S, A, P, R, \gamma)
$$

Where:

| Symbol | Meaning |
|---|---|
| $S$ | Set of states |
| $A$ | Set of actions |
| $P$ | Transition probability function |
| $R$ | Reward function |
| $\gamma$ | Discount factor |

---

## State Space

Write your answer here.

The state space should list all possible situations in which the agent can exist.

Example format:

```text
S = {
    State 1,
    State 2,
    State 3,
    ...
}
```



---

## Sample State

Write your answer here.

A sample state is one specific example from the state space.



---

## Action Space

Write your answer here.

The action space should list all possible actions available to the agent.

Example format:

```text
A = {
    Action 1,
    Action 2,
    Action 3,
    ...
}
```


---

## Sample Action

Write your answer here.

A sample action is one action selected from the action space.



---

## Transition Probability

Write your answer here.

The transition probability explains how the environment moves from one state to another after an action is taken.

General form:

$$
P(s' \mid s,a)
$$

This means:

> Probability of reaching next state $s'$ after taking action $a$ in current state $s$.


---

## Reward Function

Write your answer here.

The reward function defines the feedback received by the agent after taking an action.

General form:

$$
R(s,a,s')
$$



---

## Graphical Representation

Write your answer here.

Draw the MDP graph.

The graph should include:

1. States as nodes.
2. Actions as arrows.
3. Rewards on transitions.
4. Transition probabilities if applicable.


---

## Python Representation

Write your code here.

Use Python dictionaries to represent the MDP.


```python
# MDP Representation using Python
# print("Name:       ")
# print("Register Number:     ")

```
---
## Output

Write your Python output here.


---

## Result

Write your result here.



---

