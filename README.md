# Strategic Finance: Dynamic Unit Economics & Payback Simulator

[![Live App](https://img.shields.io/badge/Demo-Live%20App-brightgreen)](https://<your-username>.github.io/strategic-finance-unit-economics-simulator/)
[![Certification](https://img.shields.io/badge/Google%20AI-Professional%20Certificate-blue)](https://coursera.org/verify/YOUR_ID)

An interactive strategic finance dashboard built to evaluate customer acquisition cost (CAC) payback curves, customer lifetime value (LTV), and cash trough timing under shifting billing structures.

## 🚀 Live Demo
Test the live simulator in your browser: **[Open Simulator](https://deepthithakkum.github.io/strategic_finance_unit_economics_simulator/)**

---

## 💡 The Problem Solved
Strategic finance and FP&A teams frequently evaluate SaaS pricing models, expansion dynamics, and payment terms. While Excel works for static models, real-time executive decision-making requires instantaneous sensitivity modeling:
- How does shifting from **Annual Upfront** to **Monthly in Advance** impact runway and working capital?
- Where is our cumulative cash trough per customer vintage across a 36-month horizon?
- Is our LTV:CAC ratio masking an unsustainable 22-month CAC payback?

---

## 🛠️ Tech Architecture & Vibe Coding Process
This application was vibe coded in **Google AI Studio** using **Gemini**:
- **Architecture:** Zero-dependency, single-file `index.html` web application.
- **Frontend & Visualizations:** Tailwind CSS and Chart.js via CDN.
- **Model Tuning:** Temperature set to `0.2` to ensure deterministic math calculations and avoid hallucinated formula syntax.
- **Prompts:** Full system and functional prompts are documented in [`/prompt-engineering`](./prompt_engineering).

---

## 🎓 Google AI Professional Certificate Foundations
This project represents practical capstone execution stemming from the **Google AI Professional Certificate**, applying hands-on lab learning across:
- **AI for Data Analysis:** Translating structured financial logic and multi-variable equations into code.
- **AI for App Building & Vibe Coding:** Guiding LLMs via iterative requirements engineering and strict interface guardrails.
- **App Deployment:** Managing source control, environment isolation, and static hosting via GitHub Pages.
