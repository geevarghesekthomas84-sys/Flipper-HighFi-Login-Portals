# Flipper-HighFi-Login-Portals

<p align="center">
  <img src="https://github.com/user-attachments/assets/e7eae45b-2dda-4e76-8f83-b1e3c99dd852" alt="Project Banner" width="200" />
</p>

A comprehensive collection of high-fidelity frontend replica portals for security research, UI/UX study, and captive portal prototyping. Optimized specifically for the **Flipper Zero Evil Portal** module.

---

## ✨ Preview

> [!TIP]
> To view these previews locally, add your own screenshots to the `./screenshots/` directory.

### 🔍 Google Login UI
<img src="https://github.com/user-attachments/assets/bd21024e-658e-40c6-971e-e1348bb5e647" alt="Google Preview" width="100%" />

### 🍎 Apple Login UI
<img src="https://github.com/user-attachments/assets/8297f454-cb56-4026-b8b1-101e97903d99" alt="Apple Preview" width="100%" />

### 📘 Facebook Login UI
<img src="https://github.com/user-attachments/assets/46e0c383-c3cd-4ed0-99c5-85a3dcf66543" alt="Facebook Preview" width="100%" />

### 📦 Amazon Login UI
<img src="https://github.com/user-attachments/assets/d0f875eb-222d-43a7-8a41-547fe3a01cff" alt="Amazon Preview" width="100%" />

---

## 📌 Project Overview

This repository provides zero-network, self-contained authentication interfaces. It is designed to help researchers:
*   **Analyze** real-world login UX patterns and micro-interactions.
*   **Compare** multi-step authentication flows (Identifier -> Password -> Success).
*   **Test** rendering performance in resource-constrained environments (ESP32).
*   **Prototype** captive portal interfaces for security awareness training.

---

## 🎯 Key Features

*   🔹 **Pure Frontend**: 100% HTML, CSS, and Vanilla JavaScript. No backend required.
*   🔹 **Zero-External Assets**: All fonts, icons (SVG), and styles are inlined for offline reliability.
*   🔹 **Optimized for Flipper Zero**: Specifically formatted for easy deployment to the Evil Portal module.
*   🔹 **Multiple Variants**: Includes specialized versions for Discord webhooks and local storage persistence.
*   🔹 **Responsive Design**: Elegant split-pane layouts that adapt to both desktop and mobile screens.

---

## 📂 Project Structure

Each subdirectory is a standalone project:

*   **`Google_standard/`** / **`Apple_standard/`** / **`facebook_standard/`** / **`Amazon_standard/`**
    *   Optimized for standard Flipper Zero `/get` capture.
*   **`Google_discord/`** / **`Apple_discord/`** / **`facebook_discord/`** / **`Amazon_discord/`**
    *   Ready for Discord Webhook integration (requires custom webhook URL).
*   **`google_local/`**
    *   Demonstrates offline persistence using `localStorage`.
*   **`google_server/`**
    *   Configured for traditional server-side submission.
*   **`flipper_evil_portal/`**
    *   A consolidated, ultra-lean version of the Google portal.

---

## 🚀 Quick Start

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/geevarghesekthomas84-sys/Flipper-HighFi-Login-Portals.git
    cd Flipper-HighFi-Login-Portals
    ```

2.  **Run a portal:**
    Simply open the `index.html` file in any subdirectory with your web browser. Or, for Flipper Zero users, copy the desired `index.html` to your SD card under `/apps/EvilPortal/`.

---

## ⚖ Ethics & Legal Notice

> [!CAUTION]
> This project is for **strictly educational and authorized security research purposes only.**

**The author does NOT condone, support, or encourage:**
*   Phishing or social engineering against non-consenting individuals.
*   Impersonation of services for malicious gain.
*   Unauthorized data collection.

**Functional Note:** The mock portals in this repository do not connect to real authentication servers. Standard versions are configured to redirect captured data to a local `/get` endpoint for researcher logging.

---

## 👤 Author

**Geevarghese Thomas**
*   GitHub: [@geevarghesekthomas84-sys](https://github.com/geevarghesekthomas84-sys)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE.txt).

---
*If you find value in these templates for your research, please give this repository a ⭐ on GitHub!*
