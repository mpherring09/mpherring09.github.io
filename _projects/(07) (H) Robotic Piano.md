---
name: Robotic Piano
subtitle: Exhibit - Prototype - 2025
tools: [Unity, Exhibit, Robotics]
image: /assets/img/Piano_Cover.jpg
description: Interactive exhibit where guests can make beats play on a giant robot.
---

<h1 class="text-center">Robotic Piano</h1>
<h6 class="text-center text-muted">Exhibit - Prototype - 2025</h6>

<div class="text-center my-4" markdown="1">

  **Robotic Piano** is an interactive where guests can make a drum beat using a touchscreen interface. A real piano, outfitted with robotic drum sticks, will "play" the guest's beat by striking the piano in every location but the keys.

  This exhibit is currently on display at [Prototype: The Experimental Museum](https://www.prototype.org/){:target="_blank"}. I collaborated on this project during my internship at **Roto**, focusing on **hardening** and **integration** to prepare the exhibit for installation.

</div>

<div class="row">
  <div class="col-md-10 my-2 mx-auto">
    <img src="{{'/assets/img/Piano_Cover.jpg' | relative_url }}" 
     class="rounded shadow" 
     alt="Robotic Piano"
     style="width: 100%;">
  </div>
</div>

<div class="row">
  <div class="col-md-10 my-4 mx-auto">
    <div markdown="1" style="margin-bottom: -1rem;">

## Project Contributions:
I took over this project near the end of development, after it was already feature-complete. Thus, my work focused on preparing the exhibit for installation and integrating it with external systems. The highlights of my work on this project are listed here:

<br>
**Hardware Integration:**
- Collaborated with Engineering team to design an MQTT communication scheme which ensures synchronization and rhythmic accuracy between the robot and the interface
- Implementation of this MQTT communication scheme on the interface side

**Installation Features:**
- Versioning system allowing the museum to toggle the exhibit between two versions in a single build: one which uses the robot piano, and another which outputs to speakers. Both versions are on display currently.
- Production configuration allowing tuning variables to be changed easily on site

**Hardening:**
- Optimizations and cleanup of codebase, ensuring robustness against long runtime cycles and unusual touch inputs typical of high-traffic museum environments
- Polishing, final bug sweeping, and participant testing to ensure production-readiness

</div>
</div>
</div>

{% include elements/video.html id="orY2d7F-JzI" ratio="16/9" caption="Demonstration of the interface in the speaker output version." %}
