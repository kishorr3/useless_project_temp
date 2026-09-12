<img width="1280" height="640" alt="git (1)" src="https://github.com/user-attachments/assets/8920b256-2ba8-4988-b824-5351134eb4bd" />



# [RoastCam] 🎯


## Basic Details
### Team Name: [Broken Brain Cell]


### Team Members
- Team Lead: [Nandakishor k] - [geck]
- Member 1: [vaishnav k] - [geck]
- Member 2:[Nandakishor k] - [geck]

### Project Description
### Description — 280 characters max

**RoastCam is a useless yet entertaining AI web app that detects your facial emotion, raised fingers, and mouth state in real time. It combines these signals to generate hilarious roasts, speaks them aloud, and turns the experience into a gamified challenge with missions, XP, combos, and a pixel-art octopus.**

### The Problem (that doesn't exist)
People constantly struggle with serious problems like communication, productivity, and decision-making. Unfortunately, RoastCam solves none of them. Instead, it tackles the critical issue of not knowing what your face, fingers, and mouth are doing right now—even though you can already see them yourself.

### The Solution (that nobody asked for)

RoastCam uses real-time AI to analyze your **facial expression, raised fingers, and mouth position** through your webcam. It combines these detections to generate sarcastic roasts, reads them aloud using text-to-speech, and turns the whole pointless process into a gamified experience with **missions, XP, combos, and a pixel-art octopus**.


## Technical Details

For Software:

HTML5 – Webpage structure and semantic elements
CSS3 – Custom styling, animations, responsive layouts, and visual effects
JavaScript (ES6+) – Application logic, AI processing, interactions, and state management
React 18 – Component-based frontend development and Hooks
Vite – Fast development server and production build tooling
Tailwind CSS – Utility-first responsive UI styling
TensorFlow.js – Client-side facial emotion recognition
WebGL – Hardware-accelerated TensorFlow.js inference
MediaPipe Tasks Vision – Real-time face and hand landmark detection
WebAssembly (WASM) – Efficient client-side MediaPipe execution
Web Camera API (getUserMedia) – Real-time webcam access
HTML5 Canvas – Rendering face/hand landmarks, skeletons, and detection overlays
Web Speech API – Reading generated roast dialogues aloud
RequestAnimationFrame – Non-blocking real-time AI inference loop
GSAP / ScrollTrigger – Scroll-driven landing-page character animation
LocalStorage – Storing lightweight preferences such as voice settings and game progress
Git & GitHub – Version control and project hosting


### Implementation
For Software:
### Implementation

**For Software:**

The RoastCam application is implemented as a **React 18 + Vite** web application with a two-page architecture: a visually animated landing page and an interactive AI Lab.

**Landing Page**

* Implements a scroll-driven animation where the two supplied characters begin with a high-five and smoothly separate toward opposite sides as the user scrolls.
* Uses the supplied UI reference to define typography, color palette, spacing, borders, decorative elements, and overall visual style.
* Integrates the supplied pixel-art octopus as the project mascot.
* Provides navigation to the AI Lab without requesting camera access on the landing page.

**AI Lab**

* Requests webcam access using `navigator.mediaDevices.getUserMedia()` with 1280×720 ideal resolution and front-facing camera settings.
* Displays the live video with a perfectly aligned HTML5 canvas overlay.
* Mirrors both video and canvas using CSS `scaleX(-1)` while preserving the original MediaPipe coordinates for calculations.

**Face & Emotion Processing**

* Detects the face and extracts its bounding box.
* Crops the face from the raw video frame.
* Converts the crop to grayscale and resizes it to **48×48 pixels**.
* Normalizes pixel values from **0–255 to 0–1**.
* Expands the tensor to **[1, 48, 48, 1]**.
* Runs the TensorFlow.js emotion model using the **WebGL backend**.
* Displays probabilities for Angry, Disgust, Fear, Happy, Sad, Surprise, and Neutral.

**Hand & Finger Processing**

* Uses **MediaPipe Tasks Vision** for 21-point hand landmark detection.
* Detects hand handedness.
* Counts raised fingers using landmark geometry:

  * Fingers: `Y_tip < Y_pip`
  * Right thumb: `X_tip < X_ip`
  * Left thumb: `X_tip > X_ip`
* Renders hand landmarks and connecting bones on the canvas.

**Mouth Detection**

* Uses facial landmarks to determine whether the mouth is:

  * Closed
  * Slightly Open
  * Open
  * Wide Open

**Roast Engine**

* Combines emotion, finger count, mouth state, and derived expressions to select a humorous response.
* Uses randomized roast messages while preventing immediate repetition.
* Uses state stability and cooldown periods to prevent the roast from changing every inference frame.

**Voice Output**

* Uses the browser's **Web Speech API** and `SpeechSynthesisUtterance`.
* Automatically reads newly generated roast dialogues aloud.
* Provides voice enable/disable and replay controls.

**Gamification**

* Includes real-time missions based on face, hand, mouth, and multimodal combinations.
* Awards XP for successful missions.
* Tracks combo streaks.
* Displays session statistics and an end-of-session verdict.

**Performance & Memory Management**

* Uses `requestAnimationFrame()` for the real-time inference loop instead of `setInterval()`.
* Uses `tf.tidy()` for transient TensorFlow.js operations to prevent WebGL memory leaks.
* Tracks actual FPS and inference latency.
* Cancels animation loops and stops media tracks when the Lab component is unmounted.

**Privacy**

* All AI processing is designed to occur locally in the browser.
* Webcam frames are not intentionally uploaded to a remote server.
* Only lightweight preferences and game settings may be stored locally using `localStorage`.

# Installation
git clone https://github.com/YOUR_USERNAME/RoastCam.git && cd RoastCam && npm install && npm run dev

# Run
npm run dev

## 📚 Project Documentation

The complete project documentation, including the system overview, implementation details, AI workflow, UI design, assets, feature breakdown, and execution details is available below.

### 🎥 Screen Recording / Demo

[▶️ View the RoastCam Screen Recording]((https://drive.google.com/file/d/1nEBBmEF6l6amSFRJyMwQBUPfTkdcxffB/view?usp=drive_link))

> **Note:** Make sure the Google Drive file sharing is set to **Anyone with the link → Viewer** so that the recording can be accessed.



### Project Demo
# Video
https://drive.google.com/file/d/1nEBBmEF6l6amSFRJyMwQBUPfTkdcxffB/view?usp=drive_link
*Explain what the video demonstrates*


## Team Contributions
- [Nandakishor k]: [Frontend development, UI/UX design, landing-page animations, AI integration, camera module, emotion detection, roast engine, and overall project architecture.]
- [Vaishnav k]: [Hand and mouth detection, MediaPipe integration, finger-counting logic, text-to-speech, gamification features, testing, documentation, and deployment.]


---
Made with ❤️ at TinkerHub Useless Projects 

![Static Badge](https://img.shields.io/badge/TinkerHub-24?color=%23000000&link=https%3A%2F%2Fwww.tinkerhub.org%2F)
![Static Badge](https://img.shields.io/badge/UselessProjects--26-26?link=https%3A%2F%2Ftinkerhub.org%2Fevents%2F1M8ORET9A1%2Fuseless-projects-3.0)



