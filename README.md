# DexVerse Marvin/WUJI asset

This repository distributes one robot: the real-machine Marvin Pro dual arm
with two first-generation WUJI hands. The 54-joint articulation, wrist camera
mounts, dark hand appearance, and collision geometry are baked into
`robot_agents/marvin_wuji/marvin_wuji.usdc`. Its only local dependency is
`robot_agents/marvin_wuji/textures/color_121212.hdr`.

Install beside DexVerse:

```bash
bash ../DexVerse/scripts/setup/install_marvin_wuji_assets.sh "$PWD" ../DexVerse
sha256sum --check MANIFEST.sha256
```

No floating-hand assets, stock gripper URDF, generated URDF, or intermediate
CAD are part of this runtime bundle. The original user-supplied CAD and
third-party WUJI description must be obtained separately if the binary robot
asset needs to be rebuilt; editing only this USD does not reproduce the
original authoring pipeline. DexVerse owns the actuator, IK and camera settings.

## Licenses

The Marvin-derived geometry is MIT licensed, Copyright 2025 Tianxing Chen;
see `licenses/MARVIN_PRO_LICENSE`. The WUJI-derived hand geometry is MIT
licensed, Copyright 2025 Wuji Technology; see
`licenses/WUJI_DESCRIPTION_LICENSE`. Preserve both notices when redistributing
the USD. DexVerse source code is separately BSD-3-Clause licensed.
