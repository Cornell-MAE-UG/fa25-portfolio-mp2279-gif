---
layout: accordion
title: Open Design Project
description: Class Project, Intro to Mechanical Design
image: /assets/images/ODP_main.png

accordion:
  - title: Client Pitch
    content: |
    
        SLF Mechanical Repellant from Grape Harvester
    
        Team Name: Lanternfly Killers, Client(s): Cornell CALS Extension / E\&J Gallo Winery / National Grape
        
        Problem Statement: 
        
        Just 1-2 adult spotted lantern flies (SLF) can taint a kilogram of grade slurry; with how prevalent they are, this can add up rapidly.     Farmers are searching for ways of managing the SLF population without diminishing the potential crop yield. One way that the SLF population enters the crop yield is via the harvester during harvest. Finding a way to remove the flies off of the vines as the harvester intakes the grapes is important to prevent them from tainting the crop.
        
        Why it matters to the end user: 
        
        If we reduce the amount of SLF present in the crop yield, we will be able to help the farmers financially, since less crop will be thrown away due to SLF contamination. In addition, there will be less scarcity of grape products, since more products will make their way to the shelves, allowing businesses to not lose customers or profit. The consumers will also benefit from the lower costs associated with the abundance of grape products.
        
        Proposed Directions: 
        
        Concept A: Blower; A system of devices attached to the front of the harvester to blow the SLF off of the vines before they can enter the harvester. This could be similar to the end of a car wash, but less strong.
        
        1. Attached in front of the harvester pointing outward toward the grape vines.
        2. A fan would blow a steady stream of air toward the vines, causing the SLF to fly outwards to avoid the irritation.
        3. The flow of air would also stop the SLF from flying into the harvester after they left the vine.
        
        - This is better than the “status quo” of using chemicals to deter or remove SLF from the grapes, since the chemicals may end up contaminating the grape product, making it unusable.
        - This is better than the “status quo” in the way that it doesn’t just scare away bugs but physically moves them to a singular destination and traps them.
        
        Concept B: Vibration Attraction Device; A set of towers vibrating at 60 Hz placed around the field to attract the SLF to liquid chemical traps. 
        
        1. Towers with mechanical vibration devices to attract the SLF.
        2. An electrified outer cage to shock the SLF when they touch the trap.
        3. A container below to catch the dead SLF for easy removal.
        - This is better than the “status quo” because it eliminates SLF year-round without having to continuously spray.
        - This is better than the “status quo”  because it does not require any changes to the harvester and saves money because it is a one-time purchase, not a yearly cost. 
        
        Key risks / unknowns:
        
        1. Damage to grapes/vines.
        - Test by seeing how much wind store-bought grapes can take before falling off the vine.
        2. Lanternflies getting stuck in the blower
        - Test with different geometries of the mechanical design of the tube
        3. Blower’s force is not strong enough to detach lanternflies from grapes
        - Take weight samples of lanternflies and their grab force to calculate the amount of wind force needed to remove them.
        
        Our questions:
        
        1. When dealing with the SLFs, do they often stay on the vine when removing grapes?
        - Decisions Affected: This would change our blower design, as we would need to prototype to make sure that we do not remove grapes as well as the SLFs.
        2. If SLF contamination occurs in grape products, do the machines in the processing facilities need to be shut down and cleaned afterwards?
        - Decisions Affected: While this would not directly affect our decision making, this would clarify the impact on the end user, since we would be more aware of the negative impacts of SLF contamination, particularly in the cost of and time lost to temporarily shutting down facilities.
        3. Is there space in the fields to place a structure such as a tower?
        - Decisions Affected: If we are not able to place something in the field, we may not be able to implement our vibration solution in the currently intended method.
        
        
        Sources Cited:
        
        60 Hz vibration study:
        [Source](https://www.ars.usda.gov/research/publications/publication/?seqNo115=392118 )
        
        SLF needed to contaminate 1 kg slurry:
        Professor Steve Heim on Monday, February 9th during the PM lab section
  - title: Functional Prototype
    content: |
        Team M6: Lanternfly Killers
    
        Team Members: Michelle Paszek, William Wood, Angus Chang, Gurjot Gill, Hayden Bergschneider

        Project Overview:
    
        Our plan is to design and assemble a blower mechanism that will be attached to the front of the grape harvester. This device is meant to cause the Spotted Lanternflies (SLF)  to be blown off of the grape vine before the grapes enter the harvester. According to the client feedback that we received from the experts, this is a solid proposal since harvesters already have fans installed to blow off leaves and MOG (material other than grapes), so additional fans on the front of the harvester is feasible with little risk to the grape vine. SLFs are very flighty insects, so a strong enough fan may motivate them to vacate the row being harvested, and our method avoids additional labor (due to our single time installation and lack of tractor passes needed) and pesticides that could potentially impact the vine.

        Timeline: See Figure 1.

        Choosing Design Tests:
    
        What are you testing?
    
        - the wind pressure/speed
        - shape of the end of funnel 
        - material analysis on the blower -> life cycle
        - amount of force/pattern is required to push off lantern flies
    
        How did you test it?
        - wind speed: anemometer
        - wind pressure: computed from wind velocity, cross section surface area
        - shape of funnel: simulated from softwares (Fusion 360)
        - material analysis: Flex test with hand
        - required force/pattern: modeled using “grapes” simulated with tape and string in addition to a cardboard lanternfly stuck onto the “vine” with tape

        What happened?
        - wind speed: The motor was powered by 5V through Arduino Uno Minima Rev4 and generated 3,500 RPM. We were not able to use an anemometer so we found rpm via marking a fan then taking a slow motion video and counting the fan blades to get roughly 3,500 RPM.
        - wind inlet/outlet velocity relation: See Figure 2 for Calculations
        - shape of funnel: The circular funnel results in an even distribution of pressure. 
        - material analysis: The funnel (PLA) is slightly bendable by hand, which is acceptable for this prototype. However, this would need to be changed for a future prototype/final product.
        - required force/pattern: A sudden burst of air is more effective than a constant stream of air, given the “flighty” nature of the SLFs.
         [Video of Testing via Blowing into the Tube (need to increase wind pressure due to motor, see section on design improvements for details)](https://drive.google.com/file/d/1qdeoUgtQC9aZqwdsxX5bsleziYMTCLx7/view?usp=sharing)



        Design changes/Improvements:
    
        - For better wind pressure/speed, we can add in a gearbox to the motor system to increase the speed of the fan. 
        - We can add holes onto the bottom of the motor housing to increase the airflow and movement for the fan system (fan can draw in air from the outside).
        - Need to increase the height of the side walls for the motor housing so that they encompass the fan blades properly
        - We need to expand the hole sizes on the fan (for shaft), funnel (for tubing), and motor housing (for wire feedthroughs), since the tolerance was initially too small.
        - Add a planetary gearbox to step up speed
        - We can add in tube fittings to connect the nozzles to the tubing for a better connection/seal in order to prevent air from leaking.
        - We can alter the fan blade design to optimize the air flow entering the tubing. Currently, the impeller pump we are using takes in air from the side with more air and pumps it to the other since the blades are symmetric, but the side with more air is the side where we want to push air out, so we should add holes in the back for superior airflow or make the entire back open and make a better funnel system

        Success Criteria:
        - In order to dispel the lantern flies from the intake of the harvester, must be able to blow off lantern flies on the vine. Must be able to blow off adult spotted lanternflies (on average mean weight is .331 grams [Source](https://www.stopslf.org/stopslf/assets/File/Spotted-Lanternfly-RTD-Proceedings-Oct-2024.pdf)).
        - The blower does not deviate more than 10 degrees from its original position when in use. EG firmly mounted and stiff materials for the funnel.
        - The blower will be simplified to 1 unit to attach to the harvester.
        - The blower will be able to stop and start in less than 1 second to blow a quick burst of air, causing the SLF to fly away.

        Components List: See Figure 3.

        Components highlighted in yellow are ordered from McMaster. Components highlighted in blue are 3D printed in the RPL. Components highlighted in grey are sourced from the Taylor Design Studio.

        Design Documentation: See Figure 4.

        Final Product Sketch: See Figure 5.

        Assembly Instructions: See Figure 6.

    
    images:
      - path: "/assets/images/ODP_F1.jpg"
        alt: "Timeline"
        class: "project-image"
      - path: "/assets/images/ODP_F2.jpg"
        alt: "Wind Inlet/Outlet Velocity Ratios"
        class: "project-image"
      - path: "/assets/images/ODP_F3.jpg"
        alt: "Components List"
        class: "project-image"
      - path: "/assets/images/ODP_F4.jpg"
        alt: "CAD Design Documentation"
        class: "project-image"
      - path: "/assets/images/ODP_F5.jpg"
        alt: "Final Design Sketch"
        class: "project-image"
      - path: "/assets/images/ODP_F6.jpg"
        alt: "Assembly Instructions"
        class: "project-image"


  - title: Client Report
    content: |
    
        SLF Mechanical Repellant from Grape Harvester
    
        Team Name: Lanternfly Killers
    
        Team Members: Michelle Paszek, Will Wood, Angus Chang, Gurjot Gill, Hayden Bergschneider
    
        Client(s): Cornell CALS Extension / E\&J Gallo Winery / National Grape
    
        
        Context and Problem Statement:
        
        The problem we chose to focus on was stopping the spotted lantern flies from entering the harvester and tainting the product. Just 1 to 2 SLF’s in a kilogram grape slurry can taint the batch. By choosing to stop them before the harvesting process, we also stop the need to sort out SLF’s from the harvest and prevent any damage they may cause.
    
        
        Final Prototype and Application:
        
        We built a blower system to be mounted onto a Grape harvester. The blower system would be used to send air in bursts to simultaneously agitate the SLF on the vine and physically blow them off the vines without ejecting too much air, keeping the grapes on the vine. This would be a low cost, low effort, and low maintenance device to be easily mounted onto the grape harvester which would not interfere with the main use of the harvester itself or with the operator using it.
    
        
        Testing and Results:
        
        We were able to successfully meet our three criteria for success:
        
        Wind speed: We used an anemometer to find the speed of airflow output from our device. We set up two fixed sensors at the outlet and take the average of the measured wind velocity. We also ran wind tunnel simulation via Simscale on the funnel to estimate the aerodynamic properties.
        - Inlet Velocity:  3.1 m/s
        - Max Speed:  10.28 m/s
        - Max Pressure: 191.18 Pa
        - Dynamic Pressure: 183.75 Pa
        - The wind speed was 10.28 m/s which was able to displace 23,743 cm3/s which is more than our value of 1,000 cm3/s

    
        Material Strength: Motor housing integrity was testing using force gauges, showing completely elastic deformation after 177 Newtons of force was applied. Due to lab limitations, we were not able to reach the breaking point of material. Further research showed that PLA has a tensile strength of 40-60 MPa. Our PLA motor setup is able to handle the estimated vibration force of 150 Newtons, similar to the forces the system would experience while in use.
    
        Knocking Flies off: We fabricated a mock grape vine and lanternfly setup, testing the effectiveness of the nozzle shape. It took ~1-2 sec. of blowing air to knock off the lanternflies, demonstrating the viability of our product. [Testing Success Criteria of Blowing Off Lanternflies](https://drive.google.com/file/d/1qdeoUgtQC9aZqwdsxX5bsleziYMTCLx7/view?usp=sharing).
    
    
    
        Prototype and Testing Details:
        
        3/31/26:
        	Our initial design was not able to produce enough thrust on its own to be able to blow off the flies. We fixed this by supplying a higher voltage to the motor and also adjusting the housing to allow for more airflow into the device itself. We also adjusted the fan size and specs to allow for greater airflow into the device. We were able to build our testing apparatus and prove that air can blow off lanternflies showing our proposed idea is feasible, but we still hadn’t ironed out our design.
        
        4/6/26:
        	We began to overhaul our entire design and remake the system to fit these new design ideas of different directional fan-blades and more airflow getting to the fan blade. We also platted around with the idea of implementing a gear box, but we determined that they weren’t necessary for our design considering the fan speeds we were able to reach. Not much physically built.
        
        4/13/26:
        	We continued to prototype our device by modeling the entire mechanism in Fusion to be 3D printed and ordered the parts as well as specc’d the entire system for the power circuit.
        
        4/20/26:
        	We constructed our final prototype by installing the directional fan blade, the motor, and the new motor housing and funnel. After fully constructing the final prototype, we tested the blade turning on and off using an arduino, the wind speed using an anemometer, and the material strength using a spring force sensor.
    
        
        
        Conclusion and Recommendation:
    
        We have determined that this is a viable product based on our tests, both in its effectiveness and its low cost of $54.74. Next steps would be further testing to determine if it is effective on a living lanternfly and not just our model. Also testing on a moving grape in a combine harvester. All we have proven is that this product is viable and not that it is inherently usable in its current state. It would also be beneficial to build a much larger fan system (maybe utilize compressed air) and have it hooked up to multiple blowers and see how that fairs.


        References:
    
        SLF needed to contaminate 1 kg slurry: Professor Steve Heim on Monday, February 9th during the PM lab section

        [Mean Weight of Lanternflies](https://www.stopslf.org/stopslf/assets/File/Spotted-Lanternfly-RTD-Proceedings-Oct-2024.pdf).
    
        [Properties of PLA](https://plamfg.com/blog/properties-of-polylactic-acid/).

        




    
    images:


    

  - title: Final Project Poster
    images:
      - path: "/assets/images/MAE2250_Final_Poster"
        alt: "Final Poster"
        class: "project-image"


---  









