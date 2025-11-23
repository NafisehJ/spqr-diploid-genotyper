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



## 🛠️ Dependencies
- Python 3.x
- SageMath (SPQR-tree decomposition)
- libbdsg (vg’s graph backend; used to load GFA files)


