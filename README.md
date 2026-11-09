# 🌐 3Dview — Spatial DOM & 4D Layer Matrix Extension

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Manifest V3](https://img.shields.io/badge/Chrome%20Extension-Manifest%20V3-success.svg)](https://developer.chrome.com/docs/extensions/mv3/intro/)
[![GitHub Repo](https://img.shields.io/badge/GitHub-sahilkumardhala%2F3Dview-181717?logo=github)](https://github.com/sahilkumardhala/3Dview)

Transform any live 2D website into an interactive 3D spatial stack in real-time. Inspired by Firefox's classic *Tilt 3D* visualizer, **3Dview** calculates nested DOM hierarchies, transforms elements along the Z-axis using hardware-accelerated CSS `preserve-3d`, and provides a 4D time/mutation oscillation slider.

---

## 🚀 Features

- **Automatic Layer Extrusion:** Traverses document nodes and extrudes them forward along the Z-axis based on their DOM nesting depth and computed `z-index`.
- **Interactive Orbit Camera:**
  - **Click + Drag:** Orbit around the page at any angle.
  - **Scroll Wheel:** Seamlessly zoom in and out of nested components.
- **Glassmorphic On-Screen HUD:**
  - **Layer Gap (Z) Slider:** Expand or collapse vertical separation between composite elements.
  - **Perspective Zoom Slider:** Adjust camera field of view.
  - **4D Time Pulse:** Animate a phase wave across layer indices to inspect dynamic DOM updates across time.
- **Color-Coded Depth:** Automatic hue shifting along the color spectrum so distinct layers are instantly identifiable.
- **Clean Teardown:** Single-click exit button cleans up all injected styles and restores the page's original state.
- **Zero Dependencies:** Pure vanilla JavaScript, CSS, and Manifest V3. No heavy libraries or external CDNs required.

---

## 📁 Repository Structure

```text
3Dview/
├── manifest.json      # Chrome/Edge Manifest V3 extension configuration
├── background.js     # Background service worker (toggles script injection)
├── content.js        # Core engine: DOM parser, 3D transform, camera & HUD
├── styles.css        # 3D viewport perspective, glassmorphic UI, highlights
└── README.md         # Project documentation
```

---

## 📥 Installation Guide

### Desktop (Chrome, Brave, Edge, Opera, Arc)

1. Clone or download this repository:
   ```bash
   git clone https://github.com/sahilkumardhala/3Dview.git
   ```
   *(Or download and extract the `3Dview.zip` archive).*
2. Open your Chromium-based browser and navigate to:
   - **Chrome / Brave:** `chrome://extensions/`
   - **Microsoft Edge:** `edge://extensions/`
3. Toggle on **Developer mode** in the top-right corner.
4. Click **Load unpacked**.
5. Select the `3Dview` directory containing `manifest.json`.
6. Pin **3Dview** to your browser toolbar.

---

## 🎮 How to Use

1. Navigate to any website (e.g., [GitHub](https://github.com), [Wikipedia](https://wikipedia.org), [MDN](https://developer.mozilla.org)).
2. Click the **3Dview** icon in your extension bar.
3. Use the following controls:
   - **Left Click + Drag:** Rotate/orbit the website in 3D space.
   - **Mouse Wheel:** Zoom in and out.
   - **Layer Gap:** Adjust distance between nested levels.
   - **4D Time Pulse:** Trigger temporal wave oscillation across layers.
   - **Reset:** Restore default camera angle.
   - **Exit 3D:** Return the website to standard 2D view.

---

## 📱 Troubleshooting: Uploading from Mobile to GitHub

If you are uploading these files to GitHub using a mobile browser (Android/iOS) and `.js` or `.json` files appear grayed out or hidden:

### Why this happens
Mobile file selectors filter files using **MIME types** and OS security sandboxes. Android often flags `.js` files as executable scripts and excludes them from document/media pickers.

### Solutions

#### Option 1: Direct File Creation (Recommended on Phone)
1. In your GitHub repository (`https://github.com/sahilkumardhala/3Dview`), tap **Add file** $\rightarrow$ **Create new file**.
2. Type the filename (e.g., `manifest.json`, `content.js`, `background.js`, `styles.css`).
3. Copy and paste the code directly into the browser editor and tap **Commit changes**.

#### Option 2: The `.txt` Rename Trick
1. In your phone's file manager, temporarily rename the files:
   - `manifest.json` $\rightarrow$ `manifest.json.txt`
   - `content.js` $\rightarrow$ `content.js.txt`
   - `background.js` $\rightarrow$ `background.js.txt`
2. Upload the `.txt` files through GitHub's web interface.
3. On GitHub, click each file, tap the **pencil (Edit)** icon, remove `.txt` from the filename, and commit.

#### Option 3: Internal Storage Direct Browse
1. When the file chooser opens on Android, tap the **three bars / menu** in the top-left corner.
2. Select your device's **Internal Storage** directly (instead of *Recent* or *Downloads*).
3. Tap the three dots in the top-right and enable **Show hidden files**.

---

## 🛠️ Built With

- **HTML5 & CSS3** (`perspective`, `transform-style: preserve-3d`, `translateZ`)
- **JavaScript (ES6+)**
- **Chrome Extensions API (Manifest V3)**

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

**Developed & Maintained by [sahilkumardhala](https://github.com/sahilkumardhala)**
