---
title: "Multiscale Computational Plasma Lab - Research"
layout: textlay
excerpt: "Multiscale Computational Plasma Lab -- Research"
sitemap: false
permalink: /research/
---

# Research

Our research group focuses on developing advanced computational models to understand and predict the behavior of low-temperature plasmas and their interactions with materials. We combine fundamental plasma physics with practical applications in aerospace, manufacturing, and energy.

<style>
.research-areas { display: flex; flex-wrap: wrap; gap: 24px; margin: 30px 0 45px 0; }
.ra-card { flex: 1 1 calc(50% - 24px); min-width: 280px; }
.ra-img { width: 100%; height: 220px; object-fit: cover; border-radius: 8px; margin: 0; display: block; box-shadow: 0 2px 8px rgba(0,0,0,0.12); }
.ra-title { font-weight: bold; font-size: 20px; color: #2c3e50; margin: 14px 0 6px 0; }
.ra-desc { color: #555; font-size: 16px; line-height: 1.5; }
.rb-figure { max-width: 440px; margin: 0 auto 18px auto; }
.rb-figure img { width: 100%; display: block; margin: 0; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1); }
.rb-credit { display: block; margin: 5px 2px 0 0; font-size: 11px; line-height: 1.3; color: #888; text-align: right; }
.rb-duo { display: flex; flex-wrap: wrap; align-items: flex-start; justify-content: center; gap: 18px; margin: 0 auto 18px auto; }
.rb-duo figure { margin: 0; }
.rb-duo img { height: 200px; width: auto; max-width: 100%; display: block; margin: 0; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1); }
.rb-duo-lg img { height: 240px; }
.rb-pair { display: flex; flex-wrap: wrap; justify-content: center; align-items: flex-start; gap: 26px; margin: 8px auto 20px auto; }
.rb-pair-item { text-align: center; }
.rb-pair-label { font-weight: 700; color: #2c3e50; font-size: 16px; margin-bottom: 10px; }
.rb-pair-item img { height: 230px; width: auto; max-width: 100%; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1); display: block; margin: 0 auto; }
@media (max-width: 640px) { .rb-pair-item img { height: auto; width: 100%; } }
.flow3 { display: flex; align-items: flex-start; justify-content: center; flex-wrap: wrap; gap: 6px; margin: 8px auto 22px auto; }
.flow-step { flex: 1 1 200px; max-width: 270px; text-align: center; }
.flow-cap { font-weight: 600; color: #2c3e50; font-size: 16px; line-height: 1.3; margin-bottom: 10px; min-height: 44px; display: flex; align-items: flex-end; justify-content: center; }
.flow-media { height: 200px; display: flex; align-items: center; justify-content: center; }
.flow-media img { max-width: 100%; max-height: 200px; width: auto; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1); }
.flow-media svg { max-width: 100%; max-height: 200px; width: auto; }
.flow-credit { display: block; margin-top: 5px; font-size: 10px; color: #999; }
.flow-arrow { flex: 0 0 auto; align-self: center; font-size: 44px; color: #1f3a63; line-height: 1; margin-top: 48px; }
</style>

## Research Areas

<div class="research-areas">

<div class="ra-card" markdown="0">

<img src="{{ site.url }}{{ site.baseurl }}/images/research-propulsion.jpg" class="ra-img" />

<p class="ra-title">Electric Propulsion</p>

<p class="ra-desc">Kinetic and fluid models of plasma thrusters and cathodes, with a focus on alternative propellants for efficient in-space propulsion.</p>

</div>

<div class="ra-card" markdown="0">

<img src="{{ site.url }}{{ site.baseurl }}/images/research-semiconductor.jpg" class="ra-img" />

<p class="ra-title">Semiconductor Fabrication</p>

<p class="ra-desc">Plasma etching and deposition processes for next-generation semiconductor manufacturing.</p>

</div>

<div class="ra-card" markdown="0">

<img src="{{ site.url }}{{ site.baseurl }}/images/research-surfaces.png" class="ra-img" />

<p class="ra-title">Plasma&ndash;Material Interactions</p>

<p class="ra-desc">Fundamentals of how plasmas modify surfaces, and how surfaces feed back on the plasma.</p>

</div>

<div class="ra-card" markdown="0">

<img src="{{ site.url }}{{ site.baseurl }}/images/research-plasma.jpg" class="ra-img" />

<p class="ra-title">Low-Temperature Plasma Physics</p>

<p class="ra-desc">Charged-particle kinetics, transport, and chemistry in non-equilibrium gas discharges.</p>

</div>

</div>

## Why This Matters

**Low-temperature plasmas are enabling technologies for some of society's most pressing challenges**: propelling spacecraft more efficiently, manufacturing advanced semiconductors, and producing chemicals and fuels. However, these applications remain largely developed through trial and error. *The reason?* Plasmas are extraordinarily complex systems where electrons, ions, and neutral species coexist far from equilibrium, driving chemistry that wouldn't occur otherwise. When plasmas contact material surfaces, the complexity multiplies: energetic particles modify surfaces, surfaces change plasma behavior, and this feedback occurs across vastly different time and length scales.

**By bringing together advanced kinetic theory, surface simulations, and machine learning, we aim to provide understanding and predictive capability where experiments alone cannot go.** For electric propulsion, this means studying thrusters and cathodes that are compatible with alternative propellants, with predictable erosion and performance. For plasma chemistry, it means identifying the plasma conditions that maximize desired product yields. For semiconductor manufacturing, it means controlling nanoscale features by understanding plasma-surface coupling.

## Our Approach

We develop **physics-based and data-driven models of plasmas** that couple complex chemistry, electromagnetic effects, external circuits, gas flow dynamics, surface kinetics, radiative and heat transfer.

<div class="research-box" markdown="1">

### Kinetic Simulations of Low-Temperature Plasmas with Complex Chemistry

<div class="rb-pair">
<div class="rb-pair-item">
<div class="rb-pair-label">Low-Pressure Plasmas</div>
<img src="{{ site.url }}{{ site.baseurl }}/images/approach/low-pressure.png" alt="Low-pressure plasma simulation">
</div>
<div class="rb-pair-item">
<div class="rb-pair-label">Atmospheric-Pressure Plasmas</div>
<img src="{{ site.url }}{{ site.baseurl }}/images/approach/atmospheric-dbd.png" alt="Dielectric barrier discharge: applied voltage and current density over time">
</div>
</div>

Our group develops in-house Particle-In-Cell / Monte Carlo Collision (PIC/MCC), Direct Simulation Monte Carlo (DSMC), and Itô-Kinetic Monte Carlo (Itô-KMC) models that couple plasma kinetics with electrostatic and electromagnetic effects, and complex external-circuit models. Our aim is to develop sets of chemical reaction mechanisms and cross sections for low-temperature plasmas that are validated with experiments across several pressures and operating conditions.

</div>

<div class="research-box" markdown="1">

### Atomistic and Coarse-Grained Surface Models

<div class="rb-duo">
<figure>
<img src="{{ site.url }}{{ site.baseurl }}/images/approach/plasma-solid-interface.jpg" alt="The plasma-solid interface: sheath and activated surface layers">
<figcaption class="rb-credit">Plasma Sources Sci. Technol. 27, 064005 (2018)</figcaption>
</figure>
<figure>
<img src="{{ site.url }}{{ site.baseurl }}/images/approach/deposition.gif" alt="Animated kinetic Monte Carlo simulation of atomistic deposition on a surface">
</figure>
</div>

Our aim is to develop scale-bridging surface kinetics models from atomistic to mesoscopic scales to describe adsorption, recombination, and surface defects, and how they feed back on the plasma.

</div>

<div class="research-box" markdown="1">

### Data Assimilation

<figure class="rb-figure" style="max-width: 560px;">
<img src="{{ site.url }}{{ site.baseurl }}/images/approach/data-assimilation.png" alt="Digital twin: experiments, data assimilation, control, and physics-based model">
</figure>

We fuse model results with experimental data to infer quantities that cannot be measured directly, such as internal plasma parameters, cross sections, and reaction rates from spectroscopic and swarm data.

</div>

<div class="research-box" markdown="1">

### Surrogate Modeling

<div class="flow3">
<div class="flow-step">
<div class="flow-cap">From one second of plasma</div>
<div class="flow-media"><img src="{{ site.url }}{{ site.baseurl }}/images/approach/plasma-experiment.jpg" alt="Plasma experiment"></div>
<span class="flow-credit">Credit: NASA</span>
</div>
<div class="flow-arrow">&#10132;</div>
<div class="flow-step">
<div class="flow-cap">to one month on 1000s of cores</div>
<div class="flow-media"><img src="{{ site.url }}{{ site.baseurl }}/images/approach/surrogate-sim.png" alt="Particle-in-cell simulation of a plasma at t = 120 ns"></div>
</div>
<div class="flow-arrow" style="margin-right: 28px;">&#10132;</div>
<div class="flow-step">
<div class="flow-cap">to one second on a single core</div>
<div class="flow-media"><img src="{{ site.url }}{{ site.baseurl }}/images/approach/surrogate-net.png" alt="Autoencoder surrogate model for plasma-material interactions"></div>
</div>
</div>

Our goal is to develop the next generation of surrogate models and reduced-order models for plasma–material interactions, which make it feasible to explore the vast parameter space of plasma chemistry and surface conditions at a fraction of the cost.

</div>

<div class="research-box" markdown="1">

### Boltzmann Equation for Charged Particles

<div class="rb-duo rb-duo-lg">
<figure>
<img src="{{ site.url }}{{ site.baseurl }}/images/approach/eepf-boltzmann.png" alt="Electron energy probability function: Monte Carlo vs. two-term and multi-term Boltzmann solutions">
<figcaption class="rb-credit">Phys. Plasmas 33, 043501 (2026)</figcaption>
</figure>
<figure>
<img src="{{ site.url }}{{ site.baseurl }}/images/examples/MC-Flux.png" alt="Electron velocity distribution function from Monte Carlo simulation">
<figcaption class="rb-credit">Plasma Sources Sci. Technol. 28, 115015 (2019)</figcaption>
</figure>
</div>

We develop fast and accurate models for numerical solutions of the electron and ion Boltzmann equation, beyond the conventional two-term approximation, which can capture the strong anisotropy of the velocity distribution function and non-local effects. These are important for the definition of new hybrid kinetic–fluid models of plasmas.

</div>

---

![]({{ site.url }}{{ site.baseurl }}/images/respic/research_overview.png){: style="width: 70%; float: center; margin: 20px 0px"}
