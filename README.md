# Continuous Feed Printing Mechanism

This project is a pure HTML, CSS, and SVG web animation simulating a continuous-feed printing mechanism. It visually represents an industrial plotter or dot-matrix style printer operating on a tabletop, complete with synchronized gears, a dropping carriage track, and a sweeping printhead.

## Features

* **Zero JavaScript:** All movements, timings, and graphics are handled entirely natively by CSS and SVG.
* **Synchronized Animations:** * The printhead sweeps back and forth across the horizontal track.
* The carriage housing incrementally feeds downward in 5 distinct steps.
* A complex set of interconnected gears (large and small) rotate synchronously with the downward carriage drops.


* **Finite Sequence:** The animation runs a precise 20-second sequence and permanently parks itself at the bottom of the canvas when complete.
* **Detailed Graphics:** Includes custom SVG patterns for the vertical drive chains, a styled printhead with CMYK ink cartridges, a digital "PRINTING..." display, and a simulated dark-green environment with a tabletop background.

## Technologies Used

* **HTML5:** Document structure.
* **SVG (Scalable Vector Graphics):** Used for drawing all mechanical components, including the chains, gears, tracks, printhead, and background elements.
* **CSS3 Keyframes:** Drives all spatial translations (`translate`, `translateY`) and rotations (`rotate`).

## How to Run

1. Save the provided code into a file named `index.html` (or `printer-animation.html`).
2. Double-click the file to open it in any modern web browser (Chrome, Firefox, Safari, Edge).
3. The animation will start automatically upon loading. To replay the sequence, simply refresh the page.

## Animation Timing Breakdown

* **Total Sequence Duration:** 20 seconds.
* **Printhead Sweeps:** The `.print-head` completes exactly 5 back-and-forth sweeps. Each sweep takes 4 seconds, matching the 20-second total.
* **Carriage Feed:** The `.carriage` drops down in increments exactly when the printhead reaches the edges, holding its vertical position steady while the printhead moves across the middle of the canvas.
* **Gear Ratios:** The gears (`.gear-l-cw`, `.gear-s-ccw`, etc.) rotate in specific degree increments synchronized with the vertical drops. Smaller gears rotate faster (up to 750 degrees) while larger gears rotate slower (up to 450 degrees) to simulate mechanical gearing ratios.

## Customization Guide

You can easily modify the visuals and timings by adjusting the CSS and SVG attributes:

* **Colors:** * Change the surrounding room color in the `body` CSS selector (`background-color: #1a4321;`).
* Change the tabletop canvas color by modifying the `fill="#e6d5b8"` on the main background `<rect>`.


* **Timing & Speed:** * Adjust the `20s` and `4s` values in the `.print-head` and `.carriage` CSS classes to make the printer run faster or slower.
* *Note:* To maintain synchronization, ensure the total carriage time is exactly 5 times the printhead sweep time.
