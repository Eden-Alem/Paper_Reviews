# Review 3
## A2 Analog Malicious Hardware
By Kaiyuan Yang, Mathew Hicks, Qing Dong, Todd Austin, Dennis Sylvester

### What is the problem? 
Construct an attack that is *stealthy* (hides from dynamic analysis;) and *small* (if reduced to once cell, its placed in a processor with hundreds or thousands of cells that look the same; hard to spot the attack using visual inspection), *controllable by an attacker*.
 
### Summary / Contribution
- In mal research, a conventional attack where a rare, but attacker controllable event is triggered and then the counter based trigger sets off where it could count upto 12300 times before actually launching the attack. And then this is compressed down into Analog circuits (which makes the attack stealthy as it concerns visual inspection)
- Privilege escalatuin attacks are possible (moving from user mode to supervisor/privileged mode) by making use of the information gained from observation that processors reset in most privilege mode and then they gradually de-escalate privelege as they boot (hardware's reset level is in most privilege)
- To mitigate after the attack is done, side channels are not going to be of help since they're all the same. So maybe we can check the equivalency of what we sent to be fabricated in the first place vs. what we got from them (although checking won't be of help in the future as work is being done to reduce that one cell to zero cells).

### Key Insights
- **Dynamic + Static analysis** catches attacks that are small cause they are always on(issue test cases that expose malice, tested in functional verification). **Visual Inspection Side Channels** catches attacks that are large cause they use additional logic to hide from dynamic analysis. A2 is hidden from post-fab testing (testing after fabrication)
- In processors (even intel and AMD class processors) about 20-30% of the chip area is unused (was trivial to fit in one cell when most of the area if zoomed in was unused); implanting A2 into an existing chip layout

### Notable design details/strengths
- Since attacking small capacitors charge quickly (trigger will get deployed in one clock cycle, noticable via side channels) and large capacitors indue current spikes(huge current taking a lot of power from the voltage rail to fill this large capacitor), it makes use of charge sharing, conneting the small and relatively larger capacitor together to a single voltage.
- One of the values of a capacitor, is that it forgets bad programming cause its leaked. So we need like 200 instructions of the same (200 division by zeros) in a row simultaneously without anything between that (intercepting this), thus reducing the probability or triggering the attack unknowingly or during testing.

### Limitations/Weaknesses

### Summary of Key Results [Up to 3 results]


### Open Questions (Where to go from here?)
Effective mitigation techniques after the attack has took place?
