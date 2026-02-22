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
```

2. **Install dependencies:**
```bash
npm install
```

3. **Start the development server:**
```bash
npm start
```

4. **Open your browser:**
Navigate to `http://localhost:3000` (or the port specified in your terminal)

5. **Grant camera permissions** when prompted by your browser

### Build for Production
```bash
npm run build
```

---

## 📖 Usage

1. **Allow camera access** - The application requires camera permissions to track your hand
2. **Move your hand horizontally** - Rotate the black hole view
3. **Move your hand vertically** - Zoom in/out of the orbital distance
4. **Pinch your thumb and index finger** - Expand the accretion disk and increase plasma flow velocity
5. **Open hand** - Return to default state

---

## 🔒 Privacy & Security

* **Local Processing:** All camera data is processed locally in your browser using MediaPipe
* **No Data Collection:** Your camera feed is never sent to external servers
* **No Tracking:** This application does not track or store your movements
* **Camera Control:** You can disable camera access anytime through your browser settings

---

## 📁 Project Structure

```
├── src/
│   ├── components/       # React components
│   ├── shaders/         # GLSL fragment & vertex shaders
│   ├── utils/           # Hand tracking & math utilities
│   ├── App.js          # Main application
│   └── index.js        # Entry point
├── public/
│   └── index.html      # HTML template
├── package.json        # Dependencies
└── README.md          # This file
```

---

## 🎓 Physics Behind the Project

This project applies real **General Relativity** concepts:

* **Schwarzschild Metric:** Models spacetime curvature around a non-rotating black hole
* **Gravitational Lensing:** Light paths bend due to spacetime curvature
* **Photon Sphere:** The innermost stable circular orbit for light (1.5x Schwarzschild radius)
* **Accretion Disk Dynamics:** Simulates plasma behavior using Simplex noise and fluid dynamics principles

---

## 🔗 Resources & References

* [Three.js Documentation](https://threejs.org/docs/)
* [MediaPipe Hand Landmarks](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker)
* [Schwarzschild Black Holes - Physics](https://en.wikipedia.org/wiki/Schwarzschild_metric)
* [WebGL Fragment Shaders](https://www.khronos.org/opengl/wiki/Fragment_Shader)

---

## 👨‍🔬 About the Author

I am a Final Year **Physics & Astronomy** student at the **National Institute of Technology (NIT), Rourkela**. My goal is to bridge the gap between theoretical physics and computational engineering. This project represents my passion for combining astrophysics simulations with cutting-edge AI computer vision techniques.

📧 **Contact:** [Your Email]
🔗 **GitHub:** [@Aquila-42](https://github.com/Aquila-42)
🌐 **Portfolio:** [Your Portfolio Link]

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

* **Google MediaPipe** - For the excellent hand-tracking API
* **Three.js Community** - For the powerful WebGL library
* **NIT Rourkela** - For support and resources

---