# -Structural-Damage-Analysis
A Finite Element Analysis (FEA) simulation of an aircraft L-bracket under structural loading, designed and simulated using *Autodesk Fusion 360*.


#Project Overview

This project simulates real-world structural loading on an aircraft bracket — the type used in wing ribs and fuselage panels. The goal is to analyze stress distribution, deformation, and structural safety using FEA techniques.

#Objectives

- Design an aircraft L-bracket in CAD
- Apply realistic structural loads and boundary conditions
- Assign aerospace-grade material properties
- Run FEA simulation to analyze structural behavior
- Identify failure-prone zones and evaluate safety

#Tools Used

- *Autodesk Fusion 360* — CAD Design + FEA Simulation

#Material

|Property                 |Value                         |
|-------------------------|------------------------------|
|Material                 |Aluminum 6061-T6 (Cold Formed)|
|Density                  |2.700E-06 kg/mm³              |
|Young’s Modulus          |69 GPa                        |
|Poisson’s Ratio          |0.33                          |
|Yield Strength           |369 MPa                       |
|Ultimate Tensile Strength|389 MPa                       |



#Bracket Specifications

|Parameter             |Value           |
|----------------------|----------------|
|Vertical wall height  |100 mm          |
|Horizontal base length|80 mm           |
|Thickness             |10 mm           |
|Depth                 |50 mm           |
|Bolt holes            |4 × 8mm diameter|

#Simulation Setup

|Parameter       |Value                         |
|----------------|------------------------------|
|Study Type      |Static Stress                 |
|Applied Force   |5000 N (downward)             |
|Load Location   |Bottom face of horizontal base|
|Fixed Constraint|Back face of vertical wall    |
|Mesh            |Auto-generated                |

#Results

|Result               |Value        |Safe Limit|Status     |
|---------------------|-------------|----------|-----------|
|Max Von Mises Stress |22.547 MPa   |< 369 MPa | Safe     |
|Min Von Mises Stress |1.236E-04 MPa|—         | Safe     |
|Minimum Safety Factor|16.365       |> 1.5     | Excellent|
|Overall Assessment   |Very Strong  |—         | Passed   |

# Key Findings

- The bracket is *16x stronger* than the minimum aerospace safety requirement
- Highest stress concentration observed at the *base corner junction* — the critical zone where vertical wall meets horizontal base
- The vertical wall experiences near-zero stress under the applied load
- Aluminum 6061-T6 performs excellently for this loading condition

#Simulation Results

> Screenshots of all 4 FEA result views:

|Result View     |Description                       |
|----------------|----------------------------------|
|Von Mises Stress|Stress distribution across bracket|
|Safety Factor   |Safety margin visualization       |
|Displacement    |Deformation under load            |
|Strain          |Material strain distribution      |
