# 📊 Enterprise Product Management Dashboard

<p align="center">
  <img src="img/system-architecture.png" alt="System Architecture Diagram" width="700"/>
</p>

## 🚀 Project Overview

[cite_start]This project presents the end-to-end development of an enterprise-grade Product Management Dashboard[cite: 1502]. [cite_start]It was built to solve the challenge of fragmented reporting logic by establishing a governed, centralized analytical layer[cite: 1567]. [cite_start]The solution extracts and processes operational data to provide actionable insights for product, inventory, sourcing, and production analysis[cite: 1329, 1503].

## 🎯 Business Objectives

[cite_start]The primary goal is to provide consistent, traceable, and centralized reporting for business stakeholders[cite: 1503]. 

### Key Deliverables:
* [cite_start]**Data Integration:** Combine enterprise data from core SAP tables (e.g., MARC, MARA, MBEW, BOM, STPO)[cite: 1338].
* [cite_start]**Centralized Business Logic:** Perform data cleansing, categorization, and rule application within a governed semantic layer[cite: 1339].
* [cite_start]**Seamless Connectivity:** Bridge the data warehouse with reporting tools using ODBC and HANA Database connectors[cite: 1340].
* [cite_start]**Interactive Analytics:** Deliver user-friendly dashboards for stock coverage, supply network mapping, and product overview[cite: 1333, 1344].

## 🧰 Tech Stack

| Technology | Purpose |
| :--- | :--- |
| **SAP HANA** | [cite_start]Primary enterprise data source (Operational Data)[cite: 1720]. |
| **SAP Datasphere** | [cite_start]Data integration, transformation, and semantic modeling layer[cite: 1720]. |
| **SQL** | [cite_start]Complex business rule derivations and calculated columns[cite: 2347]. |
| **Microsoft Power BI** | [cite_start]Front-end interactive dashboard and visualization[cite: 1720]. |
| **ODBC / DirectQuery** | [cite_start]Data connectivity for optimized consumption[cite: 1720]. |

## 🏗️ System Architecture & Data Modeling

[cite_start]The data engineering pipeline leverages a strict layered modeling architecture in SAP Datasphere to ensure data integrity and traceability[cite: 1890, 1891]:

1.  [cite_start]**Inbound Layer:** Near-source replication of raw SAP tables[cite: 1920].
2.  [cite_start]**Harmonization Layer:** Standardization of fields, filtering, and preparation of reusable views[cite: 1921].
3.  [cite_start]**Propagation Layer:** Complex joins and business derivations (e.g., final source determination via SPK logic, MTS/MWO/DWO classifications)[cite: 1922, 2180, 2421].
4.  [cite_start]**Fact Layer:** Definition of analytical facts and core measures like *Total Inventory Value* and *Safety Stock Value*[cite: 1924, 2218].
5.  [cite_start]**Reporting Layer:** The final consumption-ready analytic model exposed to Power BI[cite: 1926].

## 📈 Dashboard Features

[cite_start]The Power BI consumption layer is divided into three highly interactive pages[cite: 2458]:

* [cite_start]📌 **Product Management Overview:** A high-level summary of all products across plants, featuring dynamic filtering by region, plant, and material group[cite: 2463, 2464].
* [cite_start]📦 **Stock Coverage Ratio:** Visualizes inventory sufficiency against safety stock, featuring KPIs for Total Inventory Value and stock distribution by planning strategy[cite: 2472, 2473].
* [cite_start]🌍 **Supply Network Map:** Traces the flow of materials from their final source to destination plants, supporting supply chain analysis and batch size planning[cite: 2482, 2484].

---
[cite_start]*Developed as part of a Bachelor of Computer Science (Data Engineering) Final Year Project.* [cite: 1473, 1474]
