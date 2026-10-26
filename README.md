# Leo Rover · Simulation Workspace

ROS 2 workspace containing Leo Rover robot descriptions, messages, teleoperation packages, and a Gazebo simulator.

## Explore the workspace

| Directory | Contents |
| --- | --- |
| [leo_common-ros2](src/leo_common-ros2/) | Robot description, messages, and teleoperation packages |
| [leo_simulator-ros2](src/leo_simulator-ros2/) | Gazebo bringup, plugins, and simulation worlds |
| [Simulation worlds](src/leo_simulator-ros2/leo_gz_worlds/) | Empty world and Marsyard terrain environments |

## Setup and simulation

Follow the bundled [simulator README](src/leo_simulator-ros2/README.md) for ROS / Gazebo compatibility, dependencies, and build instructions.

After building and sourcing the workspace, the documented simulation entry point is:

```bash
ros2 launch leo_gz_bringup leo_gz.launch.py
```

The bundled simulator also documents a Marsyard example:

```bash
ros2 launch leo_gz_bringup leo_gz.launch.py sim_world:=marsyard2021.sdf robot_ns:=leo1
```

## Current scope

The checked-in tree contains the common and simulator packages. A separate waypoint-following application is not present in this snapshot.

## Upstream packages and attribution

This workspace includes packages from [LeoRover/leo_common-ros2](https://github.com/LeoRover/leo_common-ros2) and [LeoRover/leo_simulator-ros2](https://github.com/LeoRover/leo_simulator-ros2). Their documentation and licences remain alongside the source:

- [Common packages README](src/leo_common-ros2/README.md) · [Licence](src/leo_common-ros2/LICENSE)
- [Simulator README](src/leo_simulator-ros2/README.md) · [Licence](src/leo_simulator-ros2/LICENSE)
