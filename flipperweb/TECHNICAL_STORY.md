# Technical Deep-Dive: Mechanics of a Captive Portal

This document provides an educational overview of the visual and networking mechanics that power modern captive portal research. Understanding how a high-fidelity portal interacts with a mobile device is critical for security researchers.

## 📡 1. The Gateway: Captive Portal Detection

When a mobile device (iOS/Android) connects to an open Wi-Fi network, it immediately attempts to "phone home" to a specific URL to verify internet connectivity:
- **iOS/macOS**: `http://captive.apple.com/hotspot-detect.html`
- **Android**: `http://connectivitycheck.gstatic.com/generate_204`

If the device successfully reaches these URLs, it assumes a full internet connection. If the network redirects or blocks these requests, the device triggers the **Captive Portal Browser** (a sandboxed web view) to display your `index.html`.

## 🔀 2. The Redirection: DNS Hijacking

In a "Flipper Zero Evil Portal" scenario, the device acts as both the Access Point (AP) and the DNS server. When a device requests *any* domain (like `google.com`), the DNS server responds with its own IP address instead of the actual server IP.

This is **DNS Hijacking**. Once the device thinks your Flipper Zero *is* the requested server, it sends its HTTP requests to you, allowing you to serve the high-fidelity portals in this repository.

## 🎨 3. The Visual Lie: Rendering High Fidelity

The reason these templates are "high fidelity" is to ensure the **Captive Portal Browser** renders a UI that feels authentic to the user.
- **Single-File Structure**: Since the captive portal environment is isolated, it cannot reach external CDNs for fonts or scripts. We inline everything (CSS, Google "G" SVG, etc.) to ensure the UI is 100% reliable.
- **Dark Mode Support**: Use of `prefers-color-scheme` or standard dark CSS variables (as used here) matches the user's system theme, further increasing credibility.

## 📤 4. The Finish: Data Exfiltration

Once a user enters their credentials, the "exfiltration" phase begins. There are three common patterns displayed in this project:

### A. Discord Webhook (External)
- **How it works**: Uses the JavaScript `fetch()` API to send a POST request to a Discord URL.
- **Requirement**: The researcher's hardware must have a "bridge" to the internet (e.g., via a secondary Wi-Fi module or tethered cellular connection).

### B. Local Storage (Persistent)
- **How it works**: Uses `localStorage.setItem()` to save the data directly on the user's device.
- **Requirement**: Works 100% offline. The data remains in the browser sandbox until the researcher manually inspects it or an exfiltration bridge becomes available.

### C. Server-Side Submission (Traditional)
- **How it works**: A standard HTML `<form>` submission or `fetch()` to a local backend (like a PHP or Python server running on the researcher's laptop).
- **Requirement**: A local network connection between the AP and a backend server.

---
*Disclaimer: This information is provided for educational purposes within a controlled, ethical security research environment.*
