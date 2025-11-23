> Jafarzadeh, N., Eizenga, J. M., & Paten, B. (2025). **An Efficient Graph Algorithm for Diploid Local Ancestry Inference**. 

[doi: https://doi.org/10.1101/2025.07.05.662656](https://www.biorxiv.org/content/10.1101/2025.07.05.662656v1)



## 📂 Repository Contents

### 1. [01_SP_Bubble_Validation.ipynb](01_SP_Bubble_Validation.ipynb)
Validation on **Series–Parallel (SP)** graphs.

This notebook demonstrates:
- Construction of SP input examples 
- Identification of P-nodes in the SPQR decomposition
- Enumeration of disjoint path pairs at each P-node
- Diploid graph expansion driven by P-node structures

---

### 2. [02_NonSP_Complex_Validation.ipynb](02_NonSP_Complex_Validation.ipynb)
Validation on **Non-Series–Parallel (Non-SP)** graphs.

This notebook includes:
- Construction of input graphs containing non-SP structures
- Identification of R-nodes and extraction of W-motifs using the complexity graph \(C(G)\)
- Enumeration of disjoint path pairs at W-nodes
- Diploid graph expansion driven by both P-node and W-node structures




## 🚀 Key Results

We validated the algorithm on large, randomized complex graphs containing both simple bubbles and complex bridges.

* ⚡ **Efficiency:** The diploid graph construction demonstrated linear scalability across all topologies.

  * On complex graphs mixing linear backbone, bubbles, and bridges, we observed an expansion factor of **~1.6x**.

  * On graphs consisting entirely of nested structural variations (pure SP "bubbles"), the expansion factor approached **~1.9x**.

    * **Comparison:** This linear scaling drastically outperforms standard theoretical models, **avoiding** both the quadratic growth ($O(N^2)$) of Cartesian products and the combinatorial explosion ($\binom{n}{2}$) of naive haplotype path pairing.

* ✅ **Accuracy:** The node and edge counts of the resulting graphs **matched theoretical topological predictions** derived from the SPQRW decomposition, verifying that the algorithm identifies disjoint paths **without introducing redundancy**.


## 🛠️ Dependencies
- Python 3.x
- SageMath (SPQR-tree decomposition)
- libbdsg (vg’s graph backend; used to load GFA files)


