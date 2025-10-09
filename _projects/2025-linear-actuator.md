---
layout: project
title: Linear Actuator Design
description: Class Project, Statics and Mechanics of Solids
image: /assets/images/linear_actuator_sketch.jpg
---

As part of a class project, I was asked to design a frame/mechanism that can lift the maximum possible weight to the maximum possible height, all while staying within a 2D design space of 150 cm long and 50 cm tall. The frame needed to consist of a rigid bar of fixed length, a linear actuator, and 3 pin supports (2 of which need to be mounted on the ground). 

Here is my sketch design at the maximum linear actuator extension:


<img src="https://github.com/Cornell-MAE-UG/fa25-portfolio-mp2279-gif/blob/main/assets/images/linear_actuator_sketch.JPG" width="500" />

These are my variable definitions:
- L: length of rigid bar in cm
- A: maximum length of linear actuator in cm
- h_max: maximum height possible of mechanism in cm
- d: total horizontal length of mechanism in cm
- Phi: angle between L and vertical height of triangle in degrees
- Theta: angle between A and vertical height of triangle in degrees
- Alpha: pin connecting L and ground
- Beta: pin connecting L and A
- Gamma: pin connecting A and ground
- w: force produced by applied load in kN
- d_L: horizontal length from pin Alpha to pin Beta in cm
- d_A: horizontal length from pin Beta to pin Gamma in cm
- F_A: max load supported by linear actuator in kN
- F_L: load supported by rigid bar in kN

Here is a list of my design choices:
- In this design, I used a Tolomatic IMA 55 RN05 linear actuator, with a dynamic load rating of 106.31 kN and length between 15.24 and 45.72 cm. I chose this linear actuator due to its length and loading capacities, keeping in mind the goal to lift the most weight to the highest possible height.
- L was arbitrarily set to 50 cm. This was so I could stay within the design space while still maintaining a relatively large h_max. In addition, I didn't want to make L too long (in the horizontal direction) and risk the structure failing since I can't add in any more members to the frame due to class prompt constraints.
- I decided to aim for a h_max of 45.0 cm, which seemed reasonable because the max length of the linear actuator was 45.72 cm, and by Pythagorean Theorem, the hypotenuse of the triangle produced by A, h_max, and d_A cannot be smaller than any of its sides (in this case actuator length A limits hypothenuse h_max).

Let's solve for the variables at h_max!

Using Pythagorean Theorem:
<img src="https://github.com/Cornell-MAE-UG/fa25-portfolio-mp2279-gif/blob/main/assets/images/lin_act_math1.JPG" width="500" />
- Theta = 10.1817 degrees
- Phi = 25.8419 degrees
- d_L = 21.7945 cm
- d_A = 8.0820 cm

By Sum of Forces at pin Beta:
<img src="https://github.com/Cornell-MAE-UG/fa25-portfolio-mp2279-gif/blob/main/assets/images/lin_act_math2.JPG" width="500" />
- F_L: 43.1131 kN
- w = 143.4376 kN

Summary:
- My design is able to lift up a 143.4376 kN load to a maximum possible height of 45 cm. This seems like a reasonable output, since the linear actuator itself can support 106.31 kN, and the rigid rod would support the rest of the load due to the triangular geometry of the structure. The lift height is also fairly tall, since I am working within a 50 cm limit.

FINAL VALUES:
- L: 50 cm
- A: 45.72 cm
- h_max: 45 cm
- d_L: 21.7945 cm
- d_A: 8.0820 cm
- d: 29.8765 cm
- Phi: 25.8419 degrees
- Theta: 10.1817 degrees
- F_L: 43.1131 kN
- F_A: 106.31 kN
- w: 143.4376 kN







