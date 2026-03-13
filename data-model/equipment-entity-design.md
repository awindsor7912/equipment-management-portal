# Equipment Entity Design

## Purpose

The Equipment entity serves as the central record for asset lifecycle management.

## Core Fields

Equipment ID  
Asset Type  
VIN  
Region  
Site  
Operational Status  
Lifecycle Status  
Assigned Team  

## Related Entities

Maintenance Logs  
Assignment History  
Operational Notes  
Associated Invoices with Status

## Relationship Model

Equipment (1) → (Many) Maintenance Logs  
Equipment (1) → (Many) Assignment History
