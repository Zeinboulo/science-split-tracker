# 🏋️‍♂️ Science Split Tracker

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-emerald?style=for-the-badge&logo=github)](https://zeinboulo.github.io/science-split-tracker/)
[![Single-File Mobile App](https://img.shields.io/badge/Architecture-Single--File%20PWA-cyan?style=for-the-badge)](https://zeinboulo.github.io/science-split-tracker/)
[![Offline First](https://img.shields.io/badge/Storage-100%25%20Offline%20Local-purple?style=for-the-badge)](https://zeinboulo.github.io/science-split-tracker/)

An evidence-based, mobile-first single-file gym tracker specifically engineered around modern exercise science principles (lengthened-position overload, stimulus-to-fatigue optimization, proximity-to-failure tracking via RIR/RPE, and volume landmarks).

---

## 🌐 Live Application

- **Live URL**: [https://zeinboulo.github.io/science-split-tracker/](https://zeinboulo.github.io/science-split-tracker/)
- **Repository**: [https://github.com/Zeinboulo/science-split-tracker](https://github.com/Zeinboulo/science-split-tracker)

---

## 🔬 The Science-Based 3-Day Routine

Each workout is capped at **5 movements (15 working sets)** to maximize high-quality motor unit recruitment while preventing junk volume and excessive central fatigue.

### **Workout A: Upper Pec, Squats & Pull**
| Exercise | Sets | Reps | Primary Target | Science Note |
| :--- | :---: | :---: | :--- | :--- |
| **Incline Dumbbell Press** | 3 | 6–8 | Clavicular Head (Upper Pec) | 30° bench incline; deep stretch at bottom; elbows tucked 45–60°. |
| **Barbell Back Squat / Hack Squat** | 3 | 6–8 | Quads & Glutes | Deep knee flexion with a 1s pause in the bottom stretch; Target RIR 2. |
| **Chest-Supported Neutral Row** | 3 | 8–10 | Mid-Back & Lats | Chest support eliminates lumbar axial load; full protraction at extension. |
| **Cable Lateral Raise** | 3 | 12–15 | Lateral Deltoid | Cable path provides constant mechanical tension through lengthened range. |
| **Incline Dumbbell Curl** | 3 | 10–12 | Biceps (Lengthened Position) | Shoulders extended behind torso to stretch the biceps long head. |

---

### **Workout B: Posterior Chain, Lats & Sternal Chest**
| Exercise | Sets | Reps | Primary Target | Science Note |
| :--- | :---: | :---: | :--- | :--- |
| **Romanian Deadlift (RDL)** | 3 | 8–10 | Hamstrings & Glutes | Pure hip hinge; loads hamstrings eccentrically at maximum stretch. |
| **Lat Pulldown / Weighted Pull-Up** | 3 | 6–8 | Latissimus Dorsi | Vertical line of pull; 3s controlled eccentric back to full overhead stretch. |
| **Flat Dumbbell Bench Press** | 3 | 8–10 | Sternal Pectoralis | Converging pressing path for complete horizontal adduction. |
| **Overhead Cable Triceps Extension** | 3 | 10–12 | Triceps (Long Head) | Overhead shoulder flexion maximizes stretch on the biarticular long head. |
| **Hanging Leg Raise** | 3 | 12–15 | Rectus Abdominis | Posterior pelvic tilt curling pubis toward sternum to eliminate hip flexor takeover. |

---

### **Workout C: Quad/Adductor, Upper Back & Hamstrings**
| Exercise | Sets | Reps | Primary Target | Science Note |
| :--- | :---: | :---: | :--- | :--- |
| **Leg Press or Bulgarian Split Squat** | 3 | 10–12 | Quads & Adductors | Deep knee flexion without spinal compression; controlled 2s eccentric. |
| **Wide-Grip Cable Seated Row** | 3 | 10–12 | Upper Back & Rear Delts | 45–60° elbow flare targets rhomboids, mid-traps, and posterior deltoids. |
| **Low-to-High Cable Flye** | 3 | 12–15 | Upper Chest Isolation | Follows clavicular fibers; continuous tension at peak adduction. |
| **Standing Dumbbell Lateral Raise** | 3 | 12–15 | Lateral Deltoid | Torso slightly tilted forward (15°); peaks resistance at 90° abduction. |
| **Lying Leg Curl (or Seated)** | 3 | 10–12 | Hamstrings (Knee Flexion) | Isolated knee flexion *(Note: Seated leg curl provides greater stretch per Maeo et al. 2021)*. |

---

## ⚡ Key Features

1. **📈 Workout Evaluation & Hypertrophy Index**:
   - Dynamic 0–100 score and grade badge (`GRADE A+`, `A`, `B`) calculated from **Volume Adequacy**, **RIR Discipline**, and **Progressive Overload Velocity**.
   - Per-exercise overload badges (`📈 Overload Achieved` vs. `Baseline Maintained`).
2. **🧠 CNS & Muscular Readiness Evaluator**:
   - Interactive recovery sliders (Muscle Soreness / DOMS, Sleep Quality, Systemic Energy) with live physiological coaching advice.
3. **⏱️ Hypertrophy Rest Timer**:
   - Configurable countdown with real-time SVG progress ring.
   - Built-in synthesizer sound beeps using the **Web Audio API** (no external mp3 files required).
   - Mobile haptic vibration alerts via the **Vibration API**.
4. **📊 Weekly Volume Landmarks (MEV / MAV / MRV)**:
   - Tracks weekly sets per muscle group against scientific targets (Dr. Mike Israetel / Dr. Brad Schoenfeld guidelines).
5. **🧮 Epley 1RM Calculator**:
   - Calculates estimated 1RM and computes 75% (hypertrophy) and 85% (strength) working loads.
6. **💾 100% Client-Side Persistence**:
   - Automatic local saving via `localStorage` (works completely offline on mobile).
   - JSON Export and Import for seamless device backups.

---

## 🛠️ Tools & Technologies Used

| Technology / Tool | Category | Role in Application |
| :--- | :--- | :--- |
| **HTML5 Semantic & PWA Meta** | Frontend Foundation | Viewport-fit cover, iOS status bar styling, and accessible markup. |
| **Tailwind CSS (CDN)** | Styling & UI | Mobile-first dark theme, responsive grid layouts, and custom design tokens. |
| **CSS3 Animations** | UI / Micro-interactions | Custom keyframes (`@keyframes viewFadeSlide`, `popIn`, `pulseGlow`) for smooth tab transitions and button feedback. |
| **Vanilla JavaScript (ES6+)** | Logic & Architecture | Reactive single-page tab routing, session data management, and 1RM / volume computation. |
| **Web Audio API (`AudioContext`)** | Audio Synthesizer | Generates pure frequency audio chimes (sine wave oscillators) for timer notifications without external media assets. |
| **Navigator Vibration API** | Haptics | Triggers tactile vibration patterns on mobile devices when rest intervals complete. |
| **Web Storage API (`localStorage`)** | Data Persistence | Stores active workout state, complete workout history, and exercise progression entirely client-side. |
| **Canvas Confetti** | Celebration Animation | Renders particle physics celebration bursts upon completing workouts. |
| **Git** | Version Control | Source code tracking and branching (`main`). |
| **GitHub CLI (`gh`)** | Tooling & Automation | Installed via `winget`, authenticated, and used for remote repository creation and API configuration. |
| **GitHub REST API** | Cloud Infrastructure | Configured and enabled GitHub Pages serving from repository root. |
| **GitHub Pages** | Static Cloud Hosting | Free, continuous deployment hosting the live application globally with HTTPS. |

---

## 🚀 Running Locally

No build step or Node.js server is required. Because this is a single-file application:

1. Clone the repository:
   ```bash
   git clone https://github.com/Zeinboulo/science-split-tracker.git
   cd science-split-tracker
   ```
2. Open `index.html` directly in any web browser, or launch a local preview server:
   ```bash
   # Using Python:
   python -m http.server 8000

   # Or using npx:
   npx serve .
   ```
3. Open `http://localhost:8000` on your desktop or phone.

---

## 📚 References & Scientific Principles

- **Maeo et al. (2021)**: *Greater Hamstrings Muscle Hypertrophy but Similar Damage Protection after Training at Long versus Short Muscle Lengths.* Med Sci Sports Exerc.
- **Schoenfeld, B. J. et al. (2016)**: *Dose-response relationship between weekly resistance training volume and increases in muscle mass.* J Sports Sci.
- **Schoenfeld, B. J. et al. (2017)**: *Pre-exhaustion and exercise order effects on muscle hypertrophy.* Sports Med.
- **Israetel, M. et al. (RP Hypertrophy)**: *Scientific Principles of Hypertrophy Training (MEV, MAV, MRV framework).*
