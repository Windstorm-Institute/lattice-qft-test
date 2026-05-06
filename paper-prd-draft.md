# Submission scaffold — Physical Review D

**Title:** A Lattice Quantum Field Theory Test of the Static Escrow Postulate: 1+1D and 3+1D Falsification with Modular-Hamiltonian Partial Survival

**Author:** Grant Lavell Whitmer III, The Windstorm Institute, Fort Ann, NY 12828, USA · grantwhitmer3@gmail.com

**PACS / PhySH:** Bekenstein–Hawking entropy · Bekenstein bound · Bisognano–Wichmann theorem · Modular Hamiltonian · Entropic gravity · Lattice quantum field theory · Foundations of general relativity

**Suggested section:** Section IV — General Relativity, Cosmology, and Astrophysics → Foundations / Methodology. Alternative: Section II (High Energy Physics and Field Theory) given the lattice-QFT methodology weight, with Foundations as primary.

---

## Cover-letter abstract

The Gravitational Entropy Escrow framework (companion paper, Zenodo [10.5281/zenodo.20032023](https://doi.org/10.5281/zenodo.20032023)) makes a load-bearing static identification *S*<sub>esc</sub> = |*U*<sub>grav</sub>| / *T*<sub>Unruh</sub> between gravitational binding energy and quantum-field entropy held in escrow against the local Unruh temperature. We test this identification directly using lattice quantum field theory across three independent entropy measures: bipartition entanglement entropy, mutual information between regions surrounding the masses, and modular Hamiltonian content evaluated under the Bisognano–Wichmann conjecture.

In 1+1D (free massless scalar, lattice sizes up to N = 3000, 295-point (N, L, m) parameter scan) the dimensionless ratio R = S<sub>ent</sub>/S<sub>esc</sub> spans **10.56 orders of magnitude** across the grid; mass-induced entanglement is uniformly negative; the result is N-converged to four decimal places. In 3+1D (cubic lattice up to N = 20, two independent code paths agreeing on ΔS at N = 14 to better than 2×10⁻⁵), the mass-induced ratio R<sub>Δ</sub> is bounded by 10⁻³ across the grid; mutual information decays as L⁻⁴, opposite to the linear growth required by the postulate. The literal bipartition-entropy reading of the postulate is ruled out in both dimensions.

The modular Hamiltonian content gives a partial-survival result in 1+1D: ΔK approximately recovers the BW linear asymptote ΔK ∝ d<sub>1</sub> within a small-d<sub>1</sub> window (d<sub>1</sub> ∈ [2, 6] at m = 1) with prefactor approximately 1/30 of the literal BW value. The previously-published v0.4/v0.5 figure of "ΔK ∝ L^{0.7} sublinear scaling" is here corrected to a regime-dependent characterization, with the single-power-law exponent identified as a fitting artifact across a smooth crossover (sliding-window analysis: α ≈ +1.0 in the BW window, smoothly transitioning through +0.5 in the decay tail at d<sub>1</sub> ≥ 16). A companion paper reports 3+1D ΔK does not recover the BW asymptote within the resolvable d<sub>1</sub> range. The framework's horizon-limit recoveries (Bekenstein–Hawking via surface gravity) are independent of these flat-space tests.

---

## Companion paper

This is a supplement to *Gravitational Entropy Escrow: An Interpretive Synthesis of Thermodynamic Approaches to Gravity* (Whitmer 2026), Zenodo [10.5281/zenodo.20032023](https://doi.org/10.5281/zenodo.20032023). The two papers are intended to be read together: the framework paper presents the static identification as load-bearing; this paper tests it directly.

## What's in this repo

- `paper.pdf` — full manuscript (v0.7)
- `paper/Paper13-v0.7-source.txt` — extracted-text mirror
- `paper-arxiv.tex` — arXiv submission scaffold (gr-qc, hep-lat, hep-th)
- `article.html` — long-form lay companion (mirror of [windstorminstitute.org/articles/lattice-qft-test.html](https://windstorminstitute.org/articles/lattice-qft-test.html))

## Reviewer reproducibility statement

All 1+1D numerical claims in v0.7 §VI.C are reproducible with the Python script `lattice_1d_modular.py` archived at [Windstorm-Labs/lattice-qft-test](https://github.com/Windstorm-Labs/lattice-qft-test) (`experiments/lattice_1d/`). Dependencies: numpy, scipy. CPU-only; total runtime approximately 10 minutes for the full 1+1D scan. The script implements the single-mass-in-A protocol with Williamson decomposition (vacuum-mode projection threshold 1×10⁻⁹) and validation V1/V2 (relative-entropy positivity; modal-vs-original-basis cross-check at machine precision).

The 3+1D production code (`lattice_3d_modular_external.py`) and raw production-run JSON outputs ship with the 3+1D companion paper's separate Zenodo deposit.

External-provider verification audit results (per Appendix A of `CONSOLIDATED_FINDINGS.md` in the Labs mirror): two Perplexity sandbox runs reproduced local ground-truth at ≤0.05%; one Gemini run was determined to be fabricated (no consistent error pattern; textual signature of code non-execution) and discarded. The lesson — multi-LLM cross-validation requires external ground-truth anchoring; without it, the most confident-sounding LLM may simply be the most hallucinatory — is documented as a methodological note in §IX.

## Note on scope and posture

This paper falsifies the literal bipartition-entropy reading of the framework's load-bearing static identification, and reports a partial-survival result for the modular-Hamiltonian reading in 1+1D. Both halves are honestly reported. The framework's empirical successes (constant *a*<sub>0</sub>, deep-MOND, SPARC reanalysis, Genzel five-case test) and its horizon thermodynamics are independent of these tests. We submit this work because clean falsification of one's own published framework, with explicit identification of what survives, is the kind of contribution the literature ought to reward more visibly than it currently does.
