# NEP-kappa-2.0 Paper Data (2026)

Research data organized by material, calculation method, and temperature.

- `potentials/`: Interatomic potentials, named `nep.txt` for each material.
- `structures/`: Initial and relaxed structures, named `POSCAR_initial` and `POSCAR_relaxed`. BAs uses a fixed reference structure and includes only `POSCAR_initial`; no separate relaxation was performed.
- `results/`: Force constants, thermal conductivity, QHA thermodynamic data, and TD-BTE trajectories.

`T0300K` denotes 300 K. `T0100K-T1000K` indicates that the enclosed file contains multiple temperature points within that range. `qha-points/` is organized by volume ratio. SiC QHA volume sampling, thermodynamic data, and temperature-dependent transport results are grouped under `results/SiC/temperature/QHA/`.

## Complete File Structure

```text
2026-nep-kappa-2.0/
├── potentials/
│   ├── BAs/
│   │   └── nep.txt
│   ├── Cs2AgInCl6/
│   │   └── nep.txt
│   └── SiC/
│       └── nep.txt
├── results/
│   ├── BAs/
│   │   ├── DFT/
│   │   │   └── force_constants/
│   │   │       ├── FORCE_CONSTANTS_2ND
│   │   │       ├── FORCE_CONSTANTS_3RD
│   │   │       └── FORCE_CONSTANTS_4TH
│   │   ├── MACE/
│   │   │   └── force_constants/
│   │   │       ├── FORCE_CONSTANTS_2ND
│   │   │       ├── FORCE_CONSTANTS_3RD
│   │   │       ├── FORCE_CONSTANTS_4TH
│   │   │       ├── fc2.hdf5
│   │   │       └── phono3py_disp.yaml
│   │   └── NEP/
│   │       └── force_constants/
│   │           ├── FORCE_CONSTANTS_2ND
│   │           ├── FORCE_CONSTANTS_3RD
│   │           ├── FORCE_CONSTANTS_4TH
│   │           ├── fc2.hdf5
│   │           └── fc3.hdf5
│   ├── Cs2AgInCl6/
│   │   └── temperature/
│   │       ├── Harmonic/
│   │       │   ├── T0100K-T0800K/
│   │       │   │   └── kappa-m151515.hdf5
│   │       │   ├── POSCAR_relaxed
│   │       │   ├── fc2.hdf5
│   │       │   └── phono3py_disp.yaml
│   │       ├── QHA/
│   │       │   └── T0000K-T0800K/
│   │       │       └── volume-temperature.dat
│   │       └── SSCHA_fixed_volume/
│   │           ├── T0100K/
│   │           │   ├── fc2.hdf5
│   │           │   ├── kappa-m151515.hdf5
│   │           │   └── phono3py_disp.yaml
│   │           ├── T0200K/
│   │           │   ├── fc2.hdf5
│   │           │   ├── kappa-m151515.hdf5
│   │           │   └── phono3py_disp.yaml
│   │           ├── T0300K/
│   │           │   ├── fc2.hdf5
│   │           │   ├── kappa-m151515.hdf5
│   │           │   └── phono3py_disp.yaml
│   │           ├── T0400K/
│   │           │   ├── fc2.hdf5
│   │           │   ├── kappa-m151515.hdf5
│   │           │   └── phono3py_disp.yaml
│   │           ├── T0500K/
│   │           │   ├── fc2.hdf5
│   │           │   ├── kappa-m151515.hdf5
│   │           │   └── phono3py_disp.yaml
│   │           ├── T0600K/
│   │           │   ├── fc2.hdf5
│   │           │   ├── kappa-m151515.hdf5
│   │           │   └── phono3py_disp.yaml
│   │           ├── T0700K/
│   │           │   ├── fc2.hdf5
│   │           │   ├── kappa-m151515.hdf5
│   │           │   └── phono3py_disp.yaml
│   │           └── T0800K/
│   │               ├── fc2.hdf5
│   │               ├── kappa-m151515.hdf5
│   │               └── phono3py_disp.yaml
│   └── SiC/
│       ├── baseline/
│       │   ├── dft/
│       │   │   ├── fc2.hdf5
│       │   │   ├── kappa-m313131.hdf5
│       │   │   └── phono3py_disp.yaml
│       │   ├── mace/
│       │   │   ├── fc2.hdf5
│       │   │   ├── kappa-m313131.hdf5
│       │   │   └── phono3py_disp.yaml
│       │   └── nep/
│       │       ├── fc2.hdf5
│       │       ├── kappa-m313131.hdf5
│       │       └── phono3py_disp.yaml
│       ├── tdbte/
│       │   ├── force_constants/
│       │   │   ├── fc2.hdf5
│       │   │   ├── fc3.hdf5
│       │   │   └── phono3py_disp.yaml
│       │   └── trajectory/
│       │       ├── branch-energy.csv
│       │       ├── equilibrium.npz
│       │       ├── excited.npz
│       │       └── trajectories.npz
│       └── temperature/
│           ├── Harmonic/
│           │   ├── T0100K-T1000K/
│           │   │   └── kappa-m313131.hdf5
│           │   ├── T1100K-T1200K/
│           │   │   └── kappa-m313131.hdf5
│           │   ├── POSCAR_relaxed
│           │   ├── fc2.hdf5
│           │   └── phono3py_disp.yaml
│           ├── QHA/
│           │   ├── T0300K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T0400K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T0500K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T0600K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T0700K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T0800K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T0900K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T1000K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T1100K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T1200K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── qha-points/
│           │   │   ├── 001-ratio-0.940000/
│           │   │   │   ├── POSCAR
│           │   │   │   ├── POSCAR_scaled
│           │   │   │   ├── force_constants.hdf5
│           │   │   │   ├── phonopy_params.yaml
│           │   │   │   └── thermal_properties.yaml
│           │   │   ├── 002-ratio-0.955000/
│           │   │   │   ├── POSCAR
│           │   │   │   ├── POSCAR_scaled
│           │   │   │   ├── force_constants.hdf5
│           │   │   │   ├── phonopy_params.yaml
│           │   │   │   └── thermal_properties.yaml
│           │   │   ├── 003-ratio-0.970000/
│           │   │   │   ├── POSCAR
│           │   │   │   ├── POSCAR_scaled
│           │   │   │   ├── force_constants.hdf5
│           │   │   │   ├── phonopy_params.yaml
│           │   │   │   └── thermal_properties.yaml
│           │   │   ├── 004-ratio-0.985000/
│           │   │   │   ├── POSCAR
│           │   │   │   ├── POSCAR_scaled
│           │   │   │   ├── force_constants.hdf5
│           │   │   │   ├── phonopy_params.yaml
│           │   │   │   └── thermal_properties.yaml
│           │   │   ├── 005-ratio-1.000000/
│           │   │   │   ├── POSCAR
│           │   │   │   ├── POSCAR_scaled
│           │   │   │   ├── force_constants.hdf5
│           │   │   │   ├── phonopy_params.yaml
│           │   │   │   └── thermal_properties.yaml
│           │   │   ├── 006-ratio-1.015000/
│           │   │   │   ├── POSCAR
│           │   │   │   ├── POSCAR_scaled
│           │   │   │   ├── force_constants.hdf5
│           │   │   │   ├── phonopy_params.yaml
│           │   │   │   └── thermal_properties.yaml
│           │   │   ├── 007-ratio-1.030000/
│           │   │   │   ├── POSCAR
│           │   │   │   ├── POSCAR_scaled
│           │   │   │   ├── force_constants.hdf5
│           │   │   │   ├── phonopy_params.yaml
│           │   │   │   └── thermal_properties.yaml
│           │   │   ├── 008-ratio-1.045000/
│           │   │   │   ├── POSCAR
│           │   │   │   ├── POSCAR_scaled
│           │   │   │   ├── force_constants.hdf5
│           │   │   │   ├── phonopy_params.yaml
│           │   │   │   └── thermal_properties.yaml
│           │   │   └── 009-ratio-1.060000/
│           │   │       ├── POSCAR
│           │   │       ├── POSCAR_scaled
│           │   │       ├── force_constants.hdf5
│           │   │       ├── phonopy_params.yaml
│           │   │       └── thermal_properties.yaml
│           │   ├── Cp-temperature_polyfit.dat
│           │   ├── Cv-volume.dat
│           │   ├── bulk_modulus-temperature.dat
│           │   ├── dsdv-temperature.dat
│           │   ├── e-v.dat
│           │   ├── entropy-volume.dat
│           │   ├── gibbs-temperature.dat
│           │   ├── gruneisen-temperature.dat
│           │   ├── helmholtz-volume.dat
│           │   ├── qha-key-results.csv
│           │   ├── thermal_expansion.dat
│           │   └── volume-temperature.dat
│           ├── QHA_SSCHA/
│           │   ├── T0300K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T0400K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   ├── mlpsscha.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T0500K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   ├── mlpsscha.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T0600K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T0700K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   ├── mlpsscha.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T0800K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   ├── mlpsscha.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T0900K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T1000K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   ├── mlpsscha.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   ├── T1100K/
│           │   │   ├── fc2.hdf5
│           │   │   ├── kappa-m313131.hdf5
│           │   │   ├── mlpsscha.hdf5
│           │   │   └── phono3py_disp.yaml
│           │   └── T1200K/
│           │       ├── fc2.hdf5
│           │       ├── kappa-m313131.hdf5
│           │       └── phono3py_disp.yaml
│           └── SSCHA_fixed_volume/
│               ├── T0300K/
│               │   ├── fc2.hdf5
│               │   └── kappa-m313131.hdf5
│               ├── T0400K/
│               │   ├── fc2.hdf5
│               │   ├── kappa-m313131.hdf5
│               │   ├── mlpsscha.hdf5
│               │   └── phono3py_disp.yaml
│               ├── T0500K/
│               │   ├── fc2.hdf5
│               │   ├── kappa-m313131.hdf5
│               │   ├── mlpsscha.hdf5
│               │   └── phono3py_disp.yaml
│               ├── T0600K/
│               │   ├── fc2.hdf5
│               │   └── kappa-m313131.hdf5
│               ├── T0700K/
│               │   ├── fc2.hdf5
│               │   ├── kappa-m313131.hdf5
│               │   ├── mlpsscha.hdf5
│               │   └── phono3py_disp.yaml
│               ├── T0800K/
│               │   ├── fc2.hdf5
│               │   ├── kappa-m313131.hdf5
│               │   ├── mlpsscha.hdf5
│               │   └── phono3py_disp.yaml
│               ├── T0900K/
│               │   ├── fc2.hdf5
│               │   └── kappa-m313131.hdf5
│               ├── T1000K/
│               │   ├── fc2.hdf5
│               │   ├── kappa-m313131.hdf5
│               │   ├── mlpsscha.hdf5
│               │   └── phono3py_disp.yaml
│               ├── T1100K/
│               │   ├── fc2.hdf5
│               │   ├── kappa-m313131.hdf5
│               │   ├── mlpsscha.hdf5
│               │   └── phono3py_disp.yaml
│               └── T1200K/
│                   ├── fc2.hdf5
│                   └── kappa-m313131.hdf5
├── structures/
│   ├── BAs/
│   │   └── POSCAR_initial
│   ├── Cs2AgInCl6/
│   │   ├── POSCAR_initial
│   │   └── POSCAR_relaxed
│   └── SiC/
│       ├── POSCAR_initial
│       └── POSCAR_relaxed
└── README.md
```
