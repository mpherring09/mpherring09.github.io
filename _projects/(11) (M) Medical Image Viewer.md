---
name: X-Ray Viewer
subtitle: Exhibit - Fort Worth Museum of Science and History - 2025
tools: [Unity, Exhibit, Touch Gestures]
image: /assets/img/MedicalViewer_Steel.png
description: Touchscreen exhibit where guests can compare X-Ray images.
---

<h1 class="text-center">X-Ray Viewer</h1>
<h6 class="text-center text-muted">Exhibit - Fort Worth Museum of Science and History - 2025</h6>

<div class="text-center my-4" markdown="1">

  **X-Ray Viewer** is an interactive where kids can investigate and compare real medical images using touch gestures as if they were professionals in a hospital setting.

  This interactive can be found in the [TCU Children's Gallery](https://roto.com/projects/tcu-childrens-gallery){:target="_blank"} at the [Fort Worth Museum of Science and History](https://www.fwmuseum.org/){:target="_blank"}. I was solely responsible for the implementation of this project during my internship at **Roto**, translating styleframes into a museum-ready interactive.

</div>

<div class="row">
  <div class="col-md-10 my-2 mx-auto">
    <img src="{{'/assets/img/MedicalViewer_Steel.png' | relative_url }}" 
     class="rounded shadow" 
     alt="Medical X-Ray Viewer"
     style="width: 100%;">
  </div>
</div>

<div class="row">
  <div class="col-md-10 my-4 mx-auto">
    <div markdown="1" style="margin-bottom: -1rem;">

## Project Contributions:
I was the main developer of this project, so I was responsible for turning static design documents into a fully usable interactive exhibit. The key features of the project are listed below:

<br>
**UI:**
- Implementation of team-designed UI for use on large touchscreen monitors
- Simple animations and state change indicators

**Touch Gestures:**
- Integration of a pre-existing multitouch package, enabling two finger pinch gesture for zoom and pan
- Custom extensions to this package in order to improve pinch gesture accuracy and to enforce boundaries on the images, keeping them in frame

**Production Readiness:**
- Content management allowing images and captions to be changed easily by designers and installers
- Time-based state reset to ensure a consistent entry experience

</div>
</div>
</div>

<div class="col-md-12 my-2 mx-auto">
  {% include elements/image-match.html 
    image1="/assets/img/MedicalViewer_ZoomedOut.png" 
    cap1="Fully zoomed out images."
    image2="/assets/img/MedicalViewer_ZoomedIn.png" 
    cap2="Images zoomed in using touch gestures."
    height = 200 
    capWidth = 300 %}
</div>
