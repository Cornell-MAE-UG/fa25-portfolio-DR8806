---
layout: project
title: MAE 2250 Lantern Fly Project
description: Client Pitch and Functional Prototype for Spotted Lantern Fly Project
technologies: [Autodesk Fusion]
image: 
category: "Personal Projects"
order: 5
---

# Portfolio Project Page

## Table of Contents
- [Client Pitch](#client-pitch)
- [Functional Prototype](#functional-prototype)

---

## Client Pitch
<a id="client-pitch"></a>

### Post Harvest Spotted Lanternfly Removal

**Team:** DEAd heAD  
**Client(s):** Cornell CALS Extension / E&J Gallo Winery / National Grape  

---

### Problem Statement
Spotted Lanternflies (SLF) are devastating wineries and grape processors in New York and nearby regions, with losses reaching $8.8 million in three years. During high-volume harvest periods, post-harvesting facilities must remove SLF quickly, yet current methods continue to miss insects, risking contamination and regulatory noncompliance which can lead to financial and operational strain.

---

### Impact
Solving SLF contamination would protect the wine supply chain, helping growers preserve crop value while enabling processors to increase throughput, reduce labor, and lower losses. This strengthens the agricultural economy and ensures consistent supply for consumers.

---

### Concept A (Primary) – Filtering Brushes
A car wash-like system where rotating brushes remove SLF from grapes on a conveyor belt. Brush stiffness is tuned to remove SLF while minimizing grape damage.

**User Flow:**
1. Grapes enter conveyor system  
2. Grapes pass through brush module where SLF are removed  

**Advantages:**
- Mechanically simple  
- Easy integration into existing systems  

**Proof of Concept:**
- Motor-driven spinning brushes  
- Testing with modeled grapes and SLF using force measurements  

---

### Concept B (Secondary) – Wind-Sorting Unit
A controlled airflow system that separates lighter SLF from heavier grapes.

**User Flow:**
1. Grapes enter conveyor  
2. Airflow removes SLF from stream  

**Advantages:**
- No physical contact → less grape damage  
- Easy automation  

**Proof of Concept:**
- Airflow system using fans/air guns  
- Testing with simulated SLF and airspeed measurements  

---

### Key Risks / Unknowns
- Brush clogging or jamming  
- Airflow tuning challenges  
- Potential grape damage or loss  

---

### Questions for Client
1. Are SLF intact or fragmented during processing?  
2. What are layout and integration constraints?  
3. What types of grape damage are least acceptable?  

---

### References
- https://news.cornell.edu/stories/2025/01/spotted-lanternflies-could-cost-nys-grape-industry-millions

---

## Functional Prototype
<a id="functional-prototype"></a>

### Design Overview
A rotating brush mechanism mounted above a conveyor removes SLF from grapes. The brush applies enough force to remove insects while minimizing grape damage.

---

### Components
- Laser-cut acrylic mounts and supports  
- Oak rod (shaft)  
- Strip brushes (various lengths)  
- Ball bearings  
- Hex bolt (drive connection)  

---

### Assembly Summary
1. Assemble mounting structure  
2. Cut and prepare shaft  
3. Attach brush supports  
4. Install bearings and shaft  
5. Attach strip brushes in spiral pattern  
6. Mount and connect to drill motor  

---

### Testing

#### Test 1: Brush Length
- **1” (stiff):** High SLF removal but high grape damage  
- **2”:** Moderate balance, some displacement  
- **3” (best):** Effective removal with minimal grape disruption  

**Conclusion:** 3” brush chosen  

---

#### Test 2: Speed & Direction

| Direction | Speed | SLF Removed | Stability |
|----------|------|------------|----------|
| Clockwise | ~500 RPM | 3/8 | Stable |
| Clockwise | ~2000 RPM | 6/8 | Some instability |
| Counterclockwise | ~500 RPM | 0/8 | Stable |
| Counterclockwise | ~2000 RPM | 0/8 | Unstable |

**Key Takeaways:**
- Clockwise rotation is effective  
- High speeds reduce stability  
- Mounting needs reinforcement  

---

### Success Criteria
- ≤ 5% grape damage  
- ≥ 90% SLF removal  
- Stable up to 2500 RPM (≤ 5mm movement)  
- Works across configurations  
- Conveyor speed of 1 m/s  

---

### Evaluation Plan
- Simulated conveyor testing  
- Measure:
  - SLF removal rate  
  - Grape damage  
  - RPM stability  
  - Structural movement  

---

### Optional PDF Links
- [Client Pitch PDF](/assets/client_pitch.pdf)
- [Functional Prototype PDF](/assets/functional_prototype.pdf)

