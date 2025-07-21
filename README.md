# OPTIMIZATION-MODEL
COMPANY NAME: CODTECH IT SOLUTIONS

NAME: STALLAN N PHILOS

INTER ID:CT08DL10

DOMAIN: DATA SCIENCE

DURATION: 8 WEEKS

MENTOR: NEELA SANTHOSH

# 📦 Supply Chain Optimization – Internship Project (Task 4)

This repository contains a full data science project focused on solving a supply chain optimization problem using Linear Programming. This project was assigned during my internship at CODTECH and involves minimizing the total shipping cost for a distribution network of warehouses and customers.

---

## 🎯 Objective

To **minimize the total transportation cost** of delivering products from multiple warehouses to customer zones while meeting demand and respecting warehouse capacity constraints using optimization techniques.

---

## 🛒 Problem Statement

We are given:
- **3 warehouses** with different capacities
- **4 customer zones** with fixed product demand
- **Transportation cost** (per unit) between each warehouse and customer zone

The goal is to determine the **optimal quantity of goods** to transport from each warehouse to each customer zone **at the lowest cost**, while:
- Satisfying all customer demands
- Not exceeding warehouse capacities

---

## 📈 Dataset

A manually constructed dataset was used in the form of dictionaries and matrices:
- `costs`: Matrix containing unit cost from each warehouse to each customer zone
- `warehouse_supply`: List of total units available at each warehouse
- `customer_demand`: List of total units required by each customer zone

---

## 🔧 Tools & Libraries

- Python
- **PuLP** – for defining and solving the linear programming problem
- Pandas & NumPy – for data organization and manipulation
- Matplotlib & Seaborn – for visualizing transportation plans (optional)

---

## 🔄 Methodology

### 1. Define Decision Variables
Let `x[i][j]` be the quantity shipped from warehouse `i` to customer `j`.

### 2. Objective Function
Minimize:
Total Cost = Σ (x[i][j] * cost[i][j]) over all i and j

### 3. Constraints
- **Demand constraints**: For each customer zone, total goods received should meet demand.
- **Supply constraints**: For each warehouse, total goods shipped should not exceed capacity.

### 4. Solving
Used `pulp.LpProblem` to define the optimization problem and `pulp.PULP_CBC_CMD()` as the solver.

---

## ✅ Results

- **Optimal total cost**: ₹1125
- The solver successfully assigned goods from warehouses to customer zones while satisfying all constraints.

### 🗺️ Optimal Shipment Plan:

| From → To      | C1 | C2 | C3 | C4 |
|----------------|----|----|----|----|
| **W1**         | 0  | 0  | 25 | 5  |
| **W2**         | 15 | 25 | 5  | 5  |
| **W3**         | 15 | 0  | 0  | 15 |

---

## 📊 Visualization

A heatmap was used to visualize the optimal shipment matrix showing how much each warehouse sends to each customer zone.

---

## 📁 Project Structure

supply-chain-optimization/
│
├── supply_chain_optimization.ipynb
├── README.md
└── requirements.txt # (optional)


---

## 📥 How to Run

1. Clone this repository
2. Install dependencies:

pip install pulp pandas numpy matplotlib seaborn

3. Run the Jupyter notebook:
jupyter notebook supply_chain_optimization.ipynb

---

## 📌 Deliverables

- Problem formulation
- LP model using PuLP
- Optimal shipment plan
- Total cost analysis
- Visualizations (matrix/heatmap)

---

## 🧠 Key Learnings

- How to formulate and solve linear programming problems using Python
- Real-world application of optimization in supply chains
- Trade-offs between cost, capacity, and demand
- How to visualize optimization results meaningfully

#OUTPUT

![Image](https://github.com/user-attachments/assets/2141919e-5998-43db-893b-a51ff55e5304)




