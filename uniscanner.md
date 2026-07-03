---
layout: base
title: UniScanner — UniLidar L2 Handheld 3D Scanner
meta-description: UniScanner is a ~$700 open-source handheld 3D scanning rig built on the UniLidar L2, producing colored point clouds and Gaussian Splatting scenes.
css:
  - /assets/css/index.css
  - /assets/css/uniscanner.css
---

<section class="us-hero">
  <div class="us-hero__glow"></div>
  <div class="us-hero__inner">
    <div class="us-hero__copy">
      <p class="mm-eyebrow">MapMindAI // Hardware</p>
      <h1 class="us-hero__title">UniScanner</h1>
      <p class="us-hero__subtitle">Professional 3D scanning. Now in your hands.</p>
      <p class="us-hero__desc">A handheld 3D digital acquisition rig built around the UniLidar L2 — combining LiDAR, IMU, and RGB camera to capture colored point clouds and Gaussian Splatting scenes, for about the cost of a phone.</p>
      <div class="mm-hero__ctas">
        <a href="#specs" class="mm-btn mm-btn--primary">See Specs</a>
        <a href="https://github.com/MapMindAI" target="_blank" rel="noopener" class="mm-btn mm-btn--ghost">View on GitHub ↗</a>
      </div>
      <p class="us-hero__price"><span class="us-hero__price-value">~$700</span> base build · <a href="#configurations">optional upgrades</a></p>
    </div>
    <div class="us-hero__media">
      <img src="{{ '/assets/img/uniscanner/hero.jpg' | relative_url }}" alt="UniScanner handheld 3D scanner with live point cloud scan on tablet and phone" width="1448" height="1086">
    </div>
  </div>
</section>

<section class="mm-strip">
  <div class="mm-strip__inner">
    <span class="mm-chip">Real-time Point Cloud</span>
    <span class="mm-chip">360° Scanning</span>
    <span class="mm-chip">&lt; 700g</span>
    <span class="mm-chip">USB-C</span>
    <span class="mm-chip">SDK / ROS</span>
    <span class="mm-chip">Low-Cost, High-Performance</span>
  </div>
</section>

<section class="mm-section mm-section--muted">
  <div class="mm-section__head">
    <p class="mm-eyebrow">Real Results</p>
    <h2 class="mm-section__title">Not a Render — Real Scans</h2>
  </div>
  <div class="mm-sector__media mm-sector__media--gallery us-results-grid">
    <figure class="mm-sector__figure">
      <video class="mm-sector__video" controls preload="none" poster="{{ '/assets/videos/posters/color_mapping_1.jpg' | relative_url }}">
        <source src="{{ '/assets/videos/color_mapping_1.mp4' | relative_url }}" type="video/mp4">
      </video>
      <figcaption class="mm-sector__caption">Colored Point Cloud — Demo 1</figcaption>
    </figure>
    <figure class="mm-sector__figure">
      <video class="mm-sector__video" controls preload="none" poster="{{ '/assets/videos/posters/color_mapping_2.jpg' | relative_url }}">
        <source src="{{ '/assets/videos/color_mapping_2.mp4' | relative_url }}" type="video/mp4">
      </video>
      <figcaption class="mm-sector__caption">Colored Point Cloud — Demo 2</figcaption>
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
</section>


<section class="mm-section">
  <div class="mm-section__head">
    <p class="mm-eyebrow">Inside the Scanner</p>
    <h2 class="mm-section__title">Built to Take Apart</h2>
    <p class="mm-section__desc">Precision-engineered components designed for performance, reliability, and developer extensibility.</p>
  </div>
  <div class="us-anatomy">
    <img src="{{ '/assets/img/uniscanner/exploded.jpg' | relative_url }}" alt="Exploded view of the UniScanner showing LiDAR head, RGB camera module, compute board, thermal system, battery pack, handle shell, USB-C base, and optional RTK module" width="1448" height="1086">
  </div>
  <ul class="us-parts-list">
    <li><span class="us-parts-list__num">1</span><div><strong>LiDAR Head</strong><span>UniLidar L2 360° LiDAR sensor</span></div></li>
    <li><span class="us-parts-list__num">2</span><div><strong>RGB Camera Module</strong><span>1920 × 1080 global shutter</span></div></li>
    <li><span class="us-parts-list__num">3</span><div><strong>Compute Board</strong><span>High-performance SoC for SLAM &amp; data processing</span></div></li>
    <li><span class="us-parts-list__num">4</span><div><strong>Thermal System</strong><span>Heat spreader + graphite sheet, passive cooling path</span></div></li>
    <li><span class="us-parts-list__num">5</span><div><strong>Battery Pack</strong><span>12V 5200mAh, hot-swappable Li-ion</span></div></li>
    <li><span class="us-parts-list__num">6</span><div><strong>Handle Shell</strong><span>Ergonomic overmolded grip, polycarbonate + TPE</span></div></li>
    <li><span class="us-parts-list__num">7</span><div><strong>USB-C Base</strong><span>Data / charging interface</span></div></li>
    <li><span class="us-parts-list__num">8</span><div><strong>RTK Module</strong><span>Optional high-precision GNSS for georeferenced scans</span></div></li>
  </ul>
