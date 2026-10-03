# Frameclock

A dark-mode render planner and animation frame converter. The entire tool is contained in `index.html`; no installation, build, or external assets are required.

## Render planner

- Calculate render duration in seconds, minutes, hours, and days.
- Add up to 64 devices, each with its own time per frame.
- Estimate completion from a start time, work backward from a finish deadline, or check a start/end window.
- Show a whole-frame workload split across devices.

Render estimates assume every device starts together, renders at a constant speed, and receives the displayed frame allocation. Setup and file transfers are excluded. Dates use the browser's local time zone.

## Frame converter

- Convert an animation duration into frames at a chosen FPS.
- Convert an existing frame count into playback duration.
- Calculate the FPS required for a target duration.
- Compare multiple frame rates, including custom decimal rates.
- Send the calculated frame count directly to the render planner.

For example, 40 seconds at 25 FPS requires 1,000 frames; at 30 FPS it requires 1,200. A 400-frame animation lasts 16 seconds at 25 FPS. Fitting those 400 frames into 30 seconds requires approximately 13.3333 FPS; fitting them into 40 seconds requires 10 FPS.

Frame counts round up to whole frames. Frame rate controls animation playback duration; render time per frame is a separate input.

## Use

Open `index.html` in a browser, or host this repository with GitHub Pages using the `main` branch and the root folder. All calculations run in the browser, and the tool also works offline.
