---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

## Riemann solvers for shallow-water simulations

**Project: RDycore**  
**Advisor: Prof. Jed Brown**

I work on the implementation and evaluation of approximate
Riemann solvers in RDycore, an open-source finite-volume code
for shallow-water and compound flooding simulations.

My work compares Roe, HLL, and HLLC solvers in terms of
accuracy, numerical diffusion, and computational cost.
The benchmarks include square dam-break problems,
flow over complex topography, and a Houston flooding case.

In the cases presented in my slides, HLLC produces solutions
close to Roe while achieving a computational cost close to HLL.
I also examine how mesh refinement affects the solution
relative to the choice of Riemann solver.

### Presentation

*Comparison of Roe, HLL, and HLLC Riemann Solvers in RDycore:
Accuracy, Diffusion, and GPU Considerations for Shallow-Water
Simulations*

41st Colorado Conference on Iterative and Multigrid Methods, 2026.

[View presentation slides](/files/riemann-solvers.pdf)

---

## Quasiperiodic Green’s functions for the Helmholtz equation

**Status: Work in progress**

I’m developing a Python implementation for evaluating
quasiperiodic Green’s functions for the two-dimensional
Helmholtz equation, building on formulations by Agocs and Barnett.

The implementation combines direct evaluation of nearby
sources with a lattice-sum representation of the remaining
contributions.

My current notebook explores:

- Convergence and comparisons with reference evaluations.
- Quasiperiodic translations outside the central cell.
- Recovery of the free-space Green’s function through
  inverse Floquet–Bloch integration.
- Extensions to doubly quasiperiodic Green’s functions.
- First spatial derivatives and finite-difference checks.

This work is ongoing, with an emphasis on numerical accuracy,
consistent phase conventions, and independent verification.
