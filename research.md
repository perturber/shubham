---
layout: default
title: Research
permalink: /research/
mathjax: true
---

# Research Overview  

<div class="bubble" markdown="1">

Below, I provide a slightly more elaborate (and mostly self-contained) overview of my research. Still, the best way to learn about my research is to read my articles. You can find them on the [Publications](/shubham/publications) page.  

</div>

<div class="bubble" markdown="1">

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

I work on the data analysis pipeline for the Laser Interferometer Space Antenna (LISA) [(NASA)](https://lisa.nasa.gov/), scheduled for launch in the mid-2030s [(ESA)](https://www.esa.int/Science_Exploration/Space_Science/LISA/Capturing_the_ripples_of_spacetime_LISA_gets_go-ahead). LISA will be sensitive to gravitational waves from galactic binaries, supermassive black hole mergers, and extreme-mass-ratio inspirals (EMRIs) in which a stellar-mass black hole orbits a supermassive one [(LISA Collaboration)](https://arxiv.org/abs/2402.07571). EMRIs are my primary focus.


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


Gravitational wave signals from EMRIs will last in the LISA band for years, allowing us to map the curvature of spacetime around supermassive black holes and test General Relativity (GR) with high precision. Their long inspirals also make them sensitive to environmental effects, such as migration torques from accretion disks.

</div>

<div class="bubble" markdown="1">

## Measurability of "Beyond-Vacuum-GR" effects in EMRIs  

<figure>
  <!-- Inline style on IMG sets DESKTOP max width -->
  <!-- CSS handles mobile scaling (width: 100%, max-width: 100%) -->
  <img src="{{ site.baseurl | default: '' }}/assets/joint_analysis/correlation_bias-1.png" alt="biases intrinsic" style="max-width: 450px;"/>
  <figcaption>
    <em>Figure 3: Biases (in \(\sigma\)'s) induced on the EMRI's intrinsic parameters due to an environmental effect in the signal which was not accounted for in the inference. Diagram from <a href="https://arxiv.org/abs/2312.13028" target="_blank">Kejriwal et al. (2023)</a>.</em>
  </figcaption>
</figure> 

Many proposed environmental and beyond-GR effects are added perturbatively to the EMRI's dynamics, see e.g. [Kocsis et al. (2011)](https://arxiv.org/abs/1104.2322), [Barausse et al. (2014)](https://arxiv.org/abs/1404.7149), and [Yunes and Pretorius (2009)](https://arxiv.org/abs/0909.3328). Using a generic mathematical framework, we show in our work [(Kejriwal et al. (2023))](https://arxiv.org/abs/2312.13028), that such setups can cause strong parameter correlations when multiple effects are measured simultaneously, worsening inference. On the other hand, excluding such effects from the analysis can significantly bias the inferred parameters (by \\(\gtrsim 10\sigma\\)).

</div>

<div class="bubble" markdown="1">

## Bias-Corrected Importance Sampling

<figure>
  <!-- Inline style on IMG sets DESKTOP max width -->
  <!-- CSS handles mobile scaling (width: 100%, max-width: 100%) -->
  <img src="{{ site.baseurl | default: '' }}/assets/biascorrected.png" alt="biases intrinsic" style="max-width: 450px;"/>
  <figcaption>
    <em>Figure 4: (Left panel): How biases are induced to the set of signal parameters \(\psi_S, \varphi_S\). (Right panel): The scheme proposed in <a href="https://arxiv.org/abs/2503.01120" target="_blank">Kejriwal et al. (2025)</a> to correct the biases by obtaining posterior samples along a "correction" axis.</em>
  </figcaption>
</figure> 

The cost of inference under a single hypothesis can be overwhelming, especially in the context of the LISA global fit pipeline. It is thus impractical to perform tests of environmental and beyond-GR modifications using conventional methods. In our work [(Kejriwal et al. (2025))](https://arxiv.org/abs/2503.01120), we proposes bias-corrected importance sampling, which can consistently and inexpensively obtain samples from the posterior in alternative hypotheses, given just the posterior samples under vacuum-GR.

</div>

<div class="bubble" markdown="1">

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

Quasi-periodic eruptions (QPEs) are low-frequency (\\(\sim 10^{-4}\\) Hz) soft X-ray band signals, and are emerging as candidate electromagnetic counterparts of EMRIs with accretion disks, see e.g. [Linial and Metzger (2023)](https://arxiv.org/abs/2303.16231). This poses an exciting prospect of multimessenger astronomy with EMRIs. In our work, [(Kejriwal et al. (2024))](https://arxiv.org/abs/2404.00941), we analyzed the prospect of simultaneously observing EMRIs in the X-ray band and as GWs. Such sources open a new avenue of multimessenger astronomy with EMRIs. We also analyzed RE J1034+396, a QP'O' (where 'O' is now for 'oscillations'). We found that REJ may host an orbiting compact object of mass \\(\approx 47 M_\odot\\). We also estimated that there is a \\(\approx 25\%\\) probability that REJ may be detected by LISA.

</div>

<div class="bubble" markdown="1">

## Developing Waveform Models and Data Analysis Tools

  There are multiple ongoing projects that I am actively contributing to:
  
  - **Waveform modeling:** We are developing the `SuperKludge`: a hybridized waveform model that can be used for practical data analysis of EMRIs.
  
  - **`FastEMRIWaveforms (FEW)`:** I am involved in the development of `FEW v2.0` and its data analysis implications. The pre-print is now available [here](https://arxiv.org/abs/2506.09470v1). 

  - **`StableEMRIFisher (SEF)`:** I am the creater of `StableEMRIFisher (SEF)`, a package to generate fast and robust information matrices for EMRIs. `SEF` is available publically on [Github](https://github.com/perturber/StableEMRIFisher).

<style>
.bubble {
  background: #fff;
  border-radius: 12px;
  padding: 20px;
  margin: 20px 0;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}
.video-container {
  position: relative; overflow: hidden; width: 100%; max-width: 560px; margin: auto;
}
.video-container::before { content: ""; display: block; padding-top: 56.25%; }
.video-container iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0; }
</style> 

© 2025 Shubham Kejriwal
