# Data Engineering Project using Apache Spark, Azure Databricks, Data Build Tool (DBT) using Azure as our cloud provider.

## 🎯 Project Objective

This project aims to create a robust data pipeline using Azure services and Databricks to process and transform data from an SQL database into a structured format suitable for advanced analytics and reporting.

## 🛠️ Project Components

1. **Resource Group**: Contains various services including:
   - **Azure Data Factory**: For Extract Transform Load (ETL) Pipeline.
   - **SQL Database**: Source data.
   - **Azure Data Lake Storage (Gen 2)**: With three containers:
     - **Bronze Container**: Stores raw data as received from source systems.
     - **Silver Container**: Contains cleansed, deduplicated, and validated data in a consistent format.
     - **Gold Container**: Holds the most refined data, ready for advanced analytics, reporting, or feeding into machine learning models.
   - **Databricks**: For processing and transforming massive quantities of data.
  
## 📋 Project Steps

1. **Pipeline Design**:
   - Created a new pipeline in Azure Data Factory to extract AdventureWorksLT tables from the SQL database and load them into the Bronze container in Azure Data Lake Storage (Gen 2) as Parquet files.
   
2. **Data Loading**:
   - Linked Azure Data Lake Storage (Gen 2) to a Databricks notebook to load the Parquet files into the database.
   
3. **Data Transformation**:
   - Utilized the Data Build Tool (DBT) framework to ensure reliable data transformation and dimensional modeling for the reporting team.

## 🚀 Getting Started

### Prerequisites

- Azure subscription
- Python 3.10 or higher
- Databricks CLI
- DBT (Data Build Tool)

### Installation

1. Install DBT for Databricks:
   
   ```sh
   pip install dbt-databricks
   ```
2. Install Databricks CLI:
   
   ```sh
   pip install databricks-cli
   ```

3. Configure Databricks CLI:
   
   ```sh
   databricks configure --token
   ```
   - Enter your Databricks Host
   - Enter your Databricks Token
     
4. Initialize DBT project:

   ```sh
   dbt init
   ```
  - Enter a name for your project
  - Select Databricks as the database
  - Enter your Databricks host (e.g., yourorg.databricks.com)
  - Enter the HTTP Path
  - Choose to use an access token
  - Choose not to use Unity Catalog
  - Enter the schema name

5. Navigate to your project directory:

   ```sh
   cd <name_of_your_project>
   ```

6. Debug DBT setup:

   ```sh
   dbt debug
   ```

## 📝 Notes
- Ensure all Azure services are properly configured and permissions are set.
- Regularly monitor the pipeline for any failures or data inconsistencies.
- Use DBT for reliable and repeatable data transformations.

## 📧 Contact
For any questions, please contact me at khaledfarghaly011@gmail.com.
