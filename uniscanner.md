---
layout: base
title: UniScanner — UniLidar L2 Handheld 3D Scanner
meta-description: UniScanner is an open-source handheld 3D scanning rig built on the UniLidar L2, producing colored point clouds and Gaussian Splatting scenes.
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
      <p class="us-hero__price"><a href="#configurations">Join early access to help shape pricing</a></p>
    </div>
    <div class="us-hero__media">
      <video class="us-trailer__video" controls autoplay muted playsinline preload="none" poster="{{ '/assets/videos/posters/uniscanner_trailer.jpg' | relative_url }}">
        <source src="{{ '/assets/videos/uniscanner_trailer.mp4' | relative_url }}" type="video/mp4">
      </video>
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


<section class="us-usecase" id="use-case">
  <img class="us-usecase__img" src="{{ '/assets/img/uniscanner/usercase_room.webp' | relative_url }}" alt="UniScanner colored 3D scan of a room used for measuring and designing the space" width="1672" height="941">
  <div class="us-usecase__overlay"></div>
  <div class="us-usecase__copy">
    <p class="mm-eyebrow">User Case</p>
    <h2 class="us-usecase__title">Measure and design any space</h2>
    <p class="us-usecase__desc">Walk through a room once and get a colored, to-scale 3D capture ready for measurement, layout, and design work.</p>
  </div>
</section>

<section class="mm-section">
  <div class="mm-section__head">
    <p class="mm-eyebrow">How It Works</p>
    <h2 class="mm-section__title">From Point Cloud to 3D Design Model</h2>
    <p class="mm-section__desc">Beyond a colored point cloud — auto-detected walls, floors, and openings turn a raw scan into a clean, simplified 3D model ready for measurement and design.</p>
  </div>
  <div class="us-workflow">
    <div class="us-workflow__step">
      <p class="us-workflow__num">01</p>
      <h3>Data Acquisition</h3>
      <p>Lidar + IMU + RGB (+ optional RTK), driven by the host with a Web UI for remote control, logs, and recording.</p>
    </div>
    <div class="us-workflow__step">
      <p class="us-workflow__num">02</p>
      <h3>Reconstruction</h3>
      <p>Offline or on-device laser-inertial-rgb mapping turns the raw point cloud and trajectory into a colored dense reconstruction.</p>
    </div>
    <div class="us-workflow__step">
      <p class="us-workflow__num">03</p>
      <h3>Simplified 3D Design Model</h3>
      <p>Walls, floors, doors, and windows are auto-detected from the colored point cloud and simplified into a clean, to-scale 3D model ready for measurement and design work.</p>
    </div>
    <div class="us-workflow__step">
      <p class="us-workflow__num">04</p>
      <h3>Visual 3D Display</h3>
      <p>The colored point cloud and camera trajectory can further train a Gaussian Splatting scene for immersive, browsable 3D.</p>
    </div>
  </div>
  <!-- <p></p>
  <div class="mm-sector__media mm-sector__media--gallery us-results-grid">
    <figure class="mm-sector__figure">
      <video class="mm-sector__video us-autoplay-video" controls muted loop playsinline preload="none" poster="{{ '/assets/videos/posters/color_mapping_1.jpg' | relative_url }}">
        <source src="{{ '/assets/videos/color_mapping_1.mp4' | relative_url }}" type="video/mp4">
      </video>
      <figcaption class="mm-sector__caption">Colored Point Cloud — Demo 1</figcaption>
    </figure>
    <figure class="mm-sector__figure">
      <video class="mm-sector__video us-autoplay-video" controls muted loop playsinline preload="none" poster="{{ '/assets/videos/posters/color_mapping_2.jpg' | relative_url }}">
        <source src="{{ '/assets/videos/color_mapping_2.mp4' | relative_url }}" type="video/mp4">
      </video>
      <figcaption class="mm-sector__caption">Colored Point Cloud — Demo 2</figcaption>
    </figure>
    <figure class="mm-sector__figure">
      <video class="mm-sector__video us-autoplay-video" controls muted loop playsinline preload="none" poster="{{ '/assets/videos/posters/rtk_mapping_1.jpg' | relative_url }}">
        <source src="{{ '/assets/videos/rtk_mapping_1.mp4' | relative_url }}" type="video/mp4">
      </video>
      <figcaption class="mm-sector__caption">RTK-Verified Mapping — Demo 1</figcaption>
    </figure>
    <figure class="mm-sector__figure">
      <video class="mm-sector__video us-autoplay-video" controls muted loop playsinline preload="none" poster="{{ '/assets/videos/posters/rtk_mapping_2.jpg' | relative_url }}">
        <source src="{{ '/assets/videos/rtk_mapping_2.mp4' | relative_url }}" type="video/mp4">
      </video>
      <figcaption class="mm-sector__caption">RTK-Verified Mapping — Demo 2</figcaption>
    </figure>
  </div> -->
