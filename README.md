# ADF_Project1

This repository contains an Azure Data Factory (ADF) project that demonstrates end-to-end data movement, transformation, and analytics using Azure cloud services. The project showcases a practical enterprise-style data engineering flow with ingestion from multiple sources, cleaning and transformation logic, and a curated reporting layer for analysis.

## Overview

The project is designed to handle multiple data sources and transform them into a structured, analytics-ready format. It includes:

- On-premises file ingestion
- REST API data ingestion
- Azure SQL to Data Lake ingestion
- Data transformation using Mapping Data Flows
- Delta-based storage in the silver and gold layers
- Business-ready reporting for downstream analysis

## Architecture

This solution follows a medallion-style data architecture model:

- Raw / Ingestion Layer: data is brought in from external sources
- Silver Layer: data is cleaned, standardized, and enriched
- Gold Layer: aggregated business-ready datasets are prepared for analytics and reporting

## Key Features

- Multi-source ingestion:
  - On-prem file system
  - REST API
  - Azure SQL Database
- Parameterized and reusable ADF pipelines
- ForEach looping for batch processing of multiple files
- Incremental loading using watermark logic
- Data transformation using Mapping Data Flows
- Delta format storage for analytics processing
- Business-level aggregated views for reporting
- Data quality and normalization workflows

## Project Components

### Pipelines
The repository contains pipelines for:
- SQL to Data Lake ingestion
- On-prem file ingestion
- API ingestion
- Parent orchestration pipeline
- Data transformation and serving flow

### Datasets
The project includes dataset definitions for:
- Azure SQL source data
- On-prem files
- API source and sink
- Data Lake storage
- Lookup and watermark files

### Data Flows
The repository includes Mapping Data Flows for:
- Data cleaning
- Derived column generation
- Data selection and filtering
- Business logic transformation
- Aggregation and ranking
- Gold-layer business reporting

### Linked Services
The project uses linked services for:
- Azure SQL Database
- Azure Data Lake Storage
- On-prem file connectivity
- GitHub/API-based data retrieval

## Data Processing Flow

1. Data is extracted from external sources such as on-prem files, APIs, and Azure SQL.
2. Data is moved into the storage layer for ingestion.
3. Transformation logic is applied using ADF Mapping Data Flows.
4. Standardized and enriched datasets are stored in a Silver layer.
5. Business aggregations and ranking logic generate Gold-layer insight data.

## Business Use Case

This project demonstrates how to build a simple but realistic data engineering solution that supports:
- Analytics readiness
- Reporting
- Data integration
- Data lake modernization
- Scalable ETL pipeline orchestration

## Tools and Technologies

- Azure Data Factory
- Azure Data Lake Storage
- Azure SQL Database
- Mapping Data Flows
- Delta format
- JSON and Parquet data processing
- Parameterized pipeline orchestration

## Repository Structure

```text
ADF_Project1/
├── pipeline/
├── dataflow/
├── dataset/
├── linkedService/
├── integrationRuntime/
├── README.md
├── publish_config.json
