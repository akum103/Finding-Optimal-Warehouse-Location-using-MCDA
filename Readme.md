🏢 Finding the Optimal Warehouse Location using MCDA

📌 Overview

This project presents a comprehensive optimization and simulation model to determine the best warehouse location for the company We-Doo, which specializes in last-mile delivery. It leverages the Travelling Salesman Problem (TSP) framework, integrates heuristic algorithms, and applies Multiple Criteria Decision Analysis (MCDA) to select the optimal warehouse among five candidates based on operational efficiency and cost.

🎯 Business Objective

Minimize last-mile delivery costs and improve delivery efficiency.

Determine the globally optimal warehouse location out of five options.

Consider multiple decision factors using MCDA such as operational cost, driver payment, and travel time.

📂 Dataset & City Simulation

Town Map: Randomly generated using a seed based on the student ID (x23123061) and saved in realdata.pickled.

100 Nodes: Representing locations in the town.

50 Customers: Each requiring daily deliveries.

5 Potential Warehouses:

4000,2320

4000,4000

1760,5120

4560,1200

6800,5120

⚙️ Methodology

🔧 Optimization Phase

Step 1: TSP with Greedy & Heuristic Algorithms

Implemented Greedy Algorithm (short-sighted, local best path)

Heuristic Search:

Rule 2: Reverse non-consecutive edges to reduce path length

Rule 3: Swap two edges if it shortens the route

Step 2: Evaluate All 5 Warehouses

Tested on subsets of 10, 20, and full 50 customers

Compared Optimal, Greedy, and Heuristic path lengths

Step 3: Monte Carlo Simulation

Ran multiple iterations

Selected warehouse with lowest average distance & cost: Warehouse at (4000, 2320)

🧪 Simulation Phase

Simulated delivery over 30 days with 0.15 probability of delivery per customer

Factored in realistic constraints:

Constraint

Value

Avg Speed

15/3.6 m/s

Prep Time

50 sec/parcel

Return Time

30 sec/parcel

Door Answer Time

40 sec

Missed Delivery Wait

60 sec

Op. Cost

0.00008 €/meter

Driver Pay

30 €/hour (min 60 €/day)

Day-End Procedure

10 min

📊 Simulation Result Summary

Warehouse

Avg Work Time

Mean Distance

Daily Cost

Driver Pay

4000,2320

102.96 min

20212.10 m

1.61 €

60 €

1760,5120

102.30 min

20027.50 m

1.60 €

60 €

✅ Best composite score

🧮 Multiple Criteria Decision Analysis (MCDA)

Criteria & Weights:

Criteria

Weight

Operational Cost

6

Minimum Distance

5

Driver Daily Payment

4

Std Deviation

3

Mean Distance

2

Avg Working Time

1

Applied MCDA to simulation results

Calculated Composite Score for each warehouse

Best Warehouse Based on MCDA: 1760, 5120

📈 Key Results & Findings

Heuristic search outperformed greedy in most warehouse simulations

Monte Carlo simulation supported initial results but MCDA gave a more balanced, multi-factorial decision

Warehouse (1760,5120) is the most optimal considering cost, distance, time, and driver efficiency

🛠️ Installation & Execution

1️⃣ Clone the Repository

git clone https://github.com/akum103/optimal-warehouse-mcda.git
cd optimal-warehouse-mcda

2️⃣ Install Dependencies

pip install pandas numpy matplotlib seaborn scikit-learn

3️⃣ Run the Notebook

jupyter notebook Ankit_combined.ipynb

📄 Project Report

📥 Download the full report

🚀 Future Improvements

Customer-level probability mapping for more personalized simulation

Incorporate weather data and terrain challenges

Use ensemble models (t-test, ANOVA, regression) alongside MCDA

Dynamic simulations with real-time delivery data

💡 Author: akum103🎯 GitHub Repo: optimal-warehouse-mcda

