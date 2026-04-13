# Deloitte-Australia-Data-Analytics-Job-Simulation
# 🏭 Factory Downtime Analysis using Tableau

## 🔍 Overview

This project analyzes machine telemetry data collected from multiple factories to identify operational inefficiencies and downtime patterns.

The dataset consists of real-time machine status logs collected every 10 minutes across 4 global factory locations over a one-month period (May 2021). The objective is to identify which factory experienced the highest downtime and determine the machines contributing most to failures.

---

## 🎯 Business Problem

The client, Daikibo, aimed to answer two key operational questions:

1. Which factory experienced the highest machine downtime?
2. Which machine types contributed most to downtime in that factory?

---

## 📊 Dataset Details

* Data source: Telemetry JSON dataset
* Frequency: Every 10 minutes per machine
* Duration: 1 month (May 2021)
* Factories:

  * Tokyo (Meiyo)
  * Osaka (Seiko)
  * Berlin
  * Shenzhen
* Machine types: 9 different device categories (CNC, Laser, Conveyor, etc.)

Each record includes:

* Machine ID & type
* Timestamp
* Location hierarchy (country → factory → section)
* Machine status (healthy/unhealthy)
* Temperature readings 

---

## ⚙️ Methodology

### 📌 Data Preparation

* Imported nested JSON data into Tableau
* Flattened hierarchical schema (location & data fields)
* Verified all schema levels during import

### 📌 Feature Engineering

* Created a calculated field:

  * **Unhealthy = 10 minutes downtime per event**
* Converted machine failures into measurable downtime

### 📊 Analysis Performed

1. **Downtime per Factory**

   * Aggregated total unhealthy time across all factories

2. **Downtime per Device Type**

   * Identified machine categories contributing to failures

3. **Interactive Dashboard**

   * Factory-level filtering applied
   * Drill-down into device-level downtime

---

## 📈 Key Findings

### 🏭 Factory Performance

* One factory showed **significantly higher downtime (~1000+ minutes)** compared to others
* Another factory followed with **~800+ minutes downtime**
* Remaining factories had minimal downtime (~200 minutes or less)

👉 Indicates uneven operational efficiency across locations

---

### ⚙️ Machine-Level Insights

* A specific device category (e.g., Laser/CNC type machines) contributed **majority of downtime (~1000 minutes)**
* Other machine types showed negligible or zero downtime

👉 Suggests:

* Critical failure point in specific machinery
* Possible maintenance or design issue

---

### 🌍 Operational Insight

* Downtime is **not uniformly distributed**
* Failures are concentrated:

  * In specific factories
  * Within specific machine types

---

## 📊 Dashboard Features

* Factory-wise downtime comparison
* Device-level breakdown
* Interactive filtering (factory → machine level)
* Clear visualization of operational bottlenecks

---

## 💡 Business Impact

* Helps prioritize maintenance for high-risk machines
* Enables factory-level performance benchmarking
* Supports predictive maintenance strategies
* Reduces operational downtime and cost

---

## 🛠 Tools Used

* Tableau (Dashboard & Visualization)
* JSON Data Processing

---

## 📁 Files Included

* Telemetry dataset (JSON)
* Tableau dashboard file (.twb)
* Dashboard screenshots

---

## 📌 Conclusion

This project demonstrates how machine telemetry data can be leveraged to identify critical operational issues. By analyzing downtime patterns across factories and devices, organizations can take targeted actions to improve efficiency and reduce machine failures.

---

## 🚀 Key Skills Demonstrated

* Data Cleaning & Transformation (JSON)
* Data Visualization (Tableau)
* Business Problem Solving
* KPI Creation (Downtime Analysis)
* Dashboard Design

