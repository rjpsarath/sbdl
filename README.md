Spark Bulk Data Load

Project Background:
We have an Master Data Management Platform. 

-> Master data is designed to synchronize master data within applications across the enterprise. 
Banking Systems: Clients, Employees, Products, Facilities

An MDM platform does not record transactions. 

-> Master Data shares data with other systems.
Systems: Customer Intelligence, Customer Churn, Fraud Detection, Compliance & Risk

Scope of Work: Bring transformed data from MDM Platform to Kafka cluster for further consumption by Downstream systems.

Data Details: 1. 500+ entities
	2. MDM Platform exports entities to Hadoop daily
	3. Full data load everyday
	4. Maintain 7 days of export
	5. Data export is available in hive tables partitioned by load_date.
	6. We can take data from any Load_date in hive table for building pipeline.

Hive Level Scope: 1. Data is already available in hive tables.
	2. Need to develop spark application that does the following:
	A. Take load date as an input argument
	B. Read data from hive tables for given load date.
	C. Process and prepare data according to the requirements
	D. Sends prepared data to Kafka topics
	3. Follow best practices, such as modular design, code reuse, unit testing, etc.
	4. Estimate compute requirements such as number of executors, CPU cores, memory, etc.
	5. Work with DevOps team to define a CI/CD pipeline.

So, need to create a json file at the end.

GIT Branches
Master: Production Environment
Release: QA testing environment
Dev: Development Environment


