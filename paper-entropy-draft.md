# Submission scaffold — Entropy (MDPI)

**Title:** A Lattice Quantum Field Theory Test of the Static Escrow Postulate: 1+1D and 3+1D Falsification with a Suggestive Modular-Hamiltonian Window in 1+1D

**Author:** Grant Lavell Whitmer III, The Windstorm Institute, Fort Ann, NY 12828, USA · grantwhitmer3@gmail.com

**Section:** Statistical Physics → Thermodynamics of Gravity / Entropic Gravity. Alternative: Information Theory and Quantum Information Theory (modular Hamiltonian / entanglement entropy methodology weight).

**MSC / arXiv class:** 81T25 (Quantum field theory on lattices); 80A05 (Foundations of thermodynamics); 83C45 (General relativity, foundations); gr-qc; hep-lat; hep-th

---

## Cover-letter abstract

We test the static gravitational entropy escrow postulate *S*<sub>esc</sub> = |*U*<sub>grav</sub>| / *T*<sub>Unruh</sub> of the Gravitational Entropy Escrow framework (companion paper, [10.5281/zenodo.20031931](https://doi.org/10.5281/zenodo.20031931)) using lattice quantum field theory across three independent entropy measures: bipartition entanglement entropy, mutual information between regions surrounding the masses, and modular Hamiltonian content evaluated under the Bisognano–Wichmann conjecture.

In 1+1D (295-point parameter scan, lattice sizes up to N = 3000), the literal bipartition-entropy reading is falsified by **10.56 orders of magnitude** (a factor of ~4×10¹⁰) in the dimensionless ratio across the grid; mutual information falsifies it independently by decaying as L⁻⁴ where the postulate predicts linear growth. In 3+1D (cubic lattice up to N = 20, two independent code paths agreeing at N = 14 to better than 2×10⁻⁵), the mass-induced ratio R<sub>Δ</sub> is bounded below 10⁻³.

The modular Hamiltonian content leaves a suggestive fragment in 1+1D: at m = 1, ΔK shows a positive, approximately linear window (ΔK ∝ d<sub>1</sub>, d<sub>1</sub> ∈ [2, 6]) resembling the BW shape with prefactor approximately 1/30 — but m = 1 is outside the linear-response regime where the BW asymptote is derivable, and in that regime ΔK is negative and d<sub>1</sub>-independent, so the asymptote is not recovered. The previously-published "ΔK ∝ L^{0.7} sublinear scaling" is here corrected to a regime-dependent characterization (sliding-window local exponent: α ≈ +1.0 in the BW window, smoothly transitioning through +0.5 in the decay tail). A companion paper reports 3+1D ΔK does not recover the BW asymptote within the resolvable d<sub>1</sub> range, indicating dimension-dependent recovery. The framework's horizon-limit recoveries (Bekenstein–Hawking via surface gravity) are independent of these flat-space tests.

---

## Why Entropy / MDPI

This paper sits at the intersection of (i) entropic / emergent gravity (Verlinde, Padmanabhan, Jacobson tradition), (ii) modular Hamiltonian / entanglement entropy methodology (Bisognano–Wichmann, Peschel correlator formula, Williamson decomposition), and (iii) lattice quantum field theory as a falsification tool for foundational claims about gravity-from-thermodynamics. Entropy regularly publishes both technical contributions and methodology case studies in this space.

The paper's posture is honest: it documents a *direct falsification* of a load-bearing identification in the author's own previously-published framework, identifies which structural features of the prediction survive (BW linear shape in 1+1D), and isolates a *calculable* open question (the 1/30 prefactor, conjectured to reflect a UV/IR mismatch between the BW formula and a localized lattice mass at correlation length ξ ∼ 1).

A separate methodology section documents an external-provider verification audit (three independent LLM sandboxes; two trustworthy, one fabricated) that is intended to be useful to readers running multi-LLM scientific workflows. The lesson echoes the methodology weight of our prior C8 Clarification Note in a different scientific direction: multi-LLM cross-validation requires external ground-truth anchoring; without it, the most confident-sounding LLM may simply be the most hallucinatory.

## Suggested reviewers

We do not propose specific reviewers. We welcome reviewers with expertise in (a) lattice quantum field theory and entanglement entropy methodology (Cardy, Calabrese, Casini, Huerta, Peschel tradition), (b) modular Hamiltonians and the Bisognano–Wichmann theorem (Borchers, Witten, Longo tradition), (c) entropic gravity foundations (Verlinde, Padmanabhan, Jacobson, van Putten tradition), and (d) AI-assisted scientific methodology and multi-LLM verification practice. Reviewers from group (d) may find the §IX methodology audit of independent interest beyond the gravitational-physics question.

## Repo

[github.com/Windstorm-Institute/lattice-qft-test](https://github.com/Windstorm-Institute/lattice-qft-test) hosts paper.pdf, the source-text mirror, the LaTeX scaffold, and the long-form lay companion. Code at [Windstorm-Labs/lattice-qft-test](https://github.com/Windstorm-Labs/lattice-qft-test).
