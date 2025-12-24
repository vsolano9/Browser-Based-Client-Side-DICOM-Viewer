# Project Context Analysis

## 1. Project Stack Review
The current codebase is initialized with a modern, high-performance frontend stack designed for a Single Page Application (SPA).

*   **Core Framework:** **React 18/19** with **TypeScript** for type safety and component-based architecture.
*   **Build Tool:** **Vite** for fast HMR and optimized production builds.
*   **Styling:** **Tailwind CSS** (v3.4) + **PostCSS** for utility-first, responsive styling.
*   **Medical Imaging:**
    *   **Cornerstone.js Core**: For high-performance rendering of medical images.
    *   **dicom-parser**: For parsing DICOM tags and metadata on the client side.
*   **Backend & Hosting:** **Firebase** (v12.7) implies usage of:
    *   Firebase Hosting: For serving the SPA.
    *   Firebase Auth: For user management (implied by "Pro" features).
    *   Firestore/Analytics: Likely for user data and usage tracking.

## 2. The Stitch Concept
The `.context/stitch` directory functions as a **Design System and Prototype Repository**. It contains approximately 50 sub-modules (e.g., `landing_page_1`, `dicom_viewer_interface_1`), each housing:
*   `code.html`: A static HTML implementation of the component/page.
*   `screen.png`: A visual reference of the design.

**Key Observation:** "Stitch" represents the **target state** of the application. The current `src/App.tsx` is a skeleton, whereas the Stitch directory contains the high-fidelity implementations that need to be "stitched" into the React architecture. It covers the entire user journey: Branding (Landing/About) -> Onboarding -> Core Utility (Viewer) -> Retention (Pro Dashboard).

## 3. Website Analysis
**Identity:** A privacy-first, browser-based DICOM/Medical Image Viewer SaaS.

**Core Value Proposition:**
*   **Zero Footprint:** Runs entirely in the browser (client-side), ensuring patient data privacy (no server uploads required for viewing).
*   **Professional Grade:** Integrates Cornerstone.js for diagnostic-quality rendering.
*   **SaaS Model:** The presence of `pro_user_dashboard` and `subscription` related stitches confirms a Freemium/Subscription business model.

**Architecture Strategy:**
The goal is to migrate the static `code.html` concepts from `.context/stitch` into interactive React components within `src`, connecting them to the Firebase backend and Cornerstone.js engine.
