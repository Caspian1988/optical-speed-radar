# Optical Speed Radar 🚗⚡
[![Live Demo](https://img.shields.io/badge/🚀_Launch-Live_Demo-38bdf8?style=for-the-badge&logo=github&logoColor=white)](https://caspian1988.github.io/optical-speed-radar/)

A lightweight, browser-based computer vision tool that measures vehicle speed optically using a live camera feed, fixed distance calibration, and pixel-change scanline detection. 

Built with vanilla JavaScript and the HTML5 Canvas API—no heavy Python or external AI frameworks required.

---

## How It Works

Traditional speed radar uses radio waves, but this tool uses **Optical Speed Estimation**:
1. **Calibration:** Two virtual scanlines (**Line A** and **Line B**) are placed on screen at a known physical distance apart (e.g., 20 feet).
2. **Motion Detection:** The application compares RGB values in a narrow band around each scanline frame-by-frame. When enough pixels change beyond the selected threshold, the crossing is recorded: Line A sets timestamp $t_1$, and Line B sets timestamp $t_2$.
3. **Velocity Math:** 
   $$\text{Speed (FPS)} = \frac{\text{Distance}}{\Delta t}$$
   $$\text{Speed (MPH)} = \text{FPS} \times 0.681818$$

---

## Features

* **Real-Time Video Feed:** Utilizes browser MediaDevices API for mobile or desktop camera streams.
* **Auto-Motion Scanline Trigger:** Automatically detects pixel differences when an object passes through the lines without requiring manual button presses.
* **Safety Guards & Sanity Capping:** Built-in debounce and threshold filters to eliminate false-trigger frame noise and cap out-of-range velocities.
* **Dark Executive UI:** Styled with a sleek, high-contrast dark theme (`#0f172a` backgrounds with cyan/emerald status highlights).

---

## Getting Started

1. Clone or download the repository.
2. Open `index.html` in your web browser (or use VS Code **Live Server**).
3. Click **Start Auto-Radar Camera** and grant camera permissions.
4. Input your measured distance in feet and test the motion triggers!# optical-speed-radar
