<h1 align="center">PymeBoost Prototype</h1>
<p align="center"><img src="docs/pymeboost-logo.png" alt="PymeBoost logo" width="400"></p>

<p align="center">
  Interactive UX/UI prototype of <a href="https://github.com/IsaacVil/PymeBoost">PymeBoost</a>, a platform that connects SMEs with high-performance advisors through AI matching, structured negotiation, and results-based tracking. This repository only contains the prototype deployed on Vercel.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/REACT-18.3-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React 18.3">
  <img src="https://img.shields.io/badge/BABEL-STANDALONE-F9DC3E?style=for-the-badge&logo=babel&logoColor=black" alt="Babel Standalone">
  <img src="https://img.shields.io/badge/HTML5-NO%20BUILD-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/VERCEL-DEPLOYED-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel">
  <img src="https://img.shields.io/badge/MAZE-UX%20TESTING-5C4EE5?style=for-the-badge" alt="Maze">
</p>

<p align="center">
  <a href="https://pymeboost-v1.vercel.app/">Live Demo</a> ·
  <a href="https://github.com/IsaacVil/PymeBoost">Original Repository</a> ·
  <a href="#features">Features</a> ·
  <a href="#run-locally">Run Locally</a> ·
  <a href="#deployment">Deployment</a>
</p>

---

## About

This repository exists only to host and deploy the **PymeBoost prototype on Vercel**. The full project (problem statement, architecture, backend design, and documentation) lives in the original repository:

**[github.com/IsaacVil/PymeBoost](https://github.com/IsaacVil/PymeBoost)**

**Live demo:** [pymeboost-v1.vercel.app](https://pymeboost-v1.vercel.app/)

---

## Features

The prototype simulates the main flows of the platform with sample data (the interface is in Spanish):

* **Role selection:** enter as an SME or as an advisor.
* **Landing, login, and registration:** features, process, pricing plans, and registration forms for SMEs and advisors, including membership and payment fields.
* **Advisor discovery:** SMEs browse advisors with a compatibility score from the AI matching.
* **Opportunities:** advisors review the SMEs that matched with them.
* **Messaging and negotiation:** conversations between the SME and the advisor.
* **Contract dashboard:** contract phases, progress, deadlines, and progress reports.
* **Tweaks panel:** switch between layout variants, retro style intensity, and brand fonts.
* **UX testing:** each view updates the URL hash so [Maze](https://maze.co/) can track usability tests and heatmaps.

---

## Technology Stack

* **React 18.3** and **ReactDOM** loaded from a CDN (unpkg).
* **Babel Standalone** to compile the JSX directly in the browser: there is no build step.
* **HTML and CSS** with design tokens (Retro design system) and Google Fonts.
* **Maze** snippet for usability testing and heatmaps.
* **Vercel** for static hosting.

---

## Project Structure

```text
PymeBoostPrototype/
├── PymeBoost.html        # Entry point: styles, CDN scripts, and the JSX modules
├── app/
│   ├── app.jsx           # Main app, role landing, sidebar, discovery, and tweaks
│   ├── auth.jsx          # Landing, login, and SME and advisor registration
│   ├── components.jsx    # Shared UI components (buttons, badges, panels, logo)
│   ├── dashboard.jsx     # Contract dashboard, phases, progress, and reports
│   ├── data.jsx          # Sample data
│   ├── matching.jsx      # Advisor matching views
│   ├── messaging.jsx     # Messaging and negotiation
│   └── tweaks-panel.jsx  # Tweaks panel
├── docs/                 # README images (logo)
├── vercel.json           # Rewrites "/" to PymeBoost.html
├── LICENSE
└── README.md
```

---

## Run Locally

The JSX files are loaded with `<script src>`, so the prototype needs a local web server (opening the HTML file directly does not work). From the repository root, run one of these:

```bash
npx serve .
```

```bash
python -m http.server 8000
```

Then open `http://localhost:8000/PymeBoost.html` (or the address shown by `serve`).

---

## Deployment

Vercel serves the repository as a static site with no build step. `vercel.json` rewrites the root path `/` to `PymeBoost.html`, so the prototype opens directly at the deployment URL. Every push to `main` triggers a new deployment.

---

## Authors

* Isaac Villalobos Bonilla, 2024124285
* Christopher Daniel Vargas Villalta, 2024108443
* Santiago Espinoza Rendón, 2024156530
* Jose Ignacio Paniagua Vargas, 2024163735

---

## License

Distributed under the MIT License. See [`LICENSE`](LICENSE) for details.
