---
layout: default
title: Research
permalink: /research/
mathjax: true
---

# Research Overview  

Below, I provide a slightly more elaborate (and mostly self-contained) overview of my research. Still, the best way to learn about my research is to read my articles. You can find them on the [Publications](/shubham/publications) page.  

---

## Background

### Laser Interferometer Space Antenna (LISA)

<figure>
  <!-- Inline style on IMG sets DESKTOP max width -->
  <!-- CSS handles mobile scaling (width: 100%, max-width: 100%) -->
  <img src="{{ site.baseurl | default: '' }}/assets/LISA.jpg" alt="LISA image" style="max-width: 450px;"/>
  <figcaption>
    <em>Figure 1: The space-based gravitational wave observatory LISA. Image from <a href="https://www.esa.int/ESA_Multimedia/Images/2002/02/LISA_Laser_Interferometer_Space_Antenna_line_drawing" target="_blank">ESA</a>.</em>
  </figcaption>
</figure>  

I primarily work on developing the data analysis pipeline in various contexts (as you will see below) for the upcoming space-based gravitational wave observatory, i.e. the Laser Interferometer Space Antenna (LISA) [(NASA)](https://lisa.nasa.gov/). LISA was recently adopted by the European Space Agency (ESA), and is on track to be launched sometime in the middle of the next decade [(ESA)](https://www.esa.int/Science_Exploration/Space_Science/LISA/Capturing_the_ripples_of_spacetime_LISA_gets_go-ahead). Notably, the milli-Hz frequency band of LISA will be sensitive to many source-types, including a swarm of compact binaries evolving in the Milky Way, supermassive black hole binaries in the late-inspiral stage, and extreme-mass-ratio inspirals (EMRIs) in which a stellar-mass black hole is gravitationally bound to a supermassive black hole [(LISA Collaboration)](https://arxiv.org/abs/2402.07571). EMRIs are the primary target of my study.  


### Extreme-mass-ratio inspirals (EMRIs)  

<figure>
  <!-- Video uses CSS for max-width and aspect ratio -->
  <div class="video-container">
    <iframe
            src="https://www.youtube.com/embed/WPvkzSvgHvc"
            title="Inspiralling EMRI video"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            allowfullscreen>
    </iframe>
  </div>
  <figcaption>
    <em>Figure 2: Animation of a late-stage extreme-mass-ratio inspiral. Credits: <a href="https://www.youtube.com/watch?v=WPvkzSvgHvc" target="_blank">Steve Drasco, MPIGP (AEI), Potsdam</a>.</em>
  </figcaption>
</figure>


EMRIs are inspirals of a compact object (CO) — most relevant to the context of LISA a stellar-origin black hole with mass \\(\sim 10 M_\odot\\) — orbiting a supermassive black hole (MBH) of mass \\(\sim 10^6 M_\odot\\). Their gravitational wave signals are expected to spend years in the LISA band spanning hundreds of thousands of strong-field orbits. This will allow a unique opportunity to map the curvature of spacetime around MBHs, testing General Relativity (GR) to unprecedented precision. In addition, any environmental forces (for e.g. from an accretion disk surrounding the MBH) will have a cummulative effect on the binary's long-term inspiral, making measurements extremely sensitive to such effects.

---

## Measurability of "Beyond-Vacuum-GR" effects in EMRIs  

<figure>
  <!-- Inline style on IMG sets DESKTOP max width -->
  <!-- CSS handles mobile scaling (width: 100%, max-width: 100%) -->
  <img src="{{ site.baseurl | default: '' }}/assets/joint_analysis/correlation_bias-1.png" alt="biases intrinsic" style="max-width: 450px;"/>
  <figcaption>
    <em>Figure 3: Biases induced on the EMRI's intrinsic parameters due to an environmental effect in the signal which was not accounted for in the inference. The biases scaled by the \(1\sigma\) measurement precision on each parameter are plotted along the vertical axis, showing biases of order \(10-100\sigma\). The horizontal axis shows the average correlations of the intrinsic and the unmeasured environmental effect parameter, showing a weak trend. Diagram from <a href="https://arxiv.org/abs/2312.13028" target="_blank">Kejriwal et al. (2023)</a>.</em>
  </figcaption>
</figure> 

Mathematically, environmental effects and beyond-GR modifications are generally expressed using simple power law expressions, added perturbatively to the leading-order equations of motion of the binary, see e.g. [Kocsis et al. (2011)](https://arxiv.org/abs/1104.2322) and [Barausse et al. (2014)](https://arxiv.org/abs/1404.7149), or directly to the final waveform in frequency domain, see e.g. [Yunes and Pretorius (2009)](https://arxiv.org/abs/0909.3328). When multiple such effects, which we generically tag as "beyond-vacuum-GR" effects, are being tested for during inference, the general expectation in the literature is then that they can simply be added together. However, using a generic mathematical framework, we show in our work [(Kejriwal et al. (2023))](https://arxiv.org/abs/2312.13028), that such setups can lead to extremely correlated posterior surfaces. Along with worsened inference efficiency, this also degrades the precision with which EMRI parameters can be measured. On the flip side, if such effects are excluded from the analysis but are present in the true signal, this can significantly bias the inference of EMRI's intrinsic parameters (more than \\(10\sigma\\)), effectively washing away any prospects of testing GR. Our study is a first of its kind to establish the severe impact that beyond-vacuum-GR effects can have on EMRI systems, and motivates further work to develop a consistent and systematic procedure to include such effects in the data analysis pipeline.  

<figure>
  <!-- Inline style on IMG sets DESKTOP max width -->
  <!-- CSS handles mobile scaling (width: 100%, max-width: 100%) -->
  <img src="{{ site.baseurl | default: '' }}/assets/biascorrected.png" alt="biases intrinsic" style="max-width: 450px;"/>
  <figcaption>
    <em>Figure 4: (Left panel): Schematic representation of how biases are induced to the set of signal parameters \(\psi_S, \varphi_S\) (blue cross) in a larger "signal space" (red cube) when inferred over a template space (grey manifold) which holds fixed one or more signal parameters to a fixed null value, in this case \(\varphi = \varphi_0\). The "best-fit" point is obtained at a biased location: \(\psi_{\rm MAP}, \varphi_0\). (Right panel): The scheme proposed in <a href="https://arxiv.org/abs/2503.01120" target="_blank">Kejriwal et al. (2025)</a> to correct the biases by obtaining posterior samples along the restricted axis (green stars along the vertical axis) and measuring the corresponding probability that \(\varphi \neq \varphi_0\).</em>
  </figcaption>
</figure> 

A major challenge in developing a systematic framework for inferring beyond-vacuum-GR effects is the shear number of such effects proposed in the literature. Given the cost of sampling the posterior surface in a single run with techniques like Markov Chain Monte Carlo (MCMC), and especially in the context of the LISA global fit inference pipeline, it is impractical to try and constrain all such effects simultaneously. Our latest work [(Kejriwal et al. (2025))](https://arxiv.org/abs/2503.01120) proposes an inference-based method to consistently and inexpensively obtain samples from the posterior surface in alternate beyond-vacuum-GR hypothesis, given just posterior samples from the vacuum-GR hypothesis. Within this novel framework, beyond-vacuuum-GR hypotheses can be quickly tested in a "post-processing" inference step.  

---

## Electromagnetic Counterparts of EMRIs

<figure>
  <!-- Inline style on IMG sets DESKTOP max width -->
  <!-- CSS handles mobile scaling (width: 100%, max-width: 100%) -->
  <img src="{{ site.baseurl | default: '' }}/assets/EMcounterpart.png" alt="biases intrinsic" style="max-width: 450px;"/>
  <figcaption>
    <em>Figure 5: A schematic depiction of an EMRI evolving in a matter-rich environment (yellow disk). Diagram from <a href="https://arxiv.org/abs/2404.00941" target="_blank">Kejriwal et al. (2024)</a> courtesy of Vojtěch Witzany.</em>
  </figcaption>
</figure> 

<figure>
  <!-- Inline style on IMG sets DESKTOP max width -->
  <!-- CSS handles mobile scaling (width: 100%, max-width: 100%) -->
  <img src="{{ site.baseurl | default: '' }}/assets/QPE.png" alt="biases intrinsic" style="max-width: 450px;"/>
  <figcaption>
    <em>Figure 6: Time-domain signal from the August 2020 run of eRO-QPE2 quasi-periodic eruption source. Diagram from  <a href="https://arxiv.org/abs/2411.00289" target="_blank">Pasham, Kejriwal et al. (2024)</a> courtesy of Dheeraj R. Pasham.</em>
  </figcaption>
</figure> 

Quasi-periodic eruption (QPE) events, which are low-frequency (\\(\sim 10^{-4}\\) Hz) signals of soft X-ray peaks over a quiescent background, are theorized to be electromagnetic (EM) counterparts of EMRIs. While EMRIs evolving in a vacuum are not expected to host EM counterparts, the presence of a disk around the MBH allows interactions with the compact object that can lead to EM counterparts in the X-ray or even ultraviolet bands, see e.g. [Linial and Metzger (2023)](https://arxiv.org/abs/2303.16231). This poses an exciting prospect of multimessenger astronomy with EMRIs. In our work, [(Kejriwal et al. (2024))](https://arxiv.org/abs/2404.00941), we calculated the frequency band of QPE sources that are emitting an EM signal "today", such that they may also be observed in the future by LISA as GW sources. We extended our analysis to a particularly promising QPO source (where the 'O' now stands for oscillations, not eruptions, distinguishing their intensity), RE J1034+396. REJ has shown a decreasing time period over two observations separated by a decade, which is expected of EMRIs. We found that a compact object orbiting the MBH in REJ may be of mass \\(\approx 47 M_\odot\\) and that there is a \\(\approx 25\%\\) probability that REJ (if it *is* an EMRI and follows its current inspiral trend) would be detected in the LISA band. Our study is a first of its kind to comment on the multimessenger prospects of LISA EMRIs.  

---

## Developing Waveform Models and Data Analysis Tools

  These are ongoing projects under this theme:  
  
  - **Latest waveform models:** As described in the first section, EMRIs in the LISA band will be late-stage inspirals of compact objects around MBHs. They are modeled using black hole perturbation theory and self-force theory [(Barack and Pound (2018))](https://arxiv.org/abs/1805.10385), solving Einstein's field equations perturbatively expanded in the small-mass-ratio. Waveform models can differ in accuracy or coverage of the parameter space, although ultimately, both aspects will need to be married for EMRI science with LISA. An ongoing project aims to close this gap with a waveform model that is fully relativistic at the adiabatic (leading)-order, and approximates higher-order corrections using a post-Newtonian expansion. I am involved in the code implementation of this model and in studying its data analysis implications for LISA search and inference.  
  
  - **`FastEMRIWaveforms (FEW)` Suite:** To perform data analysis with a given model, rapid waveform evaluation is required at each parameter point. The `FastEMRIWaveforms (FEW)` package [(Katz et al. (2021))](https://arxiv.org/abs/2104.04582) provides the framework to generate such waveforms, augmented by GPU-acceleration and strategically setting mode-selection cutoffs. I am involved in the development of the latest version of `FEW` and studying the data analysis implications for the latest KerrEccentricEquatorial model being introduced in this release. The manuscript is now available on arXiv: [C. E. A. Chapman-Bird et al. (2025)](https://arxiv.org/abs/2506.09470).  

  - **`StableEMRIFishers (SEF)` Package:** Fisher Information Matrices (FIMs) describe the information content of the signal at a parameter point \\(\boldsymbol{\theta}\\), and its inverse provides an upper-bound on measurement precision of \\(\boldsymbol{\theta}\\). In preparatory science for LISA and EMRIs, FIMs thus play a significant role in studies spanning large parameter spaces, where more accurate but expensive methods like MCMC become impractical. However, obtaining the FIM for GW waveforms involves taking their derivatives, which can be especially challenging for highly-correlated posterior surfaces [(Vallisneri (2007))](https://arxiv.org/abs/gr-qc/0703086), characteristic of EMRIs. In addition, various approximations are made in practical waveform generation to enable their fast computation, which amplifies the problem by introducing small "jitters" in the likelihood surface, especially for strong-field signals. In a manuscript under preparation, we have formulated a robust FIM calculator, `StableEMRIFishers (SEF)`, that attempts to systematically calculate stable derivatives and hence the FIMs given an input EMRI parameter point \\(\boldsymbol{\theta}\\). The `StableEMRIFishers (SEF)` code is used in published and ongoing studies, see e.g. [Duque et al. (2024)](https://arxiv.org/abs/2411.03436).  

---  

© 2025 Shubham Kejriwal
