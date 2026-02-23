# 🌌 Gesture-Controlled Schwarzschild Black Hole

A high-performance astrophysical simulation built purely for the fun of merging **General Relativity** with **AI-powered Computer Vision**. This project replaces traditional mouse inputs with a real-time gesture engine to manipulate a 3D spacetime environment.


## 💡 The Project Concept

I built this because I wanted to see if I could make the "invisible" math of black holes interactive. It was a personal challenge to combine complex physics shaders with modern AI libraries.

### 1. The Physics (Optics & Space)
* **Gravitational Lensing:** I wrote a custom **GLSL Fragment Shader** to simulate how light warps around a massive object. It creates that signature "Einstein Ring" effect in real-time.
* **Accretion Disk:** Uses **Simplex Noise** to simulate flowing plasma. I linked the flow speed and disk density directly to the gesture engine.
* **Event Horizon:** Features a Fresnel-effect glow and a deep-black core to represent the Schwarzschild radius.

### 2. The AI (MediaPipe Hand Tracking)
I integrated the **Google MediaPipe HandLandmarker** to create a "zero-UI" experience:
* **Neural Mapping:** The AI tracks 21 hand joints. Moving your hand in 3D space controls the camera's orbital position.
* **Pinch-to-Expand:** I wrote a logic script that calculates the distance between your thumb and index finger. As you "pinch" in the air, the accretion disk physically expands and speeds up.

---

## 🛠️ Tech Stack
* **Language:** JavaScript (ES6+), GLSL (Shaders)
* **Graphics Library:** Three.js (WebGL)
* **AI Engine:** MediaPipe Vision Tasks
* **Post-Processing:** UnrealBloom (for that cinematic glow)

## 🔧 Engineering Challenges
* **Smoothing Input:** Hand tracking can be jittery, so I implemented **Linear Interpolation (LERP)** to make the camera movement feel smooth and cinematic.
* **Optimization:** Rendering 150,000 stars and heavy shaders simultaneously meant optimizing the GPU usage to keep the frame rate high.

---

## 👨‍💻 About Me
I'm a Physics & Astronomy enthusiast who loves building computational tools and experimental projects. I spend my time exploring the intersection of theoretical science and creative coding.
