# DexVerse Marvin/Wuji Assets

Versioned robot assets for the Marvin Pro dual seven-axis arm with two Wuji
20-DoF hands. This repository is intentionally separate from the DexVerse
source repository because it contains generated USD binaries and STL meshes.

## Install

Clone this repository next to `DexVerse`, then run the installer shipped by
the source repository:

```bash
bash ../DexVerse/scripts/setup/install_marvin_wuji_assets.sh "$PWD" ../DexVerse
```

The directory layout mirrors the destination below
`source/dexverse/dexverse/robot_agents/`; the installer copies assets without
deleting or overwriting the Python integration source.

## Contents

- `robot_agents/marvin_wuji/fixed_marvin_wuji/`: runtime composite USD;
- `robot_agents/marvin_wuji/source/marvin_pro/`: pristine Marvin source URDF,
  meshes, provenance and license;
- `robot_agents/wuji/floating_wuji_left/` and `floating_wuji_right/`: floating
  Wuji USD assets used by the original-hand test paths.

The composite removes the stock Marvin grippers/cameras and attaches the Wuji
palm models to `flange_L` and `flange_R`. Runtime actuator and IK behavior is
defined in the DexVerse source repository, not in this repository.

The intermediate composite URDF is deliberately not published: Isaac Lab's
URDF importer requires resolved mesh paths, so that generated file embeds the
build machine's absolute directories. The checked-in USD is self-contained
and portable. Use the generator in the source repository if the asset must be
rebuilt on another machine.

## Integrity

After cloning, verify all assets:

```bash
sha256sum --check MANIFEST.sha256
```

No file currently exceeds GitHub's 100 MB per-file limit. Do not add Isaac
Sim, CloudXR, datasets, checkpoints, caches, or machine-local configuration.

## Licensing and provenance

This is a mixed-provenance asset bundle. See [`LICENSES.md`](LICENSES.md), the
license files under `licenses/`, and the Marvin source provenance at
`robot_agents/marvin_wuji/source/marvin_pro/SOURCE.md`. Generated USD files are
derivative representations of those source descriptions and retain their
corresponding notices.
