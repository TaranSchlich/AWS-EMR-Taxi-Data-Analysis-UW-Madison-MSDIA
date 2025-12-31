# AWS EMR Taxi Data Analysis  
Big Data Processing with Amazon EMR

**By: Taran Schlichtmann**

**Date: 12/01/2025**

Demonstrates the use of Amazon EMR (Elastic MapReduce) and PySpark to process and analyze large-scale taxi ride data for New York City. The dataset contains 2.4 million rows, with each row representing an individual taxi ride. The goal was to compute daily metrics including average trip distance, average ride cost, total trip costs, and total passenger counts.

---

## Project Overview

The objective of this assignment was to:

- Upload raw taxi ride data to Amazon S3  
- Configure and launch an EMR cluster running Spark  
- Execute a PySpark script to process millions of records  
- Generate daily aggregated metrics  
- Export the results to a CSV file for analysis  

This workflow mirrors real-world big data engineering tasks used in analytics and data processing pipelines.

---

## AWS Services Utilized

### Amazon S3
- Created an S3 bucket in **N. Virginia** (`taxi-data-###`)
- Uploaded:
  - Taxi rides dataset (89MB)
  - PySpark analysis script
- Created an `/output` folder for storing EMR results
- Enabled logging to an S3 `/logs` folder

### Amazon EMR
- Created a cluster named **My EMR Assignment Cluster**
- Region: **N. Virginia**
- Application: **Spark**
- Instance type: **m4.large**
- Default settings for networking and permissions
- Waited for cluster to enter **Waiting** state before running jobs

---

## PySpark Application

The PySpark script performed the following:

- Loaded the raw taxi dataset from S3  
- Computed daily metrics:
  - Average trip distance  
  - Average trip cost  
  - Total trip costs  
  - Total passengers  
- Saved the aggregated results to the S3 `/output` folder  

The output CSV was downloaded and used to answer the assessment questions.

---

## Analysis Results

### 1. Total Passengers on January 8, 2022  
**119,897**

### 2. Average Ride Cost on January 30, 2022  
**19.99**

### 3. Average Trip Distance on January 17, 2022  
**4.99**

These values were computed directly from the EMR PySpark output.

---

## Tools & Technologies

- Amazon S3  
- Amazon EMR  
- Apache Spark / PySpark  
- Distributed data processing  
- Cloud-based big data workflows  

---

## Skills Demonstrated

- Big data ingestion and storage  
- EMR cluster configuration and management  
- Running Spark jobs on distributed compute  
- Writing and executing PySpark scripts  
- Aggregating and exporting large datasets  
- AWS resource cleanup and cost management  

---

## Summary

This assignment provided hands-on experience with big data processing using Amazon EMR and PySpark. By analyzing millions of taxi ride records, I demonstrated the ability to build scalable data pipelines, compute daily metrics, and export results for downstream analytics.
