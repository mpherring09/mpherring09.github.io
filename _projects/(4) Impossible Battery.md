---
name: Impossible Battery
subtitle: Training Simulator - BMW - 2024
tools: [C#, Unity, VR, Meta, Industrial]
image: /assets/img/ImpossibleBattery_Battery.png
description: Rhythm / Tower Defense genre mashup game.
---

<h1 class="text-center">Impossible Battery</h1>
<h6 class="text-center text-muted">Training Simulator - BMW - 2024</h6>

<div class="text-center my-4" markdown="1">

  Impossible Battery is a proof-of-concept VR simulator developed during my internship with the BMW IT Innovations team. Designed for the Meta Quest 3, it simulates repair processes for the BMW i7 electric car battery. I played a key role in shaping the project's direction and implementation.

</div>

<div class="text-center my-4" markdown="1">

  Please see [this article](https://www.meta.com/en-gb/blog/bmw-impossible-battery-vr-mixed-reality-training-automotive/) for public information about this project.

</div>

{% capture synopsis_desc %}
Impossible Battery addresses the challenges of training technicians to repair high-voltage batteries, tasks that are dangerous, complex, and expensive to teach in person. Built for the Meta Quest 3, it provides a low-risk. immersive environment where technicians can practice and refresh their skills remotely.

In this sandbox-style simulation, trainees can attempt most actions which are possible in real-life, even if they are incorrect. Key challenges include disassembling and reassembling the battery, diagnosing issues, identifying parts to replace, selecting tools, and performing tests.

Built with reusability in mind, the software can be easily adapted for other repair simulations. All task-specific logic is stored in a configurable YAML file, requiring no additional coding for new scenarios. Moreover, an accompanying Agent-based LLM system can convert existing training documents into compatible YAML configurations. Making a new training scenario is as simple as simple as acquiring the necessary 3D models and integrating them into the system.
{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-7">
    <div>{{ synopsis_desc | markdownify }}</div>
  </div>

  <div class="col-md-5">
    <img src="{{"assets/img/ImpossibleBattery_Quest.jpg" | relative_url}}" class="img-fluid rounded shadow">
  </div>
</div>

{% capture software_desc %}
## Interaction System & World State
I led design and development for the interaction and simulation systems.
- **Hand Tracking:** Using the Meta Quest 3's hand tracking, the simulation detects when players interact with objects
- **World State:** Each part of the battery is managed using a list of tags which track its state
- **Action System:** Viable actions are defined for each part through modular prerequisites and effects
- **Action Execution:** On interaction, the system checks for available actions, determines their effects, plays the corresponding animations, and updates the states of all parts involved
- **Configuration:** This system of actions and state changes is configurable with a single YAML file, enabling our internal client to add parts, tools, and actions without writing additional code
{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-5">
    <img src="{{"assets/img/ImpossibleBattery_Battery.png" | relative_url}}" class="img-fluid rounded shadow">
    <figcaption class="text-center text-muted small">The player can interact with objects by pinching them with their hand.</figcaption>
  </div>

  <div class="col-md-7">
    <div>{{ software_desc | markdownify }}</div>
  </div>
</div>

{% capture llm_desc %}
## LLM Generated Game Logic

To easily adapt the simulation to new scenarios, I developed a system of LLM agents which generate complete game logic from existing plain-text repair instructions.

- **Agent Graph:** Using LangGraph and GPT 4.0 from OpenAI, several agents collaborate to process instructions into a YAML file
- **Resulting File:** The YAML file specifies tools, parts, and actions, including prerequisites and effects for each action
- **Configuration:** The simulation reads this YAML file, links its contents to existing models, and configures the interaction system for the new scenario
{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-8">
    <div>{{ llm_desc | markdownify }}</div>
  </div>

  <div class="col-md-4">
    <img src="{{"assets/img/ImpossibleBattery_LangGraph.png" | relative_url}}" class="img-fluid rounded shadow">
    <figcaption class="text-center text-muted small">LangGraph web API showing the seven agents which comprise this system.</figcaption>
  </div>
</div>

{% capture research_desc %}
## Gamification Research
To inform the direction of the project, I conducted in-depth research on gamification opportunities in Impossible Battery.

- **Academic Research:** I reviewed several research papers exploring gamification theory and how various techniques affect performance and retention of trainees
- **Project Evaluation:** Based on these findings, I thoroughly analyzed our project and produced feature recommendations to enhance our simulation
- **Research Presentation:** I compiled these recommendations, along with a summary of the research, into a report which I presented to our team and stakeholders
{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-6">
    <img src="{{"assets/img/ImpossibleBattery_Research.png" | relative_url}}" class="img-fluid rounded shadow">
    <figcaption class="text-center text-muted small">Chart from my report showing suggested features and their impact as evaluated by my analysis.</figcaption>
  </div>

  <div class="col-md-6">
    <div>{{ research_desc | markdownify }}</div>
  </div>
</div>

{% capture management_desc %}
## Project Management
Using my expertise in Unity, I played a key role in guiding the project and the team.
- **Technical Lead:** Because the rest of the team had little experience with Unity, I had the opportunity to lead many technical aspects of the project as an intern
- **Architecture Design:** By the end of the internship, I was primarily responsible for the overarching architecture of the simulation
- **Documentation & Knoledge Transfer:** I documented this architecture extensively with comprehensive reports and diagrams, ensuring the team could continue the project after my internship
- **Agile Development:** I also helped direct team members on a daily basis, both in and outside of standup meetings, to ensure we met sprint goals and client requirements
{% endcapture %}

<div class="row align-items-center my-4">
  <div class="col-md-7">
    <div>{{ management_desc | markdownify }}</div>
  </div>
  
  <div class="col-md-5">
    <img src="{{"assets/img/ImpossibleBattery_Systems.png" | relative_url}}" class="img-fluid rounded shadow">
    <figcaption class="text-center text-muted small">An early concept architecture diagram showing the separate systems needed for the project.</figcaption>
  </div>
</div>