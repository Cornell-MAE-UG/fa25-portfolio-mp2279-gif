---
layout: accordion
title: Open Design Project
description: Class Project, Intro to Mechanical Design
image: /assets/images/ODP_main.png

accordion:
  - title: Client Outline & Pitch
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
        https://www.ars.usda.gov/research/publications/publication/?seqNo115=392118 
        
        SLF needed to contaminate 1 kg slurry:
        Professor Steve Heim on Monday, February 9th during the PM lab section
  - title: Functional Prototype
    content: |
        Team M6: Lanternfly Killers
    
        Team Members: Michelle Paszek, William Wood, Angus Chang, Gurjot Gill, Hayden Bergschneider

        Project Overview:
    
        Our plan is to design and assemble a blower mechanism that will be attached to the front of the grape harvester. This device is meant to cause the Spotted Lanternflies (SLF)  to be blown off of the grape vine before the grapes enter the harvester. According to the client feedback that we received from the experts, this is a solid proposal since harvesters already have fans installed to blow off leaves and MOG (material other than grapes), so additional fans on the front of the harvester is feasible with little risk to the grape vine. SLFs are very flighty insects, so a strong enough fan may motivate them to vacate the row being harvested, and our method avoids additional labor (due to our single time installation and lack of tractor passes needed) and pesticides that could potentially impact the vine.

        Timeline:

        ![Timeline](/assets/images/ODP_Timeline.png)

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
        	- required force/pattern: real life simulation with an insect (lantern fly)
        		- modeled using “grapes” simulated with tape and string in addition to a cardboard lanternfly stuck onto the “vine” with tape

        What happened?
        - wind speed: The motor was powered by 5V through Arduino Uno Minima Rev4 and generated 3,500 RPM. We were not able to use an anemometer so we found rpm via marking a fan then taking a slow motion video and counting the fan blades to get roughly 3,500 RPM.
        - wind inlet/outlet velocity relation: See calculations below


        - shape of funnel: The circular funnel results in an even distribution of pressure. 
	    - material analysis: The funnel (PLA) is slightly bendable by hand, which is acceptable for this prototype. However, this would need to be changed for a future prototype/final product.
      	- required force/pattern: A sudden burst of air is more effective than a constant stream of air, given the “flighty” nature of the SLFs. 



        Design changes/Improvements
        - For better wind pressure/speed, we can add in a gearbox to the motor system to increase the speed of the fan. 
        - We can add holes onto the bottom of the motor housing to increase the airflow and movement for the fan system (fan can draw in air from the outside).
        - Need to increase the height of the side walls for the motor housing so that they encompass the fan blades properly
        - We need to expand the hole sizes on the fan (for shaft), funnel (for tubing), and motor housing (for wire feedthroughs), since the tolerance was initially too small.
        - Add a planetary gearbox to step up speed
        - We can add in tube fittings to connect the nozzles to the tubing for a better connection/seal in order to prevent air from leaking.
        - We can alter the fan blade design to optimize the air flow entering the tubing. Currently, the impeller pump we are using takes in air from the side with more air and pumps it to the other since the blades are symmetric, but the side with more air is the side where we want to push air out, so we should add holes in the back for superior airflow or make the entire back open and make a better funnel system	


---  









