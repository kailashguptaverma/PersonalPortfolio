---
title: "MeshAlyzer: Dynamic Hernia Mesh Testing Platform"
summary: "A biomedical testing device designed to simulate realistic intra-abdominal pressures for evaluating surgical hernia meshes."
date: 2025-09-15
---

### Background  
The MeshAlyzer™ was developed by a senior design team in Dr. Spencer Lake’s Musculoskeletal Soft Tissue Lab at WashU to address a major gap in hernia mesh evaluation.  

Every year, nearly 1 million hernia repairs are performed in the U.S., and yet up to 13% result in recurrence due to improper mesh selection or failure under physiological conditions. Most tests rely on static loading — but real abdominal walls experience cyclical pressure surges from breathing, coughing, or movement.

The MeshAlyzer was engineered to simulate these realistic, dynamic intra-abdominal pressures, giving researchers a way to quantify how different meshes distribute stress and strain on tissue — a critical factor in surgical outcomes.

---

### System Overview  
At its core, the MeshAlyzer uses a polyurethane balloon system capable of generating 110.8 kPa of pressure (equivalent to a human cough) in under 0.5 seconds. The balloon sits beneath tissue samples held in custom-machined aluminum clamps that stretch tissue by 10% while maintaining physiological tension.  
A machine learning–calibrated transducer network ensures 99% pressure accuracy, while a Raspberry Pi interface and intuitive Python GUI allow for real-time monitoring, calibration, and automation.  

The design prioritizes both safety (IPX4 housing, emergency shutoff, pressure relief valves) and usability, validated through user testing in Lake Lab that rated the interface ≥ 4.5 / 5 for clarity and ease of use.

---

### My Contributions  
While the MeshAlyzer was primarily developed by the senior design team, my work focused on improving the system’s mechanical and sensing performance — refining the way the device behaves under load and improving experimental reproducibility.

#### Key Modifications I Made:
- **Balloon Integrity and Pressure Optimization** — Reanalyzed the balloon’s flow-rate characteristics and supply pressure curve, verifying that ~700 kPa inlet pressure achieved the 110.8 kPa target within 0.5 s without rupture.  
- **Clamp Redesign** — Adjusted lead screw alignment and mounting tolerances to improve symmetric tensioning and reduce motor strain during long-duration tests.  
- **Sensor Noise Reduction** — Implemented revised pressure calibration routines to minimize drift, combining neural network smoothing with low-pass signal filtering.  
- **Thermal Control Integration** — Designed an improved heating-pad mount beneath the tissue frame to maintain **38.7 °C**, matching physiological temperature for future biological testing.  
- **User Interface Refinement** — Added clearer pressure feedback and system status indicators to the Python-based GUI, improving test repeatability and usability.

These changes collectively enhanced data stability, safety, and test accuracy, laying groundwork for future iterations of the device that could integrate 3D deformation tracking and automated pressure profiling.

---

### Results & Learnings  
Through this project, I learned to navigate the intersection of mechanical design and biomedical testing — where precision, ethics, and safety converge.  

The MeshAlyzer demonstrated the ability to simulate realistic cough-level pressures, maintain tissue stretch over hours, and offer repeatable, quantifiable data for mesh evaluation.  

While challenges like sensor drift and limited biological validation remain, the device represents a significant step toward data-driven mesh selection in hernia repair and sets a foundation for ongoing translational research.

---

### Reflection  
Contributing to the MeshAlyzer taught me the value of iterative design in a biomedical context — how subtle adjustments in geometry, pressure control, and data interpretation can transform experimental reliability. It also deepened my understanding of soft tissue biomechanics and medical device verification, shaping the way I now approach engineering for healthcare impact.
