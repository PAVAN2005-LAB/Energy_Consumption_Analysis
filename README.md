# 📘 Building-Level Electricity Access and Demand Analysis

**Authors:** Pavan Kumar Yadav  
**Institution:** Government Engineering College, Dahod  

---

## 📌 Introduction

Buildings represent a major portion of global energy consumption. This project focuses on analyzing **building-level electricity access and demand** to predict monthly electricity usage and classify buildings based on consumption levels. Such analysis plays a crucial role in improving **operational efficiency**, **energy planning**, and **sustainability**.

The integration of **AI-based systems** for analyzing real-time occupancy and environmental data can significantly reduce energy waste and operational costs. This approach mirrors successful implementations in smart city and energy optimization initiatives worldwide.

---

## 📊 Dataset Description

This study utilizes high-resolution building-scale energy access and demand datasets provided by the **International Energy Agency (IEA)**.

### 🔑 Key Features

- **Building Area:** Footprint size of each building (in square meters)  
- **Electricity Access:** Percentage of electricity accessibility per building  
- **Nearby Building Density:** Number of buildings within a 1 km radius  
- **Target (Regression):**  
  - `cons (kWh/month)` – Monthly electricity consumption  
- **Derived Target (Classification):**  
  - Energy Consumption Level: **Low / Medium / High**

### 📂 Data Source

- **IEA Building-Level Electricity Access and Demand Model for Sub-Saharan Africa**
- Files used:
  - `471928_geoms.csv`
  - `466151_geoms.csv`

> **Note:**  
> Although the datasets are in CSV format, they contain a `geometry` column with embedded **GeoJSON spatial data**, which is used to identify building footprints and spatial relationships.

---

## 🛠️ Methodology & Performance

The project follows a complete **machine learning pipeline**:

1. Data Cleaning & Preprocessing  
2. Feature Engineering  
3. Regression Modeling  
4. Ordinal Classification  

### 🔍 Models Used

- Linear Regression  
- Random Forest  
- XGBoost  

### 📈 Key Findings

- **Best Model:** XGBoost  
- **Classification Accuracy:** ~**98.9%**  
- **Model Robustness:**  
  - Both **Random Forest** and **XGBoost** achieved high **precision**, **recall**, and **F1-scores** across all energy consumption categories.  
- **Ordinal Analysis:**  
  - Energy consumption categories are **ordinal in nature** (Low < Medium < High).  
  - Evaluation metrics and modeling strategies were aligned with this ordered structure to improve **statistical stability** and interpretability.

---

## 📜 License & Attribution

This dataset is released under the **Open Database License (ODbL), Version 1.0**.

**Attribution:**  
© International Energy Agency (IEA).  
Data sourced from the *Building-level electricity access and demand model*.

---

## 💻 Setup & Execution

This project is designed for execution in a **Google Colab** environment.

### ⚙️ Steps to Run

1. Upload the IEA CSV files to the Colab runtime:
   - `471928_geoms.csv`
   - `466151_geoms.csv`

2. Install / import required libraries:
   ```python
   import pandas as pd
   import numpy as np
   import matplotlib.pyplot as plt
   import seaborn as sns
   from sklearn.model_selection import train_test_split
  
   from sklearn.metrics import classification_report
   from sklearn.ensemble import RandomForestClassifier
3. Run the preprocessing, regression, and classification notebooks/scripts.

### ✅ Conclusion

This project demonstrates how building-level data combined with machine learning can effectively predict electricity demand and classify consumption patterns.
The results highlight the potential of AI-driven energy analytics for smarter urban planning, energy efficiency, and sustainable infrastructure development.
