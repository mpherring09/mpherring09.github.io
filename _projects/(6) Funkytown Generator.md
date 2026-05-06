---
name: Funkytown Generator
subtitle: Graphics Demonstration - Academic - 2024
tools: [C#, Unity, Graphics, PCG, CGI, Grad-Level]
image: /assets/img/Funkytown_Bendy_0_Pretty.png
description: Demonstration of devised method for procedurally generated cities with realtime non-linear spacial warping.
---

<h1 class="text-center">Funkyown Generator</h1>
<h6 class="text-center text-muted">Graphics Demonstration - Academic - 2024</h6>

<div class="text-center my-4" markdown="1">

  Funkytown is a graphics demonstration built in Unity, which procedurally generates a 3D city with buildings and roads and animates them in realtime using non-linear spatial warping techniques. I developed and implemented the multi-step process used to achieve this result and presented it during a graduate level Procedural Content Generation (PCG) seminar at Ohio State. An abbreviated version of that presentation is shown below.

</div>

<div class="col-md-10 mx-auto my-5" markdown="1">

  {% include elements/sourced_video.html src="assets/img/Funkytown_Final_0.mp4" poster="assets/img/Funkytown_Bendy_0.png" top=true %}

</div>

<div class="text-center my-5" markdown="1">

  <h2><strong>Part 1: Generating Ordinary Cities</strong></h2>
  A city with no curves can be generated with a simple four step process.

</div>

<div class="my-5" markdown="1">

  <h3><strong>Step 1: Divide a Space</strong></h3>
  Divide a quad by slicing it several times in order to form a binary space division. This step is highly configurable and often involves randomization, allowing the user to fine-tune their output. The result below excludes triangles and weights sides by their length when choosing where to cut.

</div>

<img src="{{"assets/img/Funkytown_Portfolio_0.png" | relative_url}}" class="img-fluid rounded shadow">

<div class="my-5" markdown="1">

  <h3><strong>Step 2: Create Insets</strong></h3>
  Inset every polygon in the division. Since these polygons are always convex, the algorithm requires only simple point-line tests to clip unwanted sections. All spatial data in this project is stored in custom data structures which can be easily and efficiently enumerated over.

</div>

<img src="{{"assets/img/Funkytown_Portfolio_1.png" | relative_url}}" class="img-fluid rounded shadow">

<div class="my-5" markdown="1">

  <h3><strong>Step 3: Generate Meshess</strong></h3>
  Calculate Vertices, Indices, and UV's in order to instantiate Unity Mesh objects. Non-quad faces were originally generated using triangle fans. The height of the meshes is configurable. In this instance, it is set to be inversely proportional to the area of the building's footprint.

</div>

<div class="row">
  <div class="col-md-8 mx-auto">
    <img src="{{"assets/img/Funkytown_Portfolio_2.png" | relative_url}}"
         class="img-fluid rounded shadow">
  </div>
</div>

<div class="my-5" markdown="1">

  <h3><strong>Step 4: Apply Texutres</strong></h3>
  Apply representative textures to the meshes and line renderers to demonstrate the visual effect.

</div>

{% include elements/image-match.html 
   image1="/assets/img/Funkytown_Pretty_Flat.png" 
   image2="/assets/img/Funkytown_Pretty_Flat_Sky.png" 
   height = 250%}

<div class="text-center my-5" markdown="1">

  <h2><strong>Part 2: Distortion Effect</strong></h2>
  Making a few modifications to this process creates a warped space effect in the city.

</div>

<div class="my-5" markdown="1">

  <h3><strong>Step 1: Subdividing Edges</strong></h3>
  Enumerate over all edges, subdividing them to a configurable resolution. This subdivision takes place after generating insets but before generating meshes.

</div>

<div class="row">
  <div class="col-md-8 mx-auto">
    <img src="{{"assets/img/Funkytown_Portfolio_3.png" | relative_url}}"
         class="img-fluid rounded shadow">
  </div>
</div>

<div class="my-5" markdown="1">

  <h3><strong>Step 2: Apply Vector Field Offsets</strong></h3>
  Shift all vertices in the scene according to a configurable vector field. This example uses a Sin wave on both the x and z axes. Since the rooftops can now be concave, the Earcut Algorithm was used as opposed to triangle fans when generating meshes.

</div>

<div class="d-flex flex-wrap align-items-center justify-content-center col-md-10 my-4 mx-auto">

  <div class="p-2" style="flex: 1 1 300px;">
    <img src="{{"assets/img/Funkytown_Bendy_0.png" | relative_url}}"
         class="img-fluid rounded shadow">
  </div>

  <div class="p-2" style="flex: 1 1 300px;">
    <img src="{{"assets/img/Funkytown_Bendy_0_Pretty.png" | relative_url}}"
         class="img-fluid rounded shadow">
  </div>

</div>

<div class="text-center my-5" markdown="1">

  <h2><strong>Part 3: Animation</strong></h2>
  Since the system can enumerate over and modify all vertices in the scene, the entire scene can be procedurally animated in real time.

</div>

<div class="my-5" markdown="1">

  <h3><strong>Step 1: Automate Warp Parameters</strong></h3>
  Adding a time parameter to the vector field used in the warping allows for procedural animation. Different configurations produce diverse results.

</div>

<div class="d-flex flex-wrap align-items-center justify-content-center col-md-12 my-4 mx-auto">

  <div class="p-2" style="flex: 1 1 300px;">
    {% include elements/sourced_video.html src="assets/img/Funkytown_Flow_0.mp4" %}
  </div>

  <div class="p-2" style="flex: 1 1 300px;">
    {% include elements/sourced_video.html src="assets/img/Funkytown_Flow_2.mp4" %}
  </div>

  <div class="p-2" style="flex: 1 1 300px;">
    {% include elements/sourced_video.html src="assets/img/Funkytown_Flow_1.mp4" %}
  </div>

</div>

<div class="my-5" markdown="1">

  <h3><strong>Step 2: Adjust UV's</strong></h3>
  The user can configure the system to either use the warped vertices or the original vertices when generating UV's. Since the warping transformation is non-linear, neither of these options produces a result free of visual artifacts. To do so would require subdividing faces in addition to edges, an opportunity for future development. The unwarped UV's are shown above the version with the warped UV's for comparison.

</div>

<div class="row align-items-center my-4">
  <div class="col-md-6">
    {% include elements/sourced_video.html src="assets/img/Funkytown_Flow_0.mp4" %}
  </div>
  <div class="col-md-6">
    {% include elements/sourced_video.html src="assets/img/Funkytown_Flow_0_Pretty.mp4" %}
  </div>
</div>

<div class="row align-items-center my-4">
  <div class="col-md-6">
    {% include elements/sourced_video.html src="assets/img/Funkytown_Flow_0_UV.mp4" %}
  </div>
  <div class="col-md-6">
    {% include elements/sourced_video.html src="assets/img/Funkytown_Flow_0_UV_Pretty.mp4" %}
  </div>
</div>

<div class="text-center my-5" markdown="1">

  <h2><strong>Final Result</strong></h2>
  This system successfully produces an animated, warping city. This technique could be utilized effectively in movies or games in urban fantasy settings to dramatize spatial magic. Similar methods could also visualize waves, earthquakes, or other effects which require 3D non-linear transformation of surfaces.

</div>

<div class="row align-items-center mt-2 mb-4">
  <div class="col-md-6">
    {% include elements/sourced_video.html src="assets/img/Funkytown_Final_0.mp4" top=true%}
  </div>
  <div class="col-md-6">
    {% include elements/sourced_video.html src="assets/img/Funkytown_Final_1.mp4" %}
  </div>
</div>