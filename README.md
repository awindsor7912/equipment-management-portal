# equipment-management-portal
Architecture and documentation for a Power Platform asset management system designed to replace spreadsheet-based equipment tracking.

## Overview

The Equipment Management Portal is an internal asset management system designed to replace fragmented spreadsheet tracking and establish a centralized operational data platform.

The system provides a single source of truth for equipment lifecycle management while preparing the organization for enterprise-scale data integration.

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
- Power Apps for operational interface
- Dataflows for controlled ingestion of source data

---

## System Architecture

SQL Source Data  
↓  
Dataflow Ingestion & Cleanup with Power Query  
↓  
Dataverse Asset Tables  
↓  
Power Apps Model Driven Application  
↓  
Operations Users

---

## Key Features

- centralized equipment registry
- lifecycle status tracking
- role-based security access
- regional operational views

---

## Future Development

Planned enhancements include:

- SQL system integration
- automated lifecycle notifications
- operational dashboards
