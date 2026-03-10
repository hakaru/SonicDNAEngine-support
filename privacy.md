# Privacy Policy

**Last updated: March 10, 2026**

## Introduction

SonicDNA Engine ("we", "our", or "the app") is committed to protecting your privacy. This Privacy Policy explains how we handle information when you use our iOS application.

## Summary

SonicDNA Engine processes audio entirely on your device in real-time. IR and NAM files are stored locally and are never uploaded to any server by the app. However, the app uses third-party services — Firebase Analytics & Crashlytics, Tone3000 API, and iCloud Drive — which may collect or process certain data as described below.

## Audio Processing

All audio processing in SonicDNA Engine is performed:

- **Entirely on your device** in real-time
- Audio is **never recorded or stored** by the app
- Audio is **never transmitted** to any server
- Processing happens with zero cloud dependency

## IR and NAM Files

IR and NAM files you import into SonicDNA Engine are:

- Stored **locally on your device**
- Synced to **iCloud Drive** if iCloud sync is enabled (see below)
- **Never uploaded** to any server by the app itself
- Accessible only to you

## Data We Collect and Use

### Firebase Analytics & Crashlytics

SonicDNA Engine uses Firebase Analytics and Firebase Crashlytics, services provided by Google LLC.

- **What is collected**: Anonymous usage data (feature usage, session length, app version, device model/OS version) and crash reports (crash stack traces, device state at time of crash)
- **What is NOT collected**: Your audio, personal identity, or file contents
- **Purpose**: To understand how the app is used and to diagnose bugs and crashes
- **Processed by**: Google LLC (Firebase). See [Google's Privacy Policy](https://policies.google.com/privacy)
- **Data retention**: Per Google Firebase defaults (crash reports: 90 days, analytics: 14 months)
- **Opt-out**: You can limit ad tracking via iOS Settings > Privacy & Security > Tracking

### Tone3000 API

If you use the built-in model browser ("Store" tab) to browse or download NAM/IR models from Tone3000:

- **What is transmitted**: Search queries, model browse history, your Tone3000 account credentials (email/password handled by Tone3000's authentication), and downloaded model URLs
- **Authentication**: A Tone3000 account is required. Authentication tokens are stored securely in the iOS Keychain
- **What is NOT transmitted**: Your audio data or locally stored IR/NAM files
- **Processed by**: Tone3000. See [Tone3000's Privacy Policy](https://www.tone3000.com/privacy)
- **Optional**: The Store tab and Tone3000 features are optional. You can use the app without signing in to Tone3000

### iCloud Drive

If you enable iCloud sync:

- **What is synced**: IR files (WAV), NAM model files (JSON), and user presets across your Apple devices
- **Processed by**: Apple Inc. via iCloud Drive. See [Apple's Privacy Policy](https://www.apple.com/privacy/)
- **Control**: You can disable iCloud sync at any time via iOS Settings > [Your Name] > iCloud > SonicDNA Engine

## Microphone Access

SonicDNA Engine requires microphone access for real-time audio processing. This permission is:

- Used solely for live audio input processing
- Only active when the audio engine is running
- Audio is processed in real-time and never stored
- Controllable via iOS Settings at any time

## AUv3 Plugin

When used as an AUv3 plugin in host applications:

- SonicDNA Engine only processes audio provided by the host
- No additional data is collected or transmitted
- The plugin operates within the host app's sandbox

## Third-Party Services

| Service | Provider | Purpose | Data |
|---------|----------|---------|------|
| Firebase Analytics | Google LLC | App usage analytics | Anonymous usage stats |
| Firebase Crashlytics | Google LLC | Crash reporting | Crash reports, device info |
| Tone3000 API | Tone3000 | Model browser & download | Account auth, search queries |
| iCloud Drive | Apple Inc. | File sync across devices | IR/NAM/preset files |

## Data Storage

Local data stored on your device:

- Imported IR files (WAV)
- Imported NAM model files (JSON)
- User presets (parameter settings)
- App preferences
- Tone3000 authentication tokens (Keychain)

This data can be managed through the app and is included in your device backups.

## Data Deletion

You can delete your files at any time through the app's IR and NAM browsers. Uninstalling the app will remove all local data from your device. Tone3000 account data is managed via Tone3000's website.

## Tracking and Advertising

SonicDNA Engine does not use advertising identifiers (IDFA) and does not share data with advertisers. Firebase Analytics uses anonymous identifiers that are not linked to your personal identity.

## Children's Privacy

SonicDNA Engine does not knowingly collect personal information from children under 13. Firebase Analytics does not collect personally identifiable information.

## Changes to This Policy

We may update this Privacy Policy from time to time. We will notify you of any changes by posting the new Privacy Policy on this page and updating the "Last updated" date.

## Contact Us

If you have any questions about this Privacy Policy, please contact us at:

📧 **sonicdna@hakaru.net**

---

© 2026 hakaru.net
