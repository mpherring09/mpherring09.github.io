---
name: Moonlight Grove
subtitle: Game - Academic - 2024
tools: [C#, Unity, AI, Immersive Environment, Audio Design]
image: /assets/img/Moonlight_Guy.png
description: Horror Game featuring advanced AI enemy and immersive environment.
---

<h1 class="text-center">Moonlight Grove</h1>
<h6 class="text-center text-muted">Game - Academic - 2024</h6>

<div class="text-center text-muted my-4" markdown="1">

  *You find yourself stranded in a forest after your car mysteriously breaks down. To fix it and escape, you must find five missing parts scattered throughout the woods and bring them back to your car. However, you aren't alone. A creepy man also wanders the woods, in search of five candles needed for some sort of ritual. Unfortunately for the you, the last step of that ritual requires a human sacrifice, and the you are the prime target. You must quickly gather your car parts while also thwarting the enemy's attempts to collect the candles.  Do both in time and you just might escape!*

</div>

<div class="text-center my-4" markdown="1">

  Moonlight Grove is a first person horror game in which the player must avoid and act against an AI enemy with its own plans and goals. It was created as a combined 3-week final project for both the Game Design 2 and Graphics Techniques courses at Ohio State. The game was created as partner project, although I was entirely responsible for programming all mechanics and shared responsibility for the game's design. 

</div>

{% include elements/video.html id="cNfgpKIUrnI" ratio="16/10" caption="<i class='fas fa-volume-up'></i> A few seconds captured from the start of the game. Please turn up your volume to experience the audio cues. <i class='fas fa-volume-up'></i>" %}

{% capture ai_desc %}
## AI Action Planning
The game's antagonist is controlled using a Goal Oriented Action Planning system:
- **Academic Origin:** The system is adapted from Dr. Jeff Orkin's "Three States and a Plan: The A.I. of F.E.A.R"
- **Autonomous Planning:** The AI agent autonomously computes a plan (list of actions) in order to achieve it's goal and then executes the plan with no need for direct control or state machines
- **Limited Perception:** The agent has a limited knowledge of the world. It has vision, and based on what it learns by moving around the scene it will update its plan
- **Scalability:** The system is designed to scale easily, with new actions automatically being incorporated into the agents toolkit
- **Optimized Search:** The system uses optimized pathfinding algorithms (A*) and simplification techniques like caching to improve the performance while searching over large graphs of possible plans
{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-5">
    {% include elements/video.html id="3r-S8Wwul0E" ratio="16/9" caption="Video report demonstrating Goal Oriented Action Planning." %}
  </div>

  <div class="col-md-7">
    <div>{{ ai_desc | markdownify }}</div>
  </div>
</div>

{% capture interaction_desc %}
## Interaction System
The game features several interactable objects, which are controlled by a custom-built interaction system:
- **Generalized Interface:** Proper abstraction allows for both the player and the AI agent to interface with the interaction system
- **Available Interactions:** Both entities can interact with, pick up, and place down objects throughout the scene
- **Event System:** A widespread event system notifies other game systems (SFX, Game State, AI Agent, etc.) when certain interactions have occurred
- **Scalability:** The system allows for easy inclusion of new interactables and pickups without the need for new scripting
- **Scene Management:** A core scene manager keeps track of all objects in the scene for use in pathfinding
{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-7">
    <div>{{ interaction_desc | markdownify }}</div>
  </div>

  <div class="col-md-5">
    <img src="{{"assets/img/Moonlight_Candle.gif" | relative_url}}" class="img-fluid rounded shadow">
    <figcaption class="text-center text-muted small">Pickups can be picked up and placed down with both the left and right hand.</figcaption>
  </div>
</div>

{% capture scene_desc %}
## Scene Design
The large scene was designed and created by my teammate and I:
- **Generated Terrain:** The scene makes use of the Unity terrain and trees system to create a large forest with rolling hills
- **Effects:** Particle and lighting effects are used to create fog and fire
- **Custom Assets:** The scene incorporates both external and custom assets
- **Immersive Audio:** 3D, binaural sound effects terrify the player with unsettling drones, heartbeats, rises, stabs, and moans, while also serving a mechanical purpose of conveying state changes to the player
- **Playtesting:** Several iterations of playtests were used to refine the dynamics and layout of the scene, spacing out puzzles and clues to keep the player's attention while also allowing downtime for horror and suspense
- **UI Design:** The menus in the game are stylized to match the horror aesthetic
{% endcapture %}

<div id="carouselExample" class="carousel slide col-md-9 mt-4 mb-1 mx-auto" data-ride="carousel" data-interval="5000" data-pause="hover">

  <div class="carousel-inner">
    <div class="carousel-item">
      <img src="{{"assets/img/Moonlight_Basement.png" | relative_url}}" class="d-block w-100">
    </div>
    <div class="carousel-item">
      <img src="{{"assets/img/Moonlight_Dock.png" | relative_url}}" class="d-block w-100">
    </div>
    <div class="carousel-item">
      <img src="{{"assets/img/Moonlight_Fog.png" | relative_url}}" class="d-block w-100">
    </div>
    <div class="carousel-item">
      <img src="{{"assets/img/Moonlight_House.png" | relative_url}}" class="d-block w-100">
    </div>
    <div class="carousel-item">
      <img src="{{"assets/img/Moonlight_Tower.png" | relative_url}}" class="d-block w-100">
    </div>
    <div class="carousel-item active">
      <img src="{{"assets/img/Moonlight_Title.png" | relative_url}}" class="d-block w-100">
    </div>
  </div>

  <a class="carousel-control-prev" href="#carouselExample" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon"></span>
  </a>

  <a class="carousel-control-next" href="#carouselExample" role="button" data-slide="next">
    <span class="carousel-control-next-icon"></span>
  </a>
</div>

<div class="row align-items-center mt-1 mb-4">
  <div class="col-md-12">
    <div>{{ scene_desc | markdownify }}</div>
  </div>
</div>