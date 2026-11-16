# CrewPulse: Astronaut Health Monitoring

**Live site:** https://tonnuphuonglinh031008-cmyk.github.io/crew_pulse/
*(Click **Continue as guest** to try it. No account needed.)*

CrewPulse is a health-monitoring web app for astronauts on long-duration missions to the Moon and Mars. On Mars, a message to Earth can take 3 to 22 minutes each way, so crews can't rely on a flight surgeon answering in real time. CrewPulse helps astronauts understand their own health and know what to do next, while keeping the onboard medical officer and ground team informed.

Built for the **NASA Space Apps Challenge 2026**.

## Features

- **At-a-glance dashboard:** heart rate, blood pressure, temperature, sleep, glucose and mood, each with a 14-day trend against the astronaut's personal usual range.
- **Two-minute Daily Check:** symptoms and sensor readings combined into one clear status. When symptoms add up, it escalates to "act now" with step-by-step action cards.
- **Interactive body map:** 8 clickable areas (head, eyes, neck, shoulders, chest, abdomen, arms, legs), coloured by severity, with trends, self-care steps and how spaceflight affects each area.
- **Symptom checker:** describe a symptom in your own words; CrewPulse matches it against a library of common symptoms and warning signs.
- **Three roles:** crew member, onboard medical officer and ground flight surgeon. Changes to alert limits sent from Earth arrive after the real communication delay and need the medical officer's confirmation.
- **Environment panel:** cabin CO₂, radiation dose (real Curiosity RAD values for Mars transit and surface) and a space weather snapshot.
- **3D hardware showcase:** eight sensor devices designed by our team in CAD (wrist wearable, blood-pressure cuff, personal CO₂ clip, cabin environment sensor, radiation dosimeter, orbital mass measurement rig, medical tablet, station hub). Drag to rotate 360°, scroll or pinch to zoom.
- **Guest mode:** try everything without signing up; guest data is kept only until the tab is closed.

## Run it

- **Online:** open the live site link above.
- **Offline:** download this repository and open `index.html` in a browser. Keep the `models` folder next to it.

## Project structure

| Path | What it is |
|---|---|
| `index.html` | The whole app (HTML, CSS and JavaScript in one file) |
| `models/` | The 3D hardware models, loaded only when you open the Hardware page |
| `glb/` | The eight CAD models as standard glTF binary (`.glb`) files |
| `tools/step2glb.py` | Converts our Onshape STEP exports to `.glb` (needs NumPy and SciPy) |
| `tools/render.py` | Makes preview images of `.glb` files |

To swap a 3D model, change its path in `MODEL_PATHS` inside `index.html`.

## Built with

HTML, CSS and JavaScript (no frameworks), SVG graphics, WebGL for the 3D viewer, Onshape for CAD, Python (NumPy, SciPy) for model conversion, and Playwright for automated testing.

## Data sources

- NASA Human Research Program: Human System Risks and the Human Research Roadmap
- NASA Curiosity RAD radiation measurements (Zeitlin et al. 2013; Hassler et al. 2014)
- NASA report on the May 2024 solar storm at Mars (MAVEN / Curiosity)
- NASA CCMC DONKI space weather database
- NOAA Space Weather Prediction Center forecasts

Full links are listed on the site's Help page and in our Space Apps submission.

## Important notes

- **Not a medical device.** CrewPulse is a hackathon prototype. It helps find information and report symptoms; it does not diagnose.
- **Readings are simulated** and labelled "Simulated" in the app. The hardware is a hobby-grade CAD prototype, not flight-qualified.
- No NASA logos or branding are used.

## Use of AI (Super Intelligence) tools

This project was developed with help from **Claude (Anthropic)**, a large language model. Claude was used to help write the website code, the STEP-to-GLB converter, organise the health-risk data, draw the body figure and icons (as code), and draft text in the app and in this README. All AI-assisted output was reviewed and directed by our team. The CAD hardware designs were created by our team in Onshape.
