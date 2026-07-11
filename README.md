## 📊 Product Management Dashboard (SAP Datasphere & Power BI)

### 🚀 Project Overview

This project presents the end-to-end development of an enterprise-grade Product Management Dashboard, completed as an **industry-based Final Year Project in collaboration with PPG Coatings (Malaysia) Sdn. Bhd**. It was built to solve the challenges of fragmented reporting logic and a heavy reliance on manual Excel uploads for data integration. By establishing a governed, centralized analytical layer, the solution extracts and processes operational data directly from the enterprise system to provide actionable insights for product, inventory, sourcing, and production analysis.

<p align="center">
  <img src="img/System Overview.png" alt="System Architecture Diagram" width="500"/>
</p>

### 🎯 Business Objectives

The primary goal is to provide consistent, traceable, and centralized reporting for business stakeholders. 

#### Key Deliverables:
* **Data Integration:** Combine enterprise data from core SAP tables (e.g., MARC, MARA, MBEW, BOM, STPO).
* **Centralized Business Logic:** Perform data cleansing, categorization, and rule application within a governed semantic layer.
* **Seamless Connectivity:** Bridge the data warehouse with reporting tools using ODBC and HANA Database connectors.
* **Interactive Analytics:** Deliver user-friendly dashboards for stock coverage, supply network mapping, and product overview.

### 🧰 Tech Stack

| Technology | Purpose |
| :--- | :--- |
| **SAP HANA** | Primary enterprise data source (Operational Data). |
| **SAP Datasphere** | Data integration, transformation, and semantic modeling layer. |
| **SQL** | Complex business rule derivations and calculated columns. |
| **Microsoft Power BI** | Front-end interactive dashboard and visualization. |
| **ODBC / DirectQuery** | Data connectivity for optimized consumption. |

### 🏗️ System Architecture & Data Modeling

The data engineering pipeline leverages a strict layered modeling architecture in SAP Datasphere to ensure data integrity and traceability:

1.  **Inbound Layer:** Near-source replication of raw SAP tables.
2.  **Harmonization Layer:** Standardization of fields, filtering, and preparation of reusable views.
3.  **Propagation Layer:** Complex joins and business derivations.
4.  **Fact Layer:** Definition of analytical facts and core measures like *Total Inventory Value* and *Safety Stock Value*.
5.  **Reporting Layer:** The final consumption-ready analytic model exposed to Power BI.

### 📈 Dashboard Features

The Power BI consumption layer is divided into three highly interactive pages:

* 📌 **Product Management Overview:** A high-level summary of all products across plants, featuring dynamic filtering by region, plant, and material group.
* 📦 **Stock Coverage Ratio:** Visualizes inventory sufficiency against safety stock, featuring KPIs for Total Inventory Value and stock distribution by planning strategy.
* 🌍 **Supply Network Map:** Traces the flow of materials from their final source to destination plants, supporting supply chain analysis and batch size planning.

---
*Developed as part of a Bachelor of Computer Science (Data Engineering) Final Year Project.*
