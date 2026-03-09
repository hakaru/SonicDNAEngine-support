---
title: "Introducing SonicDNA Engine — IR/NAM Guitar Amp Simulator for iOS"
date: 2026-03-10
---

We're excited to announce **SonicDNA Engine**, a guitar amp and cabinet simulator for iPhone and iPad that brings the power of Neural Amp Modeler (NAM) and Impulse Response (IR) processing to iOS — both as a standalone effector and as an AUv3 plugin.

---

## The Concept: Capture → Play

SonicDNA Engine is the second piece of the **SonicDNA ecosystem**:

- **SonicDNA Collector** = Capture the sonic DNA of your analog gear
- **SonicDNA Engine** = Play back that sonic DNA anywhere

Together, they complete the **Capture → Play** workflow. Record the characteristics of your favorite tube amp with Collector, then load the resulting files into Engine to recreate that sound in your DAW or live rig — all on your iPhone or iPad.

Of course, you don't need Collector to use Engine. You can load any standard IR or NAM file from the community.

---

## Two Ways to Play

### Standalone Effector Mode

Connect your guitar through a USB audio interface and use SonicDNA Engine as a standalone amp simulator:

```
Guitar → Audio Interface → iPhone/iPad → Audio Interface → Amp/Headphones
                            (SonicDNA Engine)
```

Tap "Start Audio Engine" and you're playing through your favorite amp models with low-latency monitoring.

### AUv3 Plugin Mode

SonicDNA Engine works as an Audio Unit Extension in any AUv3-compatible host:

- **AUM** — The go-to iOS mixer for live performance and routing
- **GarageBand** — Quick recording and demo production
- **Logic Pro for iPad** — Professional music production
- **Cubasis, BeatMaker**, and more

Load it as an effect plugin, select your IR and NAM files, and you're ready to record.

---

## The Signal Chain

SonicDNA Engine processes your guitar signal through a carefully designed DSP chain:

```
Input → Input Gain → Noise Gate → NAM (Amp) → EQ → IR (Cabinet) → Output Level → Mix → Output
```

### NAM Amp Modeling

Load Neural Amp Modeler files to recreate the sound of real amplifiers. NAM uses machine learning to capture the nonlinear behavior of tube amps — the saturation, the dynamics, the feel. SonicDNA Engine supports WaveNet, LSTM, and Linear architectures.

Thousands of free NAM models are available on [ToneHunt](https://tonehunt.net) — from vintage Fender cleans to high-gain modern metal amps.

### IR Cabinet Simulation

Load impulse response files for accurate cabinet simulation. SonicDNA Engine uses FFT-based convolution (Overlap-Save algorithm) powered by Apple's Accelerate framework for efficient, real-time processing.

Compatible with standard IR formats used by Helix, Axe-FX, Quad Cortex, Kemper, and more.

### Built-in Effects

- **Noise Gate** — Adjustable threshold with smooth gating for clean silence between notes
- **3-Band Parametric EQ** — Low shelf (200Hz), Mid bell (1kHz), High shelf (4kHz), each ±12dB
- **Input/Output Gain** — Full signal level control
- **Dry/Wet Mix** — Blend between your original signal and the processed sound

---

## Under the Hood

### One DSP Core, Two Modes

Whether you use SonicDNA Engine as a standalone app or as an AUv3 plugin, the same DSP kernel processes your audio. This means identical sound quality in both modes.

The DSP is implemented in C++ for maximum real-time performance:

- **Convolution Engine** — vDSP FFT-based with pre-allocated buffers (zero allocations on the audio thread)
- **NAM Inference** — Custom C++ implementation using the NAMCore library
- **Noise Gate** — Envelope follower with smooth attack/release
- **Parametric EQ** — vDSP biquad filters with Audio EQ Cookbook coefficients
- All parameters use `std::atomic` for lock-free, real-time-safe operation

### Low Latency

SonicDNA Engine targets a 128-sample buffer at 48kHz (~2.7ms), keeping the total round-trip latency low enough for comfortable playing.

### Preset System

Save your favorite combinations of IR files, NAM models, and parameter settings as presets. Quickly switch between clean, crunch, and high-gain tones.

---

## What Sets Us Apart

1. **iOS-native NAM support** — Use the vast library of community NAM models on your iPhone/iPad
2. **AUv3 plugin** — Works inside your favorite DAW, not just standalone
3. **SonicDNA Collector integration** — Capture your own amp's DNA and play it back
4. **Open formats** — Standard IR (WAV) and NAM files, no proprietary lock-in
5. **Privacy-first** — All processing happens on-device, no data collection, no cloud dependency

---

## What's Next

SonicDNA Engine is currently in development. Here's what's on the roadmap:

- **Latency optimization** — Targeting sub-3ms with Core Audio direct rendering
- **SonicDNA Collector integration** — Seamless file sharing via App Groups
- **Tuner** — Built-in chromatic tuner
- **Dual Amp** — Blend two NAM models
- **MIDI Control** — Control parameters via MIDI CC
- **Setlist Mode** — Organize presets for live performance

---

## Stay Updated

Follow this blog for development updates, tips on getting the best tone, and guides for creating your own NAM models.

Questions or feedback? Reach us at **sonicdna@hakaru.net**

[← Back to Support](/)
