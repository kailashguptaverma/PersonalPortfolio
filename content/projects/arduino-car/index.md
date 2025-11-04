---
title: "Circuit Car: Bluetooth-Controlled Autonomous Vehicle"
summary: "Designing and refining a microcontroller-based vehicle with Bluetooth control, ultrasonic sensing, and custom motor circuitry."
date: 2024-12-05
---

### Background
The Circuit Car project was a small-scale autonomous system that combined mechanical design, embedded programming, and circuit integration into a single platform.  

The goal was to create a Bluetooth-controlled vehicle capable of both manual steering and autonomous obstacle avoidance using ultrasonic sensors. Built around an **Arduino Uno**, the car featured dual DC motors, a motor driver shield, a Bluetooth module, and an HC-SR04 ultrasonic distance sensor.

The system was designed to be modular, low-cost, and adaptable—allowing real-time remote control from a smartphone app while supporting onboard logic for autonomous response. Although the foundation was solid, the path to a working prototype involved multiple iterations, debugging sessions, and careful tuning of both hardware and code.

---

### Development Process
We began by developing the base control structure: PWM-driven motor speed control combined with Bluetooth serial commands. Early tests exposed a variety of issues—from electrical interference and faulty ports to incorrect timing functions in sensor readings. Rather than redesigning the whole circuit, we approached each failure as an opportunity to better understand how software and hardware interact at the micro level.

Key challenges and their solutions:

| Issue | Solution |
|-------|-----------|
| Mechanical delays, blocked USB ports, missing hardware | Replaced motor shield, sourced screws, and 3D printed chassis for free on campus |
| Serial.read() outputting corrupted data | Switched to BT.read() for stable Bluetooth communication |
| Limited motor control flexibility | Implemented the Adafruit motor control library |
| Bluetooth communication indexing errors | Wrote code to skip erroneous or repeated command inputs |
| Excessive battery drain | Replaced batteries with high-efficiency cells and reduced total vehicle weight |
| Motor control inconsistency due to poor pin mapping | Re-soldered connections to align with proper PWM output pins |
| Unreliable ultrasonic timing | Replaced delay() with micros() for accurate timing control |
| Dysfunctional motor shield ports | Wired motors in parallel to functional outputs |

---

### Results and Learnings
After iterative refinement, the car successfully responded to real-time Bluetooth commands and navigated around obstacles autonomously with smooth PWM transitions. Latency was reduced to under 0.3 seconds, and obstacle detection was accurate up to 120 cm, even under varying light conditions.  

Beyond the technical results, the process taught me the importance of debugging systematically—isolating one subsystem at a time rather than treating failures as whole-system flaws.  
I also learned how small inefficiencies in wiring and code structure can have significant effects on system responsiveness and energy usage.

---

### Reflection
The Circuit Car project was more than an exercise in electronics—it was a hands-on exploration of electromechanical design. Each iteration reinforced a habit of structured troubleshooting and showed how even small embedded systems benefit from modularity, documentation, and adaptability.