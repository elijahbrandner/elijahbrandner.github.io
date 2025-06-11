---
layout: project
type: project
image: img/Picture2.png
title: "3D Scene Reconstruction with OpenGL"
date: 2025-02-14
published: true
labels:
  - Ubuntu
  - OpenGL
  - C++
summary: "This project involved capturing a real-life photo on a smartphone and recreating the entire scene using OpenGL primitives and transformations. The selected scene featured a snowboard leaning against a white door, surrounded by a hardwood floor, ceiling, doorknob, lock, and light switch. Each element was reconstructed using geometric primitives and mathematical modeling."
---
As part of my Computer Graphics course at Grand Canyon University, I completed a project where my partner and I were tasked with capturing a real-life photo using a smartphone and recreating the scene entirely through OpenGL. The chosen scene featured a snowboard leaning against a white door, surrounded by a hardwood floor, a doorknob, lock, ceiling, and light switch. Our objective was to accurately model and render each object using OpenGL primitives, mathematical transformations, and texture mapping techniques. I implemented cubic Bézier curves to replicate the smooth curvature of the snowboard, while other elements—like the door and panels—were created using GL_QUADS and GL_LINE_LOOP with extruded depth for a realistic 3D appearance. To enhance visual fidelity, we mapped textures onto the floor and walls using SOIL, applied lighting models for reflective surfaces, and modeled fine details like snowboard bindings and door hardware. I also developed a virtual camera system that allowed for multiple dynamic viewpoints using gluLookAt, along with keyboard controls for movement and zoom. This project strengthened my understanding of geometric modeling, coordinate transformations, and the OpenGL rendering pipeline. It was both a technical and creative challenge that taught me how to translate real-world visual complexity into mathematical and graphical constructs within a 3D space.

