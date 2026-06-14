# Noise-Cancellation-in-ECG-Signal
An adaptive filtering framework designed to suppress real-time noise (like power line interference and muscle artifacts) from ECG signals. Employing LMS, NLMS, and RLS algorithms, it cleans raw signals while preserving crucial diagnostic waveforms. It provides a low-latency, high-accuracy tool ideal for cardiac monitoring and IoT wearables.

---

## 🧠 System Architecture & Key Features

* **Multi-Algorithm Filtering Core:** Evaluates and deploys Least Mean Square (LMS), Normalized Least Mean Square (NLMS), and Recursive Least Squares (RLS) adaptive filters to actively mitigate signal corruption.
* **Multi-Hazard Artifact Suppression:** Dynamically targets and cancels powerline interference (50 Hz), baseline wander, muscle artifacts (EMG noise), and severe electrode motion distortion.
* **Real-Time Morphological Preservation:** Tracks signal variances using a self-adjusting error-feedback mechanism ($E(n) = D(n) - Y(n)$) to accurately optimize filter weights and preserve clinically vital PQRST wave properties.
* **High-Rate Data Adaptation:** Engineered to interface directly with variable biomedical acquisition hardware running default sampling frequencies of 250 Hz, 500 Hz, or 1 kHz.
* **IoT Wearable Readiness:** Optimized for energy-efficient, low-latency deployment constraints typical of smartwatches, portable telemetry patches, and edge telemedicine hardware.

---

## 📈 Validated Performance Results

* **Superior RLS Performance:** Empirical testing confirms Recursive Least Squares (RLS) delivers top-tier noise cancellation and maximum clarity compared to standard baseline techniques.
* **Spectral Power Suppression:** Comparative Power Spectrum Density (PSD) analysis validated complete mathematical mitigation of the 50 Hz powerline interference spikes.
* **Morphology & HRV Safeguards:** Denoised outputs successfully maintain wave amplitude integrity, rendering signals ready for automated Heart Rate Variability (HRV) and arrhythmia diagnostics.

---

## 🛠️ Tech Stack & Dependencies

### Software & Analytics
* **Primary Environment:** MATLAB / Simulink
* **Toolboxes Used:** Signal Processing Toolbox, DSP System Toolbox
* **Scripting Languages:** MATLAB (M-Code), C/C++ (via MATLAB Coder target generation)

### Algorithm Specifications
* **Adaptive Engines:** LMS Filter, NLMS Filter, RLS Filter
* **Comparative Baseline:** Fixed Digital IIR/FIR Notch Filters
* **Signal Metrics Analyzed:** Signal-to-Noise Ratio (SNR), Power Spectrum Density (PSD)
