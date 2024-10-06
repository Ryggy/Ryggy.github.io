---
layout: post
title: Unreal Scene Composition
subtitle: The Sword in The Stone
tags: [Unreal, Lighting, Scene Composition, Design]
comments: true
author: Ryan Williamson
---
# Crafting the Perfect Scene: Lighting, Aesthetics, and Composition

![Final Scene Composition](https://www.youtube.com/watch?v=sBFK5eN76zE)

Creating a visually striking and immersive scene is an art that requires a deep understanding of lighting, composition, and aesthetic choices. In my latest project, I focused on the sword-in-the-stone legend, combining nature and myth to create a scene that draws the viewer’s eye while evoking a sense of mystery and magic.

In this blog post, I’ll break down my design process, the role of lighting, and how careful scene composition helped bring my concept to life. You can also watch the final product in [this YouTube clip](https://www.youtube.com/watch?v=sBFK5eN76zE).

## Concept and Design Process

The project started with the idea of creating a **fantasy forest** inspired by Arthurian legend. I wanted to feature **Excalibur in the stone** as the focal point, with the legendary **Lady of the Lake** watching over it. I envisioned the scene bathed in soft light rays, creating a dramatic atmosphere.

![Concept Board](https://ryggy.github.io/assets/img/conceptboard.png)

### Planning the Scene

I began by gathering references from different lighting setups. A key inspiration was **[Johan Grenier’s ArtStation scene](https://www.artstation.com/artwork/4X2Weq)**, which captures a powerful contrast of light and dark, with objects elegantly framed by god rays. After researching, I realized that I wanted to replicate the feeling of a **spotlight effect**, where rays of light draw attention to the central objects — the sword and the statue.

The environment was planned as a dense European forest, with mist and fog to create a **mystical atmosphere**. I used **Unreal Engine 5** to bring my vision to life, primarily for its robust lighting capabilities and access to high-quality assets via Quixel Megascans.

### Blockout and Terrain

To get a feel for the layout, I started with a basic blockout in Unreal Engine. This helped me plan the camera angles and overall composition. I also used Unreal’s **landscape tools** to shape the terrain, focusing on a lake at the center of the scene where the sword would reside.

![Scene Blockout](https://ryggy.github.io/assets/img/blockout.png)

For the terrain textures, I created a **blend material** to simulate different natural elements like water and grass. Using this, I painted darker areas near the lake and added grassy textures to sunlit slopes.

![Blueprint of Blend Material](https://ryggy.github.io/assets/img/blendmaterial.png)

![Blend Material On Terrain](https://ryggy.github.io/assets/img/blendmaterialterrain.png)

![Scene with Folliage](https://ryggy.github.io/assets/img/folliage.png)

## Lighting: The Key to Aesthetic

Lighting was perhaps the most critical aspect of my scene. I wanted it to do more than just illuminate the objects; I wanted it to tell a story. The scene relied heavily on **directional lighting**, **god rays**, and **vignettes** to focus the viewer’s attention.


### Post-Processing and Vignettes

To control the lighting further, I used a **post-process volume** that allowed me to adjust the overall mood of the scene. I aimed for a soft, overcast sky to diffuse the light across the environment. Additionally, I added a **vignette effect** to darken the edges, ensuring the viewer’s eye is drawn toward the sword in the center.

![Scene with Post Processing](https://ryggy.github.io/assets/img/lightingeffects.png)

By adjusting the **source angle** of my directional light, I softened the shadows, creating a more natural and atmospheric feel. The **volumetric height fog** added another layer of realism, with light scattering through the mist to enhance the magical aura of the scene. For this effect, I followed **[this YouTube tutorial on fog](https://youtu.be/e9atAxm1Cc0?si=xKvekvcX6LD7amY6)** to fine-tune the fog settings and achieve the look I wanted. 

To perfect the **god rays**, I referred to **[this tutorial on creating god rays](https://youtu.be/gOdTrIB5te0?si=30URE_tLOo5_MyF8)**, which helped me manage the interaction between light and the environment.

![God Ray](https://ryggy.github.io/assets/img/godray.png)

![God Ray Blueprint](https://ryggy.github.io/assets/img/godrayblueprint.png)

## Composition and Framing

A critical part of scene composition is ensuring that the viewer’s eye follows a clear path. To achieve this, I used a combination of the **rule of thirds** and the **golden section**. The sword is positioned at the intersection of these guides, ensuring it’s the focal point of the shot.

![Rule of Thirds Composition](https://ryggy.github.io/assets/img/ruleofthirds.png)

In the foreground, I added small details like hanging lights to make the scene feel more magical. These lights flicker softly, casting subtle reflections on the water and adding depth to the scene.

![Particle Effects](https://ryggy.github.io/assets/img/particleeffects.png)

## Blueprint System in Unreal Engine

Unreal Engine’s **Blueprint system** played a major role in this project. I used blueprints to control the scene's dynamic elements, including:
- **Lighting Adjustments**: I scripted the light rays to shift slightly over time, giving the effect of moving clouds or changing sunlight.
- **Fog Animation**: I used blueprints to adjust the intensity of the fog based on the camera’s distance, making the atmosphere more dynamic.
- **Cinematic Camera Movement**: By using keyframes in the blueprint system, I created smooth camera movements that transition between wide shots of the forest and close-ups of the sword.

The blueprint system allowed me to easily manage these dynamic elements without delving deep into the code, speeding up my workflow and allowing for real-time adjustments.

## Challenges and Solutions

One of the challenges I encountered was controlling the **god rays**. While the initial setup worked well, I noticed that the light rays weren’t blending smoothly with the fog. To solve this, I created a custom material for the fog using a **radial gradient** that faded in with distance. This helped diffuse the light around the statue and sword, making the rays feel more natural.

I also struggled with the file size of the project. High-resolution textures were significantly increasing the size, so I migrated my level to a clean project and removed unnecessary assets. This reduced the overall project size by 8GB.

## Final Touches and Cinematics

For the final render, I followed **[this tutorial on cinematic rendering](https://www.youtube.com/watch?v=YZ4gSKZh6do&feature=youtu.be)** to ensure the highest quality output for my video. I set up keyframes for camera movement, rotating the light beam as the camera zoomed in on the sword.

The final shot is framed to highlight the **statue and the sword**, with the light rays guiding the viewer's eye across the scene. I also added **ambient music** to enhance the atmosphere and match the magical theme of the scene.

## Conclusion

This project allowed me to delve deep into the aesthetics of scene composition and lighting. By focusing on how light interacts with objects and shapes the viewer’s perception, I was able to create a compelling and immersive environment. The final scene exceeded my expectations, and I look forward to applying these techniques to future projects.

For more details, you can check out the [final video here](https://www.youtube.com/watch?v=sBFK5eN76zE).

---

#### References:

- **Johan Grenier** (2021). *ArtStation Scene Inspiration*. [ArtStation](https://www.artstation.com/artwork/4X2Weq)
- **Flipped Normals Blog** (2023). *The Ultimate Guide to Lighting and Rendering for 3D Beginners*. [Flipped Normals Blog](https://blog.flippednormals.com/the-ultimate-guide-to-lighting-and-rendering-for-3d-beginners/)
- **YouTube Fog Tutorial** (2021). *Fog in Unreal Engine*. [YouTube](https://youtu.be/e9atAxm1Cc0?si=xKvekvcX6LD7amY6)
- **YouTube God Rays Tutorial** (2021). *Creating God Rays in Unreal Engine*. [YouTube](https://youtu.be/gOdTrIB5te0?si=30URE_tLOo5_MyF8)
- **YouTube Cinematic Rendering Tutorial** (2021). *Unreal Engine Cinematic Rendering*. [YouTube](https://www.youtube.com/watch?v=YZ4gSKZh6do&feature=youtu.be)