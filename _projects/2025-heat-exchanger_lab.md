---
layout: project
title: Heat Exchanger Lab
description: Class Project, Thermodynamics
technologies: [Heat Exchanger]
image: /assets/images/Heat_Exchanger_Full.JPG
---

In my thermodynamics lab, I tested out a heat exchanger setup by altering the operating conditions in an effort to observe potential changes in device performance.

A heat exchanger is a device that transfers heat between the flow of two fluids that are operating at different temperatures without the fluids physically mixing with each other. This is done so that one fluid will heat up after passing through the heat exchanger, while the other fluid will cool down. Heat exchangers are typically used in refrigeration and AC units by using coolant to keep the air cold.

![Heat Exchanger Cross Section]({{ "/assets/images/Heat_Exchanger_Cross_Section.JPG" | relative_url }}){: .inline-image-l}
Here's a view of the cross sectional area of a heat exchanger, where tubes will bring in two different fluids at different temperatures which will flow through the heat exchanger, transferrring heat via the metal barrier separating the two.

In this lab, the heat exchanger had a hot water source maintained by an attached immersion heaters in addition to a cold water source kept cool via ice and insulation surrounding the container. The two fluids were differentiated by food dye, with red coloring for the hot reservoir and blue coloring for the cold reservior.

The heat exchanger has a known mass flow rate of 210 gal/hr, so we tested the effects of same direction vs cross direction flow in addition to altering the initial temperature difference between the two reservoirs.

![Same Direction Flow]({{ "/assets/images/Same_Flow.JPG" | relative_url }}){: .inline-image-l}
Here is an image of the experimental setup with a same-directional flow.
Same directional flow means that both fluids are moving in the same direction (in this image, both move from the left side to the right side).

![Cross Direction Flow]({{ "/assets/images/Cross_Flow.JPG" | relative_url }}){: .inline-image-l}
Here is an image of the experimental setup with a cross-directional flow.
Cross directional flow means that the fluids are moving in directions opposite to each other (in this image, the blue fluid moves from left to right, while the red fluid moves from right to left).

![Schematics]({{ "/assets/images/Schematic.JPG" | relative_url }}){: .inline-image-l}
Here are drawn schematics of both the same directional flow setup and the cross directional flow setup, where Tc refers to the cold reservior, Th refers to the hot reservoir, and m dot refers to the mass flow rates through the exchanger. Since the hot reservior is maintained via an immersion heater, there is a rate of heat flow Qh into the hot reservior. The two pumps also run on electrical power, so there is a rate of work transfer into both pumps as a result.

![CV Diagram]({{ "/assets/images/CV-Diagram.JPG" | relative_url }}){: .inline-image-l}
Specifically looking at the heat exchanger as a Control Volume, we can assume that it is adiabatic (no heat transfer with surroundings), with no work rate since there are no moving parts (i.e. no shaft work, no rotors, etc.). We can also assume steady state flow, where the mass flow rate into the heat exchanger equals the mass flow rate out of the heat exchanger. 

![Energy Balance]({{ "/assets/images/Energy-Balance.JPG" | relative_url }}){: .inline-image-l}
If we perform an energy balance on the heat exchanger, assuming it is operating adiabatically at steady state with no work input or output, we can see that ideally, the temperature of one fluid will increase by the same amount that the other will decrease by.

![Entropy Balance]({{ "/assets/images/Entropy-Balance.JPG" | relative_url }}){: .inline-image-l}
If we do an entropy balance on the heat exchanger, again assuming adiabatic steady-state operation, we can see that the entropy generated will be equal to the sum of the change in entropy in both fluids multiplied by the mass flow rate of the heat exchanger.

During the lab, I observed the effects of changing the flow directionality (same or opposite) in addition to changing the temperature that the hot reservior was set to (specifically either 40.0 degrees Celsius or 35.0 degrees Celsius). Here is my data from these experiments:

Same Direction of Flow:

The first run started the hot reservior at 40.0 degrees Celsius (flow A), with the cold reservior at 6.8 degrees Celsius (flow B). The output of flow A was at 24.6 degrees Celsius, while the output of flow B was at 15.9 degrees Celsius.

The second run started the hot reservior at 35.0 degrees Celsius (flow A), with the cold reservior at 8.7 degrees Celsius (flow B). The output of flow A was at 23.7 degrees Celsius, while the output of flow B was at 21.1 degrees Celsius.

Opposite Direction of Flow:

The third run started the hot reservior at 40.0 degrees Celsius (flow A), with the cold reservior at 10.0 degrees Celsius (flow B). The output of flow A was at 19.6 degrees Celsius, while the output of flow B was at 23.9 degrees Celsius.

The fourth run started the hot reservior at 35.0 degrees Celsius (flow A), with the cold reservior at 9.2 degrees Celsius (flow B). The output of flow A was at 18.4 degrees Celsius, while the output of flow B was at 22.1 degrees Celsius.

We can judge performance based on the average temperature changes from the input flows to the output flows.

The same direction flow with Th = 40 degrees C had a temperature change of -15.4 across A and +9.1 across B, averaging to 12.25 degrees.

The same direction flow with Th = 35 degrees C has a temperature change of -11.3 across A and +12.4 across B, averaging to 11.85 degrees.

The cross direction flow with Th = 40 degrees C has a temperature change of -20.4 across A and +13.9 across B, averaging to 17.15 degrees.

The cross direction flow with Th = 35 degrees C has a temperature change of -16.6 across A and +12.9 across B, averaging to 14.75 degrees.

Overall, we can see that cross directional flow has a higher performance than the same direction flow, since we can see a greater temperature difference between the input and the output temperatures. We can also observe that a higher Th reservior temperature causes a slightly greater temperature difference between the inputs and outputs.


