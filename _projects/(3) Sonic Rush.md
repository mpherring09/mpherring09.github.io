---
name: Sonic Rush
subtitle: Game - Personal - 2023
tools: [C#, Unity, Design, Music]
image: /assets/img/SonicRush_Models.png
description: Rhythm / Tower Defense genre mashup game.
---

<h1 class="text-center">Sonic Rush</h1>
<h6 class="text-center text-muted">Game - Personal - 2023</h6>

<div class="text-center my-4" markdown="1">

  Shown below is gameplay from a demo I built on my own in Unity. I created every asset in the project except for those listed explicitly on this page. This project was completed as a personal endeavor outside of any classes.  

</div>

{% include elements/video.html id="CuUiEQtUjsQ" ratio="16/9" autoplay=true caption="<i class='fas fa-volume-up'></i> Video demonstration of the game. <i class='fas fa-volume-up'></i>" %}

{% capture design_desc %}
## Game Design
The game is designed as a mashup of the rhythm and tower defense genres.

- **Procedural Enemies:** Players face an onslaught of UFO's advancing along a trail. If the UFO's reach the end, players lose hearts.
- **Game Loop:** Players spend coins on towers which destroy UFO's, in turn earning more coins
- Tower Strategy: Four tower varieties each with four upgrades offer distinct strategic advantages and disadvantages
- **Rhythm Component:** Towers only attack to the beat of the music. To make the towers attack, the player must "record" music by playing a rhythm minigame. Every time the player hits a note, the tower corresponding to that note will attack
- **Upgrades:** Upgrading towers enhances range and damage, while upgrading the music itself increases the number of notes and thus the rate of fire (if the player can keep up)
- **Adjustable Difficulty:** Three difficulties allow anyone to play. To win the normal difficulty, the player must be strategic with their purchases and skilled at the rhythm minigame
{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-5">
    {% include elements/video.html id="j0sBXQQvjxA" ratio="1"%}
  </div>

  <div class="col-md-7">
    <div>{{ design_desc | markdownify }}</div>
  </div>
</div>

{% capture software_desc %}
## Software Design
My design enables new levels to be made without the need for any code.

- **Scripts:** 35 scripts in C#
- **Systems:** 6 larger core systems (in dark blue)
- **BeatManager:** Fully standalone component which adds rhythm game functionality to Unity, usable from the editor
- **Third Party Effects:** Incorporation of modified third party script: [DigitalRuby's Lighting Bolt Effect](https://assetstore.unity.com/packages/tools/particles-effects/lightning-bolt-effect-for-unity-59471)
{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-4">
    <div>{{ software_desc | markdownify }}</div>
  </div>
  
  <div class="col-md-8">
    <img src="{{"assets/img/SonicRush_Class.png" | relative_url}}" class="img-fluid rounded shadow">
  </div>
</div>

{% capture software_desc %}
## Asset Creation
I created or modified most of the assets in the game using a variety of software.

- **Custom Models:** 16 tower models created in Blender (some animated)
- **Modular Music:** Modular background track consisting of 17 individual tracks made in Ableton Live using Native Instruments VST's
- **External Models:**  12 UFO varieties and several floor tiles modified from Kenny's Tower Defense Kit
- **2D Graphics:**  UI images and other graphics created in Adobe Illustrator
{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-5">
    <img src="{{"assets/img/SonicRush_Models.png" | relative_url}}" class="img-fluid rounded shadow">
  </div>

  <div class="col-md-7">
    <div>{{ software_desc | markdownify }}</div>
  </div>
</div>