## Interactive Diorama WebGPU Viewer

### Description
This project is a real-time 3D diorama viewer built with WebGPU. It loads OBJ models exported from Blender, applies physically-based materials, and features advanced lighting, emission, and post-processing effects. Users can interactively explore the scene with smooth camera controls and UI adjustments.

### Features
- OBJ file import (from Blender)
- Materials: color, normal, roughness, emission maps
- Emission effects
- Interactive camera: orbit, pan, zoom
- Real-time brighness slider in live server
- Keyboard toggles for emission

### Setup & Running
1. Use a browser with WebGPU support.
2. Open `diorama.html` using the Live Server extension in VS Code (right-click the file and select "Open with Live Server").

### Usage
- **Mouse Left-Drag:** Orbit camera
- **Shift + Left-Drag:** Pan camera
- **Mouse Wheel:** Zoom in/out
- **L key:** Toggle emission
- **Exposure Slider:** Adjust scene brightness

### File Structure
- `diorama.html` — Main application (all logic and shaders)
- `meshes/` — Contains OBJ models and UV map png for colours, roughness, normals, emissions
- `textures/` — Contains the mtl file
- `README.md` — This documentation


