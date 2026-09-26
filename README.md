# SAMVEDNA

**AI-Assisted Wearable Screening for Early Knee Osteoarthritis Risk** — SIH 2026, Problem Statement **26004**.

SAMVEDNA is an ESP32 wearable knee-band plus an offline-first Flutter companion
app for early osteoarthritis (OA) risk screening in remote and underserved
populations.

## Live links

| What | URL |
| --- | --- |
| Project website | https://samvedna-ksrct.vercel.app/ |
| GitHub Pages mirror | https://kanis007.github.io/samvedna/ |
| Android APK (v1.0.0) | https://samvedna-ksrct.vercel.app/public/apk/SAMVEDNA-v1.0.0.apk |
| Release notes | https://github.com/Kanis007/samvedna/releases/tag/v1.0.0 |

## What it does

1. **Wearable sensing** — the knee band captures acoustic emission, IMU and
   plantar pressure. Waveforms stream over BLE, then hand off to a local Wi-Fi
   SoftAP for high-rate transfer.
2. **Guided screening** — a sit-stand-sit protocol with an on-screen metronome and
   a calibration gate that must pass before any session is recorded.
3. **On-device risk tier** — features (hit count, amplitude, ROM, symmetry,
   loading asymmetry) are fused into a Low / Moderate / High tier with
   confidence and contributing factors.
4. **Offline-first** — everything is processed and stored on the phone. No
   internet connection is required at any point.

## App

- Package `com.samvedna.app`, version `1.0.0+2005`, Android 7.0+ (minSdk 24)
- Multilingual: English, தமிழ், हिन्दी, অসমীয়া
- PIN lock, encrypted local storage, sync queue for later upload
- One-tap demo mode: **Demo User / PIN 1234**, with 6 pre-seeded patients
  (healthy / warning / critical)

## Research foundation

Biomarker baselines are seeded from: Verma D.K. et al. (2026), *"Knee joint
health assessment using acoustic sensors in osteoarthritis: a quantitative and
parametric study"*, Med. Eng. Phys. 147, 015006.

> ## IMPORTANT CLINICAL DISCLAIMER
>
> SAMVEDNA is a **screening aid for demonstration**, **not a medical device** and
> **not a diagnosis**. Its risk engine is a clearly labelled `demo-rule-v1`
> placeholder seeded from published reference baselines and is **not clinically
> validated**. No screen, result, log or trend here is intended for clinical
> decisions. Clinical assessment of OA must follow standard care pathways using
> the healthcare worker's own judgement. This disclaimer must remain visible.

## Repository contents

```
index.html        single-page project website (no build step)
public/images/    logo and favicon
vercel.json       static deployment config
```

The APK is served from the deployment (`public/apk/`) and mirrored in GitHub
Releases.

## License

Academic / competition submission. The wearable firmware and the Flutter app are
provided for evaluation purposes.
