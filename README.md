# 🔷 Azure End-to-End Data Pipeline Project

This project demonstrates a complete **cloud-native data pipeline** built using Microsoft Azure services. It follows the modern **Medallion Architecture** (Bronze → Silver → Gold) and showcases how raw external data can be ingested, transformed, queried, and visualized — all on the cloud.

---

## 📌 Project Highlights

- **Data Ingestion** using **Azure Data Factory** from external HTTP sources (e.g., GitHub)
- **Data Storage** in **Azure Data Lake Storage Gen2** with Bronze, Silver, and Gold layers
- **Data Transformation** using **Azure Databricks + PySpark**
- **Data Modeling and SQL querying** with **Azure Synapse Analytics**
- **Business Intelligence and Dashboards** via **Power BI**

---

## 📽️ Project Demo

🔗 **Watch the screen recording demo on LinkedIn:**  
[▶ Video Post Link](https://www.linkedin.com/posts/vishnu1702_azure-dataengineering-databricks-activity-7317900100133953536-ct9N?utm_source=share&utm_medium=member_desktop&rcm=ACoAAEZOv90BlVXEz6AoDf0TykCGkpsmrXtdjGg)

📥 **Embedded Video:**  
```html
<iframe src="https://www.linkedin.com/embed/feed/update/urn:li:ugcPost:7317899971708493825?compact=1" height="399" width="504" frameborder="0" allowfullscreen="" title="Embedded post"></iframe>
```

## ✍️ Article Walkthrough

📄 **Read the full technical article:**  
[📚 LinkedIn Article Post](https://www.linkedin.com/posts/vishnu1702_azure-data-engineering-activity-7317909241191612416-1d9L?utm_source=share&utm_medium=member_desktop)

📰 **Embedded Article View:**  
```html
<iframe src="https://www.linkedin.com/embed/feed/update/urn:li:ugcPost:7317909241191612416?collapsed=1" height="399" width="504" frameborder="0" allowfullscreen="" title="Embedded post"></iframe>
```

## 🧱 Architecture Overview

```
[HTTP Source (GitHub)] 
           ↓
[Azure Data Factory (ADF)] 
           ↓
[Bronze Layer - Raw Data Storage] 
           ↓
[Azure Databricks - Data Transformation (PySpark)] 
           ↓
[Silver Layer - Cleaned Data Storage] 
           ↓
[Azure Synapse Analytics - Querying & Modeling] 
           ↓
[Gold Layer - Business Ready Data]
           ↓
[Power BI - Dashboards and Insights]
```

## 💡 Technologies Used

- Azure Data Factory
- Azure Data Lake Storage Gen2
- Azure Databricks (PySpark)
- Azure Synapse Analytics
- Power BI
- GitHub (as HTTP data source)
- Entra ID (for secure access configuration)

## 📂 Repository Structure

```
├── adf/                          # Azure Data Factory pipelines and configurations
│   ├── pipelines/                # Data ingestion pipeline definitions
│   └── linked_services/          # Connection configurations
│
├── databricks/                   # Databricks notebooks
│   ├── bronze_to_silver/         # Transformation scripts for raw to cleaned data
│   └── silver_to_gold/           # Transformation scripts for analytics-ready data
│
├── synapse/                      # Synapse Analytics SQL scripts
│   ├── views/                    # SQL views for data modeling
│   └── stored_procedures/        # Stored procedures for data operations
│
├── powerbi/                      # Power BI report templates
│   └── dashboards/               # Business intelligence dashboard designs
│
└── docs/                         # Project documentation
    ├── architecture.md           # Detailed architecture explanation
    └── setup_guide.md            # Deployment and configuration instructions
```

## 🚀 Getting Started

### Prerequisites

- Azure subscription with contributor access
- Azure CLI or Azure PowerShell installed locally
- Basic knowledge of SQL and PySpark

### Deployment Steps

1. **Resource Provisioning**
   ```bash
   # Clone this repository
   git clone https://github.com/murthy30300/Adventure-works.git
   cd azure-data-pipeline
   
   # Deploy Azure resources using ARM template
   az deployment group create --resource-group YourResourceGroup --template-file deploy/azuredeploy.json
   ```

2. **Configure Data Factory**
   - Import the ADF pipelines from the `/adf` directory
   - Configure linked services with your storage account and key vault information

3. **Deploy Databricks Notebooks**
   - Import notebooks from the `/databricks` directory to your Databricks workspace
   - Configure cluster with required libraries (PySpark, Delta Lake)

4. **Set Up Synapse Analytics**
   - Execute SQL scripts from the `/synapse` directory
   - Configure access permissions for your data sources

5. **Configure Power BI**
   - Open the template files from the `/powerbi` directory
   - Connect to your Synapse Analytics workspace



## 📬 Let's Connect

Feel free to [connect or reach out on LinkedIn](https://www.linkedin.com/in/vishnu1702/) to discuss the project or explore collaboration opportunities!

