# Car Dealership Cloud Data Project 

This repository documents my progress in building a cloud data infrastructure for a car dealership using Microsoft Azure.

---

## Task 1: Environment Setup (Cloud Infrastructure)
In this initial task, I provisioned the foundational Azure resources required for the project. To comply with location policies, all resources were deployed in the **Italy North** region.

**Resources Created:**
* **Resource Group:** `CarDealership-RG` (Logical container for project resources).
* **Storage Account:** `cardealershipdata26` (Used for storing raw and processed data).
* **Azure Data Factory:** `CarDealershipADF26` (Used for data integration and automated pipelines).
* **Blob Container:** Created a container named `adftutorial` to hold the data files.

![Task 1 - Infrastructure Deployment](task1.png)---

## Task 2: Data Ingestion (Azure Data Factory)
The goal of this task was to simulate ingesting raw car data into our cloud storage and moving it using an automated pipeline.

**Steps Completed:**
1. **Data Preparation:** Created a local dataset `data.txt` containing car models and prices.
2. **Manual Upload:** Uploaded the dataset into the `input` folder within the `adftutorial` container in Azure Blob Storage.
3. **Pipeline Automation:** 
   * Opened **Azure Data Factory Studio**.
   * Used the **Copy Data tool** (Built-in copy task) to create an automated pipeline (`ADFQuickStart`).
   * Configured the Source (`input` folder) and Destination (`output` folder).
4. **Execution:** Successfully ran the pipeline, which automatically created the `output` folder and copied `emp.txt` into it.


![Task 2 - Pipeline Success](Task2.png)

