# 🔒 FaceLock: Biometric Security Terminal

![Version](https://img.shields.io/badge/version-1.0.0--beta-blue?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey?style=for-the-badge)

**FaceLock** is a professional-grade, localized biometric security terminal for Windows. Designed as a high-tech alternative for laptops and desktop PCs that do not support Windows Hello, it transforms any standard 2D RGB webcam into an advanced security scanner to protect your desktop with a sleek, sci-fi-inspired HUD.

---

## ✨ Features

### 🛡️ Biometric Security
* **The Ultimate Windows Hello Alternative:** Brings millisecond-fast biometric authorization to any standard webcam. No expensive Infrared (IR) depth sensors required.
* **Privacy-First Encryption:** All biometric tokens and emergency pins are encrypted using **AES-128 (Fernet)**.
* **Zero-Cloud Architecture:** 100% of your data stays on your local machine. No photos or facial markers are ever uploaded to external servers.

### 🎮 Tactical HUD UI
* **Animated Laser Scanline:** Constant vertical scanning effect for a high-security aesthetic.
* **Dynamic Targeting:** HUD brackets that visually "lock onto" the authorized user's face.
* **Live Telemetry:** Real-time data feed displaying system status, memory allocation, and encryption layers.

### 🚫 Anti-Intruder Protocol
* **Intruder Trap:** Secretly captures high-resolution photographs of unauthorized individuals after 10 frames of failed recognition.
* **Persistence:** Stays "Topmost" and intercepts `Alt+F4` to prevent intruders from simply closing the security window.
* **Emergency Failsafe:** Built-in manual override via **Ctrl + U** for low-light scenarios or hardware failure.

---

## 🚀 Getting Started

### Installation
For the most reliable experience, use our standalone "One-Click" installer:
1. Navigate to the [Releases](https://github.com/freddieallance/FaceLock/releases) page.
2. Download `FaceLock_Setup.exe`.
3. **SmartScreen Bypass:** Since this is a new beta release, Windows SmartScreen may block the installer. Click **"More info"**, then select **"Run anyway"**.
4. Run the installer (Non-admin "Current User" mode recommended for full functionality).
5. (Optional) Select **"Run at Startup"** during the wizard to automate your security.

### Initial Setup (Enrollment)
1. Launch **FaceLock**.
2. Align your face within the green targeting brackets in a well-lit area.
3. Press **SPACE** to capture and encrypt your biometric token.
4. Follow the prompt to create your **4-digit Emergency PIN**.

---

## ⌨️ Controls & Shortcuts

| Shortcut | Action |
| :--- | :--- |
| **Spacebar** | Enroll face (Initial setup only) |
| **Ctrl + U** | Trigger Manual Override (Enter PIN to unlock) |
| **Esc** | Cancel registration / Exit setup |

---

## 🛠️ Technical Stack

* **Language:** Python 3.x
* **UI Framework:** Tkinter & Pillow (PIL)
* **Vision Engine:** OpenCV & Face_Recognition (`dlib`)
* **Encryption:** Cryptography (Fernet/AES)
* **Deployment:** PyInstaller & Inno Setup

---

## 📂 Project Directory
```text
FaceLock/
├── Intruders/          # Logged photos of unauthorized access attempts
├── facelock.py         # Main terminal source code
├── user_face_data.enc  # Encrypted biometric token (Local only)
├── failsafe.enc        # Encrypted emergency PIN (Local only)
└── secret.key          # AES encryption key