</section>

<script>
  (function () {
    var videos = document.querySelectorAll('.us-autoplay-video');
    if (!videos.length || !('IntersectionObserver' in window)) return;
    var observer = new IntersectionObserver(function (entries) {
      entries.forEach(function (entry) {
        if (entry.isIntersecting) {
          entry.target.play().catch(function () {});
        } else {
          entry.target.pause();
        }
      });
    }, { threshold: 0.5 });
    videos.forEach(function (video) { observer.observe(video); });
  })();
</script>

<section class="mm-section mm-section--dark mm-section--muted">
  <div class="mm-section__head">
    <p class="mm-eyebrow">Product Direction</p>
    <h2 class="mm-section__title">
      A Hardware-Assisted Upgrade to 3D Scanning
    </h2>
    <p class="mm-section__desc">
      Our direction is to go one step further:
      use a dedicated LiDAR + RGB capture device to create higher-confidence geometry,
      cleaner structural models, professional reports, and realistic 3D previews for
      renovation, property records, and outdoor planning.
    </p>
  </div>

  <div class="us-workflow">
    <div class="us-workflow__step">
      <p class="us-workflow__num">01</p>
      <h3>Dedicated LiDAR Home Scan</h3>
      <p>
        Scan rooms, apartments, houses, gardens, and renovation sites with a handheld
        LiDAR + RGB device. Compared with phone-only scanning, the goal is more reliable
        geometry, better scale consistency, and stronger support for larger or more complex
        spaces.
      </p>
    </div>

    <div class="us-workflow__step">
      <p class="us-workflow__num">02</p>
      <h3>Measured Structural Model</h3>
      <p>
        The scan is converted into a simplified 3D design model with auto-detected walls,
        floors, ceilings, doors, windows, openings, stairs, and key outdoor elements such
        as paths, plants, fences, and gazebos.
      </p>
    </div>

    <div class="us-workflow__step">
      <p class="us-workflow__num">03</p>
      <h3>Inspection & Planning Report</h3>
      <p>
        Generate a practical report for renovation and communication: room size, ceiling
        height, floor area, opening dimensions, structural annotations, before / after
        comparison, and warnings such as uneven floor or floor depression.
      </p>
    </div>

    <div class="us-workflow__step">
      <p class="us-workflow__num">04</p>
      <h3>Realistic 3D Preview</h3>
      <p>
        Beyond the measured model, RGB images and trajectory can produce a realistic
        Gaussian Splatting scene. Users can preview furniture, renovation effects, or
        outdoor additions such as a virtual gazebo directly inside a browsable 3D scene.
      </p>
    </div>
  </div>
  <div class="us-workflow-diagram">
    <img src="{{ '/assets/img/uniscanner/how-it-works.webp' | relative_url }}" alt="Diagram showing a dedicated LiDAR home scan converted into a measured structural model, an inspection and planning report with floor plan and dimensions, and a realistic 3D preview of the interior and outdoor Gaussian Splatting scene" loading="lazy" width="1915" height="610">
  </div>
</section>

