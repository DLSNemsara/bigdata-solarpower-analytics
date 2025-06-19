# 🔆 Real-Time Solar Power Analytics with Apache Spark & Snowflake
> Real-time solar analytics pipeline powered by Apache Spark and Snowflake—built for scalable, cloud-first big data processing and forecasting.

An end-to-end big data pipeline and analytics system for monitoring, forecasting, and optimizing solar power generation using cloud-based tools and scalable data processing frameworks. Developed as part of the **Big Data Analytics (PUSL3121)** coursework at University of Plymouth.

---

## Project Overview

This project leverages real-world solar energy and weather sensor data to implement a real-time analytics system. Key features:

- **Data Ingestion & Preprocessing** using both **Apache Spark** and **Pandas**
- **Performance Benchmarking** between Pandas vs Spark for big data operations
- **Real-Time Cloud Analytics** using **Snowflake** with Snowpipe, Streams, and Tasks
- **Predictive Modeling** using Spark MLlib (Regression, Classification, Forecasting)
- **Interactive Dashboards** for live data visualization and decision support

---

## Tech Stack

| Layer         | Tools & Frameworks                                | Role                             |
| ------------- | ------------------------------------------------- | -------------------------------- |
| Preprocessing | Apache Spark, Pandas                              | Clean & transform large datasets |
| ML Models     | Spark MLlib, ARIMA                                | Forecasting, prediction          |
| Cloud & ETL   | Snowflake (Snowpipe, Streams, Tasks, Warehousing) | Real-time ingestion & processing |
| Dashboards    | Snowflake Visualizations                          | Data visualization               |
| Dev Tools     | Google Colab, GitHub, Jupyter Notebooks           | Dev + experiment environment     |


---

## Repository Structure

```

BigData-SolarPower-Analytics/
├── README.md
├── .gitignore
├── report/
│   └── BigData_SolarPower_Analytics_Report.pdf
├── notebooks/
│   ├── PUSL3121\_Data\_Preprocessing\_Pandas.ipynb
│   ├── PUSL3121\_Data\_Preprocessing\_Spark.ipynb
│   ├── Apache\_Spark\_modeling.ipynb
│   └── Snowflake\_Streaming\_Code.ipynb
└── assets/
    ├── ac-vs-dc.jpg
    ├── arima-forecast.png
    ├── daily-output.jpg
    ├── peak-generation.jpg
    └── weather-effect.jpg

```

---

## Machine Learning Models

| Model                        | Purpose                            | Metric   | Value   |
| ---------------------------- | ---------------------------------- | -------- | ------- |
| Linear Regression            | Predicting DC power                | R² Score | 0.624   |
| Random Forest Regressor      | DC power prediction                | R² Score | 0.99999 |
| Gradient Boosting Classifier | Power classification (High/Low)    | Accuracy | 99.24%  |
| ARIMA                        | Time series forecasting (DC_POWER) | RMSE     | 602.95  |

---

## Real-Time Streaming Pipeline

Snowflake was used to simulate a real-time analytics environment with:

- **Snowpipe** for continuous data loading
- **Streams** for change detection
- **Tasks** for scheduled processing
- **Materialized views** for dashboard feeds

---

## Visual Dashboards

### Peak and Off-Peak Generation

![Peak Hours](assets/peak-generation.jpg)

### Daily Power Output

![Daily Output](assets/daily-output.jpg)

### AC vs DC Power Comparison

![AC DC Diff](assets/ac-vs-dc.jpg)

### Weather Effect on Power

![Weather Effect](assets/weather-effect.jpg)

### ARIMA Forecasting

![ARIMA](assets/arima-forecast.png)

---

## Dataset

We used the [Solar Power Generation Dataset](https://www.kaggle.com/code/pythonafroz/solar-power-generation-forecast/input) from Kaggle, which includes:

- `Plant_1_Generation_Data.csv`
- `Plant_1_Weather_Sensor_Data.csv`
- `Plant_2_Generation_Data.csv`
- `Plant_2_Weather_Sensor_Data.csv`

**Note**: Due to file size and licensing, raw data files are not included in the repository. Sample views are available in the notebooks.

---

## Team Members

- **Sinel Nemsara**
- **Sachitha Eshan**
- **Yohan Nanayakkara**
- **Thejan Rajapaksha**

---

## Report

Refer to the detailed coursework submission in [`report/BigData_SolarPower_Analytics_Report.pdf`](./report/BigData_SolarPower_Analytics_Report.pdf) for full methodology, results, and evaluations.

---

## How to Run the Project

1. **Clone the repository**
   ```bash
   git clone https://github.com/DLSNemsara/bigdata-solarpower-analytics.git
   cd BigData-SolarPower-Analytics
   ```

2. **Set up your environment**
   - Use Google Colab, Jupyter, or any Spark-enabled Python environment
   - Install required packages: `pyspark`, `pandas`, `snowflake-connector-python`, etc.

3. **Configure Snowflake**
   - Create tables (based on notebook schemas)
   - Upload CSVs to a Snowflake stage
   - Set up **Snowpipe**, **Streams**, and **Tasks** for ingestion and processing

4. **Run the notebooks**
   - In order:  
     `PUSL3121_Data_Preprocessing_Pandas.ipynb` →  
     `PUSL3121_Data_Preprocessing_Spark.ipynb` →  
     `Apache_Spark_modeling.ipynb` →  
     `Snowflake_Streaming_Code.ipynb`

5. **Explore dashboards**
   - View results using Snowflake Visualizations or query materialized views

> ⚠️ Don’t forget to update Snowflake credentials and table paths in each notebook.

---

## Disclaimer

This project was submitted as part of academic coursework. Live streaming pipelines and cloud resources are no longer active.

---

## License

This project is shared for educational purposes under the MIT License.
