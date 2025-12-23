---
layout: project
type: project
image: /img/estunohub/estuno_prototype.png
title: "Estuno Hub — Offline Adaptive Learning Platform (Capstone Project)"
date: 2025-11-02
published: true
labels:
  - Capstone Project
  - Embedded Systems
  - Full-Stack
  - Accessibility
  - AI Systems
summary: "Capstone project designing an offline, privacy-preserving educational support platform for neurodivergent students. Estuno Hub integrates custom hardware, a local full-stack web system, and adaptive learning features to support focus, accessibility, and individualized pacing without internet access."
---
**Estuno Hub** is an offline, AI-assisted educational support system designed to improve focus, engagement, and individualized learning for neurodivergent students. The platform operates as a **fully self-contained device**, hosting both teacher and student dashboards on a local Raspberry Pi–generated Wi-Fi network with **no internet connectivity**, ensuring complete data privacy.

The system enables teachers to upload learning materials locally, which are transformed into adaptive study tools and visual supports for students. Teachers receive engagement insights and progress analytics, while students interact with a distraction-reduced, sensory-friendly interface tailored to accessibility needs such as ADHD and ASD.

At the time of writing, the project is approximately **35% complete**, with hardware finalized and ordered, core architecture validated, and UI wireframes completed. The project is now transitioning from design into full implementation.

---

## Project Goals
- Provide a **low-cost, offline learning platform** for classrooms without reliable internet access  
- Improve focus and engagement for neurodivergent learners through accessibility-first design  
- Support adaptive learning and individualized pacing using AI-assisted analytics  
- Maintain **strict local-only data storage** for privacy and ethical compliance  
- Deliver real-time teacher insights without intrusive monitoring  

---

## System Architecture
Estuno Hub follows a **locally hosted, three-tier architecture**:
<img src="/img/estunohub/SystemArchitectureDesign.drawio.png"
     alt="Estuno Hub System Architecture"
     style="max-width: 75%; height: auto; display: block; margin: 0 auto 1.5rem auto;">

### Hardware Platform
- **Raspberry Pi 5** acting as the central processor and Wi-Fi access point  
- **NVMe SSD via PCIe HAT** for high-speed local storage and low-latency access  
- Active cooling and enclosed hardware for stable classroom operation
<img src="/img/estunohub/EstunoHubHardwarePrototype.png"
     alt="Estuno Hub Hardware Prototype"
     style="max-width: 75%; height: auto; display: block; margin: 0 auto 1.5rem auto;">

### Software Stack
- **Frontend:** React / Next.js with Bootstrap for accessible, responsive dashboards  
- **Backend:** Python Flask server managing authentication, content, and analytics  
- **Database:** SQLite stored locally on NVMe SSD  
- **Networking:** Private offline Wi-Fi network using hostapd and dnsmasq  

All components operate entirely within the local network, with no external API calls or cloud dependencies.
<img src="/img/estunohub/estuno_wireframe_teacher.png"
     alt="Teacher Dashboard Wireframe"
     style="max-width: 75%; height: auto; display: block; margin: 0 auto 1.5rem auto;">

---

## User Experience & Accessibility
The platform provides **separate dashboards** for teachers and students:

### Teacher Dashboard
- Upload lesson materials and assignments  
- View long-term engagement trends and progress summaries  
- Monitor performance patterns without real-time surveillance
<img src="/img/estunohub/TeacherWireframe.png"
     alt="Teacher Dashboard Wireframe"
     style="max-width: 75%; height: auto; display: block; margin: 0 auto 1.5rem auto;">

### Student Dashboard
- Access adaptive learning content and visual supports  
- Use timers, icons, AAC/PECS tools, and simplified navigation  
- Interact with a sensory-friendly interface designed to reduce cognitive overload  

Accessibility decisions were guided by psychology consultants and aligned with ISO 9241 and WCAG-informed principles.
<img src="/img/estunohub/StudentWireframe.png"
     alt="Student Dashboard Wireframe"
     style="max-width: 75%; height: auto; display: block; margin: 0 auto 1.5rem auto;">

---

## My Role & Responsibilities
I serve as a **Software Engineer** on the Estuno Hub team, with responsibilities spanning architecture, frontend, backend planning, and privacy design.

Key contributions include:
- Leading frontend architecture and UI/UX planning for accessibility  
- Designing database integration and local-only data policies  
- Contributing to system architecture decisions and technology selection  
- Supporting backend API design and adaptive learning logic  
- Ensuring privacy compliance for optional attention-tracking features  
- Assisting with documentation and technical specifications  

---

## Current Progress (≈35%)
**Completed:**
- Project charter and scope definition  
- Functional requirements mapped to customer feedback and engineering standards  
- System architecture design (hardware + software)  
- Hardware selection and validation  
- UI/UX wireframes for teacher and student dashboards  

**In Progress / Upcoming:**
- Hardware bring-up and local Wi-Fi hosting  
- Backend (Flask + SQLite) implementation  
- Frontend dashboard development  
- Adaptive learning engine and engagement analytics
