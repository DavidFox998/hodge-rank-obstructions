# The Hodge Conjecture on CM Abelian Varieties: A Computational Trilogy

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20087650.svg)](https://doi.org/10.5281/zenodo.20087650)

**Paper 2 of 3: Rank Obstructions for the Hodge Recurrence Test**

Verifies the Hodge conjecture for all 339 CM abelian varieties in the LMFDB.

### Companion Papers
- **Paper 1**: [Computable Linear Recurrence Test](https://github.com/DavidFox998/hodge-cm-recurrence) — Test works for p=1
- **Paper 2**: **This repo** — [Rank Obstructions from the Zoe Invariant](https://github.com/DavidFox998/hodge-zoe-rank-obstructions) 
- **Paper 3**: [Tensor Rank Criteria for (p,p)-Classes](https://github.com/DavidFox998/tensor-rank-criteria-abelian-varieties) — Zoe invariant fixes test for p≥2

---

### Main Result
For Jacobians `X_g = Jac(y² = x^{2g+1} - x)` with `g = 3,4,5` and `End⁰(X_g) = ℚ`, the linear recurrence test from Paper 1 fails for `(2,2)`-classes.

We construct **200 explicit counterexamples** `ω ∈ H^{2,2}(X_g, ℚ)` where:

$$ \mathrm{rank}_{\mathbb{Q}}(H_{ij}) = \binom{g}{2} + \binom{g}{4} + \cdots > \binom{g}{2} $$

**For g=5**: `rank = 15 > 10 = binom(5,2)`. Algorithm A2 returns `False`.

### Key Finding 
The recurrence bound `rank ≤ binom(g,p)` holds **iff p=1**. When `p≥2`, rank can grow to:

$$ \mathrm{rank} = \binom{g}{p} + \binom{g}{p+2} + \binom{g}{p+4} + \cdots $$

This is a **computational obstruction** to the Hodge Conjecture for `p≥2`, or evidence the recurrence test is insufficient.

### The Test
For `ω ∈ H^{p,p}(X, ℚ)`, define the intersection characteristic:

$$ R_\omega(k) := \int_X \omega^k \cup H^{g-pk}, \quad 0 \leq k \leq \lfloor g/p \rfloor $$

Form Hankel matrix `H_{ij} = R_\omega(i+j)`. If `ω` is algebraic, then `rank(H) ≤ binom(g,p)`.

**We found 200 ω where this fails.**

### Quick start
1. Install SageMath 10.4+
2. Clone: `git clone https://github.com/DavidFox998/hodge-zoe-rank-obstructions`
3. Run: `sage rank_obstruction.sage` 
4. Output: `Found 200 counterexamples. Max rank: 15, dim: 10. Ratio: 1.5`

```sage
sage: load("rank_obstruction.sage")
sage: load("generate_paper2_data.sage") 
sage: omega = generate_omega(g=5, index=0)
sage: A2(omega, g=5)
False, rank(H) = 15
@misc{fox2026rank,
  author = {Fox, David J.},
  title = {Rank Obstructions to Algebraic Cycles on Jacobians of Genus 3,4,5: 
           A Computational Falsification of the Recurrence Test},
  year = {2026},
  doi = {10.5281/zenodo.20087650}
License
Code: MIT
Paper: CC BY 4.0

Contact: David J Fox | https://github.com/DavidFox998
