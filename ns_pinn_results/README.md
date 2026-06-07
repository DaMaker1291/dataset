# NS-PINN Results

Generated: 2026-06-07 22:14:27

## What is this?
Numerical simulation of 3-D incompressible Navier-Stokes equations using a
Physics-Informed Neural Network (PINN). This is **computational CFD research**
and should be described as such in any publication.

## Monte Carlo Summary (N=50 trials)
| Metric | Value |
|--------|-------|
| Mean |ω| at epicenter | 0.0002 |
| Std deviation | 0.0001 |
| Min |ω| | 0.0000 |
| Max |ω| | 0.0005 |
| Mean divergence residual | 1.35e-04 |

## File Structure
```
ns_pinn_results/
├── csv/
│   ├── singularity_metrics.csv    ← MC trial data (vorticity per trial)
│   ├── mc_summary.json            ← aggregated statistics
│   ├── training_history.csv       ← loss + divergence per epoch
│   └── midplane_slice_z05.csv     ← field values on z=0.5 slice
├── mesh/
│   └── ns_field.npz               ← full 3-D field (U,V,W,P,Omega)
├── models/
│   └── pinn_weights.pt            ← trained PyTorch model weights
└── plots/
    ├── training_history.png
    ├── vorticity_slices.png
    ├── vorticity_3d.png
    ├── blowup_radial_profile.png
    ├── velocity_streamlines.png
    └── monte_carlo_distribution.png
```

## Reynolds Number
Re = 100.0

## Scientific Disclaimer
These results are numerical observations from a PINN approximation.
They do not constitute an analytical proof of finite-time blow-up or
global regularity for the Navier-Stokes equations.
