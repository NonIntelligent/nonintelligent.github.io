---
layout: page
title: Iris - Graphics Perception
description: A testing environment to determine the degree of which players can perceive changes in high-end graphics settings during gameplay
img: assets/img/Backdrop_sharp.jpg
importance: 2
category: Graphics
tags: Unreal-Engine Graphics Perception Ray-Tracing
---

## The project

This was built as part of my university dissertation to test if players can notice changes in graphics during gameplay. The users do not know the purpose of the test to avoid bias. The 4 variables that I controlled were shadows, texture quality, anti-aliasing, and reflections. Each of which were tested at the low, medium and high preset.

I decided to build this using an early access of Unreal Engine 5 as it allowed for easy building of high-fidelity environments and an asset library to speed up development. Their new Lumen technology was crucial for fast ray-tracing performance.

<div class = "container">
    <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/2.-Adjusting-density.jpg" title="Grassland" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/4.-Wheat-field.jpg" title="Wheat Field" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/5.-Forest.jpg" title="Forest" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/6.-Rock-Field.jpg" title="Rock Field" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/Backdrop_sharp_edited.jpg" title="Office" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
</div>

## Implementation

Using the Unreal Engine’s inbuilt graphics preset, I could dynamically adjust the visual quality of the scene. I placed invisible game objects that would change the graphics quality once the player enters it’s radius.

Adjusting the assets further with shadow resolutions, roughness, and high-quality textures to create a high-fidelity experience and make visual changes more noticeable.

## Challenges

A critical issue was the fact that changing graphics settings caused noticeable lag, which would give away the purpose of the test. I solved this by adjusting the LOD of assets, view culling and ray tracing depth.

## For the future

Creating PBR (Physically Based Rendering) textures could provide a more realistic and dynamic experience with the lighting changes and so better test against the human perception.
With more time I can optimise the assets and rendering method to provide a smoother experience for the testers.
I have learnt so much about development using Unreal Engine 5 as well as the new Lumen and Nanite technology presented.
