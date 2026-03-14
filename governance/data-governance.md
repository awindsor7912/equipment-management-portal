# Data Governance Strategy

## Objective

The system is designed to maintain high standards of operational data integrity and cleanly separate enterprise source data from operational modifications.

## Governance Principles

- No hard deletes of equipment records 
- Lifecycle status tracking for historical visibility  
- Controlled administrative permissions  

## Security Roles

Admin – full control of records  
Regional Operations – edit equipment status within assigned regions  
Read Only – view equipment data only (source tables), edits stored in overlay tables

## Overlay Soft-Close Rule

To protect the integrity of the integrated SQL data sources, the system employs an Overlay Soft-Close Rule. When a SQL-sourced base Equipment record is deleted (removed from SQL and therefore removed via Dataflow), it automatically triggers an "Out of Service" status rather than executing a hard delete. This preserves historical tracking and maintenance logs.
