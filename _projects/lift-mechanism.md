---
layout: project
title: Lift Mechanism
description: A Design of Lifting Mechanism to Optimize Weight and Height
technologies: [MATLAB]
image: /assets/images/Lift_Image.png
---

For Cornell's ENGRD2020 Class on Statics and Mechanics of Solids, I designed a simple lift mechanism based on given constraints. The exact prompt (below) is simple but prompting enough to create a substaintial learning experience. 

> Given a 2D design space of 150cm long and 50cm tall, a rigid bar of a fixed length (your
choice), 3 pin supports of which two need to be mounted on the ground and a [linear
actuator](https://www.tolomatic.com/wp-content/uploads/2022/05/2700-4000_29_IMA_cat.pdf) (pick from this online catalog, use max force values only), design a
frame/mechanism to lift the maximum possible weight to the highest possible height.
Assume all the supports and bar/actuator are rigid.


After reading the prompt, I knew this was an optimization problem. First, I drew out the situation based on the given parameters and assigned variables. After doing geometry, there is two things to maximize: the height and the weight. What follows will be equations built on Statics intuition and mathematics to solve the optimization equation. 

![Shaded rendering of earlier version]({{ "/assets/images/HW4_Sketch.png" | relative_url }})
