# Automation Logic & Metric Calculation

## Overview

To provide accurate, real-time financial tracking and dashboard reporting, the Equipment Management Portal utilizes Power Automate to handle complex metric recalculations.

## Overcoming Platform Constraints

By default, standard Dataverse list record actions are often limited to a 500-row retrieval threshold. When tracking regional or enterprise-wide equipment fleets, this limitation results in highly inaccurate operational totals. 

To solve this, custom Power Automate flows were engineered to bypass the standard 500-line limitation, sequentially grabbing large-volume dataset arrays to calculate accurate, system-wide metrics. 

## Key Automated Calculations

- **KPI Summary Recalculator:** Updates active equipment and total asset record counts across the enterprise dataset. 
- **Currency Value Calculator:** Pulls active financial values to calculate the total `prefix_totalcapcost` and `prefix_totalnbv` metrics for executive dashboard reporting.
