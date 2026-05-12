---
name: Cosmic Projections
subtitle: Graphics Demonstration - Academic - 2024
tools: [JavaScript, GLSL, WebGL, Shaders, Grad-Level]
image: /assets/img/Projections_Scene.png
description: Low level interactive WebGL scene featuring custom shaders.
---

<h1 class="text-center">Cosmic Projections</h1>
<h6 class="text-center text-muted">Graphics Demonstration - Academic - 2024</h6>

<div class="text-center my-4" markdown="1">

  Cosmic Projections is an interactive animated scene created entirely with HTML, JavaScript, and GLSL, using only WebGL and glMatrix libraries. Every aspect of the rendering process — from processing vertices to calculating lighting — was coded manually. While the resulting scene is simple, it was a significant undertaking spanning several systems and thousands of lines of code.

</div>

<div class="my-4 col-md-8 mx-auto" markdown="1">

{% include elements/video.html id="jvik4pxl_wU" ratio="1" autoplay=true caption="The user can manually control the camera and objects in the scene, but if they do not, this pre-programmed animation will play." %}

</div>


{% capture modelling_desc %}
## Scene Modelling
To generate the data needed to represent the scene, I created a custom Scene Graph system.

- **Mesh Generation:** Vertices for primitives (cube, sphere, cylinder, plane) are discretized at runtime from corresponding parametric models, while complex models (e.g., trees) are imported from files.
- **Normal Generation:** Normals are procedurally generated based on the average normals of each vertex's adjacent faces.
- **Scene Graph:** Each object's transformations and materials are stored in a custom recursive tree structure.
{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-5">
    <img src="{{"assets/img/Projections_Modelling.png" | relative_url}}" class="img-fluid rounded shadow">
    <figcaption class="text-center text-muted small">An earlier version which shows the cylinder, cube, and sphere, generated parametrically.</figcaption>
  </div>

  <div class="col-md-7">
    <div>{{ modelling_desc | markdownify }}</div>
  </div>
</div>

{% capture transformation_desc %}
## Projection / Transformation
All matrices required to transform vertices into NDC space are calculated and passed to the shaders.

- **Camera:** The camera is defined as an object in the scene, with its own position and rotation, defining the eye space.
- **Transformations:** Model, view, and perspective projection transformations are computed using the data from each object and the camera.
- **Scene Hierarchy:** All transformations are calculated recursively by traversing the scene graph, supporting hierarchical, articulated models.
- **NDC Calculation:** The vertex shader receives these matrices and calculates the NDC coordinates and transformed normals for each vertex.
{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-7">
    <div>{{ transformation_desc | markdownify }}</div>
  </div>
  
  <div class="col-md-5">
    <img src="{{"assets/img/Projections_Transformation.png" | relative_url}}" class="img-fluid rounded shadow">
    <figcaption class="text-center text-muted small">Interesting camera angle demonstrating foreshortening.</figcaption>
  </div>
</div>

{% capture shading_desc %}
## Shading
I wrote complete vertex and fragment shaders specifically for this application.

- **Lighting:** Ambient, Diffuse, and Specular lighting are calculated for each pixel in the fragment shader (Phong shading), based on provided lighting and material information.
- **Texture Mapping:** The shaders support texture mapping, used for the trees and skybox
- **Reflection Mapping:** The shaders support reflection mapping (to the skybox), demonstrated by mirror-like metallic objects in the scene
{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-5">
    <img src="{{"assets/img/Projections_Shading.gif" | relative_url}}" class="img-fluid rounded shadow">
    <figcaption class="text-center text-muted small">Moving the light showcases diffuse and specular highlights.</figcaption>
  </div>

  <div class="col-md-7">
    <div>{{ shading_desc | markdownify }}</div>
  </div>
</div>

{% capture animation_desc %}
## Interactivity / Animation
The scene is responsive to user input, allowing the user to move the objects within it.

- **User Interaction:** The camera, telescope, and light source can all be controlled by the user with six degrees of freedom.
- **Idle Animation:** If the user does not manipulate the scene, a pre-made animation plays automatically.
- **Frame Update:** Based on the user's inputs or the idle animation, each object's position and rotation are updated each animation frame, and the entire scene is re-drawn.
{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-7">
    <div>{{ animation_desc | markdownify }}</div>
  </div>
  
  <div class="col-md-5">
    <img src="{{"assets/img/Projections_Animation.gif" | relative_url}}" class="img-fluid rounded shadow">
    <figcaption class="text-center text-muted small">The telescope can be moved and rotated around each axis.</figcaption>
  </div>
</div>