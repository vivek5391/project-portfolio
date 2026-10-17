# Project Portfolio

A central home for my engineering projects, source files, designs, build notes, and results.

## Projects

| Project | Build status | Documentation |
| --- | --- | --- |
| [01 — 3D Printer](projects/01-3d-printer/README.md) | Built, as reported by owner; performance validation pending | Custom Cartesian FDM, Marlin, Arduino Mega + RAMPS 1.4, CAD and build photos |
| [5-DOF Robotic Arm Digital Twin](https://github.com/vivek5391/6dof-robotic-arm-ros2) | Software/hardware validation should be confirmed on target setup | ROS 2 Humble, URDF/Xacro, Fusion 360 CAD, browser twin and servo bridge code |
| [Industrial IoT Smart Relay & Energy Monitor](https://github.com/vivek5391/esp32-industrial-iot-controller) | Prototype; measurement and safety validation required | ESP32, PlatformIO, Blynk, NVS persistence and relay-control firmware |
| [Autonomous Mobile Robot (ROS 2)](https://github.com/vivek5391/Autonomous-mobile-robot) | In development; CI passing, local simulation validation pending | ROS 2 Jazzy, Gazebo Sim, URDF/Xacro, simulated LiDAR, SLAM Toolbox and Nav2 preparation |

## Organization

Each project has its own numbered folder under `projects/`:

- `code/`: firmware, source code, and configuration
- `design/`: original CAD files and exported STL files
- `electronics/`: wiring diagrams and circuit files
- `photos/`: build photos and finished project photos
- `docs/`: components, assembly, and operating notes
- `results/`: test prints, measurements, and observations

LinkedIn drafts live in `social/linkedin/`. Add future projects as `02-project-name`, `03-project-name`, and so on, then update the table above.

Keep original editable files alongside exports. Record software versions and links to third-party components. Check files for passwords and personal information before making the repository public. Keep a separate backup of large videos and other files that are unsuitable for GitHub.

## Repository

[vivek5391/project-portfolio](https://github.com/vivek5391/project-portfolio)

To download a working copy with Git installed:

```sh
git clone https://github.com/vivek5391/project-portfolio.git
```

The previous ESP32 and relay projects are preserved in a ZIP in the parent folder's `_local-backups/` directory, outside this repository.
