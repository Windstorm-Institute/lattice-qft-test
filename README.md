# Paper 13: Lattice QFT Test of the Static Escrow Postulate

**A Lattice Quantum Field Theory Test of the Static Escrow Postulate: 1+1D and 3+1D Falsification with Modular-Hamiltonian Partial Survival**

Grant Lavell Whitmer III · Windstorm Labs, The Windstorm Institute · Fort Ann, NY, USA

[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.20057538-blue)](https://doi.org/10.5281/zenodo.20057538)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey)](https://creativecommons.org/licenses/by/4.0/)
[![Track: Entropic Bounds](https://img.shields.io/badge/Track-2_·_Entropic_Bounds-8b5cf6)](https://windstorminstitute.org/#track2)

**Zenodo:** [10.5281/zenodo.20057538](https://doi.org/10.5281/zenodo.20057538) · **Current version: v0.7** ([10.5281/zenodo.20057538](https://doi.org/10.5281/zenodo.20057538), May 2026)

**Supplement to:** [Paper 11 — Gravitational Entropy Escrow](https://github.com/Windstorm-Institute/gravitational-entropy-escrow) ([10.5281/zenodo.20032023](https://doi.org/10.5281/zenodo.20032023))

---

## What this paper does

Paper 11 introduced a framework that identifies gravitational binding energy with entropy "held in escrow" against the local Unruh temperature. The static form of the postulate is

```
S_esc = |U_grav| / T_Unruh                                                  [1]
```

This paper asks whether [1] is a literal QFT identity — that is, whether the entropy of a free scalar field in the presence of localized masses, computed by lattice quantum field theory, equals the right-hand side of [1] up to an order-unity prefactor.

Three independent entropy measures are tested:

1. **Bipartition entanglement entropy** — between the "left" and "right" halves of space, with masses placed on each side.
2. **Mutual information** — between two regions surrounding the masses.
3. **Modular Hamiltonian content** — evaluated under the Bisognano–Wichmann conjecture.

The tests are run on 1+1D lattices up to N = 3000 (a 295-point parameter scan over (N, L, m)) and on 3+1D cubic lattices up to N = 20.

## Headline results

**The literal bipartition-entropy reading of the postulate is ruled out in both 1+1D and 3+1D.**

- In 1+1D the dimensionless ratio R = S_ent / S_esc spans **10.56 orders of magnitude** across the (L, m) grid.
- In 3+1D the mass-induced ratio R_Δ = ΔS / S_esc is bounded by 10⁻³ across all grid points; mutual information decays as L⁻⁴, opposite to the linear growth required by the postulate.
- Two independent code paths (CPU NumPy + GPU torch.linalg.eigh on a current-generation Nvidia GPU) agree on ΔS at the N = 14 anchor to better than 2×10⁻⁵, ruling out implementation artifacts.

**The modular Hamiltonian gives a partial-survival result in 1+1D — right structural form, suppressed magnitude.**

- ΔK approximately recovers the Bisognano–Wichmann linear asymptote ΔK ∝ d1 in a small-d1 window (d1 ∈ [2, 6] at m = 1).
- Prefactor: approximately 1/30 of the literal BW value.
- At larger d1 the local exponent decreases smoothly into a sublinear decay tail.
- The previously-published v0.4/v0.5 figure of "ΔK ∝ L^{0.7}" is here corrected to a regime-dependent characterization. The single-power-law exponent was a fitting artifact across a smooth crossover; sliding-window analysis shows the local exponent evolves from α ≈ +1.0 in the small-d1 BW window down through α ≈ +0.5 in the decay tail at d1 ≥ 16.

**A companion paper reports the 3+1D modular content does *not* recover the BW asymptote within the d1 range the lattice can resolve**, with ΔK peaking at d1 ≈ 2 and decaying as d1⁻² to d1⁻³ for larger d1. BW recovery in 3+1D is dimension-dependent or, equivalently, the rate of approach to the continuum BW asymptote is substantially slower in 3+1D than in 1+1D.

## What this rules out and what survives

**Ruled out:** a direct identification of S_esc with the bipartition entanglement entropy of two-mass configurations in free scalar QFT, in any spacetime dimension tested. The mutual information evidence rules this out independently of the bipartition test.

**Partial survival:** a direct identification of S_esc with the modular Hamiltonian content, in 1+1D, within a small-d1 window, with a calculable suppression factor (~1/30) as the remaining open question. Whether this survival extends to 3+1D at d1 inaccessible to the present lattice is unsettled.

**Unaffected:** the framework's horizon-limit recoveries — Bekenstein–Hawking entropy via surface gravity, Gibbons–Hawking entropy via the de Sitter horizon — are independent of these flat-space tests. Those go through the surface-gravity Unruh temperature and are not flat-space modular content. The framework's *empirical* content (constant a₀, deep-MOND, SPARC reanalysis, baryonic Tully–Fisher, Genzel five-case test) is also unaffected.

## Read the paper

- **[paper.pdf](paper.pdf)** — full v0.7 manuscript (14 pages)
- **[paper/Paper13-v0.7-source.txt](paper/Paper13-v0.7-source.txt)** — extracted-text mirror (for grep / search)
- **[article.html](article.html)** — long-form lay-friendly companion (mirror of the [website article](https://windstorminstitute.org/articles/lattice-qft-test.html))
- **[paper-arxiv.tex](paper-arxiv.tex)** — arXiv submission scaffold (gr-qc, hep-lat, hep-th)
- **[paper-prd-draft.md](paper-prd-draft.md)** · **[paper-cqg-draft.md](paper-cqg-draft.md)** · **[paper-entropy-draft.md](paper-entropy-draft.md)** — journal submission scaffolds (Physical Review D, Classical and Quantum Gravity, Entropy / MDPI)
- **[CONSOLIDATED_FINDINGS.md (Labs mirror)](https://github.com/Windstorm-Labs/lattice-qft-test/blob/main/CONSOLIDATED_FINDINGS.md)** — pre-publication analysis document showing how the v0.6/v0.7 corrections were derived (sliding-window fits, single-mass-in-A protocol, 1+1D vs 3+1D dimensional difference, multi-LLM verification audit)

## Code

The 1+1D production code is mirrored at:

**[Windstorm-Labs/lattice-qft-test](https://github.com/Windstorm-Labs/lattice-qft-test)**

It uses numpy + scipy.linalg.eigh (CPU-only), reproduces all 1+1D numerical claims in §VI.C, and runs the full scan in approximately 10 minutes on a single CPU core.

Current authoritative archive: **[Zenodo (10.5281/zenodo.20057538)](https://doi.org/10.5281/zenodo.20057538)**.

## Citation

> Whitmer, G. L. III (2026). *A Lattice Quantum Field Theory Test of the Static Escrow Postulate: 1+1D and 3+1D Falsification with Modular-Hamiltonian Partial Survival.* Zenodo. [10.5281/zenodo.20057538](https://doi.org/10.5281/zenodo.20057538) (v0.7).

---

## Discuss this paper

- **Discuss the paper's ideas** → [Comments on the website article](https://windstorminstitute.org/articles/lattice-qft-test.html#comments) (powered by GitHub Discussions on the website repo)
- **Typo, citation issue, or paper-content correction?** → [Open an Issue on this repo](../../issues)
- **Bug in the analysis code, or a reproduction question?** → [Issue](https://github.com/Windstorm-Labs/lattice-qft-test/issues) or [Discussion](https://github.com/Windstorm-Labs/lattice-qft-test/discussions) on the Labs repo

---

## The Windstorm Institute — Two Research Tracks

### Track 1 — The Throughput Basin · 9 papers (Papers 1–9 globally; 1st through 9th in this track; arc complete)

| # | Paper | DOI |
|---|-------|-----|
| 1 | [The Fons Constraint](https://github.com/Windstorm-Institute/fons-constraint) | [10.5281/zenodo.19274048](https://doi.org/10.5281/zenodo.19274048) |
| 2 | [The Receiver-Limited Floor](https://github.com/Windstorm-Institute/receiver-limited-floor) | [10.5281/zenodo.19322973](https://doi.org/10.5281/zenodo.19322973) |
| 3 | [The Throughput Basin](https://github.com/Windstorm-Institute/throughput-basin) | [10.5281/zenodo.19323194](https://doi.org/10.5281/zenodo.19323194) |
| 4 | [The Serial Decoding Basin τ](https://github.com/Windstorm-Institute/serial-decoding-basin) | [10.5281/zenodo.19323423](https://doi.org/10.5281/zenodo.19323423) |
| 5 | [The Dissipative Decoder](https://github.com/Windstorm-Institute/dissipative-decoder) | [10.5281/zenodo.19433048](https://doi.org/10.5281/zenodo.19433048) |
| 6 | [The Inherited Constraint](https://github.com/Windstorm-Institute/inherited-constraint) | [10.5281/zenodo.19432911](https://doi.org/10.5281/zenodo.19432911) |
| 7 | [The Throughput Basin Origin](https://github.com/Windstorm-Institute/throughput-basin-origin) | [10.5281/zenodo.19498582](https://doi.org/10.5281/zenodo.19498582) |
| 8 | [The Vision Basin](https://github.com/Windstorm-Institute/vision-basin) | [10.5281/zenodo.19672827](https://doi.org/10.5281/zenodo.19672827) |
| 9 | [The Hardware Basin](https://github.com/Windstorm-Institute/hardware-basin) | [10.5281/zenodo.19672921](https://doi.org/10.5281/zenodo.19672921) |

### Track 2 — Entropic Bounds in Analog Systems · 6 papers (Papers 10–15 globally; 1st through 4th in this track; line of inquiry active)

| # | Paper | DOI |
|---|-------|-----|
| 10 | [Phonon Extraction Bound (BEC Analog Gravity)](https://github.com/Windstorm-Institute/phonon-extraction-bound) *(1st in track)* | [10.5281/zenodo.20014391](https://doi.org/10.5281/zenodo.20014391) |
| 11 | [Gravitational Entropy Escrow](https://github.com/Windstorm-Institute/gravitational-entropy-escrow) *(2nd in track; framework paper)* | [10.5281/zenodo.20032023](https://doi.org/10.5281/zenodo.20032023) |
| 12 | [C8 Clarification Note](https://github.com/Windstorm-Institute/c8-clarification-note) *(3rd in track; companion to Paper 11)* | [10.5281/zenodo.20041992](https://doi.org/10.5281/zenodo.20041992) |
| 13 | [Lattice QFT Test of the Static Escrow Postulate](https://github.com/Windstorm-Institute/lattice-qft-test) *(this paper — 4th in track; supplement to Paper 11)* | [10.5281/zenodo.20057538](https://doi.org/10.5281/zenodo.20057538) |
| 14 | [Spacetime as Escrow Bookkeeping](https://github.com/Windstorm-Institute/escrow-spacetime) *(5th in track; translation of standard GR results into the escrow vocabulary; companion to Paper 11)* | [10.5281/zenodo.20126091](https://doi.org/10.5281/zenodo.20126091) |
| 15 | [The 𝒩<sub>esc</sub> Recipe](https://github.com/Windstorm-Institute/nesc-recipe) *(6th in track; formalizes 𝒩<sub>esc</sub> as a cross-regime function; continuation of Paper 14)* | [10.5281/zenodo.20145106](https://doi.org/10.5281/zenodo.20145106) |
**Website:** [windstorminstitute.org](https://windstorminstitute.org)

---

*Papers: CC BY 4.0 · Code: MIT*
