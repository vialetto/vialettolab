---
title: "Multiscale Computational Plasma Lab - Research"
layout: textlay
excerpt: "Multiscale Computational Plasma Lab -- Research"
sitemap: false
permalink: /research/
---

# Research

Our research group focuses on developing advanced computational models to understand and predict the behavior of low-temperature plasmas and their interactions with materials. We combine fundamental plasma physics with practical applications in energy, manufacturing, and aerospace.

![Plasma Applications]({{ site.url }}{{ site.baseurl }}/images/examples/PlasmaApplications.png){: style="width: 85%; max-width: 800px; display: block; margin: 30px auto"}

## Why This Matters

Low-temperature plasmas are enabling technologies for some of society's most pressing challenges: propelling spacecraft more efficiently, manufacturing advanced semiconductors, and producing chemicals and fuels. However, these applications remain largely developed through trial and error. The reason? Plasmas are extraordinarily complex systems where electrons, ions, and neutral species coexist far from equilibrium, driving chemistry that wouldn't occur otherwise. When plasmas contact material surfaces, the complexity multiplies: energetic particles modify surfaces, surfaces change plasma behavior, and this feedback occurs across vastly different time and length scales.

Current simulation tools treat plasma and surface processes separately, using phenomenological parameters (like sticking coefficients or secondary electron emission yields) that are poorly known and may depend on plasma conditions themselves. This limits our ability to predict, optimize, and design plasma technologies.

## Research Questions

Our group aims to answer fundamental questions that bridge plasma physics and surface science:

- **What happens at the plasma-surface interface?** How do energetic ions, electrons, and radicals modify material surfaces? How do these modified surfaces feed back to affect plasma behavior?

- **Can we model plasma processes across scales?** From electron-level quantum processes to reactor-scale transport, spanning femtoseconds to seconds and nanometers to meters.

- **How do we accelerate discovery?** Can physics-informed machine learning help us navigate the enormous parameter space of plasma conditions?

## Our Approach

We develop **integrated computational models** that treat plasma and surface as a coupled system, rather than separate domains connected by uncertain parameters.

<div class="research-box" markdown="1">

### Fast Kinetic Methods for Non-Equilibrium Distributions 

<img src="{{ site.url }}{{ site.baseurl }}/images/examples/MC-Flux.png" alt="Electron Velocity Distribution Function" style="width: 350px; float: right; margin: 0 0 15px 20px; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">

A key challenge in plasma modeling is accurately computing electron and ion velocity distribution functions (VDFs) that are far from equilibrium. I've developed accelerated solution methods for the Boltzmann equation that achieve orders-of-magnitude speedup while maintaining accuracy:

- **Multi-term Boltzmann solvers**: Going beyond the two-term approximation to capture strong anisotropy in VDFs, critical for systems with strong electric fields
- **Fast Monte Carlo simulations**: Exploiting Markov processes in Monte Carlo simulations to reduce computational cost while preserving accuracy

These methods enable direct coupling of electron kinetics with fluid descriptions of heavy species and electromagnetic fields in realistic geometries—essential for predictive modeling of plasma reactors.

</div>

<div class="research-box" markdown="1">

### Chemistry Networks and Reaction Mechanisms

Understanding what chemical reactions actually occur in plasmas requires both accurate fundamental data and systematic model construction:

- **Cross section extraction**: Combining transport theory and swarm experiments to extract cross sections for charged particles (see [LXCat Project](https://nl.lxcat.net/home/))
- **Reaction mechanisms**: Our group is interested in developing complete chemistry sets for plasmas under different pressure and temperature conditions
- **Collisional-radiative models**: Developing population models with complex chemistry to extract internal plasma parameters from experimental spectroscopic data

</div>

<div class="research-box" markdown="1">

### Coarse-Grained Surface Kinetics Models

Rather than using fixed surface parameters, we are developing methods that model both plasma *and* material response:

<img src="{{ site.url }}{{ site.baseurl }}/images/examples/SurfaceKin.png" alt="Surface Kinetics Processes" style="width: 350px; float: right; margin: 0 0 15px 20px; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">

- **Kinetic Monte Carlo**: Developing computationally efficient mesoscopic approaches to model plasma interactions with surfaces, electron emission, and surface chemistry for understanding how surface properties (adsorbed species, roughness, composition changes) feed back to alter plasma behavior
- **Molecular dynamics with reactive force fields**: We are interested in simulating atomic-scale surface modification during plasma exposure
- **Multi-scale bridging**: Our goal is to connect quantum-mechanical surface processes to continuum plasma models through carefully constructed boundary conditions and embedding approaches

</div>

<div class="research-box" markdown="1">

### Physics-Informed Machine Learning <img src="{{ site.url }}{{ site.baseurl }}/images/Plasma-Surface-Scheme.png" alt="Machine Learning for Plasma" style="width: 400px; float: right; margin: 0 0 20px 15px; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">

The parameter space is enormous (species concentrations, electric fields, surface conditions...), making exhaustive physics-based simulation impractical. We are developing:

- **Surrogate models**: Fast ML approximations of high-fidely data, trained on physics-based model calculations or simulations
- **Reduced-order models**: Using physics to identify low-dimensional representations of high-dimensional plasma chemistry
- **Inverse modeling**: Inferring plasma conditions, reaction mechanisms, and surface properties from diagnostic measurements

This approach combines the interpretability and physical consistency of mechanistic models with the flexibility and speed of data-driven methods.

</div>

## Impact

By bringing together advanced kinetic theory, surface simulations, and machine learning, we aim to provide **understanding and predictive capability** where experiments alone cannot go: revealing reaction pathways, identifying rate-limiting processes, and suggesting optimal conditions before building hardware. For electric propulsion, this means designing thrusters with predictable erosion and performance. For plasma chemistry, it means identifying the plasma conditions that maximize desired product yields. For semiconductor manufacturing, it means controlling nanoscale features by understanding plasma-surface coupling.

---

**More details coming soon as we establish the lab at UCLA!**

![]({{ site.url }}{{ site.baseurl }}/images/respic/research_overview.png){: style="width: 70%; float: center; margin: 20px 0px"}
