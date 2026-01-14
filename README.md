# Static & Computational Analysis of a 2D Truss Structure

This repository contains a complete analysis of a two-dimensional truss structure using both **manual theoretical methods** and **software simulation**. The objective is to determine **reaction forces at supports**, **internal member forces**, and compare analytical results with simulation data from **ANSYS / SolidWorks**.

---

##  Abstract

This report presents the analysis of a 2D truss structure to compute reaction forces at supports and internal axial forces in members. The truss was analyzed using the **method of joints** and **method of sections**, and then validated through **ANSYS / SolidWorks simulation**. The simulation results were compared to theoretical calculations to identify deviations and understand modeling assumptions.

---

##  Keywords

`ANSYS` `SolidWorks` `Truss` `Static Equilibrium` `Two-Force Members` `Reaction Forces` `Distributed Loads` `Structural Analysis`

---

##  Truss Overview

A **truss** is a rigid structural framework composed of straight members connected at joints. Members experience **axial loads only** (tension or compression) and are treated as **two-force members**. Trusses are widely used in bridges, towers, roofs, and industrial structures.

### **Truss Components**
- **Joints:** Connection nodes (usually pinned)
- **Members:** Bars carrying axial force
- **External Forces:** Applied loads + support reactions

### **Common Truss Types**
- Pratt
- Howe
- Warren
- Modified Warren

---

##  Key Structural Concepts

### **Two-Force Members**
A member with forces applied at only two points. Forces are equal, opposite, and collinear.

### **Tension vs Compression**
- **Tension (+):** Member is being pulled
- **Compression (−):** Member is being pushed

### **Distributed Loads**
Distributed loads on upper chords were converted to equivalent joint loads using:
```
d = ΣWi / L
```

### **Support Types Used**
The truss utilized:
- **Pinned Support**
- **Roller Support**

---

##  Static Equilibrium Basis

For 2D static equilibrium:
```
ΣFx = 0
ΣFy = 0
ΣM = 0
```
These conditions were used to determine support reactions and member forces.

---

##  Manual Analytical Solution

Two classical methods were applied:

### **1. Method of Sections**
The truss was cut into sections and analyzed as rigid bodies using equilibrium equations.

### **2. Method of Joints**
Each joint was isolated and solved using:
```
ΣFx = 0
ΣFy = 0
```

---

##  Reaction Forces (Manual Results)

Manual solution yielded the following support reactions:
```
Hx = -2.6356 N
Ay = 5.631 N
Hy = 10.661 N
```

---

##  Internal Member Forces (Manual Results)

Selected internal forces (sign convention: + Tension, − Compression):

| Member | Force (N) |
|---|---:|
| FAB | 0 |
| FAJ | -5.631 |
| FGM | 4.000 |
| FHM | -13.456 |
| FUT | 5.004 |
| FIJ | 2.000 |
| FIO | 3.464 |
| FSM | -10.932 |
| FFS | -8.661 |
| FJB | -2.735 |
| FQB | -1.300 |
| FQR | 3.669 |
| FFL | -0.834 |
| FFG | 5.574 |
| FED | 6.414 |
| FBC | 1.461 |
| FCD | 1.461 |

---

##  Simulation in ANSYS / SolidWorks

The truss geometry was simulated in **ANSYS / SolidWorks Simulation** to extract:
- Reaction forces
- Internal axial forces
- Stress distribution
- Deformation shape

### **Sample Simulation Member Forces**

| Member | Simulation (N) |
|---|---:|
| AB | -0.0398 |
| BC | 1.596 |
| CD | 1.561 |
| DE | 2.350 |
| EF | 2.311 |
| FG | 2.233 |
| GH | 2.692 |
| HN | -0.804 |
| NM | 0.153 |
| MH | -10.007 |
| TS | 4.016 |
| SF | 6.188 |
| RQ | 1.524 |
| QP | 2.513 |
| OI | 3.195 |
| IJ | 1.845 |

---

##  Error Comparison

Percentage error formula used:
```
Error % = [(Simulation - Manual) / Simulation] × 100
```

### **Support Reactions Comparison**

| Reaction | Manual | Simulation | % Error |
|---|---:|---:|---:|
| Hy | 10.661 | 10.968 | 2.799% |
| Ay | 5.631 | 5.971 | 5.75% |
| Hx | -2.6356 | -2.6357 | 0.0037% |

---

##  Possible Sources of Deviation

Observed differences between manual and simulation results may be due to:
- Material elasticity in simulation causing deformation
- Ideal pin assumptions in manual calculations
- Neglecting self-weight of members in theory
- Solver using stiffness matrix formulations
- More realistic boundary conditions in simulation


---

##  References (Sources Used)

Reference materials included online engineering resources on:
- Truss behavior
- Static equilibrium
- Two-force members
- Support reactions
- Method of joints & sections


---
