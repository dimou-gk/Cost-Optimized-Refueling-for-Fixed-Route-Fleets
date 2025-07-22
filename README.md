# Cost‑Optimized Refueling for Fixed‑Route Fleets 🚚⛽

A fuel-efficient route optimization system for logistics fleets. This project includes:

- **Fuel-consumption model**: Regression-based prediction of per-trip fuel usage.
- **Three optimization methods**:
  - **Greedy heuristic** – simple rule-based refueling.
  - **Exhaustive (Cartesian) search** – finds the exact optimal refueling plan by evaluating all station combinations.
  - **Multi‑Objective Linear Programming** – balances fuel use, travel time, and detour-related fuel via weighted LP.

---

## 📂 Repository Structure

| Notebook | Description |
|---------|-------------|
| `1_EDA_and_Cleaning.ipynb` | Import raw trip data, perform segmentation, and extract features (distance, elevation, time, etc.). |
| `2_Trip_Segmentation.ipynb` | Train and evaluate regression models—MAE & R²—for trip-level fuel prediction. |
| `3_Model_Training_and_Evaluation.ipynb` | Implement and compare Greedy and Exhaustive refueling strategies using both predicted and actual fuel data. |
| `4_Fuel_Consumption_Optimization.ipynb` | Formulate & solve the weighted LP. Compare results, simulate routes, and analyze performance. |


📸 Pipeline Overview:

![Pipeline Diagram](docs/pipeline_diagram.png)

## 🚀 Quick Start
1. Since the project is in notebooks no requirements.txt is required.
2. We need however a file titled "emisia-sample_dataset_for_msc.csv" for the 1st notebook "1_EDA_and_Cleaning.ipynb" to work. The name can be altered if you change the first cell of the prementioned notebook. The file needs to have the at least the following columns:
| Feature | Description |
| datetime | Date(time)
|	mileage_km |
|	speed_km_h |
|	elevation_m |
|	fuel_volume_lit |
|	gross_vehicle_weight_kg |
