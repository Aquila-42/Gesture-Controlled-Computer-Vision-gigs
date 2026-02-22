# 🌌 Gesture-Controlled Schwarzschild Black Hole

An interactive, high-performance astrophysical simulation that merges **General Relativity** with **AI-powered Computer Vision**. Instead of a mouse, this project uses real-time hand tracking to manipulate a 3D spacetime environment. Features 150,000+ particles, custom noise-flow shaders, and pinch-to-zoom logic—a study in mapping human input to complex mathematical environments.

*(Note: Requires camera access for the hand-tracking AI to function. Your camera data is processed locally in your browser and is never sent to external servers.)*

---

## 📸 Live Demo

🎮 **Try it out:** [Live Demo](https://your-deployment-link.com) *(add your deployment URL)*

*For best experience, use a modern browser (Chrome, Edge, Safari) with adequate lighting.*

---

## 💡 The Core Concepts

### 1. The Physics (General Relativity)
The core of this project is a custom **GLSL Fragment Shader** that simulates **Gravitational Lensing**. 
* **Light Bending:** I implemented a distortion algorithm that calculates how light from the background stars and the accretion disk would warp around a massive object.
* **Accretion Disk:** The disk uses **Simplex Noise** to simulate the flow of superheated plasma, with its speed and density being dynamically adjustable.
* **Event Horizon:** A perfect "black" sphere (Schwarzschild radius) surrounded by a Fresnel-effect glow to represent the photon sphere.

### 2. The AI (MediaPipe Computer Vision)
I integrated the **Google MediaPipe HandLandmarker** API to create a "zero-UI" interaction model:
* **Camera Mapping:** The AI tracks 21 hand joints. I specifically mapped the "Middle Finger MCP" joint to the 3D camera coordinates.
* **Rotation & Zoom:** Moving your hand horizontally rotates the view, while vertical movement adjusts the orbital distance (Zoom).
* **Pinch-to-Expand:** I wrote custom logic that calculates the Euclidean distance between the **Thumb Tip (Index 4)** and **Index Tip (Index 8)**. As you "pinch," the accretion disk physically expands and its flow velocity increases.

---

## 🛠️ Tech Stack
* **Language:** JavaScript (ES6+), GLSL (Shaders)
* **Graphics:** [Three.js](https://threejs.org/) (WebGL)
* **AI Engine:** [MediaPipe](https://developers.google.com/mediapipe) Vision Tasks
* **Styling:** CSS3 (Glassmorphism UI)

## 🔧 Technical Challenges Solved
* **Smoothing Input:** Hand tracking can be "jittery." I implemented **Damping/Interpolation** logic to ensure the camera movement feels cinematic rather than shaky.
* **Resource Management:** Rendering 150,000 stars and complex shaders simultaneously required optimizing the `BufferGeometry` and limiting the `PixelRatio` for smoother performance on laptops.
* **Coordinate Inversion:** Corrected the "Mirror Mode" from the webcam so that moving your hand to the right actually rotates the cosmos to the right.

---

## 🚀 Getting Started

### Prerequisites
* Node.js (v14 or higher)
* npm or yarn
* A modern web browser with WebGL support
* Camera/Webcam

### Installation

1. **Clone the repository:**
```bash
git clone https://github.com/Aquila-42/Gesture-Controlled-Computer-Vision-gigs.git
cd Gesture-Controlled-Computer-Vision-gigs
