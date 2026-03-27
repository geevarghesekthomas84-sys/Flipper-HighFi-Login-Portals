# High-Fidelity UI Replication Study: Authentic Login Portals

This project is a technical study focused on the meticulous reproduction of modern, high-traffic authentication interfaces. It serves as an educational resource for frontend developers and security researchers, particularly those utilizing the **Flipper Zero Evil Portal** module, to understand complex CSS architectures, responsive split-pane layouts, and interactive captive portal designs.

## 🚀 Overview

The goal of this study was to achieve pixel-perfect parity with established UI/UX patterns used by major platforms (Apple, Google, Facebook). This involved:
- Recreating cinematic dark themes.
- Implementing custom SVG-based branding.
- Developing sophisticated "floating label" input systems.
- Designing multi-step authentication flows with smooth transitions.

## 🛠 Features

### 1. Advanced CSS Architecture
- **Responsive Split-Pane**: A 2-column layout that elegantly stacks on mobile devices.
- **Glassmorphism & Shadows**: High-fidelity depth through subtle gradients and drop shadows.
- **Micro-Animations**: Smooth interactivity during state changes and focus events.

### 2. Interactive Authentication Flows
- **Step-by-Step Logic**: Seamless transitions between identity and password steps without page reloads.
- **Domain Intelligence**: Functional examples of email domain validation and auto-appending.
- **Refined Feedback**: Polished success states and error handling for a premium user experience.

### 3. Localization & Privacy
- **Zero-Network Assets**: All branding elements (SVG codes), fonts, and icons are embedded or local, ensuring fast loads and a self-contained environment.
- **Privacy-Centric Study**: Demonstrates functional logic (like Discord webhook integration) for educational purposes to show how frontend data can be transmitted to external services.

## 📖 Educational Purpose

This repository is intended for:
- **Security Enthusiasts**: To study the visual structure of modern authentication portals and the mechanics of captive portal redirects.
- **Flipper Zero Researchers**: To utilize high-fidelity, zero-network HTML templates for the **Evil Portal** module.
- **UI/UX Designers**: To study spacing, typography, and color harmony in premium interfaces.

## 🐬 Flipper Zero Integration

These templates are specifically optimized for the **Evil Portal** module:
- **Single-File Portability**: CSS and JavaScript are inlined/local to avoid external dependency failures on isolated Access Points.
- **Resource Efficiency**: Optimized SVG paths and lean vanilla JavaScript ensure smooth performance on ESP32-based hardware.
- **Flexible Flow**: Easily modifiable `index.html` structure to fit the Evil Portal's naming conventions and server requirements.

## ⚖ License

This project is licensed under the MIT License. It is provided "as-is" for educational and research purposes only.

---
*Disclaimer: This project is a visual study and is not affiliated with, endorsed by, or representative of the actual platforms being studied.*
