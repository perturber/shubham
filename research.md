---
title: Research
permalink: /research/
mathjax: true
---

<h1 class="page-title">Research</h1>
<p class="page-lede">An overview of the main themes of my research. For details, see the <a href="{{ site.baseurl }}/publications/">papers</a>.</p>

<div class="card" markdown="1">

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

EMRI signals stay in the LISA band for months to years and complete $$\sim 10^5$$ orbital cycles. That lets us map the spacetime around massive black holes and test General Relativity (GR) very precisely. Their long inspirals also make them sensitive to small perturbations, such as torques from an accretion disk or deviations from GR.

This sensitivity is both an opportunity and a challenge. Leaving such "beyond-vacuum-GR" effects out of the analysis can badly bias the inferred source parameters, while including several at once introduces strong correlations between them. A large part of my work is developing inference methods that measure these effects reliably and cheaply, for single sources and across a population, and that stay robust when the waveform models or the data are imperfect.

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
