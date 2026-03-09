# Changelog

All notable changes to SonicDNA Engine will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.0] - 2026-03-10

### 🎉 Initial Release

First public release of SonicDNA Engine.

### Added

- **Core Features**
  - 🎸 NAM (Neural Amp Modeler) amp simulation
  - 🔊 IR (Impulse Response) cabinet simulation via FFT convolution
  - 🎛️ Noise Gate with adjustable threshold
  - 📊 3-Band Parametric EQ (Low/Mid/High)
  - 🎚️ Input Gain, Output Level, Dry/Wet Mix controls

- **Audio Engine**
  - 48kHz sample rate
  - 128-sample buffer (~2.7ms latency)
  - USB audio interface support
  - Real-time DSP processing

- **AUv3 Plugin**
  - 🔌 Audio Unit Extension (Effect type)
  - Full parameter automation support
  - IR/NAM file loading from within plugin
  - Compatible with AUM, GarageBand, Cubasis, etc.

- **User Interface**
  - 📱 Standalone effector mode with knob controls
  - 📁 IR file browser with import
  - 🧠 NAM model browser with import
  - 💾 Preset save/load system
  - ⚙️ Settings with input device selection

- **File Support**
  - WAV IR files (any sample rate)
  - NAM model files (WaveNet, LSTM, Linear)
  - Demo IR and NAM files included

---

## [Unreleased]

### Planned

- Latency optimization (SinkNode / Core Audio RemoteIO)
- SonicDNA Collector integration via App Groups
- Additional effect types
- iPad optimization
- Tuner

---

[← Back to Support](/)
