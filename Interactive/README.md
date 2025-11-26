
## Interactive Diorama WebGPU Viewer

### Description
This project is a real-time 3D diorama viewer built with WebGPU. It loads OBJ models exported from Blender and reads material properties (like color, normal, roughness, and emission maps) from the accompanying MTL file. The viewer features the scene with lighting, emission, and post-processing effects. Users can interactively explore the scene using mouse controls to control the camera and adjust scene brightness.

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

### Import and Drawing

Initially, the file initializes a WebGPU context on a canvas element. This creates a rendering pipeline, including shaders for vertex and fragment processing. Models are imported as .obj files from blender which contain geometry (vertices, normals, UVs) and are put into the folder. The function ParseOBJWithUVs is then used to read the OBJ file and extract positions, normals, and face indices and build vertex data arrays that can be computed by the GPU. 

These arrays are then put through a VertexBuffer and IndexBuffer to upload the vertex and index data to the GPU. With this, the buffers are ready and rendering can begin. In the render loop, the rendering pipeline is set and all buffers are binded appropriately. After the buffers are binded, it issues calls to render the geometry onto the canvas. Then, the render is submitted to the GPU to be outputted on the screen.

### Materials, Shaders and Lighting

Materials are defined by four main texture maps: color, normal, roughness, and emission specified in the model’s MTL file:

- **Color map:** Sets the main color of the surface.
- **Normal map:** Adds bumps and small details to the surface.
- **Roughness map:** Controls if the surface looks shiny or matte.
- **Emission map:** Makes parts of the model glow.

For lighting,  single point light is placed above the diorama, and each pixel’s color is affected by ambient, diffuse, and specular light. The normal and roughness maps control how light reflects off the surface, making highlights sharper or softer. 

These textures are loaded and used in the fragment shader to create realistic materials. The shaders are written in WGSL and included in `diorama.html`.

The vertex shader transforms 3D geometry and passes attributes (UVs, normals, tangents, world position) to the fragment shader. The fragment shader combines the material textures with lighting and emission calculations, then applies tone mapping to adjust colours for bright and dark areas. 

### File Structure
- `diorama.html` — Main application (all logic and shaders)
- `meshes/` — Contains OBJ models and UV map png for colours, roughness, normals, emissions
- `textures/` — Contains the mtl file
- `README.md` — This documentation


