> Jafarzadeh, N., Eizenga, J. M., & Paten, B. (2025). **An Efficient Graph Algorithm for Diploid Local Ancestry Inference**. 
[doi: https://doi.org/10.1101/2025.07.05.662656](https://www.biorxiv.org/content/10.1101/2025.07.05.662656v1)



## 📂 Repository Contents

This repository contains the reference implementation using **SageMath** and **Jupyter notebooks** reproducing the validation experiments described in the paper.

### 1. [01_SP_Bubble_Validation.ipynb](01_SP_Bubble_Validation.ipynb)
**Validation on Series-Parallel (SP) Graphs.**
This notebook demonstrates the core concept of the algorithm using simple graph structures:
* **Decomposition:** Identifies standard genomic "bubbles" as **P-nodes** (Parallel components) in the SPQR tree.
* **Diploid Construction:** Validates the linear expansion formula for SP graphs: $V_{diploid} = V_{input} + 2|P|$.

### 2. [02_NonSP_Complex_Validation.ipynb](02_NonSP_Complex_Validation.ipynb)
**Handling Non-Series-Parallel (Non-SP) Complex Variation.**
This notebook covers the advanced contributions of the paper regarding complex topology:
* **W-Motif Identification:** Demonstrates the detection of **W-nodes**, extracted from **R-nodes** in standard SPQR trees, and upgrades them to **W-nodes** using the complexity graph $C(G)$ method.
* **Disjoint Path Extraction:** Visualizes the extraction of "crossing" path pairs (diplotypes) through complex snarls.
* **Scalability Stress-Test:** Generates large synthetic chromosomes with mixed P and W structures (30+ segments) to validate the generalized expansion efficiency: 
    $$|V_{diploid}| = |V_{input}| + 2(|P| + |W|)$$

## 🚀 Key Results

We validated the algorithm on large, randomized complex graphs containing both simple bubbles and complex bridges.

* ⚡ **Efficiency:** In a representative example containing dense structural variation, the algorithm produced a diploid graph with an expansion factor of approximately **1.6x** relative to the haploid input size. This **linear scaling** is significantly more efficient than standard theoretical approaches, **avoiding** both the quadratic growth ($O(N^2)$) of a Cartesian product and the combinatorial explosion ($\binom{n}{2}$) of naive haplotype path pairing.

* ✅ **Accuracy:** The node and edge counts of the resulting graphs **matched theoretical topological predictions** derived from the SPQRW decomposition, verifying that the algorithm identifies disjoint paths **without introducing redundancy**.


## 🛠️ Dependencies
* **Python 3.x**
* **SageMath**: Required for the underlying graph theory primitives and Triconnectivity/SPQR decomposition algorithms.


