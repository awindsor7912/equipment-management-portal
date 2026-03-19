# System Architecture & Integration Logic

## 🏗️ Layered Architecture
The system is built on a four-layer model to ensure a clean separation between source data and operational activity:

1. **Data Source Layer:** Authoritative equipment data originates from enterprise SQL-based systems.
2. **Data Integration Layer:** Utilizes Dataflows to ingest SQL data into Dataverse as a read-only mirror, protecting the integrity of the original system of record.
3. **Operational Data Layer:** Dataverse stores structured records and manages "Operational Overlays"—fields where users can add notes and updates without impacting the source data.
4. **Application Interface Layer:** A model-driven Power App provides a security-trimmed interface for regional filtered views and lifecycle management.

## ⚙️ Advanced Automation Logic
To provide accurate reporting, the system utilizes **Power Automate** to overcome standard platform constraints:
* **Bypassing Retrieval Thresholds:** Standard Dataverse actions often limit record retrieval to 500 rows. EMP uses custom-engineered logic to sequentially process large-volume datasets, ensuring fleet-wide financial totals are accurate.
* **Metric Recalculation:** Automated flows update the `prefix_totalcapcost` and `prefix_totalnbv` fields across the enterprise whenever asset records are modified.
