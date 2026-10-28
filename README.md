# PathPulse 360° — Assistive Navigation Concept

**An interactive assistive-navigation prototype designed to demonstrate how visually impaired people could receive obstacle alerts and step-by-step spoken guidance while navigating their surroundings.**

> ⚠️ **Prototype Notice:** PathPulse is currently a software simulation for demonstration and educational purposes. It does not connect to real-world sensors or detect actual obstacles, and it must not be used for real-world navigation.

## 🌟 Project Overview

PathPulse 360° explores an assistive-navigation concept in which a system monitors the surrounding environment, identifies potential obstacles, evaluates possible routes, and communicates the next action through friendly voice instructions.

The prototype provides an interactive street simulation where users can move through different environments, encounter obstacles, and observe how the system responds.

Our goal is to demonstrate a possible approach to making navigation assistance more understandable, interactive, and accessible.

## 🎯 Problem Statement

Visually impaired people can face challenges when identifying obstacles, road boundaries, and unexpected hazards while moving through unfamiliar environments.

PathPulse explores a potential software-based guidance interface that could:

- Warn users about simulated obstacles.
- Recommend stopping when a path is blocked.
- Evaluate alternative routes to the left or right.
- Provide clear, spoken movement instructions.
- Explain why a particular route decision was made.

## ✨ Key Features

- **Interactive Street Simulation:** Navigate through a virtual road environment.
- **360° Sensor-Field Visualization:** Displays a simulated top-down view of surrounding obstacles.
- **Obstacle Detection Logic:** Checks the simulated walking corridor for objects and road boundaries.
- **Smart Route Assessment:** Evaluates whether alternative routes are clear within the simulation.
- **Voice Guidance:** Speaks instructions such as “Stop,” “Turn left slowly,” and “Proceed slowly.”
- **Multiple Environments:** Quiet sidewalk, busy street, night street, left blocked/right clear, and both sides blocked.
- **Safety Demonstration:** Runs a predefined obstacle-navigation scenario.
- **Emergency Stop:** Pauses movement and requests a stop state.
- **Explainable Decisions:** Shows the reasons behind simulated route recommendations.
- **Responsive Interface:** Includes keyboard controls and an on-screen directional pad.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| HTML5 | Page structure and interactive controls |
| CSS3 | Styling, layout, and responsive design |
| JavaScript | Simulation, obstacle checks, route logic, and application state |
| HTML Canvas 2D API | Drawing the road, obstacles, and radar visualization |
| Web Speech API | Text-to-speech voice instructions |
| DOM API | Handling buttons, keyboard input, and interface updates |
| `requestAnimationFrame()` | Updating the animated simulation |

**External dependencies:** The basic prototype is implemented in a standalone HTML file and does not require a separate backend server or package installation.

## ⚙️ How PathPulse Works

1. **Environment Selection:** The user selects a simulated environment containing predefined obstacles.
2. **Scene Rendering:** Canvas draws the road, user position, obstacles, and sensor-field visualization.
3. **Surroundings Check:** JavaScript checks the planned walking corridor for intersections with simulated obstacles or road boundaries.
4. **Risk Assessment:** When an obstacle blocks the corridor, the system evaluates possible alternative routes.
5. **Decision Making:** The simulation selects a clear side when one is available, or recommends remaining stopped when both sides are blocked.
6. **Voice Assistance:** The browser's speech-synthesis functionality reads the current instruction aloud.
7. **Continuous Updates:** The simulation updates as the user moves and can reassess the route when conditions change.

### Example Guidance Flow

`Path Clear → Caution → Stop → Assess Routes → Turn → Proceed`

If no safe alternative is available in the simulated scene, PathPulse recommends remaining stopped.

## 🧪 Testing and Demonstration

The prototype can be manually tested using the following scenarios:

| Test Scenario | Expected Demonstration |
|---|---|
| Quiet sidewalk | Navigate around predefined obstacles |
| Busy street | Respond to multiple obstacles, including moving objects |
| Night street | Demonstrate the alternate night-scene visualization |
| Left blocked, right clear | Evaluate the available alternative route |
| Both sides blocked | Recommend remaining stopped |
| New hazard | Add a simulated scooter obstacle |
| Voice guidance | Read the current instruction aloud |
| Emergency stop | Stop movement and pause the simulation |

These are **manual demonstration scenarios**, not claims of a completed automated test suite or independently validated safety performance.

