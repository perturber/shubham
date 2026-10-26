---
title: Research
permalink: /research/
mathjax: true
---

<h1 class="page-title">Research</h1>
<p class="page-lede">A short, mostly self-contained overview. The <a href="{{ site.baseurl }}/publications/">papers</a> have the full story.</p>

<div class="card" markdown="1">

## Background: LISA and extreme-mass-ratio inspirals

<figure>
  <img class="research-img" src="{{ site.baseurl }}/assets/LISA.jpg" alt="Line drawing of the LISA constellation" loading="lazy">
  <figcaption>The space-based gravitational-wave observatory LISA. Image: <a href="https://www.esa.int/ESA_Multimedia/Images/2002/02/LISA_Laser_Interferometer_Space_Antenna_line_drawing">ESA</a>.</figcaption>
</figure>

I work on data analysis for the Laser Interferometer Space Antenna ([LISA](https://www.lisamission.org/)), which is scheduled to launch in the mid-2030s ([ESA](https://www.esa.int/Science_Exploration/Space_Science/LISA/Capturing_the_ripples_of_spacetime_LISA_gets_go-ahead)). LISA will detect gravitational waves from galactic binaries, from mergers of massive black holes, and from extreme-mass-ratio inspirals (EMRIs). In an EMRI, a stellar-mass compact object spirals into a massive black hole ([LISA Definition Study Report](https://arxiv.org/abs/2402.07571)).

<figure>
  <div class="video-container">
    <iframe src="https://www.youtube-nocookie.com/embed/WPvkzSvgHvc" title="Animation of an extreme-mass-ratio inspiral" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen loading="lazy"></iframe>
  </div>
  <figcaption>Animation of a late-stage EMRI. Credit: <a href="https://www.youtube.com/watch?v=WPvkzSvgHvc">Steve Drasco, AEI Potsdam</a>.</figcaption>
</figure>

EMRI signals stay in the LISA band for months to years and complete $$\sim 10^5$$ orbital cycles. That lets us map the spacetime around massive black holes and test General Relativity (GR) very precisely. Their long inspirals also make them sensitive to small perturbations, such as torques from an accretion disk. The same feature makes them hard to analyze: small modeling errors build up over the long signal.

</div>

<div class="card" markdown="1">

## Robust inference of long-inspiral sources

A fully phase-coherent analysis needs a waveform model that is accurate over the whole multi-year signal. If the model misses any physics, for example an environmental effect, the inferred parameters can be badly biased. In [Kejriwal (2026)](https://arxiv.org/abs/2606.13728) I introduce **SPLIT**, a GPU-accelerated pipeline that splits the data into blocks, analyzes each block coherently, and combines the blocks loosely. This limits how much phase error can build up. In an environment-rich injection, the coherent vacuum-GR analysis was biased by about $$5\sigma$$. SPLIT kept the biases to about $$0.5\sigma$$, at the cost of a small loss in signal-to-noise ratio. SPLIT is also robust against outliers in the data.

</div>

<div class="card" markdown="1">

## Measuring beyond-vacuum-GR effects

<figure>
  <img class="research-img" src="{{ site.baseurl }}/assets/joint_analysis/correlation_bias-1.png" alt="Biases on intrinsic EMRI parameters" loading="lazy">
  <figcaption>Biases (in units of \(\sigma\)) in an EMRI's intrinsic parameters when the signal contains an environmental effect that the analysis leaves out. From <a href="https://arxiv.org/abs/2312.13028">Kejriwal et al. (2024)</a>.</figcaption>
</figure>

Many proposed environmental and beyond-GR effects enter an EMRI's dynamics as small perturbations; see e.g. [Kocsis et al. (2011)](https://arxiv.org/abs/1104.2322), [Barausse et al. (2014)](https://arxiv.org/abs/1404.7149) and [Yunes & Pretorius (2009)](https://arxiv.org/abs/0909.3328). Using a generic framework, we showed that measuring several such effects at once creates strong parameter correlations, which weakens the inference. Leaving them out entirely can bias the inferred parameters by $$\gtrsim 10\sigma$$ ([Kejriwal et al. 2024](https://arxiv.org/abs/2312.13028)). We also used eccentric EMRIs to study what accretion physics can be constrained ([Duque et al. 2025](https://journals.aps.org/prd/abstract/10.1103/PhysRevD.111.084006)).

### Bias-corrected importance sampling

<figure>
  <img class="research-img" src="{{ site.baseurl }}/assets/biascorrected.png" alt="Schematic of bias-corrected importance sampling" loading="lazy">
  <figcaption>Left: how biases arise in the signal parameters \(\psi_S, \varphi_S\). Right: the correction scheme, which draws posterior samples along a "correction" axis. From <a href="https://arxiv.org/abs/2503.01120">Kejriwal et al. (2025)</a>.</figcaption>
</figure>

Inference under even one hypothesis is expensive, especially inside the LISA global fit, so testing many alternative hypotheses with standard methods is impractical. Bias-corrected importance sampling takes posterior samples obtained under vacuum GR and turns them into consistent, inexpensive samples from alternative hypotheses ([Kejriwal et al. 2025](https://arxiv.org/abs/2503.01120)).

### Population-level tests

One source rarely separates an astrophysical environment from a change to gravity, but a population can. Environmental effects vary from source to source, while a modified-gravity effect should be the same everywhere. We build hierarchical models of gravitational-wave populations that use this difference to tell the two apart ([Kejriwal, Barausse & Chua 2025](https://arxiv.org/abs/2510.17398)).

</div>

<div class="card" markdown="1">

## Electromagnetic counterparts of EMRIs

<figure>
  <img class="research-img" src="{{ site.baseurl }}/assets/EMcounterpart.png" alt="Schematic of an EMRI in an accretion disk" loading="lazy">
  <figcaption>An EMRI evolving in a matter-rich environment (yellow disk). From <a href="https://arxiv.org/abs/2404.00941">Kejriwal et al. (2024)</a>, courtesy of Vojtěch Witzany.</figcaption>
</figure>

Quasi-periodic eruptions (QPEs) are repeating soft X-ray flares with periods of hours ($$\sim 10^{-4}$$ Hz). They are emerging as possible electromagnetic counterparts of EMRIs embedded in accretion disks; see e.g. [Linial & Metzger (2023)](https://arxiv.org/abs/2303.16231). We studied the prospect of observing the same EMRI in X-rays and in gravitational waves ([Kejriwal et al. 2024](https://arxiv.org/abs/2404.00941)). We also analyzed the quasi-periodic oscillation source RE J1034+396, which may host an orbiting compact object of $$\approx 47\,M_\odot$$ and has a $$\approx 25\%$$ chance of being detected by LISA.

<figure>
  <img class="research-img" src="{{ site.baseurl }}/assets/QPE.png" alt="X-ray light curve of eRO-QPE2" loading="lazy">
  <figcaption>X-ray light curve from the August 2020 observation of the QPE source eRO-QPE2. From <a href="https://arxiv.org/abs/2411.00289">Pasham, Kejriwal et al. (2024)</a>, courtesy of Dheeraj R. Pasham.</figcaption>
</figure>

QPE timings can also constrain the parameters of the EMRI and of the massive black hole ([Chakraborty et al. 2025](https://iopscience.iop.org/article/10.3847/1538-4357/ae003b)).

</div>

<div class="card" markdown="1">

## Waveforms and software

- **[StableEMRIFisher (SEF)](https://github.com/perturber/StableEMRIFisher):** a package I created for computing fast, numerically stable Fisher information matrices for EMRIs.
- **[FastEMRIWaveforms (FEW)](https://github.com/BlackHolePerturbationToolkit/FastEMRIWaveforms):** I contributed to FEW v2.0 and to the study of what it means for data analysis ([Chapman-Bird et al. 2025](https://arxiv.org/abs/2506.09470)).
- **SPLIT:** a GPU-accelerated, loosely-coherent inference pipeline for long-inspiral sources ([Kejriwal 2026](https://arxiv.org/abs/2606.13728)).
- **LISA science forecasts:** I contributed to a study of how LISA's instrument performance affects the science return from IMRIs and EMRIs ([Speri et al. 2026](https://arxiv.org/abs/2603.17072)).

</div>
