---
layout: page
title: Boids
subtitle: Flock Yeah! Emergent Behaviour!
---

#### Boids

<div style="position: relative; width: 960px; height: 600px;">
  <iframe src="https://ryggy.github.io/assets/BoidsWebGL/index.html" width="100%" height="100%" frameborder="0" style="position: absolute; top: 0; left: 0;" scrolling="no" allowfullscreen></iframe>
</div>

## Description

The boids algorithm demonstrates how simple rules lead to complex interactions. Experiment with the parameters to gain insight into flocking dynamics.


# Boids Algorithm Usage Guide

This guide explains the adjustable parameters in the boids algorithm, allowing you to customize the flock's behavior.

## Sliders and Their Functions

1. **Alignment**: Adjusts how boids align their direction with nearby boids. Higher values create smoother, synchronized movements.

2. **Cohesion**: Controls how boids stay close to their neighbors. Increasing this value results in tighter group formations.

3. **Separation**: Prevents boids from crowding too closely. Higher values lead to more dispersed flocks, reducing collisions.

4. **Avoid World Edge**: Ensures boids steer clear of the simulation boundaries. Stronger settings keep boids within the defined area.

5. **Stay in Radius**: Keeps boids within a specific radius from a center point. Increasing this value centralizes the flock's movements.

6. **Avoid Obstacles**: Allows boids to detect and steer clear of obstacles. Higher avoidance strength leads to more agile navigation.

