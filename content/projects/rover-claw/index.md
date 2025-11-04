---
title: "Mars Rover Robotics: End Effector Design"
summary: "Designing a durable, high-torque claw for the WashU Mars Rover Team’s 2024–25 University Rover Challenge entry"
date: 2025-11-01
---

### Background
The WashU Mars Rover Team competes annually in the University Rover Challenge (URC) — an international competition pushing students to design rovers capable of traversing rough, Mars-like terrain and performing complex tasks like sample collection and equipment handling.  
At the heart of those missions lies the arm subsystem, the part of the robot responsible for interacting with game elements. For the 2024–25 season, I led the design of a worm-gear-driven mechanical claw optimized for strength, precision, and manufacturability that integrated into our very own 5 DOF arm. For the current 2025-2026 season, I'm an arm design lead and I'm currently leading a subteam of 8 members with the united goal of producing a highly functional 5 DOF robotic arm.

---

### Design
The claw was born in SolidWorks, evolving from napkin sketches into a three-pound end-effector printed in PLA and powered by a high-torque hobby servo. Its defining feature is a worm gear drive — a compact system that converts rotary motion into the claw's distinct self-locking grasp. Each claw finger is mounted on shafted bearings for low-friction motion, with rubber pads added to increase grip on irregular objects. A mounted camera provides visual feedback for target detection, alignment, and optimized control.

We needed something strong enough to lift 2–3 lb payloads, precise enough to handle sample tubes, and light enough to stay within our arm torque budget. To achieve that, I tuned gear ratios to triple output torque while keeping total rotation under 90°, ensuring predictable, stable motion during pickup tasks.

---

### Prototyping & Testing
The first prototype was completed in December 2024 after just six weeks of CAD modeling, vendor ordering, and 3D printing. Testing showed strong compliance under load, with grasping torque exceeding 0.6 N·m and repeatable control via Arduino-based servo commands. With the worm gear only transmitting torque in one direction, it confirmed the claws non-backdrivability — meaning it could hold objects even when powered off.

By January 2025, a second-generation revision with optimized structural components, formalized shafts with snapper ring grooves, new bearing retainment plates, and an entirely redesigned claw finger led to much improved performance.

---

### Lessons & Next Steps
Through this build, I learned a ton of things.

One key learning was working on a team with a relatively low budget. Sometimes, it was difficult to afford components and I had to work and adapt to the components the team already had in supply. That meant being incredibly flexible and prototyping a lot with the options available. This also confirmed how seemingly small design choices — gear alignment, wall thickness, and print orientation — directly impact torque transmission and durability.  
Looking forward to this upcoming year, the current claw under construction will:
- Reduce mass by ~25% using lighter materials and reducing motor sizing to generate more RPM (and less torque)
- Explore more compliant finger geometries for adaptive grasping.
- Integrate a modular quick-mount for easier servicing

---

### Reflection
Designing the claw taught me how to balance mechanical simplicity with functional reliability.  
It’s a system that translates pure geometry and physics into controlled, purposeful movement — something that captures exactly what drew me to robotics in the first place.
