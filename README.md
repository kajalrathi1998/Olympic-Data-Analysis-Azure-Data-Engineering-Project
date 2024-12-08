# **Tokyo Olympic-Data-Analysis-Azure-Data-Engineering-Project**

---

## **Project Overview**
This project showcases a complete data engineering and analytical pipeline using the Tokyo Olympics dataset. The workflow integrates multiple Azure services to ingest, transform, analyze, and visualize data, providing actionable insights into the dataset.

---

## **Dataset Details**
- **Dataset**: Tokyo Olympics Dataset (2021)  
- **Description**: Contains details of over 11,000 athletes, 47 disciplines, and 743 teams. Includes athlete names, countries, gender, disciplines, and coach details.  

---

## **Azure Services Used**
1. **Azure Data Factory**: Data ingestion from GitHub.  
2. **Azure Data Lake Storage Gen2**: Primary storage solution for raw and transformed data.  
3. **Azure Databricks**: Data transformation and enrichment.  
4. **Azure Synapse Analytics**: Advanced analytics and reporting.  
5. **Power BI**: Visualization of insights.  

---

## **Workflow**

### **1. Initial Setup**
1. Create an **Azure Free Subscription**.  
2. Create a **Resource Group** named `tokyo-olympic-data` to manage resources.  
3. Set up a **Storage Account** with Azure Data Lake Storage (ADLS) Gen2.  
4. Create a **Container** with two directories:
   - `raw-data`: For storing raw data.  
   - `transformed-data`: For storing transformed data.  

---

### **2. Data Ingestion Using Azure Data Factory**
1. Set up an **Azure Data Factory** workspace within the resource group.  
2. Upload the Tokyo Olympics dataset to a GitHub repository.  
3. Create a **Data Integration Pipeline** in Azure Data Factory:
   - Use the **HTTP connector** to fetch data from the GitHub repository.  
   - Configure the **Linked Service** for the source and sink.  
   - Define the file format for each dataset.  
4. Load datasets such as `athletes.csv`, `medals.csv`, etc., into the **raw-data** directory in ADLS Gen2.  

---

### **3. Data Transformation Using Azure Databricks**
1. Create an **Azure Databricks Workspace** in the resource group.  
2. Configure the **Compute Cluster** in Databricks.  
3. Create and configure a notebook for transformations:  
   - **Mount ADLS Gen2** using credentials (Client ID, Tenant ID, Secret).  
   - Perform data cleaning and transformation in the notebook.  
   - Save the transformed data back to the **transformed-data** directory in ADLS Gen2.  

---

### **4. Analytics with Azure Synapse Analytics**
1. Set up an **Azure Synapse Analytics Workspace**.  
2. Create a **Lake Database** named `TokyoOlympicDB`.  
3. Use transformed data from ADLS Gen2 to create tables in Synapse.  
4. Perform exploratory data analysis using SQL scripts in Synapse.  

---

### **5. Visualization with Power BI**
1. Connect Power BI to Synapse or ADLS Gen2.  
2. Generate interactive dashboards to visualize insights, such as:  
   - Medal distribution by country.  
   - Gender representation in disciplines.  
   - Performance of teams across events.  

---

