# The Quiet Hour — Interactive Literary Personality Quiz

**[Play the Live Demo Here](https://your-vercel-link-here.vercel.app/)**

## Overview
"The Quiet Hour" is a self-contained, interactive web application that matches users with one of eight classic literary archetypes based on a psychological and aesthetic questionnaire. 

Designed with a refined, editorial UI suited for a "quiet library" aesthetic, this project bridges elegant user-centric design with robust backend state management. It was intentionally built using **Vanilla JavaScript, HTML5, and Tailwind CSS** to demonstrate core DOM manipulation, algorithmic scoring, and zero-dependency performance without relying on heavy frontend frameworks.

## Key Technical Features

### 1. Weighted Scoring Matrix (Algorithm)
Instead of a basic 1-to-1 question-to-result mapping, the application utilizes a weighted scoring matrix. Every user choice distributes variable points across multiple authors simultaneously based on shared psychological traits (e.g., choosing an isolated, analytical response might distribute +3 to Dickinson, +1 to Camus, and +2 to Poe). The state tracks all 8 variables concurrently and dynamically computes the highest aggregate score upon completion.

### 2. Zero-Dependency Vanilla Architecture
The entire application logic, state management, UI transitions, and content arrays are bundled into a single, lightweight `index.html` file. This eliminates build steps, bypasses `node_modules` bloat, and guarantees instantaneous browser rendering.

### 3. Dynamic SVG Silhouette Rendering
To maintain a crisp, resolution-independent aesthetic without relying on external image hosting, all eight author portraits are drawn using custom inline SVG `<path>` data. The application dynamically injects the correct vector mathematics into the DOM based on the matrix's calculated winner.

### 4. Client-Side Image Generation
The application integrates `html2canvas` to allow users to generate and download a high-resolution "screenshot" of their personalized result card directly in the browser. The DOM tree is temporarily manipulated to hide UI buttons before rendering the canvas, ensuring a clean, shareable asset.

## Tech Stack
*   **Structure & Logic:** HTML5, Vanilla JavaScript (ES5/ES6 concepts)
*   **Styling:** Tailwind CSS (via CDN)
*   **Typography:** Google Fonts (Fraunces, Source Serif 4)
*   **Libraries:** `html2canvas` (for client-side DOM-to-image exporting)
*   **Deployment:** Vercel (CI/CD via direct directory upload)

## Local Execution
Because this project requires no build tools or package managers, running it locally takes one step:
1. Clone the repository.
2. Open `index.html` directly in any modern web browser.
