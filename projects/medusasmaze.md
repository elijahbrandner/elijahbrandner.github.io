---
layout: project
type: project
image: img/medusa/medusas_maze_card.png
title: "Medusa’s Maze — VR Survival Game (Unity XR)"
date: 2025-12-14
published: true
labels:
  - Unity
  - VR
  - XR Interaction Toolkit
  - Game Development
  - AI Systems
summary: "VR survival maze game inspired by Percy Jackson mythology where players explore a dark labyrinth, collect magical pearls, and evade Medusa using spatial awareness, movement strategy, and immersive XR systems."
---
**Medusa’s Maze** is a VR survival game prototype inspired by *Percy Jackson & The Olympians: The Lightning Thief*. Players take on the role of Percy Jackson and must navigate a fog-filled labyrinth while being actively hunted by Medusa. The experience emphasizes tension, spatial awareness, and immersive VR interaction rather than traditional combat mechanics.

The project was developed in Unity using the **XR Interaction Toolkit** and designed specifically for standalone VR hardware such as the Meta Quest. The game focuses on a tight, replayable gameplay loop that balances exploration, risk, and performance constraints inherent to VR systems.

---

## Core Gameplay Loop
1. Explore Medusa’s maze  
2. Collect Poseidon’s pearls to increase score  
3. Avoid Medusa’s pursuit  
4. Survive as long as possible  
5. Restart upon defeat  

This loop creates constant pressure, encouraging careful navigation and situational awareness.

---

## Gameplay Systems

### Pearl Collection & Scoring
- Pearls spawn randomly within predefined collider regions  
- Ground raycasts ensure valid placement  
- Collision checks prevent spawning inside walls  
- Maximum of **3 active pearls** at a time for performance stability  
- Pearls respawn immediately after collection  
- Score increments dynamically and resets upon defeat  

This design enables endless replayability within a single environment.

---

### Enemy AI (Medusa)
- Uses AI pathfinding to patrol and pursue the player  
- Moves faster than the player to maintain urgency  
- Collision-based attacks reduce player health  
- Player defeat triggers level reset and score reset  

Medusa’s behavior transforms the maze from a puzzle space into a predatory environment where movement decisions matter.

---

## UI & XR Interaction Design

### Player UI
- **Health Bar:** Slider-based UI that visually communicates damage without numeric clutter  
- **Pearl Counter:** TextMeshPro UI displaying real-time score  
- UI elements are anchored to the XR camera for consistent visibility  

### Controls (Meta Quest)
- **Left Joystick:** Movement (relative to headset direction)  
- **Right Joystick:** Smooth turning / snap rotation  
- **A Button:** Jump (grounded only)  
- **Right Grip:** Pick up pearls within interaction range  

All interactions are validated to prevent false triggers.

---

## Audio & Immersion
- Timed footstep audio with pitch variation  
- Jump and landing sounds validated by grounded state  
- Environmental ambience (rain, thunder) to reinforce tension  
- Spatialized pearl pickup sound for feedback  

Audio is routed through centralized playback systems to prevent overlap and maintain performance.

---

## Technical Architecture

| System Component | Responsibility |
|-----------------|---------------|
| Pearl Manager | Spawning, tracking, score updates |
| Player Health | Health tracking and defeat state |
| Medusa AI | Navigation, pursuit, and attack logic |
| UI Manager | Health bar and score updates |
| Audio Manager | Action and environmental sounds |

Systems are modular and coordinated through a closed gameplay loop:
**Explore → Collect → Update UI → Avoid → Defeat → Reset**

---

## My Role & Contributions
This was a **team-based final integration project**. My contributions included:
- Implementing core gameplay systems and system coordination  
- Designing and implementing the pearl collection and respawn system  
- Integrating XR-optimized UI elements  
- Supporting locomotion and interaction logic  
- Assisting with performance optimization and modular system design  
- Contributing to overall gameplay balance and final integration  

---

## Public Showcase & Outreach
The completed VR experience was **demoed live to middle school students** as part of an educational outreach initiative. Players interacted directly with the game using VR headsets, providing real-time feedback on usability, engagement, and immersion.

The project and demonstration were featured in a published article that specifically mentions our team members by name:

- **Article:**  
  [Their Olympian Task: To Design VR Video Games Based on Junior High Curriculum](https://news.gcu.edu/gcu-news/their-olympian-task-to-design-vr-video-games-based-on-junior-high-curriculum/)

This experience provided valuable insight into designing interactive systems for younger audiences and non-technical users.

---

## Key Takeaways
- Gained experience developing **performance-conscious VR systems**  
- Learned to coordinate AI, UI, audio, and XR interaction systems  
- Strengthened understanding of VR UX and accessibility considerations  
- Practiced modular system architecture within Unity  
- Developed intuition for tension-based and immersive gameplay design  

---

## Future Adaptations
- Multi-level progression and expanded environments  
- Additional mythological enemies and encounters  
- Narrative-driven progression tied to pearl collection  
- Expanded AI behaviors and boss mechanics  

---

## Demo & Links
- **Gameplay Demo:** https://go.screenpal.com/watch/cTl6iGnY28C  
- **GitHub Repository:** https://github.com/ayojawshmp3/CST-320-Project-Percy-Jackson-and-The-Lightning-Thief  
