# Multi-Objective Goal Programming for Production Planning (Case Study: André Meat Products)

This repository contains the mathematical modeling, optimization code, and data implementation of my **B.Sc. Thesis in Industrial Engineering**.

The project formulates and solves an aggregate production and supply chain planning problem using **Multi-Choice Weighted Goal Programming (GP)** implemented in **Python (Pyomo)** and solved with the **GLPK** branch-and-cut solver.

---

## 📌 Project Overview
- **Case Study:** André Protein & Meat Products Co.
- **Horizon:** 12 Weeks (Quarterly operational horizon)
- **Scope:** 28 Final Products, 17 Raw Materials, 3 Warehouse Types (Protein, Cold, Dry).
- **Core Methodology:** Mixed-Integer Linear Programming (MILP) & Goal Programming.

### 🎯 Objective Goals & Priorities:
1. **Goal 1 (Profit Target):** Achieving target quarterly operational profit (Minimizing negative deviation $d_p^-$).
2. **Goal 2 (Workforce Stability):** Minimizing workforce fluctuations, hiring, and firing ($d_{cw}^+$).
3. **Goal 3 (Customer Satisfaction):** Minimizing order backorders and delivery delays ($d_{id}^+$).

---

## ⚙️ Key Constraints Handled
- **Bill of Materials (BOM) & Inventory Dynamics:** Exact formulation consumption per product.
- **Perishability & Shelf-Life:** Protein raw material shelf-life (3 weeks) and finished products shelf-life (2 weeks).
- **Capacity Limits:** Specialized machine bottlenecks (Cutter, Cooking, Packaging lines), warehouse space limits, and supplier capacities.
- **Workforce Capacity:** Regular vs. Overtime hours with hire/fire bounds.

---

## 🛠️ Tech Stack & Requirements
- **Language:** Python 3.9+
- **Modeling Framework:** `Pyomo`
- **Solver:** `GLPK` (GNU Linear Programming Kit)
- **Reporting / Export:** `pandas`, `openpyxl`

---

## 📂 Repository Structure
```text
├── data.py                   # Model parameters, BOM, demand, costs, capacities
├── goal_programming_model.py # Pyomo MILP formulation and solver execution
├── requirements.txt          # Python dependencies
└── README.md                 # Project documentation
