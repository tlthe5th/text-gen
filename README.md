# text-gen

A single-file, zero-dependency 3D WebGL kinetic text and sunburst intro generator built with Three.js. Runs directly in the browser with no backend server, build step, or subscription required.

**Live App:** [https://tlthe5th.github.io/text-gen/](https://tlthe5th.github.io/text-gen/)

## Features

* **Custom 3D Typography:** Enter any phrase (up to 28 characters) to generate beveled, procedural stone-textured 3D letter meshes in real time.
* **Per-Letter Physics & Lighting:** Choose any character to fracture and shatter into falling 3D rubble, and any character to ignite into a glowing solar core with volumetric god-rays.
* **15-Second Cinematic Timeline:** Transitions from shadowed darkness through stone reveal, letter shatter, solar ignition, and bloom into bright daylight.
* **1080p Browser Video Export:** Uses the browser's `MediaRecorder` API to capture and download a 1920×1080, 30 fps 15-second video clip directly to your device.

## How to Use

1. Open [https://tlthe5th.github.io/text-gen/](https://tlthe5th.github.io/text-gen/) (or open `index.html` in a modern desktop browser).
2. Type your custom phrase into the text field at the bottom of the screen.
3. Select which character **Shatters** and which character acts as the **Sun**, then click **Generate** to preview the 15-second sequence.
4. Click **Record 15s Video** and keep the browser tab visible until the download finishes automatically.

## Optional: Convert `.webm` to `.mp4` Locally

Depending on your browser, `MediaRecorder` exports either `.mp4` or `.webm`. If your browser saves a `.webm` file and you want a standard H.264 `.mp4`, convert it with FFmpeg:

```powershell
ffmpeg -i text-gen-15s.webm -c:v libx264 -pix_fmt yuv420p text-gen-15s.mp4
