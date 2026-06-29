# Engineering Case 001

# Chacao Suspension Bridge (Chile) — Cable Shape Finding Analysis Using HCableAnalysis

---

## Project Overview

The Chacao Suspension Bridge is one of the most significant long-span bridge projects currently under construction in South America. Located in southern Chile, the bridge crosses the Chacao Channel and connects Chiloé Island with the Chilean mainland.

The bridge adopts an asymmetric three-tower suspension bridge configuration with two unequal main spans, making it one of the most challenging suspension bridge projects in terms of structural analysis, construction, and cable system design.

After completion, it will become the largest suspension bridge in Latin America and one of the world's most representative multi-span suspension bridges.

---

## Bridge Information

| Item | Value |
|------|------|
| Project | Chacao Suspension Bridge |
| Location | Chacao Channel, Chile |
| Bridge Type | Three-Tower Suspension Bridge |
| Total Length | Approximately 2750 m |
| Main Spans | 1155 m + 1055 m |
| Deck | Four-lane Highway |
| Structural Feature | Asymmetric Multi-span Suspension Bridge |

---

## Bridge Layout

![Bridge Layout](./ChacaoBridge-layout.png)

---

## Project Rendering

![Bridge Rendering](./ChacaoBridge.png)

---

# Background

Cable shape finding is the first and one of the most critical procedures in suspension bridge analysis.

A reliable initial cable configuration is essential because it determines the unstressed cable length, initial cable force, sag profile, and equilibrium geometry used in subsequent finite element analyses.

For large suspension bridges with asymmetric spans and multiple towers, numerical shape finding is considerably more difficult than that of conventional two-tower bridges due to the strong coupling between cable forces and geometry.

HCableAnalysis provides an efficient numerical framework for solving this nonlinear equilibrium problem.

---

# HCableAnalysis Workflow

The overall workflow is summarized as follows:

1. Define bridge geometry.
2. Generate cable discretization.
3. Apply dead loads.
4. Solve nonlinear cable equilibrium.
5. Update cable coordinates iteratively.
6. Check convergence.
7. Export the final cable geometry.

The solver automatically adjusts cable coordinates until the residual force satisfies the prescribed convergence tolerance.

---

# Numerical Analysis

The cable system was established according to publicly available bridge information.

The objective of this example is to demonstrate the capability of HCableAnalysis for suspension bridge cable shape finding rather than to reproduce the complete construction design.

Analysis assumptions include:

- Dead-load equilibrium only
- Elastic cable behavior
- Three-dimensional cable geometry
- Nonlinear iterative solution
- Automatic convergence control

---

# Analysis Results

The nonlinear shape-finding analysis converged successfully.

Final convergence tolerance:

```
Residual = 1.0 × 10⁻⁵
```

The obtained cable profile satisfies the equilibrium requirements under the specified dead load.

The resulting geometry can be directly exported for subsequent finite element modeling in commercial software such as ANSYS or Abaqus.

---

# DXF Geometry

The generated cable geometry can be downloaded below.

**Download**

👉 [ChacaoBridge.dxf](./ChacaoBridge.dxf)

The DXF file contains the equilibrium cable profile after shape finding and can be imported into most CAD software.

---

# Summary

This engineering case demonstrates the application of HCableAnalysis to a representative long-span suspension bridge.

The analysis successfully obtained the equilibrium cable configuration with a convergence accuracy of **1 × 10⁻⁵**, illustrating the robustness and numerical stability of the HCableAnalysis framework.

The resulting cable geometry can serve as the initial configuration for further finite element analyses, including structural analysis, construction stage simulation, and bridge system modeling.

---

# References

The bridge dimensions and general project information presented in this example are compiled from publicly available information released by the Chilean Ministry of Public Works and project participants.

This case study is intended solely as a demonstration of HCableAnalysis capabilities and does not represent the official design model of the project.

---

**Software**

HCableAnalysis

**Analysis Type**

Cable Shape Finding

**Status**

Converged ✓

**Convergence Tolerance**

1 × 10⁻⁵