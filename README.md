# Azure-Healthcare-end-to-end-project

Project Overview
The project utilizes Azure cloud services to create a robust data pipeline that processes healthcare data through various stages:
Data Ingestion: From multiple sources including EMR systems, claims data, and medical coding APIs.
Data Processing: Implementing a medallion architecture (Bronze, Silver, Gold layers) for data refinement.
Data Storage: Utilizing Azure Data Lake Storage Gen2 for scalable data storage.
Data Transformation: Applying cleaning, Common Data Model (CDM) implementation, and Slowly Changing Dimension (SCD) Type 2 for historical tracking.
Data Analysis: Creating fact and dimension tables for business intelligence and reporting.
Key Components
Azure Data Factory (ADF): For orchestrating data movement and transformation processes.
Azure Databricks: For data processing and transformation tasks.
Azure SQL Database: Serves as the source for EMR data.
Azure Key Vault: For secure storage of credentials and secrets.
Azure Storage Account: For storing raw files, parquet files, and configuration data.
Data Sources
EMR Data (Azure SQL DB)
Claims Data (Flat files)
National Provider Identifier (NPI) Data (Public API)
International Classification of Diseases (ICD) Data (API)
Current Procedural Terminology (CPT) Codes (Flat files)
Project Structure
/configs: Contains configuration files for data loading and processing.
/scripts: Databricks notebooks and scripts for data transformation.
/adf_pipelines: JSON definitions of Azure Data Factory pipelines.
/docs: Additional documentation and data dictionaries.
Key Features
Metadata-driven pipeline for flexible data ingestion.
Implementation of data quality checks and quarantine process.
SCD Type 2 implementation for tracking historical changes.
Parallel processing in ADF for improved performance.
Integration with Azure Key Vault for enhanced security.