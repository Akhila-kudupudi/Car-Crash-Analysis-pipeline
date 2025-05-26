# 🚗 Car Crash Analysis Pipeline 

This project is a full-stack data analytics pipeline developed for car crash analysis. It focuses on analyzing car crash data from Montgomery County, Maryland, to uncover key insights, perform geospatial analysis, and build predictive models that identify primary factors contributing to driver-at-fault incidents.

---

## Project Objectives

- **Analyze crash trends** using historical data
- **Visualize** accident hotspots through geospatial mapping
- **Preprocess and clean** raw data using PySpark
- **Connect MongoDB Atlas and Databricks** to scale data handling
- **Engineer features** relevant for predictive modeling
- **Build machine learning models** to classify at-fault crashes
- **Evaluate model performance** using metrics like accuracy and F1-score

---

## 📊 Dataset Summary

- **Source**: Montgomery County, MD Crash Reporting - Drivers Data
- **Data Points**: ~172,000
- **Features**: 43
- **Last Updated**: February 9, 2024
- **Collected From**: Maryland State Police Automated Crash Reporting System (ACRS)
- **Reported By**: Montgomery County, Gaithersburg, Rockville Police, etc.

---

## 🛠️ Tech Stack

| Category              | Tools & Platforms                             |
|----------------------|-----------------------------------------------|
| Data Cleaning        | PySpark, Python                                |
| Storage & Access     | MongoDB Atlas, MongoDB Compass                |
| Processing           | Databricks (Apache Spark)                     |
| Visualization        | Tableau                                        |
| ML Modeling          | PySpark MLlib                                  |
| Collaboration        | GitHub, Google Colab                          |

---

## Instructions to Run

### 1. Open the Notebook
- Open `google_colab_team1.ipynb` using [Google Colab](https://colab.research.google.com).

### 2. Upload the Clean Dataset
- Upload the file: `car_crashdata_pysparkclean (1).csv`.

### 3. Run the Notebook
- Follow the steps inside the notebook. It contains:
  - Data loading and cleaning
  - Exploratory data analysis (EDA)
  - Machine learning model building and evaluation

## MongoDB + Databricks Integration

To handle large-scale processing and storage, we used MongoDB Atlas for NoSQL data and Databricks for distributed processing.

- Installed `mongo-spark` connector on Databricks
- Enabled IP access to MongoDB Atlas
- Connected Databricks via connection string from MongoDB Compass
- Code is available in the Colab and Databricks notebooks

📄 Refer to:
- [`docs/Mongodb connections.pdf`](docs/Mongodb%20connections.pdf)
- [`docs/connecting databricks and mongodb.pdf`](docs/connecting%20databricks%20and%20mongodb.pdf)

## Machine Learning Models Tested

We tested five classification models using PySpark MLlib:

| Model                    | Accuracy    |
|--------------------------|-------------|
| Random Forest            | **87.71%**  |
| Gradient Boosted Trees   | 78.22%      |
| Decision Tree            | 74.16%      |
| Logistic Regression      | 53.11%      |

Random Forest gave the best results and was used for final predictions.

Key Features Used:
- Vehicle Movement
- Driver Distractions
- Collision Type
- First Impact Location
- Second Impact Location


## Geospatial Analysis (Tableau)

We used Tableau to map crash locations and identify high-risk areas based on:
- Time of day
- Severity of crash
- Driver fault frequency

📊 See: [`FinalProject_Tableau_results.twbx`](tableau/AIT614_finalProject_Tableau_results.twbx)


##  Final Presentation

View our full presentation here:  
📂 [`ProjectPresentation.pptx`](presentation/AIT614_ProjectPresentation_Team1.pptx)

