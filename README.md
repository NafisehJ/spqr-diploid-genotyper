> Jafarzadeh, N., Eizenga, J. M., & Paten, B. (2025). **An Efficient Graph Algorithm for Diploid Local Ancestry Inference**. 

[doi: https://doi.org/10.1101/2025.07.05.662656](https://www.biorxiv.org/content/10.1101/2025.07.05.662656v1)



## 📂 Repository Contents

This repository contains the reference implementation using **SageMath** and **Jupyter notebooks** reproducing the validation experiments described in the paper.

### 1. [01_SP_Bubble_Validation.ipynb](01_SP_Bubble_Validation.ipynb)

**Validation on Series-Parallel (SP) Graphs.**

This notebook demonstrates the core concept of the algorithm using simple graph structures:

* **Decomposition:** Identifies standard genomic "bubbles" as **P-nodes** (Parallel components) in the SPQR tree.
* 
* **Diploid Construction:** Validates the linear expansion of the diploid graph size relative to the input haploid graph.


### 2. [02_NonSP_Complex_Validation.ipynb](02_NonSP_Complex_Validation.ipynb)

**Handling Non-Series-Parallel (Non-SP) Complex Variation.**
This notebook covers the advanced contributions of the paper regarding complex topology:

* **W-Motif Identification:** Demonstrates the detection of **W-nodes**, extracted from **R-nodes** in standard SPQR trees, and upgrades them to **W-nodes** using the complexity graph $C(G)$ method.
* 
* **Disjoint Path Extraction:** Visualizes the extraction of "crossing" path pairs (diplotypes) through complex snarls.
* 
* **Scalability Stress-Test:** Generates large synthetic chromosomes with mixed P and W structures (30+ segments) to confirm the algorithm maintains efficient linear scaling even with complex structural variations.


## 🚀 Key Results

We validated the algorithm on large, randomized complex graphs containing both simple bubbles and complex bridges.

* ⚡ **Efficiency:** The diploid graph construction demonstrated linear scalability across all topologies.

  * On complex graphs mixing linear backbone, bubbles, and bridges, we observed an expansion factor of **~1.6x**.

  * On graphs consisting entirely of nested structural variations (pure SP "bubbles"), the expansion factor approached **~1.9x**.

    * **Comparison:** This linear scaling drastically outperforms standard theoretical models, **avoiding** both the quadratic growth ($O(N^2)$) of Cartesian products and the combinatorial explosion ($\binom{n}{2}$) of naive haplotype path pairing.

* ✅ **Accuracy:** The node and edge counts of the resulting graphs **matched theoretical topological predictions** derived from the SPQRW decomposition, verifying that the algorithm identifies disjoint paths **without introducing redundancy**.


## 🛠️ Dependencies
* **Python 3.x**
* **SageMath**: Required for the underlying graph theory primitives and Triconnectivity/SPQR decomposition algorithms.


