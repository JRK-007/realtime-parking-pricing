🚗 Dynamic Pricing for Urban Parking Lots

> 📊 **Capstone Project | Summer Analytics 2025**  
> Hosted by Consulting & Analytics Club × Pathway

---

## 📚 Project Overview

Urban parking is a scarce and highly demanded resource. Static pricing often results in either overcrowding or underutilization of parking spaces.  
This project builds a **dynamic, data-driven pricing engine** to adjust parking fees in real-time based on:

- Occupancy levels
- Traffic congestion
- Queue length
- Special events or holidays
- Vehicle type
- Nearby competitor pricing

🎯 **Goal:** Improve utilization, enhance customer experience, and maximize revenue by implementing intelligent pricing models.

---

## 🛠️ Tech Stack Used

| Area             | Stack / Tools                                  |
|-------------------|-----------------------------------------------|
| Language          | Python (Google Colab environment)             |
| Data Processing   | Pandas, Numpy                                 |
| Streaming Engine  | Pathway                                       |
| Visualization     | Bokeh                                          |
| Geospatial Logic  | Haversine distance calculations               |
| Notebook / IDE    | Google Colab                                  |

---
## 📐 Formulas & Mathematical Models Used

This project implements a **multi-stage pricing engine** using mathematical models to dynamically adjust parking prices in real time.


### 🚀 1. Baseline Linear Pricing Model

A simple model to serve as a reference.  
Adjusts price based on how full the parking lot is.

Price_{t+1} = Price_t + α × (Occupancy / Capacity)


✅ **Where:**
- `Occupancy / Capacity` gives how full the lot is (0 to 1).
- `α` is a sensitivity factor.

🔎 **Purpose:**  
- Ensures prices automatically increase as the lot fills, preventing overloading.

---

### 🔥 2. Demand Function-Based Pricing Model

A more advanced approach using multiple features to calculate demand.

#### 📈 Demand Calculation

✅ **Components:**
- `Occupancy / Capacity`: Fraction filled.
- `QueueLength`: Normalized number of vehicles waiting.
- `Traffic`: Level of nearby congestion (higher traffic may discourage demand).
- `SpecialDay`: Binary flag (1 if holiday/event, else 0).
- `VehicleTypeWeight`: Multiplier by vehicle type (e.g., Car=1, Bike=0.6, Truck=1.5).

---

#### 💵 Price Adjustment Formula

After calculating the demand score, we adjust the price:

Demand = α × (Occupancy / Capacity)
+ β × QueueLength
- γ × Traffic
+ δ × SpecialDay
+ ε × VehicleTypeWeight


✅ **Constraints:**
- `NormalizedDemand` ensures demand stays between 0 and 1.
- Prices are typically **clipped between 0.5× and 2× BasePrice** to avoid wild swings.

---

### 💼 3. Competitive Pricing Model

Adds location intelligence by considering competitor prices.

#### 📊 Competitive Logic

- Calculate distance to nearby parking lots using **Haversine formula**.
- If:
  - Our lot is nearly full **and**
  - Nearby competitors are **cheaper**,
  
  then we **reduce our price** slightly or suggest rerouting vehicles.

- If:
  - Nearby lots are **more expensive**,
  
  we **increase our price**, staying under competitor levels to still be attractive.

---

## ✅ Summary

This multi-layered pricing approach combines:
- 📊 **Historical occupancy patterns** (baseline)
- 🧮 **Real-time multi-factor demand adjustments** (demand model)
- 🌐 **Market responsiveness** (competitive pricing with geospatial awareness)

to deliver a **smart, dynamic pricing system** for urban parking lots that balances demand, maximizes revenue, and reduces congestion.

---



---
## 🏗️ System Architecture & Workflow

| Step | Description |
|------|-------------|
| **1. Raw Data CSV** | Historical data of 14 parking lots over 73 days, sampled every 30 min. |
| **2. Pathway Ingestion** | Loaded CSV into Pathway, streamed row by row in time order. |
| **3. Feature Engineering** | Calculated occupancy rates, normalized queue, traffic flags, vehicle weights, competitor proximity. |
| **4. Pricing Engine** | Ran through 3 models:<br>• Baseline linear<br>• Demand-based<br>• Competitive pricing |
| **5. Pricing Predictions** | Produced real-time price adjustments based on current lot state and market. |
| **6. Pathway Emits** | Pathway continuously emitted new prices as data streamed. |
| **7. Bokeh Live Plots** | Visualized prices, occupancy, and competitor trends in real-time dashboards. |



## 📁 Repository Structure

| File / Folder              | Description                                      |
|-----------------------------|-------------------------------------------------|
| `DynamicPricing_Colab.ipynb` | Main Google Colab notebook with full pipeline   |
| `dataset.csv`               | Simulated historical + streaming data           |
| `README.md`                 | This project documentation file                 |
| `pricing_report.pdf`        | *(Optional)* Detailed project report if included|
| `visuals/`                  | Folder for Bokeh HTML exports or static images  |


📬 **Connect with me:**  
[LinkedIn](https://linkedin.com/in/rahulkrishna-j) | [GitHub](https://github.com/JRK-007)

---
