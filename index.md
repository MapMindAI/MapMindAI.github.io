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
      <a href="#showcase" class="mm-btn mm-btn--primary">See It In Action</a>
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

<section id="focus" class="mm-section mm-section--muted">
  <div class="mm-section__head">
    <p class="mm-eyebrow">At a glance</p>
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

<section id="showcase" class="mm-section">
  <div class="mm-section__head">
    <p class="mm-eyebrow">What We Build</p>
    <h2 class="mm-section__title">In Action</h2>
  </div>

  <div class="mm-sector">
    <div class="mm-sector__media mm-sector__media--gallery">
      <figure class="mm-sector__figure">
        <video class="mm-sector__video" controls preload="none" poster="{{ '/assets/videos/posters/color_mapping_1.jpg' | relative_url }}">
          <source src="{{ '/assets/videos/color_mapping_1.mp4' | relative_url }}" type="video/mp4">
        </video>
        <figcaption class="mm-sector__caption">Color Mapping — Demo 1</figcaption>
      </figure>
      <figure class="mm-sector__figure">
        <video class="mm-sector__video" controls preload="none" poster="{{ '/assets/videos/posters/color_mapping_2.jpg' | relative_url }}">
          <source src="{{ '/assets/videos/color_mapping_2.mp4' | relative_url }}" type="video/mp4">
        </video>
        <figcaption class="mm-sector__caption">Color Mapping — Demo 2</figcaption>
      </figure>
      <figure class="mm-sector__figure">
        <video class="mm-sector__video" controls preload="none" poster="{{ '/assets/videos/posters/rtk_mapping_1.jpg' | relative_url }}">
          <source src="{{ '/assets/videos/rtk_mapping_1.mp4' | relative_url }}" type="video/mp4">
        </video>
        <figcaption class="mm-sector__caption">RTK-Verified Mapping — Demo 1</figcaption>
      </figure>
      <figure class="mm-sector__figure">
        <video class="mm-sector__video" controls preload="none" poster="{{ '/assets/videos/posters/rtk_mapping_2.jpg' | relative_url }}">
          <source src="{{ '/assets/videos/rtk_mapping_2.mp4' | relative_url }}" type="video/mp4">
        </video>
        <figcaption class="mm-sector__caption">RTK-Verified Mapping — Demo 2</figcaption>
      </figure>
    </div>
    <div class="mm-sector__copy">
      <p class="mm-eyebrow">Sector 01</p>
      <h3 class="mm-sector__title">Unilidar Color 3D Scanner</h3>
      <p class="mm-sector__desc">Real-time colorized point clouds from the Unitree Lidar L2, fused with camera color and a live trajectory overlay. Mapping accuracy is verified against RTK GNSS ground truth, powered by FAST-LIO2 and ESIKF sensor fusion.</p>
      <ul class="mm-sector__links">
        <li><a href="https://github.com/MapMindAI/UniLidar-SDK-Mapping" target="_blank" rel="noopener">UniLidar-SDK-Mapping ↗</a></li>
        <li><a href="https://github.com/MapMindAI/UniLidar-SDK-Collection" target="_blank" rel="noopener">UniLidar-SDK-Collection ↗</a></li>
      </ul>
    </div>
  </div>

  <div class="mm-sector mm-sector--reverse">
    <div class="mm-sector__media mm-sector__media--stack">
      <video class="mm-sector__video mm-sector__video--single" controls preload="none" poster="{{ '/assets/videos/posters/esp32_robot_test.jpg' | relative_url }}">
        <source src="{{ '/assets/videos/esp32_robot_test.mp4' | relative_url }}" type="video/mp4">
      </video>
      <div class="mm-spec-panel">
        <p class="mm-spec-panel__label">Hardware / Software Spec</p>
        <div class="mm-spec-panel__grid">
          <div class="mm-spec-panel__item">
            <span class="mm-spec-panel__key">MCU</span>
            <span class="mm-spec-panel__value">ESP32-WROOM-32</span>
          </div>
          <div class="mm-spec-panel__item">
            <span class="mm-spec-panel__key">Video</span>
            <span class="mm-spec-panel__value">WebRTC · H.264</span>
          </div>
          <div class="mm-spec-panel__item">
            <span class="mm-spec-panel__key">Control</span>
            <span class="mm-spec-panel__value">MQTT + CAN bus</span>
          </div>
          <div class="mm-spec-panel__item">
            <span class="mm-spec-panel__key">Link</span>
            <span class="mm-spec-panel__value">Wi-Fi, low-latency</span>
          </div>
        </div>
      </div>
    </div>
    <div class="mm-sector__copy">
      <p class="mm-eyebrow">Sector 02</p>
      <h3 class="mm-sector__title">ESP32 Robot Platform</h3>
      <p class="mm-sector__desc">A low-cost, hackable robot base driven entirely by an ESP32 — live WebRTC video, low-latency drive controls from a tablet, and MQTT/CAN bus integration for talking to other hardware on the robot.</p>
      <ul class="mm-sector__links">
        <li><a href="https://github.com/MapMindAI/ESP32-Robot-Control" target="_blank" rel="noopener">ESP32-Robot-Control ↗</a></li>
        <li><a href="https://github.com/MapMindAI/ESP32-Robot-WebRTC" target="_blank" rel="noopener">ESP32-Robot-WebRTC ↗</a></li>
      </ul>
    </div>
  </div>

  <div class="mm-sector">
    <div class="mm-sector__media mm-sector__media--stack">
      <figure class="mm-sector__figure">
        <video class="mm-sector__video mm-sector__video--da3" controls preload="none" poster="{{ '/assets/videos/posters/da3_rk3588.jpg' | relative_url }}">
          <source src="{{ '/assets/videos/da3_rk3588.mp4' | relative_url }}" type="video/mp4">
        </video>
        <figcaption class="mm-sector__caption">DA3 split stream — RGB, depth, and 3D trajectory</figcaption>
      </figure>
      <figure class="mm-sector__figure">
        <video class="mm-sector__video mm-sector__video--wide" controls preload="none" poster="{{ '/assets/videos/posters/arcore_da_depth_compare.jpg' | relative_url }}">
          <source src="{{ '/assets/videos/arcore_da_depth_compare.mp4' | relative_url }}" type="video/mp4">
        </video>
        <figcaption class="mm-sector__caption">RGB vs. ARCore depth vs. Depth Anything depth</figcaption>
      </figure>
    </div>
    <div class="mm-sector__copy">
      <p class="mm-eyebrow">Sector 03</p>
      <h3 class="mm-sector__title">Depth Anything Edge Pipeline</h3>
      <p class="mm-sector__desc">Benchmarking and deploying Depth Anything for monocular depth and visual odometry on embedded hardware — live RGB, rendered depth, and a streamed 3D trajectory/point cloud, served through a single Dockerized ONNX/TensorRT inference stack alongside SuperPoint and LightGlue.</p>
      <div class="mm-pipeline__row mm-pipeline__row--inline">
        <span>Depth Anything 2/3</span>
        <span class="mm-pipeline__arrow">→</span>
        <span>ONNX</span>
        <span class="mm-pipeline__arrow">→</span>
        <span>TensorRT</span>
        <span class="mm-pipeline__arrow">→</span>
        <span>RK3588 / GPU</span>
      </div>
      <ul class="mm-sector__links">
        <li><a href="https://github.com/MapMindAI/DepthAnythingOnnx" target="_blank" rel="noopener">DepthAnythingOnnx ↗</a></li>
        <li><a href="https://github.com/MapMindAI/DA3-RK3588" target="_blank" rel="noopener">DA3-RK3588 ↗</a></li>
        <li><a href="https://github.com/MapMindAI/EasyTensorRT" target="_blank" rel="noopener">EasyTensorRT ↗</a></li>
      </ul>
    </div>
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
