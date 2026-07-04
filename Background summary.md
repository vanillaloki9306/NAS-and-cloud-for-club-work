# Project Backstory 6/2026

Plan as of July 1st 2026, prior to building but after original testing.

---

## Timeline and Budget

The project began on **June 1st, 2026** with the initial draft of the parts list. Updates were made to optimize the structure of the NAS.

* **Design Iterations:** 9 versions drafted between June 1st and June 24th.
* **Parts Finalization:** June 26th, 2026.
* **Sourcing Strategy:** Capitalized on being physically present in Mainland China to source components directly from the local market (primarily ordered off JD) at a significantly lower price point than the US.

### Budget Variance Analysis
| Milestone | Date | Estimated Cost | Notes |
| :--- | :--- | :--- | :--- |
| **First Complete Estimate** | June 20, 2026 | \$995 | Baseline target configuration. |
| **Final Sourcing Total** | June 26, 2026 | \$1,532 | Adjusted for hardware upgrades and market availability. |

---

## Bench Test

Quickly conducted a test to ensure hardware functionality before shipping the components internationally. 

> **Observations**
> The prototype test bench ran for **2 hours** and exposed major component flaws, leading to a redesign.

### 1. Motherboard CMOS Failure (Maxsun B760I D4 Terminator)
* **Symptom:** System failed to save BIOS settings, reverting to factory defaults upon every power cycle.
* **Diagnosis:** Suspected a dead CMOS battery. Disassembled the motherboard's I/O armor to expose the CMOS wiring. 
* **Result:** Multimeter probe verified **0.0V** across the battery leads.
* **Conclusion:** The CMOS battery was wrapped in a proprietary yellow enclosure and permanently glued to the side of the integrated Wi-Fi module, making replacement impossible without risking damage and voiding warranty.

### 2. Clearance Conflict (Thermalright AXP120-X67)
* **Symptom:** Physical obstruction during CPU cooler installation.
* **Diagnosis:** The low-profile cooler could not be fully torqued down due to clearance conflicts with the RAM heatspreaders.
* **Result:** The cooler maintained safe thermal thresholds during brief BIOS navigation, but physical stress on the DIMM slots made it unviable for the build.

### 3. Expansion Card Verification (Mellanox ConnectX-3)
* **Symptom:** The PCIe device list was unavailable/unreadable within the Maxsun BIOS interface.
* **Diagnosis:** Likely a firmware limitation within the Maxsun BIOS environment.
* **Result:** Inspection confirmed the network card's heatsink was warm to the touch, indicating the card was successfully pulling power from the PCIe slot.

---

## Current Status as of July 2nd 2026

Based on the information gathered during the bench test, the following revisions were made before leaving China:

* **Returned:** `Maxsun B760I D4 Terminator` *Reason:* Defective, non-replaceable CMOS battery; restrictive BIOS firmware.
* **Returned:** `Thermalright AXP120-X67` *Reason:* Insufficient physical clearance for chosen RAM modules.

### Current Milestone: Form Factor Arrived in US
All verified functional components (including the Mellanox ConnectX-3 10GbE card) have been safely packed, transported, and unboxed in California. The replacement motherboard and a larger, high-clearance CPU cooler are arrived.
