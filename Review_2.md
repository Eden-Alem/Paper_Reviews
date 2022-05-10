# Review 2
## Meltdown: Reading Kernel Memory from User Space
By Moritz Lipp, Michael Schwarz, Daniel Gruss, Thomas Prescher, Werner Haas, Anders Fogh, Jann Horn, Stefan Mangard, Paul Kocher, Daniel Genkin, Yuval Yarom, Mike Hamburg

### What is the problem? 
- Exploits side effects of out-of-order execution (necessary performance feature in a wide range of modern processors) to read arbitrary kernel memory locations accessing personal information (breaks security guarantees of address space isolation).

### Summary / Contribution [Up to 3 sentences]

### Key Insights[Up to 2 insights]
- Vulnerable out-of-order processors allow unprivileged user processes to load data from a privileged (kernel/physical) address into a temporary CPU register and even further performs computations based on the register value.

### Notable design details/strengths [Up to 2 details/strengths]

### Limitations/Weaknesses [up to 2 weaknesses]

### Summary of Key Results [Up to 3 results]

### Open Questions[ Where to go from here?]


Memory isolation: feature of OSes that ensure user programs don't access memory of eachother's or the kernel memory. The isola
