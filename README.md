<img width="2048" height="2048" alt="AndroidDoctor" src="https://github.com/user-attachments/assets/eb07d651-93d5-4974-aec4-cadb477e4900" />

### Morphs Android Doctor (v4.7) — Product Overview

**Morphs Android Doctor** is a high-performance, 100% client-side mobile diagnostic and hardware verification workstation built for Android environments and modern mobile web containers (Chrome Mobile, PWAs, Web2Android, AppCreator24, and local WebView wrappers). Operating entirely in local device memory with zero external tracking or data transmission, it provides real-time silicon telemetry, automated sensor pipelines, interactive digitizer tests, and deep operating-system forensics.

---

### Core Architectural Features

* **High-Entropy Silicon & Display Telemetry:** Interrogates `navigator.userAgentData` and WebGL contexts to surface unmasked GPU renderers (Adreno / Mali), exact OEM device models (Samsung Galaxy, Google Pixel, Xiaomi, OnePlus), physical RAM allocations, CPU concurrency cores, display refresh rates (60Hz / 90Hz / 120Hz), and live DPR screen geometry.
* **3D Gyroscope & Dynamic Fluid Level:** Continuous 60 FPS real-time accelerometer and orientation tracker rendering pitch, roll, and alpha tilt across a dual-ring reticle with an integrated fullscreen leveling mode.
* **Hardware Dead-Zone Safe Buffer Shield:** A toggleable, hazard-striped upper safe spacer (44px–85px) that dynamically shifts all interactive touch targets below physical camera cutouts, notches, or cracked upper digitizer rows.
* **Zero-Reload In-Memory Hot Reset Engine:** Performs bare-metal application purges directly in RAM (clearing IndexedDB buckets, `caches`, `localStorage`, active media streams, and WebGL animation pipelines) without triggering page navigations or Android WebView `ERR_CONNECTION_REFUSED` crashes.
* **Comprehensive Master Health Ledger:** Generates structured session diagnostic reports categorizing tests into prioritized results (Fail ➔ Warn ➔ Pass) with built-in export to raw text, system clipboard copy, and native OS Share Sheet integration.

---

### Diagnostic Rooms & Automated Pipelines

#### 1. Quick System Scan (8 Automated Baselines)
Designed for rapid, non-invasive verification of foundational device health:
* **Multi-CDN Ping & DNS Latency:** Concurrently probes Cloudflare, Google, and AWS edge points to isolate DNS latency and packet jitter.
* **Battery Hardware & Thermal Headroom:** Samples charging state, power intake levels, and thermal boundaries via the Battery Status API.
* **Stereo Audio Separation Sweep:** Emits a calibrated triangular wave oscillator sweep from 150 Hz to 12,000 Hz to evaluate speaker clarity and channel separation.
* **Visual DOM Layout & Reflow Stress:** Renders 3,000 DOM elements in real time to calculate tree throughput (nodes/sec) and browser compositor latency.
* **IndexedDB Storage Quota & I/O:** Executes a 500-record database write transaction to audit storage throughput and persistent quota allocations.
* **8-Second Parallel Fiber Speedometer:** Multi-stream throughput probe calculating sustained bandwidth (Mbps), ping, and jitter against edge CDN targets.
* **Hardware Video Codec Acceleration:** Audits direct SoC VPU hardware decoding pipelines across H.264, HEVC/H.265, AV1, and VP9.
* **Subpixel & Burn-In RGBW Flasher:** Fullscreen high-intensity primary color sequence (Red, Green, Blue, White, Black) to inspect AMOLED burn-in, subpixel uniformity, and stuck pixels.

#### 2. Expanded Hardware Lab (13 Automated Tests + Interactive Bench)
Adds deep sensor evaluation and physical hardware benches:
* **GPS Sat-Lock & TTFF Meter:** Measures Time-To-First-Fix and radial accuracy (±meters) using high-precision positioning sensors.
* **Haptic Motor Cadence:** Verifies actuator and linear resonant coils via a 3-stage sequence: single tick (15ms), alert pulse, and continuous rumble.
* **Biometric Enclave HUD:** Audits the device hardware keystore, TEE (Trusted Execution Environment), StrongBox cryptographic enclaves, and OS WebAuthn platform authenticators.
* **Kinetic Scroll & Frame Pacing:** Renders high-density vector cards in a rapid compositor scroll loop to detect dropped frames and micro-stutters.
* **10-Second Dual-Phase 3D GPU Benchmark:** Fullscreen WebGL stress test executing a 36,000-polygon Torus Knot followed by a 4-point dynamic specular PBR fill-rate render.

#### 3. Advanced Forensic Suite (16 Automated Tests + Power-User Tools)
Engineered for deep pre-purchase audits, performance triage, and root-cause analysis:
* **25-Second 5-Phase Fullscreen WebGL Benchmark:** Evaluates GPU capabilities across five distinct phases:
  1. *Instanced Geometry Grid:* Transform-heavy matrix rendering.
  2. *High-Poly 36k Torus Knot:* Dense vertex pipeline calculation.
  3. *4-Light Specular PBR:* High fill-rate multi-light surface illumination.
  4. *5,000-Particle Kinetic Swarm:* Unbound physics calculation and point-sprite rendering.
  5. *Volumetric Cyber Tunnel:* Dynamic Fresnel core and procedural neon ring shaders.
* **60-Second Thermal Throttle Curve:** Sustained load test recording continuous frame pacing to chart performance degradation and thermal mitigation decay.
* **Audio Roundtrip Echo Latency:** Emits a 1,000 Hz acoustic tick to calculate the DAC-to-microphone loopback delay in milliseconds (detecting Bluetooth or driver lag).
* **Container Permission Detective:** Audits platform sandbox permissions (Camera, Microphone, Geolocation, Notifications) directly from the runtime.

---

### Interactive Manual Bench & Diagnostic Utilities

* **Fullscreen Touch Matrix (Micro-Grid):** A high-density 24×44 grid (1,056 blocks) mapping digitizer dead zones, broken trace lines, and multi-axis swipe continuity.
* **12-Second Ghost Touch Sentry:** A hands-off idle stability trap featuring a 2-second arming buffer to detect ground hum faults, static jitter, or erratic digitizer phantom touches.
* **Live Multi-Touch Pad:** Tracks and renders concurrent finger coordinates (1 to 10 points) with dynamic contact radii.
* **Calibrated dB Acoustic Studio:** Real-time logarithmic decibel meter (20–110 dB) featuring peak-hold markers and a live FFT audio waveform visualizer.
* **Camera Sensor Lab:** Live viewfinder diagnostics testing front and rear optical sensors, focal parameters, and aspect ratios.
* **USB-C Port & Charge Velocity Sentry:** Audits physical port pin continuity, connection stability, and charging current intake.
* **In-Browser APK ZIP & Manifest Deconstructor:** Local ZIP parser extracting package names, Target SDK levels, Dalvik bytecode structure (`classes.dex`), and native binary architectures (`arm64-v8a` vs. `armeabi-v7a`) without cloud uploads.
* **Storage Large File Hunter:** Client-side file auditor flagging batch-selected files and media exceeding 50 MB.
* **Developer Options Master Codex:** Searchable reference manual detailing critical system toggles (e.g., 0.5× animation scales, Samsung GPUWatch, cached app freezer, 4× MSAA) with plain-English safety classifications (*Safe*, *Caution*, *Danger*).
* **Symptom Solver Correlation Engine:** Interactive troubleshooter correlating live battery, thermal, network, and digitizer readings to diagnose common failure states (rapid standby battery drain, gaming throttling, erratic touch during charging).