## ▶️ How to Run the Project

1. Clone or download this repository.
2. Locate the main HTML file, for example `Main_pluse.html` or `PathPulse_Improved.html`, depending on the version you upload.
3. Open the HTML file in a modern web browser such as Google Chrome or Microsoft Edge.
4. Select an environment.
5. Click **Start** or **Run Safety Demonstration**.
6. Use `W`, `A`, `S`, `D` or the arrow keys to move.
7. Enable voice guidance and listen to the instructions.

A browser and operating-system speech voice must be available for spoken guidance to work.

## 🎮 Controls

| Control | Action |
|---|---|
| Start | Start the simulation |
| Pause / Resume | Pause or continue |
| Restart | Reset the selected scenario |
| New Hazard | Add a simulated obstacle |
| Run Safety Demonstration | Load the demonstration scene |
| Voice On/Off | Enable or mute spoken guidance |
| Repeat | Repeat the current instruction |
| Emergency Stop | Stop movement and request a stop state |
| W / A / S / D | Move forward, left, backward, or right |
| Arrow Keys | Alternative movement controls |
| Directional Pad | Touch-friendly movement controls |
| Walking Speed | Select slow, normal, or fast movement |

## 🔬 Research and Technical References

The following links document the web technologies used by the prototype. They are technical references, not independent validation of PathPulse's effectiveness.

- [MDN — HTML](https://developer.mozilla.org/en-US/docs/Web/HTML): Structure of web applications.
- [MDN — CSS](https://developer.mozilla.org/en-US/docs/Web/CSS): Styling and responsive interface design.
- [MDN — JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript): Programming language used for the simulation and decision logic.
- [MDN — Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API): Rendering graphics and visualizations.
- [MDN — Web Speech API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API): Browser speech functionality.
- [MDN — SpeechSynthesis](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesis): Text-to-speech control interface.
- [MDN — requestAnimationFrame()](https://developer.mozilla.org/en-US/docs/Web/API/Window/requestAnimationFrame): Animation update scheduling.
- [W3C — Web Content Accessibility Guidelines (WCAG)](https://www.w3.org/WAI/standards-guidelines/wcag/): Accessibility guidance for web content.

## 📁 Project Structure

The current prototype is a standalone HTML application containing:

- **HTML:** Interface structure and controls.
- **CSS:** Visual design and responsive layout.
- **JavaScript:** Simulation state, obstacle logic, route assessment, voice guidance, and canvas rendering.

No separate backend, database, trained machine-learning model, or external sensor integration is currently required for the simulation.

## 🚧 Current Limitations

- Obstacles and distances are simulated.
- The 360° radar is a visualization, not a real sensor feed.
- The application does not currently process live camera images.
- No physical infrared, ultrasonic, LiDAR, or other sensor is connected.
- No trained machine-learning model is implemented in the current prototype.
- Route decisions operate on the simulated environment and do not guarantee real-world safety.
- Speech availability and voice selection depend on the browser and device.

## 🔮 Future Scope

Future development could explore:

- Real-time obstacle detection using a mobile camera.
- Integration with validated computer-vision models.
- Hardware integration with appropriate distance sensors.
- Improved direction and distance estimation.
- Navigation guidance using accessible maps and positioning systems.
- Multilingual voice guidance.
- More extensive automated tests and controlled usability evaluations with visually impaired participants.
- Privacy, reliability, and safety testing before any real-world deployment.

These are planned possibilities, not existing features.

## 💡 Why PathPulse?

PathPulse focuses not only on identifying a simulated obstacle, but also on communicating a possible next action.

Its interactive interface demonstrates the concept through a visible environment, route assessment, explainable decisions, and spoken instructions.

👥 Team

**Project:** PathPulse 360°  
**Category:** Assistive Technology / Accessibility  
**Format:** Interactive Software Prototype

Add your actual team members, institution, and hackathon details here.

📜 Disclaimer

PathPulse is an educational concept prototype and is not a certified assistive device. It must not replace a mobility cane, guide dog, trained orientation and mobility techniques, or other established mobility aids. Real-world use would require substantial engineering, safety validation, accessibility testing, and expert evaluation.

📄 License

No license has been specified yet. Add a `LICENSE` file before declaring the project open source, and choose a license appropriate for your team's ownership and permissions.

---

**Built to explore a more accessible way of experiencing navigation assistance.**
