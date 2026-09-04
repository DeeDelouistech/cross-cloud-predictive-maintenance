# cross-cloud-predictive-maintenance
# Cross-Cloud Predictive Maintenance Pipeline (AWS S3 & Microsoft Fabric)

An end-to-end cloud data engineering and MLOps project that ingests IoT sensor telemetry from AWS S3, processes it using Microsoft Fabric (OneLake & Delta Lake), trains a machine learning classifier with automated tracking via MLflow, and visualizes failure risks in Power BI.

## 🏗️ Architecture & Data Flow
1. **Source:** Raw IoT sensor data (`temperature`, `vibration`) stored in **AWS S3**.
2. **Ingestion:** Virtual zero-copy connection established via **Microsoft Fabric OneLake Shortcuts**.
3. **Data Engineering:** Processed raw data and converted it into ACID-compliant **Managed Delta Tables** (`sensor_telemetry`) using PySpark.
4. **Machine Learning & MLOps:** Trained a **Random Forest Classifier** using Scikit-Learn to predict machine failures, with parameters and metrics tracked via **MLflow**.
5. **Batch Inference:** Executed batch scoring to generate `failure_probability` scores, written back to a downstream Delta table (`sensor_predictions`).
6. **Visualization:** Built a **Power BI** semantic model and dashboard to display high-risk equipment.

---

## 📸 Project Visuals

### 1. Lakehouse Data Architecture (Delta Tables)
*(Insert screenshot of your Lakehouse tables here)*

### 2. MLOps Experiment Tracking (MLflow)
*(Insert screenshot of your MLflow run here)*

### 3. Power BI Predictive Dashboard
*(Insert screenshot of your failure probability bar chart here)*

---

## 🚀 Tech Stack
* **Cloud Storage:** AWS S3, Microsoft Fabric OneLake
* **Data Processing:** PySpark, Delta Lake, Spark SQL
* **Machine Learning:** Scikit-Learn, MLflow
* **Visualization:** Power BI
