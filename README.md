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

| Current State    | Action     | Next State       | Probability |
| ---------------- | ---------- | ---------------- | ----------- |
| Start            | Move Right | Carrying Package | 0.9         |
| Start            | Move Right | Hit Obstacle     | 0.1         |
| Carrying Package | Move Up    | Delivery Point   | 0.95        |
| Carrying Package | Move Left  | Obstacle         | 0.05        |

Meaning:

90% chance the robot successfully moves.
10% chance it collides with an obstacle.
Probabilities may vary depending on the environment.

---

## Reward Function

The reward function provides feedback after each action.

General form:

$$
R(s,a,s')
$$

Reward Table:
| Situation               | Reward |
| ----------------------- | ------ |
| Successful Delivery     | +100   |
| Every Movement          | -1     |
| Collision with Obstacle | -20    |
| Battery Exhausted       | -50    |

Example:

Move Successfully → -1
Hit Obstacle → -20
Deliver Package → +100
Battery Exhausted → -50


---

## Graphical Representation



## Python Representation


```python
# MDP Representation using Python

print("Name:SANIYA G")
print("Register Number:212223240147")

states = [
    "Start",
    "Move Up",
    "Move Down",
    "Move Left",
    "Move Right",
    "Near Obstacle",
    "Hit Obstacle",
    "Carrying Package",
    "Delivery Point",
    "Goal",
    "Battery Exhausted"
]

actions = [
    "Up",
    "Down",
    "Left",
    "Right"
]

transition_probability = {
    ("Start", "Right"): {
        "Carrying Package": 0.9,
        "Hit Obstacle": 0.1
    },

    ("Carrying Package", "Up"): {
        "Delivery Point": 0.95,
        "Hit Obstacle": 0.05
    }
}

reward = {
    "Move": -1,
    "Hit Obstacle": -20,
    "Delivery": 100,
    "Battery Exhausted": -50
}

discount_factor = 0.9

print("\nStates")
print(states)

print("\nActions")
print(actions)

print("\nTransition Probability")
for key, value in transition_probability.items():
    print(key, "->", value)

print("\nReward Function")
for key, value in reward.items():
    print(key, ":", value)

print("\nDiscount Factor =", discount_factor)
```
---
## Output

<img width="988" height="372" alt="image" src="https://github.com/user-attachments/assets/ba525ae5-4b69-4423-800e-2808221fa1bd" />

---

## Result

Thus, the warehouse delivery robot problem was successfully represented as a Markov Decision Process (MDP) by defining its state space, action space, transition probability function, reward function, discount factor, graphical representation, and Python implementation. This MDP model enables the robot to learn an optimal policy that maximizes cumulative rewards while ensuring safe and efficient package delivery.

---

