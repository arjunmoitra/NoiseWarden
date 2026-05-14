# NoiseWarden 🔊

A browser-based web application that lets users upload audio files, analyzes their sound levels against established noise safety standards, and tags each recording with geolocation data. Built as a full-stack JavaScript project with a focus on real-world usability and clean UI.

---

## What it does

Noise pollution is a documented public health risk — prolonged exposure above 85 dB can cause hearing damage. NoiseWarden gives users a simple tool to:

- Upload any audio file and get an instant decibel analysis
- See whether the recording exceeds safe noise thresholds (based on OSHA/WHO guidelines)
- Tag the recording with the geographic location where it was captured
- View a visual breakdown of sound levels over the duration of the clip

---

## Features

- **Audio upload & analysis** — accepts common audio formats and computes sound level metrics
- **Safety threshold comparison** — flags recordings that exceed safe exposure limits
- **Geolocation integration** — captures and stores location metadata with each upload
- **User authentication** — signup/login flow to save and revisit past recordings
- **Clean responsive UI** — built with vanilla HTML, CSS, and JavaScript; no framework dependencies

---

## Tech stack

| Layer | Technology |
|---|---|
| Frontend | HTML5, CSS3, JavaScript (vanilla) |
| Audio processing | Web Audio API |
| Geolocation | Browser Geolocation API |
| Auth flow | Custom signup/login (signup.html) |

---

## Project structure

```
NoiseWarden/
├── index.html          # Main app interface
├── signup.html         # User registration page
├── app.js              # Core audio analysis logic
├── style.css           # Main stylesheet
├── signup.css          # Auth page styles
├── js/                 # Supporting JS modules
└── Pictures/           # UI assets
```

---

## How to run

No build step required — this is a pure frontend project.

```bash
git clone https://github.com/arjunmoitra/NoiseWarden.git
cd NoiseWarden
# Open index.html in your browser
open index.html
```

> Note: The Geolocation API requires the page to be served over HTTPS or localhost. If geolocation doesn't trigger, serve with a local server:
> ```bash
> npx serve .
> ```

---

## What I learned

- Working with the **Web Audio API** to programmatically decode and analyze audio buffers
- Handling **async browser APIs** (file reader, geolocation) and managing their race conditions
- Designing a clean **user authentication flow** without a backend framework
- Structuring a vanilla JS project without letting it become unmaintainable

---

## Future improvements

- Backend integration (Node.js / FastAPI) to persist recordings and analysis history
- Support for real-time microphone input instead of file upload only
- Comparison dashboard across multiple recordings and locations
- Export analysis results as PDF or CSV

---

*Built by [Arjun Moitra](https://github.com/arjunmoitra)*