</section>

<section class="mm-section mm-section--muted">
  <div class="mm-section__head">
    <p class="mm-eyebrow">Configurations</p>
    <h2 class="mm-section__title" id="configurations">Start at $700</h2>
    <p class="mm-section__desc">A complete scanning rig ready out of the box, with optional upgrades for georeferencing and on-device real-time reconstruction.</p>
  </div>
  <div class="us-pricing-grid">
    <div class="us-pricing-card us-pricing-card--base">
      <p class="us-pricing-card__tier">Base Build</p>
      <p class="us-pricing-card__price">~$700</p>
      <ul class="us-pricing-card__items us-pricing-card__items--plain">
        <li>Unitree UniLidar L2 360° LiDAR</li>
        <li>RK3566 acquisition host + Web UI</li>
        <li>2K RGB camera</li>
        <li>12V Li-ion battery, hot-swappable</li>
      </ul>
      <p class="us-pricing-card__note">Everything needed to collect data and produce colored point clouds.</p>
    </div>
    <div class="us-pricing-card">
      <p class="us-pricing-card__tier">+ RTK Module</p>
      <p class="us-pricing-card__price">+$60</p>
      <p class="us-pricing-card__note">Optional high-precision GNSS for globally consistent trajectories and stronger loop-closure constraints.</p>
    </div>
    <div class="us-pricing-card">
      <p class="us-pricing-card__tier">+ RK3588 Real-Time</p>
      <p class="us-pricing-card__price">+$280</p>
      <p class="us-pricing-card__note">On-device compute upgrade for real-time mapping — turns the rig into an acquisition + reconstruction all-in-one.</p>
    </div>
  </div>
</section>

<section class="mm-section" id="specs">
  <div class="mm-section__head">
    <p class="mm-eyebrow">Engineering</p>
    <h2 class="mm-section__title">Spec Sheet</h2>
  </div>
  <div class="us-blueprint">
    <img src="{{ '/assets/img/uniscanner/engineering-drawing.jpg' | relative_url }}" alt="UniScanner engineering drawing with front, side, back, and top views, dimensions, and specification table" width="1448" height="1086">
  </div>
  <div class="mm-spec-panel us-spec-panel--wide">
    <p class="mm-spec-panel__label">Specifications</p>
    <div class="mm-spec-panel__grid us-spec-panel__grid--wide">
      <div class="mm-spec-panel__item"><span class="mm-spec-panel__key">LiDAR</span><span class="mm-spec-panel__value">UniLidar L2 (360°)</span></div>
      <div class="mm-spec-panel__item"><span class="mm-spec-panel__key">Camera</span><span class="mm-spec-panel__value">2K RGB global shutter (1920×1080)</span></div>
      <div class="mm-spec-panel__item"><span class="mm-spec-panel__key">Accuracy</span><span class="mm-spec-panel__value">±20 mm (typical)</span></div>
      <div class="mm-spec-panel__item"><span class="mm-spec-panel__key">Range</span><span class="mm-spec-panel__value">0.05 – 120 m</span></div>
      <div class="mm-spec-panel__item"><span class="mm-spec-panel__key">FOV (LiDAR)</span><span class="mm-spec-panel__value">360° × 59°</span></div>
      <div class="mm-spec-panel__item"><span class="mm-spec-panel__key">Point Rate</span><span class="mm-spec-panel__value">Up to 640,000 pts/s</span></div>
      <div class="mm-spec-panel__item"><span class="mm-spec-panel__key">Battery</span><span class="mm-spec-panel__value">12V, 5200mAh (62.4Wh)</span></div>
      <div class="mm-spec-panel__item"><span class="mm-spec-panel__key">Runtime</span><span class="mm-spec-panel__value">Up to 2.5 hrs (typical)</span></div>
      <div class="mm-spec-panel__item"><span class="mm-spec-panel__key">Weight</span><span class="mm-spec-panel__value">&lt; 700 g</span></div>
      <div class="mm-spec-panel__item"><span class="mm-spec-panel__key">Connectivity</span><span class="mm-spec-panel__value">USB-C, Wi-Fi (optional)</span></div>
      <div class="mm-spec-panel__item"><span class="mm-spec-panel__key">Operating Temp.</span><span class="mm-spec-panel__value">-10°C to 50°C</span></div>
      <div class="mm-spec-panel__item"><span class="mm-spec-panel__key">IP Rating</span><span class="mm-spec-panel__value">IP54</span></div>
    </div>
  </div>
</section>

