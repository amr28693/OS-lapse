# Continuity of ADM variables across the Oppenheimer–Snyder boundary in the unit-lapse gauge

**Author:** Anderson M. Rodriguez  

## Summary

The N = 1 (Painlevé–Gullstrand) gauge is the unique constant-lapse ADM gauge in which the lapse, shift, and spatial metric are individually continuous across the matter–vacuum boundary of the Oppenheimer–Snyder dust collapse. In Schwarzschild gauge, the lapse gap ΔN = 1 − √(1 − 2M/R) grows from zero to unity as the dust surface approaches the horizon. We call this property *decomposition continuity* and distinguish it from the coordinate-invariant Israel junction conditions, which are satisfied in any gauge.

## Repository contents

```
.
├── README.md
├── generate_figures.py                   # Reproduces all figures
├── terminal_output.txt                     # Terminal log showing verification
└── figures/
    ├── fig1_lapse_comparison.pdf           # Fig. 1: Lapse N(r), PG vs Schwarzschild
    ├── fig2_velocity_matching.pdf           # Fig. 2: Shift vector matching at dust surface
    └── figS1_metric_continuity.pdf          # Fig. S1: Metric coefficients g_TT, g_Tr, g_rr
```

## Reproducing the figures

Requires Python 3 with NumPy and Matplotlib.

```bash
python3 generate_figures.py
```

Figures are written to `figures/`. The script also prints the metric coefficient continuity verification to the terminal:

```
g_TT continuity: int=0.600000, ext=0.600000, delta=1.11e-16
g_Tr continuity: int=0.632456, ext=0.632456, delta=1.11e-16
```

The residuals (δ ∼ 10⁻¹⁶) sit at floating-point roundoff, as expected since the interior and exterior expressions are algebraically identical at the surface; the check guards against transcription error in the code rather than independently confirming agreement.


````
## Key result
````

Among constant-lapse gauges, N = 1 is the unique choice for which the lapse is continuous across the OS boundary: the interior comoving metric fixes N = 1, and a constant exterior lapse continuous with it must equal 1. Continuity of all three ADM variables then singles out the standard (flat-slice) Painlevé–Gullstrand chart — the unique unit-lapse spherically symmetric vacuum gauge with intrinsically flat spatial slices; the generalized Painlevé–Gullstrand family shares unit lapse but has curved slices that cannot match the flat interior.

## License

MIT
