# 🌌 Gesture-Controlled Black Hole Simulation

A high-fidelity, interactive astrophysical simulation that combines **General Relativity** concepts with **Computer Vision**. Built during my final year at **NIT Rourkela**, this project explores how we can use AI to interact with complex physical environments.

## 🚀 [Click Here for the Live Demo]

## 🛠️ How it Works

### 1. The Physics (General Relativity & Optics)
Most black hole visualizations are static. In this project, I used **GLSL Shaders** to implement:
* **Gravitational Lensing:** A custom shader that calculates light distortion around the Schwarzschild radius.
* **Accretion Disk Dynamics:** I used Simplex noise to simulate the "flow" of gas. The disk isn't just a texture; it's a dynamic system where the flow speed reacts to your gestures.
* **150,000 Stars:** To make the background feel like deep space, I used `BufferGeometry` to render a massive starfield with minimal performance lag.

### 2. The AI (MediaPipe Hand Tracking)
I replaced the mouse with an **AI Hand-Gesture Engine**. By integrating **Google MediaPipe**, the code tracks 21 points on your hand:
* **Orbit:** Moving your hand in the air rotates the camera around the event horizon.
* **Pinch-to-Scale:** I wrote a function that calculates the distance between your thumb and index finger. As you "pinch" in the air, the accretion disk expands or contracts.
* **Real-time Processing:** The simulation runs at a high FPS by offloading the hand-tracking logic to the GPU.


## 💻 Tech Stack
* **Graphics:** Three.js (WebGL)
* **AI/ML:** MediaPipe Vision Tasks
* **Shaders:** GLSL (Vertex & Fragment)
* **UI:** HTML5/CSS3 (Glassmorphism design)

## 🧠 Challenges I Overcame
* **Jitter Control:** Real-time hand tracking can be shaky. I implemented a **Damping Algorithm** (linear interpolation) to ensure the camera movement feels smooth and cinematic.
* **Mathematical Mapping:** Translating 2D webcam coordinates into 3D orbital coordinates required some tricky trigonometry to make the "interaction" feel natural to the user.


## 🛰️ About Me[project.html](https://github.com/user-attachments/files/25471116/project.html)

I'm a Physics major at **NIT Rourkela** passionate about bridging the gap between theoretical science and computational tools. This project is a step toward making "invisible" physics interactive.
[project.html](https://github.com/user-attachments/files/25471108/project.html)
