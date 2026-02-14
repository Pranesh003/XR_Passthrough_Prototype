<img width="1919" height="1023" alt="Screenshot 2026-02-14 194612" src="https://github.com/user-attachments/assets/347e4a3a-ad7e-4c60-a719-e463be2b35d0" />
<img width="1919" height="315" alt="Screenshot 2026-02-14 195837" src="https://github.com/user-attachments/assets/31ba357e-9199-4d71-899e-74d43a338a9a" />

# XR Home Interface Prototype (Unity + OpenXR Simulation)

## 📌 Overview

This project is a Unity-based XR-style home interface prototype developed as part of a Design & Unity Developer Intern assessment.

The objective was to simulate a system-level XR home menu featuring:

- Live system date and time
- Passthrough toggle functionality
- Webcam-based passthrough simulation (for non-XR systems)
- Volume and brightness controls
- Dummy app launcher system
- Smooth XR-style UI animations

The project demonstrates structured problem-solving, UI system design, runtime logic handling, and simulation of hardware-dependent XR features without requiring physical XR devices.

---

## 🎯 Problem Statement

Design a single-screen XR home interface that:

- Displays live system date and time (auto-updating)
- Includes multiple application buttons (dummy apps allowed)
- Provides brightness and volume controls
- Implements a passthrough toggle using OpenXR
- Simulates passthrough visually using a webcam (for editor testing)
- Logs passthrough ON/OFF states in console
- Includes a 3-minute explanation video

Since real passthrough cannot be visualized inside the Unity Editor without XR hardware, a simulation-based approach was required.

---

## 🧠 Approach & Design Decisions

### 1️⃣ XR System UI Structure
The interface was built using Unity Canvas UI in a modular format:

- Single unified Home Screen
- Grid-based app launcher layout
- Overlay-based brightness simulation
- AudioListener-based volume control
- Webcam texture simulation for passthrough

---

### 2️⃣ Passthrough Simulation Strategy

**Challenge:**  
Unity Editor cannot preview real XR passthrough.

**Solution:**
- Implemented OpenXR-style passthrough logic using console logs.
- Simulated visual passthrough using `WebCamTexture`.
- Same button controls both logic and visual simulation.

This ensures:
- Task requirement compliance
- Hardware-independent testing
- Clear state visibility during runtime

---

### 3️⃣ XR-Style UI Enhancements

To improve realism and user experience:

- Smooth fade & scale animations using Coroutines
- CanvasGroup-based opacity transitions
- Grid Layout Group for XR-style app arrangement
- Modular script structure for scalability

---

## ✨ Key Features

### 🕒 Live Date & Time
- Uses `System.DateTime.Now`
- Automatically updates during runtime
- No manual refresh required

### 🔘 Passthrough Toggle
- Logs ON/OFF state in console
- Activates webcam simulation
- Single-button state management

### 📷 Webcam-Based Passthrough Simulation
- Uses `WebCamTexture`
- Full-screen RawImage display
- Automatically turns ON/OFF with passthrough state

### 🎛 Brightness Control
- Black overlay using Image component
- Alpha channel manipulatio
