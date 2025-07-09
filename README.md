
# 🚗 Dynamic Pricing for Urban Parking Lots

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
## 📚 Project Summary

This project simulates a **dynamic pricing engine for urban parking lots**, designed to optimize utilization based on real-time demand, competition, and environment conditions.

We used:
- 📈 **Historical & real-time data** from 14 parking spaces over 73 days
- 🧮 Implemented all models from scratch using **Python, Numpy, Pandas**
- 🚀 Streamed data & predictions using **Pathway**
- 📊 Visualized real-time pricing with **Bokeh**

---

## 💡 Models Implemented

- **Model 1:** Baseline linear pricing based on occupancy
- **Model 2:** Demand function using occupancy, queue, traffic, special days, vehicle type
- **Model 3:** Competitive pricing with geo-location proximity and competitor rates

---

## ⚙️ Execution

- 🔥 All code and simulations written & executed in **Google Colab**
- Real-time data ingestion & processing via **Pathway**
- Visualized dynamic price curves for each parking lot using **Bokeh**

---

## 📝 Deliverables

- 📔 Well-commented **Google Colab notebook**
- 📊 Real-time line plots comparing own vs competitor pricing
- 📝 Report explaining demand functions, assumptions, and pricing logic

---

## 🚀 Key Takeaways

- Showcased how **data-driven pricing** can reduce overcrowding & increase revenue
- Integrated economics + machine learning for practical smart-city use cases
- Built fully from scratch without high-level ML libraries


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

---

📬 **Connect with me:**  
[LinkedIn](https://linkedin.com/in/rahulkrishna-j) | [GitHub](https://github.com/JRK-007)

---
