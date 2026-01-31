<h1 align="center">Space Shooter: SFML Multimedia Experience</h1>

<p align="center">
  <a href="https://isocpp.org/">
    <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" alt="C++">
  </a>
  <a href="https://www.sfml-dev.org/">
    <img src="https://img.shields.io/badge/SFML-8CC445?style=for-the-badge&logo=sfml&logoColor=white" alt="SFML">
  </a>
  <a href="https://visualstudio.microsoft.com/">
    <img src="https://img.shields.io/badge/Visual_Studio-5C2D91?style=for-the-badge&logo=visual-studio&logoColor=white" alt="Visual Studio">
  </a>
  <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="MIT License">
  </a>
</p>

<p align="center">
  A high-performance 2D <b>Space Shooter</b> built with <b>C++</b> and the <b>SFML 2.6.1</b> framework. Featuring an object-oriented design, hardware-accelerated sprite rendering, and precise collision detection, this project delivers a polished arcade experience with high-resolution assets.
</p>

<p align="center">
  <a href="#technical-architecture">
    <img src="https://img.shields.io/badge/Architecture-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#project-structure">
    <img src="https://img.shields.io/badge/Structure-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#game-mechanics">
    <img src="https://img.shields.io/badge/Mechanics-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#technical-specifications">
    <img src="https://img.shields.io/badge/Specs-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#deployment--installation">
    <img src="https://img.shields.io/badge/Deploy-222222?style=flat" />
  </a>
</p>

---
<br>

<h2 align="center">Technical Architecture</h2>

This implementation transitions from procedural logic to a robust **Object-Oriented Architecture**, utilizing SFML's specialized modules for performance and asset management:

1.  **Modular Entities:** Employs discrete classes for `Player`, `Enemy`, and `Bullet`, each encapsulating its own state, textures, and transformations.
2.  **Asset Pipeline:** Implements a centralized loading system for high-resolution `.png` textures and `.ttf` typography, ensuring efficient memory usage via pointer-based texture sharing.
3.  **Collision System:** Leverages SFML’s `FloatRect` intersection logic for high-precision AABB collision detection between game entities.
4.  **Framerate Orchestration:** Features a synchronized game loop with a capped 15Hz logic-tick to maintain consistent gameplay physics across different hardware configurations.

---
<br>

<h2 align="center">Project Structure</h2>

```
ArcadeSpaceShooter_SFML/
├── LICENSE                                   # MIT License
├── README.md                                 # Project documentation
│
├── SFML/                                     # Source Code & Assets
│   ├── SpaceShooter.cpp                      # OO Game Implementation
│   ├── player.png / enemy.png                # High-res sprites
│   ├── bullet.png / background.jpg           # Game assets
│   ├── arial.ttf                             # UI Typography
│   └── SpaceShooter.sln                      # Visual Studio Solution
│
├── SFML-2.6.1/                               # SFML Framework binaries
│   ├── bin/                                  # Runtime DLLs
│   ├── include/                              # Header headers
│   └── lib/                                  # Static libraries
│
└── SFML_Screenshots/                         # Gameplay visual previews
```

---
<br>

<h2 align="center">Game Mechanics</h2>

- **Sprite-Based Navigation**: Vertical player movement mapped to low-latency input.
- **Rapid Fire System**: Timer-controlled projectile firing with dynamic vector storage.
- **Enemy Swarm Logic**: Randomized spawn vectors and horizontal translation towards the player.
- **Fail-State Logic**: Integrated collision triggers that monitor both health depletion and boundary breaches.
- **Layered HUD**: Real-time rendering of Cyan-colored scores and health status via binary categorization.

### Player Controls
<table align="center">
  <tr>
    <th align="center">Action</th>
    <th align="center">Key</th>
  </tr>
  <tr>
    <td align="center">Thrust Up</td>
    <td align="center"><b>W</b></td>
  </tr>
  <tr>
    <td align="center">Thrust Down</td>
    <td align="center"><b>S</b></td>
  </tr>
  <tr>
    <td align="center">Deploy Weapon</td>
    <td align="center"><b>Space</b></td>
  </tr>
</table>

---
<br>

<h2 align="center">Technical Specifications</h2>

<table align="center">
  <tr>
    <th align="center">Component</th>
    <th align="center">Specification</th>
  </tr>
  <tr>
    <td align="center"><b>Paradigm</b></td>
    <td align="center">Object-Oriented Programming (OOP)</td>
  </tr>
  <tr>
    <td align="center"><b>Graphics Library</b></td>
    <td align="center">SFML 2.6.1 (Simple and Fast Multimedia Library)</td>
  </tr>
  <tr>
    <td align="center"><b>Logic Tick</b></td>
    <td align="center">15 FPS Limit (Configurable)</td>
  </tr>
  <tr>
    <td align="center"><b>Rendering</b></td>
    <td align="center">800x600 Hardware-Accelerated Viewport</td>
  </tr>
  <tr>
    <td align="center"><b>Assets</b></td>
    <td align="center">Alpha-blended PNGs / JPEGs / TTF Font</td>
  </tr>
</table>

---
<br>

<h2 align="center">Deployment & Installation</h2>

### 1. Environment Setup
Ensure you have a C++ compiler installed (GCC or MSVC) and the SFML developer headers corresponding to version 2.6.1.

### 2. Acquisition
```bash
git clone https://github.com/Zer0-Bug/ArcadeSpaceShooter_SFML.git
```
```bash
cd ArcadeSpaceShooter_SFML
```

### 3. Download SFML Library
The SFML library must be installed on your system. You can download it from [here](https://www.sfml-dev.org/download.php). 

### 4. Compilation (GCC/Linux/MingW)
Ensure the SFML library paths are correctly linked in your environment:

```bash
g++ SFML/SpaceShooter.cpp -o space-shooter -lsfml-graphics -lsfml-window -lsfml-system
```

### 5. Running the Game
Execute the binary. Note: The external DLLs in `SFML-2.6.1/bin` may need to be in the same directory as the executable on Windows.

```bash
./space-shooter
```

---
<br>

<h2 align="center">Contribution</h2>

Contributions are always appreciated. Open-source projects grow through collaboration, and any improvement—whether a bug fix, new feature, documentation update, or suggestion—is valuable.

To contribute, please follow the steps below:

1. Fork the repository.
2. Create a new branch for your change:  
   `git checkout -b feature/your-feature-name`
3. Commit your changes with a clear and descriptive message:  
   `git commit -m "Add: brief description of the change"`
4. Push your branch to your fork:  
   `git push origin feature/your-feature-name`
5. Open a Pull Request describing the changes made.
<br>
All contributions are reviewed before being merged. Please ensure that your changes follow the existing code style and include relevant documentation or tests where applicable.

---
<br>
<p align="center">
  <a href="mailto:777eerol.exe@gmail.com">
    <img src="https://cdn.simpleicons.org/gmail/D14836" width="40" alt="Email">
  </a>
  <span> × </span>
  <a href="https://www.linkedin.com/in/eerolexe/">
    <img src="https://upload.wikimedia.org/wikipedia/commons/c/ca/LinkedIn_logo_initials.png"
         width="40"
         alt="LinkedIn">
  </a>
</p>

---

<p align="center" style="margin-top:10px; letter-spacing:4px;">
  ∞
</p>
