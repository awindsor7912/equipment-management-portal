# Data Model & Entity Design

## 📑 Core Entity: Equipment
The Equipment entity is the primary object for asset lifecycle management, featuring:
* **Standardized Unique IDs:** Normalizes data across legacy Excel sources to ensure clean relationships.
* **Relational Mapping:** 1:N relationships to **Maintenance Logs**, **Assignment History**, and **Associated Invoices**.

## 📊 Performance & Financial Metrics
The system tracks critical KPIs directly within the data layer:
* **Total Capital Cost:** `prefix_totalcapcost`
* **Total Net Book Value:** `prefix_totalnbv`
* **Active Equipment Count:** `prefix_totalactiveequipmentcount`

## 🛡️ Data Governance & Security
* **Overlay Soft-Close Rule:** When a source record is removed from the SQL mirror, the system triggers an "Out of Service" status rather than a hard delete, preserving all maintenance and historical logs.
* **Security Roles:**
    * **Regional Operations:** Edit permissions restricted to assets within assigned areas.
    * **Read Only:** View-only access to source tables, with edits permitted only in operational overlay fields.