<section class="mm-section mm-section--muted">
  <div class="mm-section__head">
    <p class="mm-eyebrow">Multi-Angle &amp; Mounts</p>
    <h2 class="mm-section__title">One Body, Two Accessories</h2>
    <p class="mm-section__desc">A 1/4"-20 threaded mount accepts the optional RTK module or a phone mount for on-the-go compute and display.</p>
  </div>
  <div class="us-anatomy">
    <img src="{{ '/assets/img/uniscanner/overview.jpg' | relative_url }}" alt="UniScanner labeled component overview, multi-angle views, and optional RTK module and phone mount accessories" width="1448" height="1086">
  </div>
</section>

<section class="mm-section">
  <div class="mm-section__head">
    <p class="mm-eyebrow">How It Works</p>
    <h2 class="mm-section__title">From Raw Scan to 3D Scene</h2>
  </div>
  <div class="us-workflow">
    <div class="us-workflow__step">
      <p class="us-workflow__num">01</p>
      <h3>Data Acquisition</h3>
      <p>UniLidar L2 + IMU + RGB (+ optional RTK), driven by the RK3566 host with a Web UI for remote control, logs, and recording.</p>
    </div>
    <div class="us-workflow__step">
      <p class="us-workflow__num">02</p>
      <h3>Laser Reconstruction</h3>
      <p>Offline or on-device FAST-LIO2 / laser-inertial mapping turns the raw point cloud and trajectory into a dense reconstruction.</p>
    </div>
    <div class="us-workflow__step">
      <p class="us-workflow__num">03</p>
      <h3>Color Fusion</h3>
      <p>RGB images are registered against the reconstructed point cloud and pose to project color onto the 3D geometry.</p>
    </div>
    <div class="us-workflow__step">
      <p class="us-workflow__num">04</p>
      <h3>Visual 3D Display</h3>
      <p>The colored point cloud and camera trajectory can further train a Gaussian Splatting scene for immersive, browsable 3D.</p>
    </div>
  </div>
</section>

<section class="mm-section" id="open-source">
  <div class="mm-section__head">
    <p class="mm-eyebrow">Open Source</p>
    <h2 class="mm-section__title">Two Repos, Fully Open</h2>
  </div>
  <div class="mm-project-grid">
    <a class="mm-project-card" href="https://github.com/MapMindAI/UniLidar-SDK-Collection" target="_blank" rel="noopener">
      <span class="mm-project-card__tag">Acquisition</span>
      <h3 class="mm-project-card__title">UniLidar-SDK-Collection</h3>
      <p class="mm-project-card__desc">Device deployment, data collection, Web-based remote control, calibration, and optional RTK — everything that runs on the scanner itself.</p>
      <span class="mm-project-card__link">View source ↗</span>
    </a>
    <a class="mm-project-card" href="https://github.com/MapMindAI/UniLidar-SDK-Mapping" target="_blank" rel="noopener">
      <span class="mm-project-card__tag">Reconstruction</span>
      <h3 class="mm-project-card__title">UniLidar-SDK-Mapping</h3>
      <p class="mm-project-card__desc">FAST-LIO2 / laser-inertial reconstruction of UniLidar data — offline today, with an RK3588 real-time path in progress.</p>
      <span class="mm-project-card__link">View source ↗</span>
    </a>
  </div>
</section>

<section class="mm-cta">
  <div class="mm-cta__glow"></div>
  <div class="mm-cta__inner">
    <h2>Want to build one?</h2>
    <p>The full hardware BOM and both repos are open source — start scanning for the cost of a phone.</p>
    <div class="mm-hero__ctas">
      <a href="https://github.com/MapMindAI/UniLidar-SDK-Collection" class="mm-btn mm-btn--primary" target="_blank" rel="noopener">Get Started on GitHub ↗</a>
      <a href="{{ '' | relative_url }}#showcase" class="mm-btn mm-btn--ghost">Back to MapMindAI</a>
    </div>
  </div>
</section>

<section class="mm-section mm-section--muted" id="survey">
  <div class="mm-section__head">
    <p class="mm-eyebrow">Help Shape UniScanner</p>
    <h2 class="mm-section__title">Join Early Access</h2>
    <p class="mm-section__desc">Thinking of buying one, or just curious? A couple minutes of your feedback helps us prioritize what to build next.</p>
  </div>
  <div class="mm-hero__ctas us-survey-ctas">
    <a href="https://deepmirror.sg.larksuite.com/share/base/form/shrlgiBYUPgo5PODDczFLXnTHPe" class="mm-btn mm-btn--primary" target="_blank" rel="noopener">Join Early Access — English ↗</a>
    <a href="https://deepmirror.sg.larksuite.com/share/base/form/shrlgL9xhLq2B0k2J0YleeGqvCg" class="mm-btn mm-btn--ghost" target="_blank" rel="noopener">加入抢先体验 — 中文 ↗</a>
  </div>
</section>

<a href="#survey" class="us-survey-fab">
  <span class="us-survey-fab__dot"></span>
  Join Early Access
</a>
