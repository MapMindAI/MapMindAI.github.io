---
layout: base
title: MapMindAI — Open-source AI-powered SLAM for robotics
meta-description: MapMindAI builds open-source SLAM, visual localization, edge AI inference, and robot control tools for autonomous robotics.
css:
  - /assets/css/index.css
---

<section class="mm-hero">
  <div class="mm-hero__glow mm-hero__glow--a"></div>
  <div class="mm-hero__glow mm-hero__glow--b"></div>
  <div class="mm-hero__grid"></div>
  <div class="mm-hero__inner">
    <p class="mm-eyebrow">MapMindAI // Open Source Robotics</p>
    <h1 class="mm-hero__title">AI-Powered SLAM<br>for Autonomous Robots</h1>
    <p class="mm-hero__subtitle">We build open-source mapping, localization, and perception tools — from LiDAR SLAM to visual odometry on the edge — so robots can understand the world around them.</p>
    <div class="mm-hero__ctas">
      <a href="#projects" class="mm-btn mm-btn--primary">Explore Projects</a>
      <a href="https://github.com/MapMindAI" class="mm-btn mm-btn--ghost" target="_blank" rel="noopener">View on GitHub ↗</a>
    </div>
    <p class="mm-hero__note">11 open-source repositories · Hong Kong</p>
  </div>
</section>

<section class="mm-strip">
  <div class="mm-strip__inner">
    <span class="mm-chip">FAST-LIO2</span>
    <span class="mm-chip">ESIKF / ESKF</span>
    <span class="mm-chip">ONNX · TensorRT</span>
    <span class="mm-chip">Depth Anything</span>
    <span class="mm-chip">SuperPoint · LightGlue</span>
    <span class="mm-chip">ESP32 · WebRTC</span>
    <span class="mm-chip">Gaussian Splatting</span>
  </div>
</section>

<section id="focus" class="mm-section">
  <div class="mm-section__head">
    <p class="mm-eyebrow">What we build</p>
    <h2 class="mm-section__title">Focus Areas</h2>
  </div>
  <div class="mm-feature-grid">
    {% for info in site.data.learn_info %}
    <div class="mm-feature-card">
      <div class="mm-feature-card__icon">{{ info.icon }}</div>
      <div class="mm-feature-card__text">{{ info.content }}</div>
    </div>
    {% endfor %}
  </div>
</section>

<section id="projects" class="mm-section mm-section--muted">
  <div class="mm-section__head">
    <p class="mm-eyebrow">Open Source</p>
    <h2 class="mm-section__title">Projects</h2>
    <p class="mm-section__desc">Every project ships in the open under the <a href="https://github.com/MapMindAI" target="_blank" rel="noopener">MapMindAI</a> organization on GitHub.</p>
  </div>
  <div class="mm-project-grid">
    {% for app in site.data.portfolio %}
    <a class="mm-project-card" href="{{ app.url }}" target="_blank" rel="noopener">
      <span class="mm-project-card__tag">{{ app.tag }}</span>
      <h3 class="mm-project-card__title">{{ app.title }}</h3>
      <p class="mm-project-card__desc">{{ app.description }}</p>
      <span class="mm-project-card__link">View source ↗</span>
    </a>
    {% endfor %}
  </div>
</section>

<section class="mm-cta">
  <div class="mm-cta__glow"></div>
  <div class="mm-cta__inner">
    <h2>Building robots? Start here.</h2>
    <p>Every project is open source, documented, and built for developers and makers to extend.</p>
    <div class="mm-hero__ctas">
      <a href="https://github.com/MapMindAI" class="mm-btn mm-btn--primary" target="_blank" rel="noopener">Browse the GitHub org ↗</a>
      <a href="{{ 'aboutme' | relative_url }}" class="mm-btn mm-btn--ghost">About MapMindAI</a>
    </div>
  </div>
</section>
