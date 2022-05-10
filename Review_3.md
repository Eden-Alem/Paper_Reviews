# Review 3
## A2 Analog Malicious Hardware
By Kaiyuan Yang, Mathew Hicks, Qing Dong, Todd Austin, Dennis Sylvester

### What is the problem? 
Construct an attack that is *stealthy* (hides from dynamic analysis;) and *small* (if reduced to once cell, its placed in a processor with hundreds or thousands of cells that look the same; hard to spot the attack using visual inspection), *controllable by an attacker*.

**Side note:**  **Dynamic + Static analysis** catches attacks that are small cause they are always on(issue test cases that expose malice, tested in functional verification). **Visual Inspection Side Channels** catches attacks that are large cause they use additional logic to hide from dynamic analysis.

### Summary / Contribution [Up to 3 sentences]
- 

### Key Insights [Up to 2 insights]

### Notable design details/strengths [Up to 2 details/strengths]
- Since attacking small capacitors charge quickly (trigger will get deployed in one clock cycle, noticable via side channels) and large capacitors indue current spikes(huge current taking a lot of power from the voltage rail to fill this large capacitor), it makes use of charge sharing, conneting the small and relatively larger capacitor together to a single voltage.
- One of the values of a capacitor, is that it forgets bad programming cause its leaked. 


Limitations/Weaknesses [up to 2 weaknesses]

Summary of Key Results [Up to 3 results]

Open Questions[ Where to go from here?]
