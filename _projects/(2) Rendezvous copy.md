---
name: Rendezvous
subtitle: Exhibit - COSI - 2024
tools: [C#, Unity, Exhibit, Publicly Deployed]
image: /assets/img/Rendezvous_Physics.png
description: Educational game / simulation about orbital mechanics.
---

<h1 class="text-center">Rendezvous</h1>
<h6 class="text-center text-muted">Exhibit - COSI - 2024</h6>

<div class="text-center my-4" markdown="1">

  Rendezvous is an educational game where players manipulate a rocket's orbit to intercept a satellite. I developed this game during an internship at COSI, a science museum in Columbus, OH. I designed and produced the project from start to finish with help from the scientists and designers at COSI. It is currently installed on the mezzanine level of the museum where it is enjoyed by thousands of guests every week.

</div>

{% include elements/video.html id="3vUDgsJ6RZo" %}

{% capture physics_desc %}
## Physics Simulation

The core gameplay is driven by a physically accurate orbital simulator.
- **Real-Time Simulation:** Thrust and gravity are calculated each frame and applied using Unity's physics system
- **Trajectory Previews:** Object trajectories are calculated using Verlet integration, providing players with constant feedback of how their actions influence their path
- **Realism:** Times, distances, forces, and weights are accurately calculated to model an authentic Hohmann transfer scenario
- **Scalability:** Time and distance scales can be adjusted to speed up or slow down the simulation and to keep coordinates within precision range
- **Autopilot:** The rocket can autonomously execute an optimal transfer (calculated for this scenario). This is displayed on the home screen of the game and is used for testing
{% endcapture %}

{% include elements/side-image.html 
    side="left" 
    image="/assets/img/Rendezvous_Physics.gif" 
    text=physics_desc 
%}

{% capture ui_desc %}
## Dynamic UI
The UI displays comprehensive game information in real-world values.

- **HUD:** The HUD dynamically displays information about the rockets travel, adjusted according to the simulation's scaling parameters
- **Contextual Popups:** Popups smoothly fade in and out to show relevant information only when needed
- **Macro View:** A detailed "map" view of the orbits is displayed on the right screen, giving players a high-level visualization of the scenario
{% endcapture %}

{% include elements/side-image.html 
    side="right" 
    image="/assets/img/Rendezvous_UI.gif" 
    text=ui_desc 
%}

{% capture ui_desc %}
## Design & Effects
I worked closely with the exhibits team to refine the visual and gameplay design.

- **Crisp Aesthetic:** A clean, minimalistic design ensures that players can easily digest the information presented
- **Accessible Gameplay:** The game is designed to be intuitive for first-time players, including children, while preserving physical accuracy
- **Custom Assets:** I created most of the game's 2D and 3D assets, with select effects sourced from external resources
{% endcapture %}

{% include elements/side-image.html 
    side="left" 
    image="/assets/img/Rendezvous_Model.png" 
    text=ui_desc 
%}