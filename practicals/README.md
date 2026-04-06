# Code Files

## demo_example1.Rmd — Toggle-Switch Boolean Network (Demo)

An introductory, fully worked demonstration of Boolean network simulation using the BoolNet package. The network models a 5-node toggle-switch circuit consisting of two fixed input nodes (Sg and Cn) and three dynamic nodes (A, B, C) that are updated synchronously at each time step.

**Boolean update rules:**
```
Sg* = Sg        (fixed input — Signal, e.g. growth factor)
Cn* = Cn        (fixed input — Condition, e.g. nutrient availability)
A*  = Sg OR NOT B
B*  = Cn AND NOT A
C*  = A OR B
```

**What the script covers:**
- Loading and printing the network structure
- Simulating all 4 input combinations (Sg=1/0, Cn=1/0) over time using synchronous updating
- Plotting heatmaps of node states across time steps (pheatmap)
- Plotting state transition sequences from each initial condition (plotSequence)
- Computing all attractors exhaustively and their basins of attraction
- Drawing the full state transition graph

**Biological motivation:** Nodes A and B form a mutual inhibition (toggle-switch) motif — the same circuit architecture that underlies Th1/Th2 immune cell fate switching, epithelial-to-mesenchymal transition (EMT) in cancer biology, and classic bistable switches in synthetic biology (Gardner et al. 2000, *Science*).

---

## lac_operon_boolean_dynamics.Rmd — Lac Operon Boolean Model

A complete simulation of the Boolean network model of the *Escherichia coli* lac operon, based on the published model of Veliz-Cuba & Stigler (2011) and extended following Montalva-Medel et al. (2021). **This file is the starting point for the Practical Exam.** Run all code and make sure you understand Models 1 and 2 before attempting the exam tasks.

**Biological question:** Under what combinations of external glucose and lactose availability does *E. coli* switch the lac operon ON, OFF, or exhibit bistability — where either state is stable depending on the cell's history?

**Model inputs (environmental conditions — fixed during each simulation):**

| Node | Meaning |
|------|---------|
| `v_Ge` | Extracellular glucose (1 = high, 0 = low/absent) |
| `v_Le` | Extracellular lactose at high concentration |
| `v_Lem` | Extracellular lactose at medium concentration |

**Model output (operon phenotype):**
- Operon **ON**: `v_M = 1`, `v_P = 1`, `v_B = 1`
- Operon **OFF**: `v_M = 0`, `v_P = 0`, `v_B = 0`

**Six environmental conditions simulated:**

| Condition | Glucose | Lactose | Expected operon state |
|-----------|---------|---------|----------------------|
| (i) | Low | Low | OFF |
| (ii) | High | Low | OFF |
| (iii) | Low | Medium | **Bistable** (OFF or ON) |
| (iv) | High | Medium | OFF |
| (v) | Low | High | ON |
| (vi) | High | High | OFF |

**What the script covers:**
- Loading the SBML model (Veliz-Cuba & Stigler 2011) from the provided `.sbml` file
- Visualising the network wiring diagram
- Simulating and plotting all 6 environmental conditions
- Computing all attractors by exhaustive search
- Demonstrating bistability for condition (iii): finding both stable fixed points and their basin sizes
- Extending the model to remove catabolite repression (`v_C = 1`) and comparing attractor outcomes across all 6 conditions

---

# Software Requirements

All practical files use **R**. Install the following packages before running any `.Rmd` file:

```r
install.packages("BoolNet")
install.packages("pheatmap")
install.packages("igraph")
```

The file `lac_operon_boolean_dynamics.Rmd` requires the SBML model file `lac-operon-model_corrected.sbml`, which is included in the `practicals/` folder of this repository. In RStudio, set your working directory to the `practicals/` folder before knitting (Session → Set Working Directory → To Source File Location).

**Recommended R version:** ≥ 4.2.0  
**Recommended IDE:** RStudio — knit to HTML for submission
