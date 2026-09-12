# 🏙️ A Beautiful City — 2D OpenGL Simulation & Animation

[![C++](https://img.shields.io/badge/C++-11%2B-blue.svg?style=flat&logo=c%2B%2B)](https://isocpp.org/)
[![OpenGL](https://img.shields.io/badge/OpenGL-GLUT%2FFreeGLUT-green.svg?style=flat&logo=opengl)](https://www.opengl.org/)
[![IDE](https://img.shields.io/badge/IDE-Code%3A%3ABlocks-orange.svg?style=flat)](https://www.codeblocks.org/)
[![Course](https://img.shields.io/badge/Academic-Computer%20Graphics-purple.svg)](#)

An interactive 2D graphics simulation and animation project created for the **Computer Graphics** course (7th Semester). Built with **C++** and **OpenGL (GLUT)**, this project renders an animated urban landscape complete with architectural structures, nature, dynamic traffic, rotating structures, celestial motion, and interactive weather changes (daylight and rainy weather).

---

## 🌟 Key Features

- 🏛️ **Urban Architecture & Cityscape**:
  - Intricately designed multi-story buildings, residential blocks, windows, and decorative structures.
  - Commercial zones including a dedicated Food Court.
  - Communication / Observation Tower featuring real-time rotating blades / antennas.
- 🌳 **Rich Environment & Scenery**:
  - Handcrafted layered greenery and round foliage trees.
  - Geometric pine / fir triangle trees arranged along sidewalks and background zones.
  - Multi-lane roadway with pedestrian crossings and curbs.
- ⛅ **Dynamic Weather & Atmosphere (Day & Rain)**:
  - **Daytime / Sunny Scene**: Radiant sky with a rising and shining sun and passing clouds.
  - **Rainy Scene**: Moody overcast sky with an animated multi-drop rainfall particle simulation.
- 🚌 **Interactive Urban Mobility**:
  - Moving public transit buses cruising along the city highway with adjustable speeds and braking.
  - Wind simulation with interactive cloud velocity controls.

---

## 🎮 Interactive Controls

You can interact with the simulation in real time using both **keyboard** and **mouse** inputs:

### ⌨️ Keyboard Shortcuts

| Key | Action | Description |
| :---: | :--- | :--- |
| <kbd>T</kbd> | **Daytime / Sunny Mode** | Switches the atmosphere to clear skies with bright daylight and sunshine. |
| <kbd>R</kbd> | **Rainy Weather Mode** | Transitions the city into a rainy downpour with custom particle rainfall. |
| <kbd>S</kbd> | **Start / Accelerate Bus** | Starts the bus if stopped, or increases the vehicle's driving speed. |
| <kbd>A</kbd> | **Brake / Stop Bus** | Immediately halts the bus along the road (`speed = 0`). |

### 🖱️ Mouse Controls

| Button | Action | Description |
| :---: | :--- | :--- |
| **Left Click** | **Accelerate Clouds** | Increases the wind / cloud movement speed across the horizon. |
| **Right Click** | **Decelerate Clouds** | Decreases cloud movement speed (minimum speed capped at `0.1`). |

---

## 🛠️ Computer Graphics Concepts Applied

- **Primitive Assembly**: Extensive use of `GL_QUADS`, `GL_TRIANGLE_FAN`, `GL_LINES`, and `GL_POLYGON` for architectural models and terrain.
- **Parametric Curves & Circles**: Trigonometric vertex computation (`x = r * cos(θ)`, `y = r * sin(θ)`) for circular elements, wheels, sun, and cloud curves.
- **Coordinate Systems & Projections**: 2D orthographic projection configured via `glOrtho(0, 700, 0, 800, -10.0, 10.0)`.
- **Double Buffering & Frame Rendering**: Utilizing `GLUT_DOUBLE` / `glutSwapBuffers()` and `glutPostRedisplay()` to achieve tear-free smooth animations.
- **Particle System**: Real-time randomized rainfall simulation utilizing position arrays (`dropX`, `dropY`) and delta updates via `glutTimerFunc`.
- **Hierarchical Modeling & Transformations**: Rotating windmill / tower blades using trigonometric angle rotation and dynamic transformations.

---

## 🚀 Getting Started & Build Instructions

### Prerequisites
- **C++ Compiler**: MinGW (GCC) or equivalent
- **OpenGL & GLUT**: `freeglut` or `glut` development libraries installed
- **IDE** (Recommended): [Code::Blocks](https://www.codeblocks.org/)

### Method 1: Using Code::Blocks (Recommended)
1. Clone or download this repository.
2. Ensure your Code::Blocks MinGW installation has FreeGLUT / GLUT headers (`GL/glut.h`) and libraries (`libfreeglut.a` or `glut32.lib`) configured.
3. Open `final_project.cbp` in Code::Blocks.
4. Press **F9** (or click **Build and Run**).

### Method 2: Command Line Compilation (MinGW)
If you have MinGW with FreeGLUT installed, run:

```bash
g++ main.cpp -o city_simulation -lfreeglut -lopengl32 -lglu32 -lwinmm -lgdi32
```

Then launch the executable:
```bash
./city_simulation
```

---

## 📁 Repository Structure

```text
computer-graphics/
│
├── .gitignore          # Git exclusion rules for build/cache artifacts
├── final_project.cbp   # Code::Blocks project configuration file
├── main.cpp            # Complete OpenGL/GLUT source code (3,700+ lines)
└── README.md           # Project overview and documentation
```

---

## 👤 Author

- **Numman**
- GitHub: [@Numman297](https://github.com/Numman297)
- 7th Semester Computer Graphics Final Project
