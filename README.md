# 🔒 FaceLock: Biometric Security Terminal

![Version](https://img.shields.io/badge/version-1.0.0--beta-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey)

**FaceLock** is a professional-grade, localized biometric security terminal for Windows. It transforms your standard webcam into a high-tech security scanner, using advanced facial recognition to protect your desktop with a sci-fi-inspired HUD.

---

## ✨ Features

* **Biometric Authorization:** Uses the state-of-the-art `dlib` facial recognition engine for high-speed, accurate matching.
* **Tactical HUD UI:** A sleek, dark-themed interface featuring:
    * **Animated Laser Scanline:** Constant vertical scanning effect.
    * **Targeting Brackets:** Dynamic UI that tracks your face.
    * **System Telemetry:** Live data feed displaying system status and encryption level.
* **Privacy-First Encryption:** * All biometric tokens and pins are encrypted using **AES-128 (Fernet)**.
    * **100% Local Storage:** No photos or facial data ever leave your machine.
* **Intruder Trap:** Secretly captures high-resolution photographs of unauthorized users after 10 frames of failed recognition. 
* **Anti-Bypass Protection:** Blocks `Alt+F4` and stays "Topmost" to prevent intruders from closing the lock screen.
* **Emergency Failsafe:** Built-in manual override via **Ctrl + U** for low-light or hardware failure scenarios.

---

## 🚀 Getting Started

### Installation
For the easiest experience, use our standalone installer:
1.  Navigate to the [Releases](https://github.com/YOUR_USERNAME/FaceLock/releases) page.
2.  Download the `FaceLock_Setup.exe`.
3.  Run the installer (Supports "Run at Startup" configuration).

### Initial Setup (Biometric Enrollment)
1.  Launch **FaceLock** for the first time.
2.  Align your face within the green targeting brackets.
3.  Ensure you are in a well-lit area and press **SPACE** to capture your biometric token.
4.  Follow the prompt to create your **4-digit Emergency PIN**.

---

## ⌨️ Controls & Shortcuts

| Key | Action |
| :--- | :--- |
| **Spacebar** | Enroll face (During initial setup only) |
| **Ctrl + U** | Trigger Manual Override (Enter PIN to unlock) |
| **Esc** | Cancel registration/exit setup |

---

## 📂 Project Structure

```text
FaceLock/
├── Intruders/          # Captured photos of unauthorized access attempts
├── facelock.py         # Main application source code
├── user_face_data.enc  # Encrypted biometric token (Local only)
├── failsafe.enc        # Encrypted emergency PIN (Local only)
└── secret.key          # AES encryption key
