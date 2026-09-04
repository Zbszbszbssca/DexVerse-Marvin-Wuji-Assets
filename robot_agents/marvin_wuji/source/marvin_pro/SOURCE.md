# Marvin Pro source

- Upstream: https://github.com/KLMmotion/marvin_pro_robotwin
- Upstream asset directory: `assets/embodiments/tianji`
- Imported commit: `1e30f003984ddb82d2994474b015f0933c131d94`
- Imported files: `marvin_robot.urdf`, `config.yml`, and `meshes/`
- License: MIT; see `LICENSE` in this directory.

The upstream model calls the robot both "Marin Pro" and "Marvin Pro".  The
hardware and repository names used by this integration are "Marvin Pro".
The stock parallel-gripper branches are retained in the pristine source URDF
only.  DexVerse generates a separate composite URDF that replaces them with
left and right WUJI hands.
