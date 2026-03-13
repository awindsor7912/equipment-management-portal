# System Architecture

## Overview

The Equipment Management Portal is designed as a centralized operational data platform built using Microsoft Power Platform technologies. The system integrates enterprise data sources while providing a controlled operational interface for asset management.

## Architecture Layers

The system is composed of four primary layers:

1. Data Source Layer
2. Data Integration Layer
3. Operational Data Layer
4. Application Interface Layer

## Data Source Layer

Enterprise equipment data originates from SQL-based operational systems.

These systems remain the authoritative system of record.

## Data Integration Layer

Dataflows are used to ingest equipment data into Dataverse in a controlled and repeatable process.

This ensures:
- consistent data refresh cycles
- validation of source data
- separation of source data from operational edits

## Operational Data Layer

Dataverse stores structured equipment records and supports relational data modeling.

This layer manages:

- equipment registry
- lifecycle status tracking
- assignment history
- maintenance notes

## Application Interface Layer

A model-driven Power App provides operational users with a structured interface for interacting with equipment records.

Capabilities include:

- role-based access
- filtered regional views
- search functionality
- lifecycle state updates
- invoice tracking
