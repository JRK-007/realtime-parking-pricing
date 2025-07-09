[# 🚗 Dynamic Pricing for Urban Parking Lots

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


.
├── DynamicPricing_Colab.ipynb   # Main Google Colab notebook
├── dataset.csv                  # Parking time-series data
├── visuals/                     # Bokeh HTML exports or screenshots
├── pricing_report.pdf           # (Optional) Detailed assumptions & plots
└── README.md                    # This documentation


📬 **Connect with me:**  
[LinkedIn](https://linkedin.com/in/rahulkrishna-j) | [GitHub](https://github.com/JRK-007)

---
