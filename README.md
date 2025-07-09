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

## 🏗️ Project Architecture & Workflow

```mermaid
flowchart TD
    A[Raw Parking Data (CSV)] -->|Loaded in Pathway| B[Real-Time Data Streams]
    B --> C[Feature Engineering]
    C --> D[Pricing Models]
    D --> E[Baseline Model]
    D --> F[Demand Model]
    D --> G[Competitive Model]
    E --> H[Price Predictions]
    F --> H
    G --> H
    H --> I[Pathway Stream Emit]
    I --> J[Bokeh Real-Time Plots]
](https://github.com/JRK-007/realtime-parking-pricing)
