---
title: "Introducing SonicDNA Engine — IR/NAM Audio Processor for iOS"
date: 2026-03-10
---

We're excited to announce **SonicDNA Engine**, a versatile audio processor for iPhone and iPad that brings the power of Neural Amp Modeler (NAM) and Impulse Response (IR) processing to iOS — both as a standalone effector and as an AUv3 plugin.

---

## The Concept: Capture → Play

SonicDNA Engine is the second piece of the **SonicDNA ecosystem**:

- **SonicDNA Collector** = Capture the sonic DNA of your analog gear
- **SonicDNA Engine** = Play back that sonic DNA anywhere

Together, they complete the **Capture → Play** workflow. Record the characteristics of your favorite tube amp, vintage preamp, or studio compressor with Collector, then load the resulting files into Engine to recreate that sound in your DAW or live rig — all on your iPhone or iPad.

Of course, you don't need Collector to use Engine. You can load any standard IR or NAM file from the community.

---

## Who Is This For?

### Musicians of All Kinds

SonicDNA Engine isn't limited to guitarists. It's a general-purpose audio processor that works with any audio source:

- **Guitarists & Bassists** — Load NAM amp models and IR cabinet simulations for a complete amp-in-a-box experience
- **Keyboardists & Synth Players** — Run your keyboard or synthesizer through vintage preamp models and speaker IRs to add analog warmth to digital sounds
- **Vocalists & Podcasters** — Use microphone IRs to simulate classic studio microphones, apply subtle preamp coloring to your vocal chain
- **Audiophiles & Sound Designers** — Experiment with room IRs, speaker simulations, and equipment modeling to shape your listening experience

If it outputs audio, SonicDNA Engine can process it.

---

## Two Ways to Play

### Standalone Effector Mode

Connect your instrument or microphone through a USB audio interface and use SonicDNA Engine as a standalone processor:

```
Instrument/Mic → Audio Interface → iPhone/iPad → Audio Interface → Speakers/Headphones
                                    (SonicDNA Engine)
```

Tap "Start Audio Engine" and you're processing audio through your favorite equipment models with low-latency monitoring.

### AUv3 Plugin Mode

SonicDNA Engine works as an Audio Unit Extension in any AUv3-compatible host:

- **AUM** — The go-to iOS mixer for live performance and routing
- **GarageBand** — Quick recording and demo production
- **Logic Pro for iPad** — Professional music production
- **Cubasis, BeatMaker**, and more

Load it as an effect plugin on any track — guitar, vocals, keyboards, synths, drums — and shape the sound with equipment modeling and convolution.

---

## The Signal Chain

SonicDNA Engine processes your audio through a carefully designed DSP chain:

```
Input → Input Gain → Noise Gate → NAM (Equipment Model) → EQ → IR (Convolution) → Output Level → Mix → Output
```

### NAM Equipment Modeling

Load Neural Amp Modeler files to recreate the sound of real audio equipment. NAM uses machine learning to capture the nonlinear behavior of analog gear — the saturation, the dynamics, the character. SonicDNA Engine supports WaveNet, LSTM, and Linear architectures.

While NAM is widely known for guitar amp modeling, the technology works for any audio equipment: preamps, channel strips, tape machines, and more.

Thousands of free NAM models are available on [Tone3000](https://www.tone3000.com).

### IR Convolution Processing

Load impulse response files for accurate simulation of:

- **Speaker cabinets** — Guitar cabs, bass cabs, studio monitors
- **Microphones** — Simulate the character of classic studio mics
- **Rooms & spaces** — Concert halls, studios, acoustic environments
- **Equipment** — Any linear system captured as an IR

SonicDNA Engine uses FFT-based convolution (Overlap-Save algorithm) powered by Apple's Accelerate framework for efficient, real-time processing.

### Built-in Effects

- **Noise Gate** — Adjustable threshold with smooth gating for clean silence
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

SonicDNA Engine targets a 128-sample buffer at 48kHz (~2.7ms), keeping the total round-trip latency low enough for comfortable live performance.

### Preset System

Save your favorite combinations of IR files, NAM models, and parameter settings as presets. Quickly switch between different equipment setups.

---

## What Sets Us Apart

1. **Versatile audio processor** — Not just for guitar; works with any instrument, microphone, or audio source
2. **iOS-native NAM support** — Use the vast library of community NAM models on your iPhone/iPad
3. **AUv3 plugin** — Works inside your favorite DAW, not just standalone
4. **SonicDNA Collector integration** — Capture your own equipment's DNA and play it back
5. **Open formats** — Standard IR (WAV) and NAM files, no proprietary lock-in
6. **Privacy-first** — All processing happens on-device, no data collection, no cloud dependency

---

## What's Next

SonicDNA Engine is currently in development. Here's what's on the roadmap:

- **Latency optimization** — Targeting sub-3ms with Core Audio direct rendering
- **SonicDNA Collector integration** — Seamless file sharing via App Groups
- **Tuner** — Built-in chromatic tuner
- **Dual processing** — Blend two NAM models
- **MIDI Control** — Control parameters via MIDI CC
- **Setlist Mode** — Organize presets for live performance

---

## Stay Updated

Follow this blog for development updates, tips on getting the best sound, and guides for using IR/NAM files with different instruments and setups.

Questions or feedback? Reach us at **sonicdna@hakaru.net**

[← Back to Support](/)
