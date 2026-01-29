---
linkTitle: Tutorial 1
title: "Tutorial 1"
weight: 1
sidebar:
  open: true
---

# DP capability analysis for an offshore wind turbine installation vessel

## 1. Introduction

This tutorial demonstrates how to use the **DP Capability Tool** to perform **feasibility calculation** and **capability analyses** for an offshore wind turbine installation vessel equipped with:

- **2 azimuth thrusters at the bow**
- **3 tunnel thrusters at the stern**

The complete tutorial model is provided within the software and is accessible from the Help menu.

![Tutorial menu](./images/Snipaste_2026-01-27_08-53-13.png)

---

## 2. Vessel data (Optional)

In a standard DP capability analysis, the first step is to input **vessel data**, which defines the vessel reference frame and serves as a container for thruster positions.

This step is optional but recommended for clarity and future model extension.

> **Note:** The vessel outline is used for visualization only and does **not** affect DP calculation results.

### Vessel outline coordinates 

| X (m) | Y (m) |
|------:|------:|
| 120.0 | 0.0 |
| 90.0 | 25.0 |
| -120.0 | 25.0 |
| -120.0 | -25.0 |
| 90.0 | -25.0 |

These outline points are linked together into a closed frame, helping users visually check and confirm the thruster locations relative to the vessel's hull.

---

## 3. Thruster configuration

This vessel configuration includes:

- **Azimuth thrusters (bow)**  
  Capable of generating thrust in any direction from **0° to 360°**

- **Tunnel thrusters (stern)**  
  Capable of generating thrust to either **port** or **starboard**

There are **no shaft propellers** in this tutorial case.

---

### 3.1 Thrusters

For each azimuth or tunnel thruster, the following parameters must be defined:

- Thruster name
- X coordinate (m)
- Y coordinate (m)
- Propeller diameter (m)
- Maximum power (kW)
- Maximum nominal thrust (kN)
- Default thrust loss factor

Each thruster is positioned relative to the vessel reference coordinate system. When a thrust loss factor curve is not supplied, the default thrust loss factor is applied to calculate the thrust force. It is especially applicable to azimuth thrusters.

#### Azimuth thrusters

| Name | X (m) | Y (m) | Diameter (m) | Max power (kW) | Nominal thrust (kN) | Default thrust loss factor |
|------|------:|------:|-------------:|--------------:|--------------------:|---------------------------:|
| Th1  | -108.6 | -8.2 | 0 | 4,500.00 | 694.428 | 0.9 |
| Th2  | -108.6 | 8.2  | 0 | 4,500.00 | 694.428 | 0.9 |

#### Tunnel thrusters

| Name | X (m) | Y (m) | Diameter (m) | Max power (kW) | Nominal thrust (kN) | Default thrust loss factor |
|------|------:|------:|-------------:|--------------:|--------------------:|---------------------------:|
| Th3  | 102.8 | 0 | 0 | 2,200.00 | 252.36 | 0.9 |
| Th4  | 96.8  | 0 | 0 | 2,200.00 | 252.36 | 0.9 |
| Th5  | 90.2  | 0 | 0 | 2,200.00 | 252.36 | 0.9 |

The thruster position plot displays each azimuth thruster, tunnel thruster, and shaft propeller using a distinct shape and color for each type. When a thruster is selected in the list, it will be highlighted in the plot accordingly.

![Thruster positions plot](./images/ThrusterPositionPlot.gif)

---

## 5. Failure mode definition

Failure modes are organized into **failure mode groups**, each representing a specific operational scenario, such as:

- Intact condition (all thrusters active)
- Single thruster failure
- Multiple thruster failures

The user must:

1. Create a failure mode group with a meaningful name
2. Define one or more failure modes within the group
3. Specify which thrusters are **active** or **failed** in each mode
4. Specify azimuth thruster thrust loss factor curves and restricted azimuth sectors

---

### 5.1 Azimuth thruster restrictions

For azimuth thrusters, additional constraints can be applied:

- **Thrust factor curve** over the full **0–360°** range  
- **Multiple forbidden azimuth zones**, where thrust is restricted or not allowed  

These settings allow realistic modeling of mechanical, structural, or operational limitations. 

DNV-ST-0111 and the ABS Guide for Dynamic Positioning Systems provide detailed guidance on how to account for thrust loss factor curves and forbidden zones.

In this tutorial, the thrust loss factor for **Th1** is set to 0.9 over the full 360° azimuth range, with a forbidden zone defined between 71° and 109°.

![Th1 - Thrust loss factor curve and forbidden zones](./images/Snipaste_2026-01-29_10-57-11.png)

The thrust loss factor for **Th2** is identical to that of **Th1**, while its forbidden zone is defined on the opposite side, ranging from 251° to 289°.

![Th2 - Thrust loss factor curve and forbidden zones](./images/Snipaste_2026-01-29_10-58-37.png)

The thrust loss factor curve is presented in the right-side plot, and the forbidden zones are marked on the azimuth thrusters in the thruster position view.

![Thrust loss factor curve and forbidden zones](./images/ThrustLossFactorForbiddenZones.gif)


---

## 6. Environmental load definition

Environmental loads are defined for both feasibility calculations and capability analysis to assess the resistance capacity of the dynamic positioning system.

Environmental loads are organized into groups, each representing a specific wind speed or wind speed series, which is particularly suitable for capability analysis to evaluate the maximum wind speed or DP capability number that the dynamic positioning system can withstand.

In this tutorial, two environmental load groups are used:

1. **Site loads**
   - Used for feasibility calculation  
   - Represents single site-specific environmental condition  

2. **Capability loads**
   - Used for capability analysis  
   - Includes multiple wind load cases with increasing wind speeds  
   - Used to determine the **maximum wind speed or DP capability number** the DP system can withstand  

---

## 7. Analysis settings

In the **Analysis settings** panel, the user can define:

- **Skipped zones** (heading sectors of no operational interest)

These zones are excluded from calculation to:

- Improve computational efficiency  
- Focus on operationally relevant headings only  

---

## 8. Feasibility calcuation and capability Analysis

### 8.1 Defining an Analysis Case

A feasibility calculation or capability analysis is defined by combining:

- One **failure mode group**
- One **environmental load group**

Each combination represents a unique DP analysis case.

---

### 8.2 Running Calculations

- Calculations can be run **individually** or **in batch**
- Multiple calculation attempts can be performed to improve solution robustness

Possible outcomes include:

- Feasible solutions found  
- No feasible solution found  
- Additional calculation attempts required  

---

### 8.3 Result Visualization

Once results are available, they can be visualized as:

- **DP capability plots**
- **DP rose plots**

All plots are displayed in the **right-side plotting area** of the software.

---

## 9. Reporting

Since all calculations in this tutorial are pre-computed, the user can directly use the **reporting function**.

Key features include:

- User-selectable report content  
- Automatic formatting  
- **One-click generation** of a complete DP work report  

---

## 10. Rule Utilities

The DP Capability Tool includes built-in **rule utilities** to support industry compliance, including:

- **DNV-ST-0111**
- **ABS Guide for Dynamic Positioning Systems**

These utilities help verify calculations and interpret results according to class requirements.
