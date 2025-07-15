# Boundary Value Analysis – Week 3

## Task 1.1 – BVA Table for Speed Evaluation

| EP          | min-1 | min | max | max+1 |
|-------------|-------|-----|-----|--------|
| EP1 – NOTHING HAPPENS | -     | 0   | 90  | 91     |
| EP2 – WARNING         | 90    | 91  | 110 | 111    |
| EP3 – FINE            | 110   | 111 | 130 | 131    |
| EP4 – LICENSE REVOKED | 130   | 131 | -   | -      |

---

## Task 1.2 – Values that Cover All BVA Boundaries

| EP               | min-1 | min | max | max+1 |
|------------------|-------|-----|-----|--------|
| EP1 – Icy Cool   | 9     | 10  | 10  | 11     |
| EP2 – Chilled Out| 10    | 11  | 15  | 16     |
| EP3 – Cool Man   | 15    | 16  | 19  | 20     |
| EP4 – Too Warm   | 19    | 20  | 22  | 23     |
| EP5 – Hot & Sweaty | 22  | 23  | -   | -      |

### ✅ Values that cover boundaries:  
10, 11, 15, 16, 19, 20, 22, 23

---

## Task 1.3 – Sample Test Cases for BVA (2-Point Method)

| Test ID | Speed Value (km/h) | Expected Action              |
|---------|--------------------|------------------------------|
| T1      | 50                 | Nothing will happen          |
| T2      | 51                 | You will be warned           |
| T3      | 55                 | You will be warned           |
| T4      | 56                 | You will be fined            |
| T5      | 60                 | You will be fined            |
| T6      | 61                 | License will be suspended    |

---

**Note:** This task applies 2-point Boundary Value Analysis (BVA) to identify key threshold values that divide equivalence partitions. It verifies correct behavior at critical limits.
