# References and Resources
### Mathematical Modeling in Biology — MSc Bioinformatics 2026

---

## Core Papers — Boolean Modeling

These are the primary research papers directly relevant to the lecture and practical content. 

1. **Wang & Albert (2012)** — Boolean modeling in systems biology: an overview of methodology and applications. *Physical Biology* 9, 055001.
[doi:10.1088/1478-3975/9/5/055001](https://doi.org/10.1088/1478-3975/9/5/055001)
> Comprehensive review of Boolean network methodology and its applications across gene regulation, signaling, and cell fate. **Start here** if you are new to Boolean modeling.

2. **Schwab, Kühlwein, Ikonomi et al. (2020)** — Concepts in Boolean network modeling: What do they all mean? *Computational and Structural Biotechnology Journal* 18, 571–582.
[doi:10.1016/j.csbj.2020.03.001](https://doi.org/10.1016/j.csbj.2020.03.001)
> Clarifies terminology and concepts in Boolean modeling — attractors, basins, update schemes, robustness — with worked examples. Highly recommended alongside the lecture slides.

3. **Veliz-Cuba & Stigler (2011)** — Boolean models can explain bistability in the lac operon. *Journal of Computational Biology* 18(6), 783–794.
[Link](https://journals.sagepub.com/doi/abs/10.1089/cmb.2011.0031)
> The original Boolean model of the *E. coli* lac operon used in `lac_operon_boolean_dynamics.Rmd`. Read this to understand the network structure and update rules before running the practical.

4. **Montalva-Medel, Ledger, Ruz & Goles (2021)** — Lac operon Boolean models: Dynamical robustness and alternative improvements. *Mathematics* 9(6), 600.
[Link](https://www.mdpi.com/2227-7390/9/6/600)
> Extends and refines the Veliz-Cuba & Stigler model. **Required reading for the practical exam** — the Improved Original Model (Figure 9) and Improved Reduced Model (Figure 10) that students implement are described here. Table 6 is the target for result reproduction.

5. **Ozbudak et al. (2004)** — Multistability in the lactose utilization network of *Escherichia coli*. *Nature* 427, 737–740.
[PubMed](https://www.ncbi.nlm.nih.gov/pubmed/14973486)
> The experimental paper whose observations the lac operon Boolean models are built to reproduce. Read this to understand what bistability looks like in a real biological system and why it was surprising.

6. **Albert, Thakar et al. (2008)** — Boolean network simulations for life scientists. *Source Code for Biology and Medicine* 3, 16.
> A practical guide to implementing and interpreting Boolean simulations, written for biologists rather than mathematicians. Useful companion to the BoolNet practical files.

---

## Core Papers — Biological Applications of Boolean Modeling

7. **Zhang et al. (2008)** — Network model of survival signaling in large granular lymphocyte leukemia. *PNAS* 105(42), 16308–16313.
[doi:10.1073/pnas.0806447105](https://doi.org/10.1073/pnas.0806447105)
> Boolean model of T-LGL leukemia survival signaling discussed in Lecture 2. Demonstrates how Boolean models identify therapeutic targets in cancer.

8. **Mendoza & Xenarios (2006)** — A method for the generation of standardized qualitative dynamical systems of regulatory networks. *Theoretical Biology and Medical Modelling* 3, 13.
> Covers methods for constructing Boolean regulatory networks from experimental evidence — directly relevant to the 6-step workflow taught in Lecture 2.

9. **Kauffman (1969)** — Metabolic stability and epigenesis in randomly constructed genetic nets. *Journal of Theoretical Biology* 22(3), 437–467.
> The foundational paper that introduced Boolean networks as models of gene regulation. Short and historically important.

---

## Textbooks

### Directly Relevant

10. **Alon, U. (2007)** — *An Introduction to Systems Biology: Design Principles of Biological Circuits.* Taylor & Francis. ISBN: 9781584886426.
> Highly readable and biologically grounded. Covers network motifs, feedback loops, and the design logic of gene regulatory circuits. Strongly recommended as a companion to Lectures 1 and 2.

11. **Klipp, Liebermeister, Wierling & Kowald (2016)** — *Systems Biology: A Textbook*, 2nd Edition. Wiley-Blackwell. ISBN: 978-3-527-33636-4.
> Comprehensive graduate-level textbook covering ODE-based modeling, stoichiometric analysis, and Boolean networks. Use as a reference for topics beyond the scope of this course iteration.

12. **Covert, M.W. (2015)** — *Fundamentals of Systems Biology: From Synthetic Circuits to Whole-cell Models.* CRC Press. ISBN: 9781138582927.
> Bridges mathematical modeling and synthetic biology. Good background reading for understanding how Boolean models relate to ODE and constraint-based approaches.

13. **Palsson, B.Ø. (2011)** — *Systems Biology: Simulation of Dynamic Network States.* Cambridge University Press. ISBN: 9781139495424.
> Focuses on dynamic simulation of biological networks. More mathematically demanding but useful for students wishing to go beyond Boolean models.

14. **Haefner, J.W. (2005)** — *Modeling Biological Systems: Principles and Applications.* Springer. ISBN: 978-0-387-25011-3.
> Broad and accessible introduction to biological modeling across ecology, physiology, and molecular systems. Good for understanding the modeling process described in Lecture 1.

---

## Software Documentation

### BoolNet (R)

- **BoolNet CRAN vignette** — Full package documentation with worked examples:
[https://cran.r-project.org/web/packages/BoolNet/vignettes/BoolNet_package_vignette.pdf](https://cran.r-project.org/web/packages/BoolNet/vignettes/BoolNet_package_vignette.pdf)

- **BoolNet Tutorial (Nanjing)** — Step-by-step tutorial covering network loading, simulation, attractor analysis, and visualisation:
[https://sysbio.uni-ulm.de/tutorial-nanjing/nanjing_tutorial.pdf](https://sysbio.uni-ulm.de/tutorial-nanjing/nanjing_tutorial.pdf)

### BooleanNet (Python)

- **BooleanNet GitHub repository** — Python implementation of Boolean network simulation supporting synchronous, asynchronous, and ranked-asynchronous update schemes:
[https://github.com/ialbert/booleannet](https://github.com/ialbert/booleannet)

### Boolean Models in SBML

- **biodivine Boolean models repository** — Curated collection of published Boolean network models in SBML format, including the lac operon model used in this course:
[https://github.com/sybila/biodivine-boolean-models](https://github.com/sybila/biodivine-boolean-models/tree/02763132a675cba69adc8bd3d982da260397a560)

---

## Online Courses and Tutorials

- **EBI: Mathematical Modelling for Biologists** — Introductory online course from the European Bioinformatics Institute covering what mathematical models are, how they are built, and how they are used:
[https://www.ebi.ac.uk/training/online/courses/mathematical-modelling-biologists/](https://www.ebi.ac.uk/training/online/courses/mathematical-modelling-biologists/what-is-a-mathematical-model/)

- **UBC MATH360: Mathematical Modeling Process** — Clear, well-structured overview of the modeling process, from problem definition to validation:
[https://ubcmath.github.io/MATH360/process/overview.html](https://ubcmath.github.io/MATH360/process/overview.html)

- **Boolean Network Basics (Clemson University lecture slides)** — Concise and mathematically clear slides on Boolean network fundamentals — state space, update rules, attractors:
[https://www.math.clemson.edu/~macaule/classes/f24_math9850/slides/part2_boolean-basics.pdf](https://www.math.clemson.edu/~macaule/classes/f24_math9850/slides/part2_boolean-basics.pdf)

- **Biological Modeling: Gray-Scott Reaction-Diffusion** — Interactive introduction to reaction-diffusion modeling; useful for intuition about continuous spatial models beyond the scope of this course:
[https://biologicalmodeling.org/prologue/gray-scott](https://biologicalmodeling.org/prologue/gray-scott)

- **3MC Mathematical Modelling in Biology (Julien Arino)** — Graduate-level course materials on mathematical modeling in biology including ODEs, stochastic models, and epidemiological frameworks:
[https://julien-arino.github.io/3MC-mathematical-modelling-in-biology/](https://julien-arino.github.io/3MC-mathematical-modelling-in-biology/)

---

## Video Lectures

- **Reka Albert — Network-based dynamic modeling of biological systems: toward understanding and control**
ISCBacademy Webinar hosted by SysMod. Excellent overview of Boolean and network modeling in biology by one of the leading researchers in the field.
[https://www.youtube.com/watch?v=f-kxfaVCzlg](https://www.youtube.com/watch?v=f-kxfaVCzlg)

- **Dr. Ganesh Vishwanathan — Boolean Modeling lecture**
[https://www.youtube.com/watch?v=2v39W8XU6sI](https://www.youtube.com/watch?v=2v39W8XU6sI)

---

*Last updated: April 2026*