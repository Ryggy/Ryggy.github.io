---
layout: post
title: Dino Sim - GOAP AI
subtitle: There's lots to learn!
gh-repo: JoshuaWMarshall/CreatureFeature
gh-badge: [star, fork, follow]
tags: [dino sim, GOAP, AI]
comments: true
mathjax: true
author: Ryan Williamson
---

# Building a Flexible Dinosaur AI in Unity


![Procedural Generation Demo](https://ryggy.github.io/assets/img/goapai.gif)

Creating dynamic and responsive AI in games is critical for immersion, especially when simulating behaviors like hunting, grazing, or fleeing in an open-world setting. In this blog post, I’ll walk through the process of developing a **dinosaur AI system** in Unity, focusing on the integration of **Goal-Oriented Action Planning (GOAP)** with a high-level **state manager**. I'll also cover how this hybrid approach enables obstacle avoidance and pathfinding for more realistic behavior.

## References
Throughout the development of the AI system, several resources influenced the structure and approach:

1. **Chaudhari, V. (2017). Goal Oriented Action Planning.** [Medium Article](https://medium.com)
2. **De Byl, P. (2022). GOAP: Goal-Oriented Action Planning.** [Holistic 3D Video](https://youtu.be)
3. **Unity AI Tutorials. (2020). AI for Unity Developers.** [Unity Learn](https://learn.unity.com)

These references helped shape the foundation of the AI system, from decision-making models to pathfinding integration.

## Planning the System
The initial goal was to develop an AI system that could handle both **low-level decision-making** and **high-level state management**. By combining GOAP for detailed action planning with a state machine for broader decisions, we achieved an AI that adapts dynamically to its environment while maintaining efficiency.

### Key Components of the AI System

1. **Goal-Oriented Action Planning (GOAP)**:
   - **Dynamic Adaptability**: GOAP allows each dinosaur to evaluate its current state (e.g., hunger, safety) and dynamically plan a sequence of actions to achieve specific goals, such as finding food or evading predators.
   - **Modularity**: The GOAP framework is flexible, allowing us to easily add new actions and goals as we introduce different dinosaur species or gameplay mechanics.

2. **High-Level State Manager**:
   - **State Management**: The state manager controls the overarching behavior of the dinosaur (e.g., idle, searching for food, fleeing) and ensures smooth transitions between different goals and actions.
   - **Coordination**: It coordinates between different actions, ensuring the dinosaur acts in a way that aligns with its broader objectives.

### Obstacle Avoidance and Pathfinding
The hybrid AI system integrates **pathfinding** and **obstacle avoidance** to ensure dinosaurs navigate their environment smoothly. By using Unity's **NavMesh system**, the dinosaurs can avoid obstacles and reach their destinations efficiently.

- **Pathfinding**: The A* algorithm helps the AI find the optimal path to a target, considering obstacles and terrain features.
- **Obstacle Avoidance**: As dinosaurs navigate through their world, they adapt their paths to avoid obstacles like rocks, trees, or other dinosaurs.

## Steps to Build the System

### 1. GOAP Setup

The GOAP framework requires defining **actions** and **goals**. Each action has **preconditions** (what must be true before the action is valid) and **effects** (the outcome of the action). The system then generates a plan to achieve the highest-priority goal.

#### Example:
- **Action**: Find Food
  - **Precondition**: Hunger > 50%
  - **Effect**: Hunger < 10%

This modularity allows us to easily expand the system as needed.

### 2. State Manager Integration

The state manager oversees the transitions between the dinosaur’s goals. It ensures the dinosaur switches between states (e.g., from grazing to fleeing) smoothly, depending on external stimuli like the presence of a predator.

#### Example:
- **State**: Searching for Food
  - If a predator is detected, the dinosaur transitions to a **Fleeing** state.
  
### 3. Obstacle Avoidance and Pathfinding

By integrating Unity’s **NavMesh** for pathfinding, the dinosaurs can navigate the environment while avoiding obstacles. The GOAP system works in tandem with the pathfinding, ensuring that the dinosaur plans its actions in a way that accounts for obstacles on its route.

- **Dynamic Path Updates**: If an obstacle appears mid-path, the dinosaur recalculates the optimal route using A*.
- **Edge Avoidance**: The pathfinding system also helps prevent the AI from walking off cliffs or into water.

### 4. Performance Optimization

GOAP can be computationally expensive if too many actions or goals are involved. To mitigate this, we employed several optimization techniques:
- **Action Caching**: Frequently used action results are cached to avoid unnecessary recalculations.
- **A* Algorithm**: Efficient pathfinding helps reduce the computational load during complex navigational tasks.

## In-Game UI Integration

Additionally, an **in-game UI** was developed to display the dinosaur’s current state and goal. This feature is particularly useful for debugging and ensures that players can understand why dinosaurs behave the way they do.

## Conclusion

This hybrid approach to AI development in Unity—combining GOAP with high-level state management—allows for dynamic, realistic dinosaur behaviors. Whether it’s a Velociraptor hunting prey or a Stegosaurus fleeing from danger, the AI responds to its environment in a way that feels natural and engaging.

By structuring the system in this modular, expandable way, we’ve set the foundation for future AI improvements and additional gameplay features.

---

#### References:
1. **Chaudhari, V.** (2017). *Goal Oriented Action Planning*. Medium.
2. **De Byl, P.** (2022). *GOAP: Goal-Oriented Action Planning*. Holistic 3D.
3. **Unity AI Tutorials** (2020). *AI for Unity Developers*. Unity Learn.
