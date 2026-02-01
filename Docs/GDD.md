
# 🎭 Game Design Document: Midnight Masquerade

## 1. Project Overview

* **Genre:** Top-Down Stealth / Infiltration
* **Theme:** Identity is your greatest disguise.

* *********Platform:** ?????:*********

* **Target Loop:** Infiltrate -> Swap Mask -> Steal Artifact -> Escape.

## 2. Gameplay Objectives

The player must infiltrate a high-society estate and retrieve **three unique artifacts** without being captured:

1. **The Noble Crest** (Located in the Grand Hall)
2. **The Servant’s Ledger** (Located in the Servant Quarters)
3. **The Golden Rose** (Located in the Hedge Maze)

## 3. Core Mechanics

### 🎭 Identity & Mask System

Access to different zones depends on the active mask.

* **Crimson Mask (Noble):** Allowed in the Grand Hall. High suspicion in Quarters/Garden.
* **Azure Mask (Servant):** Allowed in the Servant Quarters. Suspicious in Grand Hall/Garden.
* **Emerald Mask (Gardener):** Allowed in the Hedge Maze. Suspicious in Hall/Quarters.
* **Swap Rule:** Swapping masks is only possible in designated **"Safe Zones"** (areas where no guard has line-of-sight).

### 👁️ Detection System

* **Vision Cones:** Guards have a 2D vision cone.
* **Suspicion Meter:** * **Matching Mask:** Meter fills very slowly (social blending).
* **Mismatched Mask:** Meter fills rapidly.
* **No Mask/Caught in Act:** Instant capture.
* **Capture Condition:** If suspicion reaches 100%, the player is caught.

## 4. Level Design (Zones)

| Zone | Primary Mask | Visual Aesthetic | Hazard Type |
| --- | --- | --- | --- |
| **Grand Hall** | Crimson | Luxury, Red Carpets, Gold | Open spaces, long vision lines. |
| **Servant Quarters** | Azure | Gritty, Blue/Grey, Cramped | Narrow corridors, tight corners. |
| **Hedge Maze** | Emerald | Nature, Green, Dark | Complex paths, many hiding spots. |

## 5. Technical Specifications

* **Resolution & Art:** 16x16 Pixel Art (Point Filter).
* **Camera:** Fixed top-down or slight follow-smoothing.
* **AI Architecture:** Finite State Machine (Patrol -> Suspect -> Investigate -> Chase -> Search).
* **Scene Management:** All zones are connected via a single master map or individual scene transitions (TBD based on performance).
