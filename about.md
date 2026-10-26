---
title: About
permalink: /about/
---

<h1 class="page-title">About</h1>
<p class="page-lede">Education, positions and awards, plus a little about life outside research.</p>

I am a gravitational-wave astronomer working on data analysis pipelines for future detectors, including the Laser Interferometer Space Antenna (LISA). I employ various Bayesian statistics and machine learning techniques in my work, and have also helped develop new inference methods with the help of these tools.

<h2 class="section-title">Positions</h2>

<div class="card">
  <div class="entry">
    <div class="entry-head"><span class="entry-title">Postdoctoral Researcher</span><span class="entry-meta">2026 – present</span></div>
    <div class="entry-sub"><a href="https://www.aei.mpg.de/">Max Planck Institute for Gravitational Physics (Albert Einstein Institute)</a>, Potsdam, Germany</div>
    <ul>
      <li>Astrophysical and Cosmological Relativity (ACR) group; supervisor: Dr. Jonathan Gair</li>
      <li>Supported by the ERC grant <em>"Making Sense of the Unexpected in the Gravitational-Wave Sky"</em></li>
    </ul>
  </div>
</div>

<h2 class="section-title">Education</h2>

<div class="card">
  <div class="entry">
    <div class="entry-head"><span class="entry-title">Ph.D. in Physics</span><span class="entry-meta">2023 – 2026</span></div>
    <div class="entry-sub"><a href="https://www.nus.edu.sg/">National University of Singapore</a>, Gravitational Waves Group, Department of Physics</div>
    <ul>
      <li>Thesis: <em>"New Challenges in Gravitational Wave Astronomy: data analysis implications of extreme-mass-ratio inspirals as precision astronomy probes"</em></li>
      <li>Advisor: <a href="https://www.physics.nus.edu.sg/faculty/chua-alvin-jk/">Asst. Prof. Alvin J. K. Chua</a></li>
    </ul>
  </div>
  <div class="entry">
    <div class="entry-head"><span class="entry-title">B.Sc. (Research) in Physics, Minor in Mathematics (Distinction)</span><span class="entry-meta">2018 – 2022</span></div>
    <div class="entry-sub"><a href="https://snu.edu.in/home/">Shiv Nadar University</a>, Delhi, India</div>
    <ul>
      <li>Thesis: <em>"On the Effects of Relative Motion on Gravitational Waves from Extreme-Mass-Ratio Inspirals"</em></li>
      <li>Advisors: Asst. Prof. Arindam Chatterjee (internal), Asst. Prof. Alvin J. K. Chua (external)</li>
    </ul>
  </div>
</div>

<h2 class="section-title">Awards</h2>

- NUS Department of Physics Best Graduate Researcher Award (2025)
- NUS Research Scholarship (2023–2026)
- Dean's List Academic Excellence Award (×3), Shiv Nadar University (2019, 2020)

<h2 class="section-title">Beyond academia</h2>

When I'm not working, I sometimes [vlog](https://www.youtube.com/@ShubhamKejriwal). I love travelling and trying different cuisines, within the limits of being vegetarian. I'm a big Formula One fan. I enjoy both trekking and swimming, so I'm a mountain *and* a beach person.

<div class="gallery">
  <figure><img src="{{ site.baseurl }}/assets/icecave.jpg" alt="Inside an ice cave" loading="lazy"><figcaption>Ice cave on Katla Glacier, Iceland</figcaption></figure>
  <figure><img src="{{ site.baseurl }}/assets/swissalps.jpg" alt="The Alps seen from Mt. Pilatus" loading="lazy"><figcaption>The Alps from Mt. Pilatus, Switzerland</figcaption></figure>
  <figure><img src="{{ site.baseurl }}/assets/joshuatree.jpg" alt="Night sky over Joshua Tree" loading="lazy"><figcaption>Night sky, Joshua Tree, USA</figcaption></figure>
  <figure><img src="{{ site.baseurl }}/assets/mtbromo.jpg" alt="Mt. Bromo" loading="lazy"><figcaption>Mt. Bromo, Indonesia</figcaption></figure>
  <figure><img src="{{ site.baseurl }}/assets/bambooforestjapan.jpg" alt="Bamboo forest" loading="lazy"><figcaption>Bamboo forest near Kyoto, Japan</figcaption></figure>
  <figure><img src="{{ site.baseurl }}/assets/krabi.jpg" alt="Ao Nang beach" loading="lazy"><figcaption>Ao Nang Beach, Krabi, Thailand</figcaption></figure>
</div>

<div class="lightbox" id="lightbox" role="dialog" aria-modal="true" aria-label="Photo viewer">
  <button class="lightbox-btn lightbox-close" aria-label="Close"><i class="fas fa-xmark"></i></button>
  <button class="lightbox-btn lightbox-prev" aria-label="Previous photo"><i class="fas fa-chevron-left"></i></button>
  <figure class="lightbox-figure">
    <img alt="">
    <figcaption><span class="lightbox-caption"></span><span class="lightbox-count"></span></figcaption>
  </figure>
  <button class="lightbox-btn lightbox-next" aria-label="Next photo"><i class="fas fa-chevron-right"></i></button>
</div>

<script>
(function () {
  var items = Array.prototype.slice.call(document.querySelectorAll(".gallery figure"));
  var box = document.getElementById("lightbox");
  var img = box.querySelector("img");
  var cap = box.querySelector(".lightbox-caption");
  var count = box.querySelector(".lightbox-count");
  var index = 0, lastFocus = null;

  function show(i) {
    index = (i + items.length) % items.length;
    var src = items[index].querySelector("img");
    img.src = src.src;
    img.alt = src.alt;
    cap.textContent = items[index].querySelector("figcaption").textContent;
    count.textContent = (index + 1) + " / " + items.length;
  }
  function open(i) {
    lastFocus = document.activeElement;
    show(i);
    box.classList.add("open");
    document.body.classList.add("lightbox-open");
    box.querySelector(".lightbox-close").focus();
  }
  function close() {
    box.classList.remove("open");
    document.body.classList.remove("lightbox-open");
    if (lastFocus) lastFocus.focus();
  }

  items.forEach(function (fig, i) {
    fig.tabIndex = 0;
    fig.setAttribute("role", "button");
    fig.setAttribute("aria-label", "View photo: " + fig.querySelector("figcaption").textContent);
    fig.addEventListener("click", function () { open(i); });
    fig.addEventListener("keydown", function (e) {
      if (e.key === "Enter" || e.key === " ") { e.preventDefault(); open(i); }
    });
  });

  box.querySelector(".lightbox-prev").addEventListener("click", function () { show(index - 1); });
  box.querySelector(".lightbox-next").addEventListener("click", function () { show(index + 1); });
  box.querySelector(".lightbox-close").addEventListener("click", close);
  box.addEventListener("click", function (e) { if (e.target === box) close(); });

  document.addEventListener("keydown", function (e) {
    if (!box.classList.contains("open")) return;
    if (e.key === "Escape") close();
    else if (e.key === "ArrowLeft") show(index - 1);
    else if (e.key === "ArrowRight") show(index + 1);
  });

  var startX = null;
  box.addEventListener("touchstart", function (e) { startX = e.touches[0].clientX; }, { passive: true });
  box.addEventListener("touchend", function (e) {
    if (startX === null) return;
    var dx = e.changedTouches[0].clientX - startX;
    if (Math.abs(dx) > 50) show(dx > 0 ? index - 1 : index + 1);
    startX = null;
  });
})();
</script>
