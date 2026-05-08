# hodge-rank-obstructions

**Paper 2 of 3: Rank Obstructions for the Hodge Recurrence Test**

**Main Result**: For CM abelian varieties with CM field degree p≥2, the linear recurrence test from Paper 1 fails. We construct 200 explicit counterexamples where rank = 15 > 10 = g.

**Key Finding**: The recurrence bound `rank ≤ g` holds iff p=1. When p≥2, rank can grow to p·g.

### Quick start
1. Install SageMath 10.4+
2. Run: `sage rank_obstruction.sage` 
3. Output: `Found 200 counterexamples. Max rank: 15, dim: 10. Ratio: 1.5`

### Files
- `rank_obstruction.tex`: 6-page paper with counterexamples
- `rank_obstruction.sage`: Code generating 200 examples with rank > g
- `counterexamples.csv`: LMFDB labels + ranks for 200 cases

### Companion Papers
- **Paper 1**: `hodge-cm-recurrence` — Test works for p=1
- **Paper 3**: `hodge-zoe-invariant` — Zoe invariant fixes test for p≥2

**License**: MIT
   # The Hodge Conjecture on CM Abelian Varieties: A Computational Trilogy
   
   [[DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20087650.svg)](https://doi.org/10.5281/zenodo.20087650)
   
   **Paper 1**: [Computable Linear Recurrence Test](https://github.com/DavidFox998/hodge-cm-recurrence)
   
   **Paper 2**: [Rank Obstructions from the Zoe Invariant](https://github.com/DavidFox998/hodge-zoe-rank-obstructions)
   
   **Paper 3**: [Tensor Rank Criteria for (p,p)-Classes](https://github.com/DavidFox998/tensor-rank-criteria-abelian-varieties)
   
   Verifies the Hodge conjecture for all 339 CM abelian varieties in the LMFDB.
## License

**Paper**: [CC BY 4.0](./LICENSE-CC-BY-4.0) 

**Code**: [MIT License](./LICENSE)
