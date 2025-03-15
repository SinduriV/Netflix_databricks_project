# **Netflix Data Engineering Pipeline**

## 📌 Project Overview  
This project builds an end-to-end **data engineering pipeline** using **Azure Data Factory, Databricks, and Unity Catalog**, following the **Medallion Architecture** (Bronze, Silver, Gold). The pipeline efficiently ingests, processes, and transforms **Netflix dataset files** from **GitHub** into a structured Delta Lakehouse.

---

## ⚙️ Technology Stack  
- **Cloud:** Microsoft Azure  
- **Data Ingestion:** Azure Data Factory (ADF)  
- **Storage:** Azure Data Lake Storage Gen2 (ADLS)  
- **Processing & Transformation:** Databricks (PySpark, Delta Live Tables)  
- **Data Governance:** Databricks Unity Catalog  
- **Streaming:** Databricks Autoloader  
- **File Format:** CSV, Delta  

---

## 🏗 Project Architecture  
The project follows the **Medallion Architecture** to handle structured data efficiently:  

1. **Bronze Layer (Raw Ingestion)**
   - **Azure Data Factory (ADF)** loads Netflix dataset from **GitHub** to the **Bronze Layer in ADLS**.  
   - **Databricks Autoloader** is used for streaming data from the **Landing Page in ADLS** to the **Bronze Layer**.  

2. **Silver Layer (Data Cleansing & Transformation)**  
   - Cleaned and transformed raw data.  
   - Removed duplicates, handled missing values, and standardized formats.  
   - Stored as **Delta tables** for optimized querying.  

3. **Gold Layer (Business-Ready Data)**  
   - Created **Delta Live Tables (DLT)** for real-time, high-quality analytics.  
   - Stored aggregated, business-friendly data ready for visualization and reporting.  

---

## 🚀 Key Features  
✅ **End-to-End ETL pipeline** from ingestion to transformation.  
✅ **Parameterized ADF Pipeline** for flexible data loading.  
✅ **Streaming Ingestion** using **Databricks Autoloader**.  
✅ **Unity Catalog Integration** for data governance.  
✅ **Delta Lake Format** for efficient storage and querying.  
✅ **Medallion Architecture** ensuring a structured and scalable approach.  

---

## 📂 Dataset  
- **Source:** Netflix Dataset (from Kaggle)  
- **Format:** CSV  
- **Contains:** Movie & TV show details, release year, genre, country, etc.  


