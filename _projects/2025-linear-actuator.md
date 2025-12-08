---
layout: project
title: Linear Actuator Design
description: Class Project, Statics and Mechanics of Solids
technologies: [Designing, Linear Actuator, Force Balance, Beam Deflection, Beam Buckling]
image: /assets/images/linear_actuator_sketch.JPG
---

As part of a class project, I was asked to design a frame/mechanism that can lift the maximum possible weight to the maximum possible height, all while staying within a 2D design space of 150 cm long and 50 cm tall. The frame needed to consist of a rigid bar of fixed length, a linear actuator, and 3 pin supports (2 of which need to be mounted on the ground). As an addition to this assignment, I will then look at the design with a non-rigid beam and do beam bending analysis, ultimately choosing a material type and beam shape to satisfy the condition that beam deflection cannot be greater than 2% of its length while still being as mass efficient as possible. Additionally, I will conduct a beam buckling analysis on this design.

Here is my sketch design at the maximum linear actuator extension:

![Frame Design when Actuator is at Full Extension]({{ "/assets/images/linear_actuator_sketch.JPG" | relative_url }}){: .inline-image-l}
My design features a rigid beam of length L that is mounted to ground and pinned to a linear actuator of maximum length A (which is also mounted to ground). The load will be applied to the structure at pin Beta, and the device will lift this weight by extending the linear actuator on a line in the xy-plane, giving it one degree of freedom.

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
We can conduct static analysis on the device to solve for unknown variables, specifically using Pythagorean Theorem to solve for Theta, Phi, d_L, and d_A as well as a Force Balance at pin Beta to solve for F_L and w.


![Here's my work]({{ "/assets/images/lin_act_math1.JPG" | relative_url }}){: .inline-image-l}

Using Pythagorean Theorem:

- Theta = 10.1817 degrees
- Phi = 25.8419 degrees
- d_L = 21.7945 cm
- d_A = 8.0820 cm

![Here's my work]({{ "/assets/images/lin_act_math2.JPG" | relative_url }}){: .inline-image-l}

By Sum of Forces at pin Beta:

- F_L = 43.1131 kN
- w = 143.4376 kN

Summary:
- My design is able to lift up a 143.4376 kN load to a maximum possible height of 45 cm. This seems like a reasonable output, since the linear actuator itself can support 106.31 kN, and the rigid rod would support the rest of the load due to the triangular geometry of the structure. The lift height is also fairly tall, since I am working within a 50 cm limit.

FINAL VALUES POST STATIC ANALYSIS:
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

Now it's time to do some beam deflection analysis, no longer treating the bar as rigid. Instead, the beam will bend due to the combined forces of the applied load and the actuator force.

Since the bar is a two force member that is pinned at both ends, there should in theory be no bending due to a lack of shear forces or internal moments. For the sake of this assignment, however, the system can be modeled like so:

![Drawing of Approximation]({{ "/assets/images/Beam_Bend_Approx.jpg" | relative_url }}){: .inline-image-l}

This drawing features the bar of length L with a fixed support on the left and a free end on the right. The fixed support represents pin Alpha (connecting L and ground), with the assumption that the forces applied will NOT cause the bar to rotate about Alpha. This helps to simplify analysis by keeping the bar in static equalibrium. The free end, on the other hand, is a representation of what is occuring at Beta (treating the pin and the bar as one object) transverse/perpendicular to the beam. Force F is a sum of the transverse components of load w and actuator force F_A, which again simplifies analysis.

F was found to be equivalent to -34.86876157 kN.

![FBD]({{ "/assets/images/Bend_FBD_Full.jpg" | relative_url }}){: .inline-image-l}
Here is a free body diagram of the beam approximation. Solving for the reaction forces:
- R_x = 0
- R_y = 34.86876157 kN
- M_r = 17.43438079 kNm

![FBD - internal loads]({{ "/assets/images/Bend_FBD_Int.jpg" | relative_url }}){: .inline-image-l}
Now let's find the internal loads:
- T_I = 0
- V_I = 34.86876157 kN
- M_I(x) = (17434.38079-34868.76157x) Nm
As a preliminary check, we can see that M_I(0) = 17.43438079 kNm = M_r, which makes sense since this is the fixed end with a now known moment. We can also see that M_I(0.5) = 0, which makes sense for the free end.

![Bend Analysis]({{ "/assets/images/Bend_Analysis.jpg" | relative_url }}){: .inline-image-l}
We can use the relationship EIy''(x) = M(x) to find function y(x), which is the Equation of the Elastic Curve and corresponds to the deflection of the beam at a given x value. The boundary conditons used for this approximation are y'(0) = 0 and y(0) = 0, since the beam will not move or change slope at the fixed end. 
To summarize: 
EIy = 8717.190395x^2 - 5811.460263x^3

![Deflection Max]({{ "/assets/images/Max_Deflection.jpg" | relative_url }}){: .inline-image-l}
The maximum deflection in the beam will occur at x = L = 50 cm = 0.5 m. Plugging this x value into the equation found above, we can see that y_max = 1452.865066/(EI) m.

Due to the truss-like nature of my design, it makes the most sense to do a beam buckling analysis, as depicted below:
![Buckling Analysis]({{ "/assets/images/Beam_Buckling.jpg" | relative_url }}){: .inline-image-l}
Taking the critical load to be w = 143.4376 kN and Leq = L = 0.5 m (since the bar is in the pinned-pinned configuration), we can find that EI would have to be 3633.316853 Nm^2.

We should also check this with the minimum EI value needed for beam deflection to be less than 2% of its length.
![ymax]({{ "/assets/images/Beam_bend_ymax.jpg" | relative_url }}){: .inline-image-l}
This bending analysis gives an EI value of 145286.5066 Nm^2. To satisfy both bending and buckling cases, EI should have a value of at least 145286.5066 Nm^2.

Now, here's my Excel Spreadsheet of various material choices coupled with potential beam shapes (information sourced from Appendices C and D from "Statics and Mechanics of Materials: Third Edition" by Ferdinand P. Beer, E. Russell Johnston Jr., John T. DeWolf, and David F. Mazurek). 

![Excel Sheet]({{ "/assets/images/Statics_Beam_Excel.jpg" | relative_url }}){: .inline-image-l}

I calculated EI and the weight for each choice, ultimately finding that the best solution was a C150X12.2 beam made of Magnesium Alloy AZ31 for its light weight of 1.36290 kg and EI value of 245250 Nm^2. This combination was the most light-weight choice of the list, and it satisfied the condition that EI >= 145286.5066 Nm^2.














