---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

## Shallow-water simulations in RDycore

With Prof. Jed Brown, University of Colorado Boulder.

I compare the Roe, HLL, and HLLC Riemann solvers in RDycore to study how
the choice of solver affects wave fronts and runtime in shallow-water
simulations. My tests include a square dam break, flow over four mounds,
and a flooding case in Houston.

[![Water depth computed with three Riemann solvers on the same mesh](/images/riemann-comparison.png)](/images/riemann-comparison.png)

*Square dam-break test on a fixed mesh. Roe and HLLC produce similar
wave fronts, while the HLL solution shows more numerical diffusion.*

[Conference talk, June 2026](/talks/2026-06-riemann-solvers/) · [Slides (PDF)](/files/riemann-solvers.pdf)

## Quasiperiodic Green’s functions for the 2D Helmholtz equation

With Prof. Fruzsina Agocs, University of Colorado Boulder.

I’m developing a Python implementation to compute the wave field from a
periodic array of sources with a prescribed phase shift between neighboring
cells. Following the formulation of Agocs and Barnett, I evaluate the three
nearest sources directly and use a series expansion for the rest of the
array. The figures below show three checks of the implementation.

[![Absolute error against a spectral reference in three convergence tests](/images/green-convergence.png)](/images/green-convergence.png)

*Convergence against a spectral reference. From left to right, I vary the
number of quadrature nodes, the integration cutoff, and the number of
terms in the expansion.*

[![Maximum error versus cell shift and a spatial error map](/images/green-outside-cell.png)](/images/green-outside-cell.png)

*Evaluation outside the central cell. The left panel shows the maximum
error as the target is shifted by whole periods. The right panel maps
the error across a grid of target points for period d = 1.*

[![Free-space reconstruction error and the weighted contour integrand](/images/green-reconstruction.png)](/images/green-reconstruction.png)

*Inverse Floquet–Bloch reconstruction. At four target points, the error
relative to the known free-space Green’s function decreases as I refine
the quadrature. The right panel shows the weighted integrand at one
of those points.*
