# Submission scaffold — Classical and Quantum Gravity

**Title:** A Lattice Quantum Field Theory Test of the Static Escrow Postulate: 1+1D and 3+1D Falsification with Modular-Hamiltonian Partial Survival

**Author:** Grant Lavell Whitmer III, The Windstorm Institute, Fort Ann, NY 12828, USA · grantwhitmer3@gmail.com

**Topic area:** Entropic gravity foundations · Horizon thermodynamics · Modular Hamiltonian / Bisognano–Wichmann · Lattice quantum field theory · Methodology of physics

---

## Cover note

This paper supplements a companion paper, *Gravitational Entropy Escrow* (Whitmer 2026, [10.5281/zenodo.20032023](https://doi.org/10.5281/zenodo.20032023)), under separate submission.

The framework paper introduces the static identification *S*<sub>esc</sub> = |*U*<sub>grav</sub>| / *T*<sub>Unruh</sub> as load-bearing for the entire interpretive picture: Newton's law follows from it, Bekenstein–Hawking entropy follows from it, the deep-MOND acceleration scale falls out of it. Section 7.6 of that paper notes explicitly that derivation of this identity from quantum field theory first principles is the natural next test. This paper performs that test, on a lattice, directly.

The headline result is dimensional. In 1+1D the literal bipartition-entropy reading is falsified by 10⁵⁶ on the dimensionless ratio across the parameter grid; mutual information falsifies it independently by decaying as L⁻⁴ where the postulate predicts linear growth. In 3+1D the mass-induced ratio is bounded below 10⁻³. The modular Hamiltonian reading partially survives in 1+1D in a small-*d*<sub>1</sub> window with prefactor approximately 1/30; a companion paper extends the modular test to 3+1D and finds the BW asymptote is not recovered within the resolvable distance range.

We submit this paper to CQG because it is the kind of result a healthy literature on emergent / entropic gravity ought to make space for: a direct falsification of a load-bearing postulate, with explicit identification of which structural features of the prediction survive (BW linear scaling shape) and which do not (literal bipartition entropy; 3+1D BW recovery). The companion framework paper's empirical content (constant *a*<sub>0</sub>, deep-MOND, SPARC + Genzel reanalyses) and horizon-limit recoveries (Bekenstein–Hawking via surface gravity, Gibbons–Hawking via the de Sitter horizon) are independent of these flat-space tests; what fails is specifically the static identification in its literal QFT form.

The methodology section (§IX) documents an external-provider verification audit relevant to anyone running multi-LLM scientific workflows: two Perplexity sandbox runs reproduced local ground-truth at ≤0.05%; one Gemini run was determined to have fabricated numbers (no consistent error pattern; signature of code non-execution). The lesson — multi-LLM cross-validation requires external ground-truth anchoring — echoes the methodology weight of our prior C8 Clarification Note (Zenodo 10.5281/zenodo.20041992, in a different scientific direction).

---

## What's in this repo

- `paper.pdf` — full manuscript (v0.7)
- `paper/Paper13-v0.7-source.txt` — extracted-text mirror
- `paper-arxiv.tex` — arXiv submission scaffold

## Code and reproducibility

Mirrored at [Windstorm-Labs/lattice-qft-test](https://github.com/Windstorm-Labs/lattice-qft-test). Self-contained Python (numpy + scipy.linalg.eigh, no GPU); approximately 10-minute CPU runtime for the full 1+1D scan. Williamson decomposition with vacuum-mode projection; validation V1 (relative-entropy positivity) and V2 (basis cross-check at machine precision). The 3+1D production code ships with the companion paper's deposit.