<section class="mm-section" id="use-cases">
  <div class="mm-section__head">
    <p class="mm-eyebrow">User Cases</p>
    <h2 class="mm-section__title">From Scan to Decision</h2>
    <p class="mm-section__desc">Three ways a single walkthrough scan becomes something you can measure, inspect, and share.</p>
  </div>
  <div class="us-usercases">
    <div class="us-usecase us-usecase--case us-usecase--left">
      <img class="us-usecase__img" src="{{ '/assets/img/uniscanner/inspection-report.webp' | relative_url }}" alt="Indoor inspection and planning report view showing a scanned apartment with floor plan, dimensions, ceiling height, and floor-level warning overlays" loading="lazy" width="1672" height="941">
      <div class="us-usecase__overlay"></div>
      <div class="us-usecase__copy">
        <p class="mm-eyebrow">Indoor</p>
        <h3 class="us-usecase__title">Inspection &amp; Planning Report</h3>
        <p class="us-usecase__desc">Turn a walkthrough scan into a report that is easier to share with owners, designers, and contractors. Room dimensions, ceiling heights, openings, and layout details can be organized into one practical planning view.</p>
        <div class="mm-pipeline__row mm-pipeline__row--inline">
          <span>Scan</span>
          <span class="mm-pipeline__arrow">-></span>
          <span>Measured model</span>
          <span class="mm-pipeline__arrow">-></span>
          <span>Inspection report</span>
        </div>
        <ul class="us-usecase-points">
          <li>Room size, ceiling height, and floor area in one report</li>
          <li>Doors, windows, and openings ready for renovation planning</li>
          <li>One view that is easier to review with owners and contractors</li>
        </ul>
      </div>
    </div>

    <div class="us-usecase us-usecase--case">
      <img class="us-usecase__img" src="{{ '/assets/img/uniscanner/abnormal-detection.webp' | relative_url }}" alt="House scan inspection view showing detected abnormalities including uneven floor and a crack on the ceiling highlighted with technical warning overlays" loading="lazy" width="1672" height="941">
      <div class="us-usecase__overlay"></div>
      <div class="us-usecase__copy">
        <p class="mm-eyebrow">Inspection</p>
        <h3 class="us-usecase__title">Detect Abnormal Conditions</h3>
        <p class="us-usecase__desc">When inspecting a house scan, UniScanner can highlight abnormal areas that need attention. Uneven floors, local depressions, and ceiling cracks can be surfaced visually so the user knows what should be checked or fixed first.</p>
        <div class="mm-pipeline__row mm-pipeline__row--inline">
          <span>House scan</span>
          <span class="mm-pipeline__arrow">-></span>
          <span>Surface analysis</span>
          <span class="mm-pipeline__arrow">-></span>
          <span>Issue alerts</span>
        </div>
        <ul class="us-usecase-points">
          <li>Detect uneven floor and floor depression from the scan</li>
          <li>Highlight ceiling cracks for faster inspection follow-up</li>
          <li>Notify the user about issues before renovation or move-in</li>
        </ul>
      </div>
    </div>

    <div class="us-usecase us-usecase--case us-usecase--left">
      <img class="us-usecase__img" src="{{ '/assets/img/uniscanner/outdoor-gazebo-preview.webp' | relative_url }}" alt="Outdoor realistic 3D preview of a scanned backyard with a virtual gazebo placed in the scene to show how it would look before construction" loading="lazy" width="1672" height="941">
      <div class="us-usecase__overlay"></div>
      <div class="us-usecase__copy">
        <p class="mm-eyebrow">Outdoor</p>
        <h3 class="us-usecase__title">Realistic 3D Preview</h3>
        <p class="us-usecase__desc">Create a realistic outdoor 3D scene from the scan, then place planned additions directly into it. A virtual gazebo can be positioned in the yard so users can see how it looks before any build decision is made.</p>
        <div class="mm-pipeline__row mm-pipeline__row--inline">
          <span>Garden scan</span>
          <span class="mm-pipeline__arrow">-></span>
          <span>3D scene</span>
          <span class="mm-pipeline__arrow">-></span>
          <span>Virtual placement</span>
        </div>
        <ul class="us-usecase-points">
          <li>Preview gazebos, paths, fences, or furniture in context</li>
          <li>Use realistic geometry instead of rough manual mockups</li>
          <li>Communicate outdoor planning ideas with a browsable 3D view</li>
        </ul>
      </div>
    </div>
  </div>
</section>


<section class="mm-section mm-section--muted">
  <div class="mm-section__head">
    <p class="mm-eyebrow">Inside the Scanner</p>
    <h2 class="mm-section__title">Built to Take Apart</h2>
    <p class="mm-section__desc">Precision-engineered components designed for performance, reliability, and developer extensibility.</p>
  </div>
  <div class="mm-sector">
    <div class="mm-sector__media">
      <img class="mm-sector__image mm-sector__image--diagram" src="{{ '/assets/img/uniscanner/exploded.webp' | relative_url }}" alt="Exploded view of the UniScanner showing LiDAR head, RGB camera module, compute board, thermal system, battery pack, handle shell, USB-C base, and optional RTK module" loading="lazy" width="1448" height="1086">
    </div>
    <div class="mm-sector__copy">
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
    </div>
  </div>
</section>

