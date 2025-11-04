---
title: "Fulfil Solutions: Tote Clip Compliance"
summary: "Improving bag retention reliability in automated grocery systems through compliant spring design and tolerance optimization."
background: "content/projects/compliance-mechanism/cover.jpg"
date: 2025-08-14
---

### The Story

**[Fulfil Solutions](https://www.fulfil.com/)**, a company based in the Bay Area I worked at over the summer, is committed to building automated grocery fulfillment systems. They integrate mobile robots, dense storage trays, and computer vision to pick, pack, and deliver items across all temperature zones—aiming for high accuracy and sharply reduced labor costs.

![Fulfil Technology](images/fulfilTech.jpg)

When I joined Fulfil, the team was working through a significant design challenge: keeping grocery bags open during high-speed automated packing.  

Fulfil’s robots handle thousands of totes per hour, each carrying multiple open bags held in place by clips. Clips are needed to secure the bag and maintain enough tension to keep it open, but with too much tension, tearing is also a concern. It was a deceptively simple problem that required a lot of analysis and a deep dive into compliance mechanics.

![Fulfil Technology](images/fulfilBots.jpg)

---

### Understanding the Problem

The existing clips that proved to be an issue were incredibly rigid. Their design didn't account for the degrees of tolerance at play or the variation in bag placement. That meant a clip that was perfect on one assembly might over-compress or under-tension on another.

![Totes](images/toteSS.jpg)

My goal was to redesign the clip to tolerate that variance without sacrificing consistency or manufacturability.  
Through some initial testing and background work, a few targets were set at the start:

- **Tension range:** 2–6 N (enough to hold the bag open, but not tear it)  
- **Deflection range:** 5–8 mm under load  
- **Yield safety factor:** ≥ 1.5 under maximum deflection  
- **Cycle life:** 1M+ operations

---

### Design Exploration

I started by modeling the existing geometry and overlaying the worst-case dimensional stack-up from CAD. Generating a spreadsheet of all the GD&T informed dimensions and combining that into an overall tolerance stackup made the amount of spring range much clearer. Using both Excel-based tolerance simulations and SolidWorks interference checks, I quantified the maximum allowable clip deflection.

From there, I compared three design families:
1. **Conical compression springs** — simple, but hard to control force linearly.  
2. **Torsion springs** — compact, but difficult to package cleanly around the tote wall.  
3. **Flat spring mechanisms** — manufacturable, tunable, and ideal for high-cycle flexure.

I ran quick analytical models for each, calculating stress, deflection, and strain energy. After verifying their effectiveness, I designed 3D-printable prototypes and ordered variations of all three spring types from COTS providers. After receiving all the springs and assembling them, it was time for some initial testing.

### Testing and Iteration

The first prototype immediately showed improvement: consistent retention and no bag tearing.  
But under dynamic loads, the clips bottomed out just before full tote engagement — meaning our preload was too high. 

Updating my constraints and iterating on my prototype, I eventually developed a finalized prototype that accomplished the goals set out at the start. It was designed for a 3D printed clip, but the compliant component would be a hardened 17-7PH CH900 steel flat spring. Ultimately, it was time to think about designing for production.

### Manufacturing and Integration

In order to move to a production version, I ironed out a few details:
- Ran an FEA on the prototype and verified fatigue life through S-N analysis
- Spec’d the material as 17-7PH CH900, laser-cut, bent, and heat-treated for fatigue strength  
- Optimized bend radii to minimize stress risers and maintain repeatable springback  
- Reduced per-unit clip cost by 38%  
- Ensured the clip cover could be injection molded while the clip itself could be milled
- Presented my final production process & final design to R&D design team 

---

### Reflections

* I learned a ton throughout this project. 
* I learned that tiny compliance errors can cascade into major system issues. A few tenths of a millimeter in a stack-up could mean the difference between smooth automation and a jammed line. 
*I learned to trust a process that moves fluidly between analysis, physical prototyping, and iterative testing — and how to balance elegant design with rugged reliability.

In the end, we turned a fragile, temperamental mechanism into a robust, production-ready spring system that works across every tote, every cycle, and is implementable in every one of Fulfil's automation facilities.

---

**Key Outcomes**
- Reduced tolerance-induced failure rate by **>75%**  
- Extended clip life beyond **120k cycles** without fatigue failure  
- Lowered material cost by **38%**  
- Maintained consistent bag tension within **±0.3 N**