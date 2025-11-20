# 3D Vector Field Visualizer

An interactive 3D particle system that visualizes mathematical vector fields in real-time using Three.js.

## How It Works

The app renders thousands of particles that move according to user-defined vector functions. Each particle's velocity is calculated based on its current position (x, y, z) and optional time variable (t), creating dynamic fluid-like animations.

### Core Features

- **Custom Vector Functions**: Define Vx, Vy, Vz using JavaScript math expressions
- **Real-time Visualization**: 5,000-20,000 particles updated every frame
- **Interactive 3D Controls**: Orbit, pan, and zoom the camera
- **Preset Patterns**: Saddle points, spirals, attractors, and wave patterns
- **Visual Feedback**: Color-coded particles show velocity magnitude

## Technical Details

**Rendering**: Three.js WebGL with BufferGeometry for performance
- Uses `PointsMaterial` with vertex colors and additive blending
- Euler integration updates particle positions each frame
- Particles respawn when leaving the boundary box

**Vector Field Parsing**: Functions are compiled using JavaScript's `Function` constructor with Math context injected, allowing expressions like `sin(z + t)` or `x * cos(y)`.

**Responsive Design**: Mobile-optimized with CSS media queries
- Auto-collapse UI on mobile devices
- Touch-friendly controls with larger hit targets
- Adaptive panel sizing and positioning

## Usage

1. Open `3D_animation.html` in a modern browser
2. Select a preset or enter custom vector functions
3. Adjust particle count and speed with sliders
4. Click "Update Field" to apply changes
5. Use mouse/touch to interact with the 3D view

## Controls

- **Left Click + Drag**: Rotate view
- **Right Click + Drag**: Pan camera
- **Scroll**: Zoom in/out
- **Hide UI Button**: Toggle control panel

No build process or dependencies required - runs directly in the browser.
