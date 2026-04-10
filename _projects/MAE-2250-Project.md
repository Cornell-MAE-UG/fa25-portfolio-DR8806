---
layout: project
title: MAE 2250 Lantern Fly Project
description: Client Pitch and Functional Prototype for Spotted Lantern Fly Project
technologies: [Autodesk Fusion]
image: 
category: "Personal Projects"
order: 5
---

# Portfolio

**Jump to:**  
[Client Pitch](#client-pitch) · [Functional Prototype](#functional-prototype)

---

## Client Pitch
<a id="client-pitch"></a>

**Post Harvest Spotted Lanternfly Removal**  
Team: DEAd heAD  
Client(s): Cornell CALS Extension / E&J Gallo Winery / National Grape  

---

**Problem Statement**  
Spotted Lanternflies (SLF) are devastating wineries and grape processors in New York and nearby regions, with losses reaching $8.8 million in three years. During high-volume harvest periods, post-harvesting facilities must remove SLF quickly, yet current methods continue to miss insects, risking contamination and regulatory noncompliance which can lead to financial and operational strain. 

**Impact**  
Solving the SLF contamination would protect the wine supply chain, helping growers in New York preserve crop value while enabling processors to increase throughput, reduce labor, and lower losses, stabilizing supply for distributors and retailers. This keeps regional producers competitive, strengthens the broader agricultural economy, and ensures millions of consumers continued access to quality wine. 

---

**Concept A (Primary) – Filtering Brushes**  
A car wash-like machine where rotors will brush off SLF on the conveyor belt. Brushes will be tuned in stiffness to be able to remove SLF, minimizing product loss.  

*How it would be used (user flow):*  
Step 1: Grapes enter the post-processing conveyor belt.  
Step 2: Product passes through brush module, where brushes knock SLF off of harvested grapes.  

*Why it’s better than the status quo:*  
This is a mechanically simple mechanism that could prove to be effective, and it’s easily integrated into pre-existing post-harvest processing conveyors.  

*End-of-semester proof-of-concept:*  
A simple motor mechanism with spinning brushes, testing by modeling grapes and SLF with a force gauge to test the force of the brushes. 

---

**Concept B (Secondary) – Wind-Sorting Unit**  
A controlled airflow module that removes lighter SLF from heavier grapes moving along a conveyor belt. 

*How it would be used (user flow):*  
Step 1: Grapes enter on a conveyor belt.  
Step 2: Belt passes through the wind-sorting unit, where airflow blows SLF off of grape stream. 

*Why it’s better than the status quo:*  
No direct contact with grapes is needed, so grapes will not be harmed during the process. The unit is easy to automate and integrate with existing processing equipment.  

*End-of-semester proof-of-concept:*  
An airflow unit that uses small air guns or fans to blow SLF off the grapes. Testing by simulating SLF on grapes and using airspeed sensors to measure the force of air.  

---

**Key Risks / Unknowns**  
● For Concept A, there could be clogging due to jamming on the conveyor belt or on the brushes.  
We will compare with existing designs and test with simulated grapes and SLF.  

● For Concept B, airflow intensity and direction will need to be tuned to ensure grape quality does not degrade. We will test this by simulating grape processing under varied conditions.  

● Both proposed solutions include the possibility of excessive grape removal or damage. We will test this by experimenting with different brush stiffnesses, rotation speeds, and airflow intensities.  

---

**Questions for the Client**  

1. Are SLF entering post-harvest processing primarily alive and intact, or dead and fragmented within the grape stream/slush?  
Decision affected: Determines whether mechanical separation is viable or if removal must occur earlier, since fragmented SLF may be harder to remove.  

2. What does a typical processing layout look like, and where would sanitation, space, or workflow constraints limit adding equipment?  
Decision affected: Defines integration limits so the design fits operational and regulatory realities, and supports solutions that can scale across facilities without major infrastructure changes.  

3. Which forms of product damage are least acceptable (juice release, skin breakage, berry loss, or cluster disruption)? Please rank if possible.  
Decision affected: Sets force and contact limits, guiding mechanism selection and tuning so the design minimizes losses within acceptable damage tolerances.  

---

**References**  
https://news.cornell.edu/stories/2025/01/spotted-lanternflies-could-cost-nys-grape-industry-millions

---

### Full PDF
<iframe 
    src="https://cornell-mae-ug.github.io/fa25-portfolio-DR8806/assets/client_pitch.pdf" 
    width="100%" 
    height="600px" 
    style="border:none;">
</iframe>
---

## Functional Prototype
<a id="functional-prototype"></a>

**O5: Functional Prototype**

**Design Documentation**  
Our concept is a filtering brush mechanism designed to remove SLF from grapes during the harvesting processing. Grapes will travel along the harvesting machine’s conveyor belt and pass through a rotating brush placed above. The brush will lightly contact the product stream, applying enough force to knock off the SLF from the grapes while minimizing product loss.  

---

**Components**

| Component | Quantity | Fabrication/Purchase |
|----------|--------|----------------------|
| Mounting Plate | 2 | In house, Laser Cut Acrylic |
| Mounting Base | 2 | In house, Laser Cut Acrylic |
| Mounting Support | 4 | In house, Laser Cut Acrylic |
| Oak Rod, 36" Long, 1" Diameter | 1 | McMaster, 96825K82 |
| Brush Support | 4 | In house, Laser Cut Acrylic |
| Hex Bolt 4.5mm | 1 | In house, Taylor Design Studio |
| Strip Brush (1" height) | 1 | McMaster, 1469N21 |
| Strip Brush (2" height) | 1 | McMaster, 1469N22 |
| Strip Brush (3" height) | 1 | McMaster, 1469N23 |
| Steel Ball Bearing (R16) | 2 | McMaster, 1469N23 |

---

**Design Illustration**  
![design-intent-placeholder](https://cornell-mae-ug.github.io/fa25-portfolio-DR8806/assets/images/design_intent.png)

---

**Assembly Instructions**  

1. Assemble the mounts. Put supports together and use CA glue to secure.  
![assembly1](https://cornell-mae-ug.github.io/fa25-portfolio-DR8806/assets/images/assembly1.png)
2. Cut the oak rod down to 12 in. Space the custom-cut brush supports evenly throughout the oak rod and use CA glue to secure in place.  
3. Use a rubber mallet to secure the ball bearings on either end of the oak rod. Secure either side of both bearings with hot glue.  
![assembly2](https://cornell-mae-ug.github.io/fa25-portfolio-DR8806/assets/images/assembly2.png)
4. Center drill the oak rod and insert a hex bolt. After ensuring concentricity, secure the hex bolt in place with CA glue.  
5. Cut the strip brushes to 3 pieces of 20 in. length. Thread the strip brushes through the brush supports, winding them a quarter-turn between each support.  
![assembly3](https://cornell-mae-ug.github.io/fa25-portfolio-DR8806/assets/images/assembly3.png)
6. Press the ball bearings into the mounts at an equal height on either end. Ensure the shaft can rotate freely without interference from the brushes and trim as needed.  
7. Mount drill to brush assembly by tightening drill chuck to protruding hex bolt. Drive at varying speeds.  
![assembly4](https://cornell-mae-ug.github.io/fa25-portfolio-DR8806/assets/images/assembly4.png)

---

**Design Tests**

*Test 1: Brush Lengths*

| Brush Length | Observations |
|-------------|-------------|
| 1” (shortest, stiffest) | Bristles were highly rigid and transferred significant force upon contact. This caused frequent grape displacement... |
| 2” | Provided a moderate balance between stiffness and flexibility... |
| 3” (longest, least stiff) | Bristles exhibited greater flexibility... |

Based on these observations, it is clear that the 3” brush was the most effective.  

---

*Test 2: Maximum Rotation Speed and Brush Direction Test*

| Driving Direction | Speed | SLF Removed | Movement |
|------------------|------|------------|----------|
| Clockwise | ~500 RPM | 3/8 | Manageable (1-2mm) |
| Clockwise | ~2000 RPM | 6/8 | >5mm |
| Counterclockwise | ~500 RPM | 0/8 | Manageable (1-2mm) |
| Counterclockwise | ~2000 RPM | 0/8 | >5mm |

Conclusion:  
For drill speeds higher than the first setting, our mounts moved > 5mm...  

---

**Success Criteria**

● The brushes should not damage, crush, or visibly harm more than 5% of grapes.  
● The brushes should be tuned to remove at least 90% of SLF from grapes in a single pass.  
● The system should be able to withstand rotations of up to 2500 rpm, without shifting more than 5mm.  
● The brush geometry and layout should be able to clear 90% of debris regardless of brush length.  
● The system should be able to process grapes on a conveyor belt at a speed of 1 m/s.  

---

**Evaluation Plan**  
We will measure our criteria by building a mock conveyor belt and modelling grapes and SLF as our product stream...

---

### Full PDF
<iframe 
    src="https://cornell-mae-ug.github.io/fa25-portfolio-DR8806/assets/functional_prototype.pdf" 
    width="100%" 
    height="600px" 
    style="border:none;">
</iframe>