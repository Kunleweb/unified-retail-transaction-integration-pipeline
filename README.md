Retail Sales Integration Pipe


Retail Sales pipeline for ecommerce project 
--- we want to see how we can help an ecommerce company move toward cloud-based integration and analytics system. 
--- Each regional branch currently exports sales, customer and inventory data as csv reports that are manually uploaded into shared drive by branch managers. 
---


challnegs
- manual data upload ; inconsistent file naming conventions
- Data solos ; company wide perfomance analysis
- Limited visibility; stale data
- High error rate from copying an merging spreadsheets
- Lack of Central Repository(lake or warehouse) ; no single source of truth of executive descision making 
- 



Project Objectives

1) design and implement a cloud native data pipeline: that is from raw data generation into a cloud data warehouse 

2) Build a central data lake using s3 for all raw and semi-processed data with cversioning and folder hirarchy

3) Use Airbyte for automated integration: for configuring data sync jobs to run on a defined schedule 

4) Learn ELT concepts in practice; data is loaded before transformtion to optimise performance 

5) Develop Query validation skills; write sql queries to validate data consistency between the data lake and warehouse

Tech Stack:

- Python & Faker : used to generate and simulate retail data sucha as saales, customes and product records

- S3 
- Airbyte : for ELT 
-Motherduck: target warehouse 
- CSV/JSON: file formats 
-  Airbyte UI & SQL queries 



## How we will do it
----- Data Simulation-----
- Sales, products and customers dataset will be provided 
- Each dataset will contain 10,000+ records
- Upload datasets to AWS s3 using boto3 SDK
- define structured folder hierarchy
- Implement file versioning and lifecycle policies on the s3 bucket 

--- Airbyte Configuration ----
- Use airbyte cloud
- Add s3 as data source, define bucket name , region and path prefix
- add motherduck as the destination connector, authenticatinng via credentials. 
- configure the pipeline for daily data extraction
- Load into staging tables withing the warehouse 
- Maintain schema consistency 

