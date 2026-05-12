---
name: Zelda Remake
subtitle: Game - Academic - 2023
tools: [HLSL, MonoGame, Shaders]
image: /assets/img/Zelda_Cover.png
description: Reverse engineered implementation of The Legend of Zelda (NES) with added pallette shaders.
---

<h1 class="text-center">Zelda Remake</h1>
<h6 class="text-center text-muted">Game - Academic - 2023</h6>

<div class="text-center my-4" markdown="1">

  During my **Interactive Systems** and **Design Patterns** course, I worked with a **software development team** of six students. Following the principles of **Agile development**, we fully reproduced the first and second dungeons from the The Legend of Zelda (NES) in the **MonoGame** engine (built on .NET). The video below shows some gameplay from the first dungeon.

</div>

{% include elements/video.html id="f9bVLm7McuE" ratio="16/10" caption="In this project, I took responsibility for architecting and implementing core systems since MonoGame is a relatively low level engine." %}

{% capture collisions_desc %}

## Collisions
I create a collision detection system which could be used in any game.

- **Collision Testing:** The collision manager tests collisions each frame using axis-aligned bounding boxes and sends relevant event messages to collided objects
- **Utilities:** Additional tools support snapping colliders to edges and calculating the direction of collisions
- **Debugging:** Collision boxes can be drawn to the screen to help with debugging

{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-6">
    <div>{{ collisions_desc | markdownify }}</div>
  </div>

  <div class="col-md-6">
    {% include elements/video.html id="xxvZzHOpHJQ" ratio="16/9" caption="Video demonstrating the collision system with hitboxes drawn." %}
  </div>
</div>

{% capture drawing_desc %}

## Sprite Drawing
Similarly, I created a generalized graphics system which could to draw complex sprites in any game.

- **Modular Animations:** Modular sprite system enables layered special effects such as flashing, blinking, and tinting
- **Initialization:** A sprite factory handles asset loading and can create all needed sprites in the game
- **Dynamic Cameras:** Camera system which supports multiple reactive, moving cameras

{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-6">
    {% include elements/video.html id="1kmisVymR5s" ratio="16/9" caption="Video demonstrating the sprite drawing system with animated sprites." %}
  </div>

  <div class="col-md-6">
    <div>{{ drawing_desc | markdownify }}</div>
  </div>
</div>

{% capture shaders_desc %}

## Adjustable Shaders
I later expanded the sprite drawing system to allow for multiple drawing systems which can be swapped at runtime.

- **Shader-Based System:** One such drawing system can apply various HLSL shaders to the sprites
- **Palette Shader:** A custom HLSL shader samples generic color data from sprites and returns adjusted colors based on a provided palette
- **PCG Palettes:** Several unique palettes are generated both explicitly and procedurally for use with this shader

{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-6">
    <div>{{ shaders_desc | markdownify }}</div>
  </div>

  <div class="col-md-6">
    {% include elements/video.html id="RAwo7GuXP7c" ratio="16/9" caption="Video demonstrating the sprite drawing system with animated sprites." %}
  </div>
</div>