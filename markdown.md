# A Humble Food Web

## Overview
"A Humble Food Web" is a single-file HTML5 web application designed for students, educators, and scientists to easily build, customize, and export clean ecological food chains and webs. It runs entirely in the browser using Vanilla JavaScript and Canvas API.

## Key Features
*   **Interactive Canvas:** Drag-and-drop nodes (organisms) around a crisp HTML5 canvas. Bounds-checking prevents nodes from being dragged off-screen.
*   **Connection Mode:** Draw energy flows (arrows) between organisms with an intuitive click-to-connect interface. Check the lock box to draw multiple flows continuously. 
*   **Self-Loops:** Click the same organism twice while in Connection Mode to draw a cannibalistic energy flow loop.
*   **Customizable Properties:** Edit organism names and assign trophic levels (None, Producer, Primary Consumer, Secondary Consumer, Tertiary Consumer, or Decomposer).
*   **Image Integration:** Upload local image files to fill organism nodes. The app automatically renders a semi-transparent backdrop behind the text to maintain readability.
*   **Dynamic Styling:** Toggle between straight or curved connecting lines. Adjust global node sizes and font sizes on the fly.
*   **Trophic Color Coding:** Switch from a minimalist Black & White layout to a color-coded trophic mode, complete with an auto-generating key.
*   **Undo & Quick Delete:** Built-in history stack allows users to undo recent actions (via UI button or `Ctrl+Z` / `Cmd+Z`). Select a node and hit `Delete` or `Backspace` for rapid removal.
*   **Frictionless Export:** Download the canvas as a high-resolution PNG or copy it directly to the system clipboard for easy pasting into documents and presentations.

## Architecture
The application is entirely self-contained within `index.html`.
*   **HTML/CSS:** Responsive split-layout design utilizing CSS Grid and Flexbox. Tabler Icons are loaded via CDN for UI elements.
*   **JavaScript:** Vanilla JS handles all state management, canvas rendering, and event listening. 
*   **State Management:** Data is stored in lightweight `nodes` and `edges` arrays. The UI is completely redrawn on every state change via the `render()` function to ensure visual consistency.

---

> **IMPORTANT:** Do not change or increment the application version number in the HTML header (e.g., `V 1.0.0 — 09-16-2026`) unless explicitly directed to do so by the user.

---

## Usage Guide
1.  **Add Organisms:** Click "Add Organism" to spawn a new node on the canvas. Click the node to edit its name, trophic level, or image in the left-hand Inspector panel.
2.  **Add Energy Flows:** Click "Add Energy Flow" to enter connection mode. Click the organism being eaten, then click the eater. Check "Keep connection mode active" to lock the tool on.
3.  **Adjust Layout:** Drag nodes freely around the canvas. Use the Chart Options to toggle curved lines, scale node sizes, or adjust font sizes.
4.  **Color Coding:** Check "Color Trophic Levels" to apply background colors based on each organism's ecological role.
5.  **Exporting:** Use the "Download PNG" or "Copy to Clipboard" buttons at the bottom of the left panel to export your finished food web.