# Representation-of-a-Real-World-Problem-as-a-Markov-Decision-Process


## Aim

To represent a real-world warehouse delivery robot problem as a Markov Decision Process (MDP) by defining its states, actions, transition probabilities, reward function, and objective for optimal decision-making.

## Problem Statement
A warehouse robot is responsible for picking up packages from storage locations and delivering them to the correct loading area. The robot operates in a grid-based warehouse where it must avoid obstacles, navigate efficiently, and conserve battery power. At every step, the robot decides whether to move up, down, left, or right. It receives a positive reward for successfully delivering a package, a small negative reward for each movement (to encourage shorter paths), and a large negative reward if it collides with an obstacle. The robot continues making decisions until it successfully completes the delivery or its battery is exhausted.
### Problem Description

A warehouse delivery robot is tasked with transporting packages from storage locations to designated delivery points inside a warehouse. The robot operates in a grid-based environment containing obstacles such as shelves and walls. At each step, it must choose an action—move up, down, left, or right—to reach its destination while avoiding collisions and minimizing travel time. The robot receives a positive reward for successfully delivering a package, a small penalty for each movement to encourage shorter paths, and a large penalty for hitting obstacles or running out of battery. The objective is to determine the optimal sequence of actions that maximizes the total reward and enables safe, efficient package delivery.


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

The state space should list all possible situations in which the agent can exist.

```text
S = {
    S₁ = Robot at Start Position
S₂ = Robot Moving Up
S₃ = Robot Moving Down
S₄ = Robot Moving Left
S₅ = Robot Moving Right
S₆ = Robot Near Obstacle
S₇ = Robot Hits Obstacle
S₈ = Robot Carrying Package
S₉ = Robot at Delivery Location
S₁₀ = Package Successfully Delivered (Goal State)
S₁₁ = Battery Exhausted (Terminal State)
}
```



---

## Sample State

S₈ = Robot Carrying Package

This means the robot has successfully picked up the package and is navigating toward the delivery location.

---

## Action Space

The robot can perform the following actions:

```text
A = {
    Move Up
Move Down
Move Left
Move Right
}
```


---

## Sample Action

Move Right

The robot moves one cell to the right.

---

## Transition Probability

The transition probability specifies the probability of moving from one state to another after taking an action.

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

