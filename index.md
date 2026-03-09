# SonicDNA Engine Support

Welcome to SonicDNA Engine support page.

SonicDNA Engine is an IR/NAM guitar amp simulator app with AUv3 plugin support for iOS.

---

## 🎯 Overview

SonicDNA Engine transforms your iPhone or iPad into a guitar amp and cabinet simulator. Load IR (Impulse Response) files for cabinet simulation and NAM (Neural Amp Modeler) files for amp modeling, with real-time low-latency audio processing.

---

## ✨ Key Features

### 🎸 NAM Amp Modeling
Load Neural Amp Modeler files to recreate the sound of real amplifiers with AI-powered digital modeling.

### 🔊 IR Cabinet Simulation
Load impulse response files for accurate cabinet simulation using FFT-based convolution.

### 🎛️ Built-in Effects
- **Noise Gate** - Adjustable threshold with smooth gating
- **3-Band EQ** - Low shelf, Mid bell, High shelf parametric EQ
- **Input/Output Gain** - Full signal level control
- **Dry/Wet Mix** - Blend between original and processed signal

### 🔌 AUv3 Plugin
Use SonicDNA Engine as an Audio Unit Extension in any AUv3-compatible host:
- AUM, GarageBand, Cubasis, BeatMaker, and more
- Full parameter control within host apps
- IR/NAM file loading from within the plugin

### 🎵 Standalone Effector Mode
Connect your guitar via USB audio interface and use as a standalone amp simulator:
- Real-time audio processing with low latency
- Support for USB audio interfaces
- 48kHz sample rate

### 💾 Preset System
Save and recall your favorite settings including IR/NAM selection and all parameter values.

---

## 🔌 Setup Guide

### Standalone Mode

```
Guitar → Audio Interface → iPhone/iPad → Audio Interface → Amp/Headphones
                            (SonicDNA Engine)
```

1. Connect your USB audio interface to iPhone/iPad
2. Connect guitar to audio interface input
3. Connect audio interface output to amp/headphones
4. Launch SonicDNA Engine
5. Tap "Start Audio Engine"
6. Load IR and/or NAM files

### AUv3 Plugin Mode

1. Open your AUv3 host app (AUM, GarageBand, etc.)
2. Add SonicDNA Engine as an Audio Unit effect
3. Load IR/NAM files from the plugin interface
4. Adjust parameters as needed

---

## 📱 Using the App

### Loading IR Files

1. Go to the **IR** tab
2. Tap **+** to import WAV files
3. Select the IR file to activate it
4. Supported format: WAV (any sample rate, mono/stereo)

### Loading NAM Files

1. Go to the **NAM** tab
2. Tap **+** to import .nam/.json files
3. Select the NAM model to activate it
4. Supported: WaveNet, LSTM, Linear architectures

### Signal Chain

```
Input → Input Gain → Noise Gate → NAM → EQ → IR Convolution → Output Level → Mix → Output
```

### Controls

| Control | Range | Description |
|---------|-------|-------------|
| **INPUT** | 0 - 2x | Input gain before processing |
| **OUTPUT** | 0 - 2x | Output level after processing |
| **MIX** | 0% - 100% | Dry/Wet blend (0%=dry, 100%=wet) |
| **Noise Gate** | -96 to 0 dB | Gate threshold |
| **EQ Low** | -12 to +12 dB | Low shelf (200 Hz) |
| **EQ Mid** | -12 to +12 dB | Mid bell (1 kHz) |
| **EQ High** | -12 to +12 dB | High shelf (4 kHz) |

---

## ❓ FAQ

### What audio interfaces are supported?
Any class-compliant USB audio interface should work. Tested with common interfaces like ZOOM AMS-22.

### Where can I get IR files?
IR files are available from many sources:
- Create your own with [SonicDNA Collector](https://apps.apple.com/app/id6758269736)
- Download from communities like ToneHunt
- Many free and commercial IR packs are available online

### Where can I get NAM files?
NAM models can be found at:
- [ToneHunt](https://tonehunt.net) - Community NAM model sharing
- Train your own using [Neural Amp Modeler](https://github.com/sdatkinson/neural-amp-modeler)

### What NAM architectures are supported?
SonicDNA Engine supports WaveNet, LSTM, and Linear NAM architectures.

### Is there latency?
The app uses a 128-sample buffer at 48kHz (~2.7ms). Total round-trip latency depends on your audio interface.

### Can I use this with GarageBand?
Yes! SonicDNA Engine works as an AUv3 effect plugin in GarageBand and other AUv3 hosts.

### What is the relationship with SonicDNA Collector?
SonicDNA Collector captures the sonic characteristics of analog equipment. SonicDNA Engine plays back those captured characteristics. Together they form the SonicDNA ecosystem: Capture → Play.

---

## 📧 Contact

If you have questions or feedback, please contact us at:

📧 **sonicdna@hakaru.net**

---

## 🔗 Links

- [Privacy Policy](privacy)
- [Changelog](changelog/)
- [Blog](blog/en/)

---

© 2026 hakaru.net