<section class="mm-section" id="specs">
  <div class="mm-section__head">
    <p class="mm-eyebrow">Engineering</p>
    <h2 class="mm-section__title">Spec Sheet</h2>
    <p class="mm-section__desc">Full mechanical dimensions across front, side, back, and top views, plus the complete specification table.</p>
  </div>
  <div class="mm-sector">
    <div class="mm-sector__media">
      <img class="mm-sector__image mm-sector__image--diagram" src="{{ '/assets/img/uniscanner/engineering-drawing.webp' | relative_url }}" alt="UniScanner engineering drawing with front, side, back, and top views, dimensions, and specification table" loading="lazy" width="1448" height="1086">
    </div>
    <div class="mm-sector__copy">
      <div class="mm-spec-panel">
        <p class="mm-spec-panel__label">Specifications</p>
        <div class="mm-spec-panel__grid">
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
    </div>
  </div>
</section>

<!-- <section class="mm-cta" id="open-source">
  <div class="mm-cta__glow"></div>
  <div class="mm-cta__inner mm-cta__inner--wide">
    <p class="mm-eyebrow">Open Source</p>
    <h2>Two Repos, Fully Open — Want to Build One?</h2>
    <p>The full hardware BOM and both repos are open source — start scanning for the cost of a phone.</p>
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
    <div class="mm-hero__ctas">
      <a href="https://github.com/MapMindAI/UniLidar-SDK-Collection" class="mm-btn mm-btn--primary" target="_blank" rel="noopener">Get Started on GitHub ↗</a>
      <a href="{{ '' | relative_url }}#showcase" class="mm-btn mm-btn--ghost">Back to MapMindAI</a>
    </div>
  </div>
</section> -->

<section class="mm-section mm-section--muted">
  <div class="mm-section__head">
    <p class="mm-eyebrow">Configurations</p>
    <h2 class="mm-section__title" id="configurations">Help Us Narrow the Price</h2>
    <p class="mm-section__desc">We are still narrowing the final price and configuration. Early access feedback helps us understand which setup matters most and where the price should land.</p>
  </div>
  <div class="us-pricing-grid">
    <div class="us-pricing-card us-pricing-card--base">
      <p class="us-pricing-card__tier">Early Access</p>
      <p class="us-pricing-card__price"><a href="https://deepmirror.sg.larksuite.com/share/base/form/shrlgiBYUPgo5PODDczFLXnTHPe" target="_blank" rel="noopener">Join Early Access ↗</a></p>
      <ul class="us-pricing-card__items us-pricing-card__items--plain">
        <li>Tell us which configuration you would actually buy</li>
        <li>Help us prioritize the right balance of capability and cost</li>
        <li>Get first access when UniScanner is ready</li>
      </ul>
      <p class="us-pricing-card__note">We want early users to help narrow the final price before launch.</p>
    </div>
    <div class="us-pricing-card">
      <p class="us-pricing-card__tier">What We Are Evaluating</p>
      <p class="us-pricing-card__price">Core vs. Pro</p>
      <p class="us-pricing-card__note">We are comparing a simpler base scanner against more advanced options such as RTK and on-device real-time reconstruction.</p>
    </div>
    <div class="us-pricing-card">
      <p class="us-pricing-card__tier">Your Input Matters</p>
      <p class="us-pricing-card__price">2-Minute Survey</p>
      <p class="us-pricing-card__note">If you are interested in buying or building with UniScanner, tell us your target use case and price expectations.</p>
    </div>
  </div>
</section>


<section class="mm-section" id="survey">
  <div class="us-survey-card">
    <div class="us-survey-card__glow"></div>
    <span class="us-survey-card__badge"><span class="us-survey-card__badge-dot"></span>Early Access · Limited Spots</span>
    <p class="mm-eyebrow">Help Shape UniScanner</p>
    <h2 class="us-survey-card__title">Join Early Access</h2>
    <p class="us-survey-card__desc">Thinking of buying one, or just curious? A 2-minute survey helps us prioritize what to build next — early respondents get first access when we ship.</p>
    <div class="mm-hero__ctas us-survey-ctas">
      <a href="https://deepmirror.sg.larksuite.com/share/base/form/shrlgiBYUPgo5PODDczFLXnTHPe" class="mm-btn mm-btn--primary us-survey-btn" target="_blank" rel="noopener">Join Early Access ↗</a>
    </div>
  </div>
</section>

<a href="#survey" class="us-survey-fab">
  <span class="us-survey-fab__dot"></span>
  Join Early Access
</a>
