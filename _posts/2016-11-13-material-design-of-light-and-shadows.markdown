---
layout: post
comments: true
title:  "Takeaways from Google's Material Design"
date:   2016-11-13 00:26:00 +0800
categories: CS3216, Design
---

Hi. It has been a while since I had blogged on CS3216 and this time round I wish to write about my takeaways after reading through [Google's Material Design Principles](https://material.google.com/). Having utilised the [Material UI Library](http://www.material-ui.com/#/) for React in Assignment 3 and my Final Project, the need to understand the underlying principles of Material Design had been more or less abstracted away and I am guilty of not reading up the documentation before working on my projects ><. (Side note: this is not a comprehensive summary of Google's Material UI and only aims to jot down key points which I think is important.)

**Material Thickness**  
Did you know that the thickness of all materials has to be 1dp? Hence, things appear like paper (or planes) and that is also why nobody remembers seeing any 3D objects (like spheres, cubes, cone) in Google's Material Design. The main differentiating factor between the components would be the play of lighting and shadows to show the difference of elevation of the objects.  

**Light and Shadow**  
There are 2 kinds of lighting in the Material UI environment --key lights that create directional shadows and ambient light that creates soft shadows from all angles.

<!-- | <img src="https://material-design.storage.googleapis.com/publish/material_v_9/0B6Okdz75tqQsSFZUZ01GTk13T28/whatismaterial_environment_shadow1.png" width="200"> | | <img src="https://material-design.storage.googleapis.com/publish/material_v_9/0B6Okdz75tqQsdDhaaTMwMTFVLTA/whatismaterial_environment_shadow2.png" width="200"> | |<img src="https://material-design.storage.googleapis.com/publish/material_v_9/0B6Okdz75tqQsNnVmbTNMUF9DR0U/whatismaterial_environment_shadow3.png" width="200"> |
|:---:|:---:|:---:|:---:|:---:|
| *Shadow cast by key light* | | *Shadow cast by ambient light* | | *Combined shadow from key and ambient lights* | -->

<img src="https://material-design.storage.googleapis.com/publish/material_v_9/0B6Okdz75tqQsSFZUZ01GTk13T28/whatismaterial_environment_shadow1.png" width="500">  
*Shadow cast by key light*

<img src="https://material-design.storage.googleapis.com/publish/material_v_9/0B6Okdz75tqQsdDhaaTMwMTFVLTA/whatismaterial_environment_shadow2.png" width="500">  
*Shadow cast by ambient light*

<img src="https://material-design.storage.googleapis.com/publish/material_v_9/0B6Okdz75tqQsNnVmbTNMUF9DR0U/whatismaterial_environment_shadow3.png" width="500">  
*Combined shadow from key and ambient lights*  
(Pictures taken from official Google's Material Design Documents)

Shadows are an essential part of Material Design and deciding how the shadow should appear on a component can be difficult without knowledge of the Material Design principles. On retrospection, I realized my mistake when designing the shadow effect for my module timetable planner for Assignment 3. For a hover animation, a module card is expected to elevate from its resting position and cast shadows to planes under it. However, my failure to realize that ambient light is involved in the Material Design environment led me to only implement a key light shadow effect.

![Missing ambient light](/images/progwebapp/missing-ambient-light.png)  
*Missing ambient light for floating module card.*

**Gravity-influenced Movement**  

This is something new to me. I have never noticed that animations moves along an arc to simulate the influence of gravity on the object. For example, objects moving upwards has decreasing acceleration as it moves along the arc to show that rising against gravity requires effort, while objects moving downwards has increasing acceleration to simulate gravity pulling the object down.

<img src="https://material-design.storage.googleapis.com/publish/material_v_9/0BybB4JO78tNpWnRtS1RnaVk3Sjg/02-movement.png" width="500">  
*Movement along an Arc*

That's the keypoints for this post! The official documentation for Material Design has been an enlightening read on how material objects respond to user interactions and it is interesting to see design incorporate real-world elements (light, gravity, 3-dimensional space) to make objects and movements feel natural to the user.