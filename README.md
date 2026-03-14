# Equipment Management Portal (EMP)
Architecture and documentation for a Power Platform Enterprise Asset Management (EAM-lite) system designed to replace spreadsheet-based equipment tracking.

## Overview

The Equipment Management Portal is an internal Enterprise Asset Management platform designed to replace fragmented spreadsheet tracking and establish a centralized operational data platform.

The system provides a single source of truth for equipment lifecycle management, featuring an expandable architecture designed to integrate with enterprise SQL data sources.

---

## Problem

Equipment data was historically tracked using independent regional spreadsheets, which created:

- inconsistent updates
- duplicate data entry
- limited operational visibility
- high administrative overhead

---

## Solution

A centralized Power Platform application built using:

- Dataverse for asset data modeling
- Power Apps for a model-driven administrative interface
- Dataflows for controlled ingestion of enterprise SQL data
- Power Automate for large-volume KPI calculation

---

## System Architecture

SQL Source Data (Read-Only Mirror) 
↓  
Dataflow Ingestion & Cleanup with Power Query   
↓  
Dataverse Asset Tables (Operational Overlays) 
↓  
Power Apps Model Driven Application  
↓  
Operations Users

---

## Key Features

- **Centralized Equipment Registry:** Normalized Dataverse tables for Equipment, Locations, Assignments, and Status Tracking.
- **Live Financial KPI Tracking:** Calculates Total Capital Cost (`cr6c3_totalcapcost`) and Total Net Book Value (`cr6c3_totalnbv`).
- **Large-Volume Automation Logic:** Utilizes custom Power Automate logic to bypass standard Dataverse 500-record retrieval limits, ensuring accurate metric calculations across large datasets.
- **Enterprise SQL Synchronization:** Architected to synchronize with live SQL databases while protecting source data integrity.
- **Role-Based Security:** Controlled access and regional operational views.
