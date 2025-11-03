# optimal-charging-stations-cycleway
This project tackles the problem of optimally locating charging stations for e-bikes along a long linear cycle path — such as the Vento (Venezia–Torino) or Danube cycleways.

# ⚡ Optimal Charging Station Location on a Cycleway

This project focuses on the optimal placement of e-bike charging stations along a long linear cycle path, such as the Vento (Venezia–Torino) or Danube cycleways.

Developed as part of an **optimization assignment**, the goal is to design a charging infrastructure that ensures **complete route coverage** while minimizing overall cost and allowing cyclists to access **Points of Interest (POIs)** along the way.

---

## 🧭 Project Overview

E-bikes have introduced new challenges in the design of sustainable transport infrastructure.  
Because recharging requires a non-negligible time, charging stations should be located in places where cyclists can perform alternative activities — such as visiting restaurants, museums, or other amenities — known as **Points of Interest (POIs)**.

However, these POIs are **not directly on the main path** but require **small detours**.  
The objective is to determine **where to install charging stations** along the route to ensure full energy coverage while minimizing total installation costs.

---

## 📊 Problem Description

The cycle path is represented as a **graph** `H = (V, E)`,  
where:
- `V` are the nodes (locations along or near the path)
- `E` are the edges (segments connecting them)

Each edge has an **energy consumption value** associated with it, proportional to its length and terrain slope.

We assume:
- The biker starts with a **fully charged battery** at the starting node.
- The biker must **complete the trip** from the start node `s` to the end node `t`.
- The biker may **deviate from the main path** to visit all available POIs.

---

## 🧩 Problem 1 — Forward Traversal (s → t)

> **Goal:**  
> Determine in which nodes of `H` to install charging stations so that:
> - The **maximum energy consumption** between two consecutive charging stations is ≤ **Δ**.  
> - The **total installation cost** is minimized.

This models a biker moving **from the beginning (s)** to the **end of the path (t)**.

---

## 🔄 Problem 2 — Backward Traversal (t → s)

> **Goal:**  
> Determine in which nodes of `H` to install charging stations so that:
> - The **maximum energy consumption** between two consecutive charging stations is ≤ **Δ**.  
> - The **total installation cost** is minimized.

This corresponds to the biker **returning from t to s**, accounting for possibly different elevation profiles or consumption patterns.






