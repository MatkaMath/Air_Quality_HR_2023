# 🌫️ Air Quality Analysis in Croatia (2023)

This project analyzes daily PM2.5 measurements collected across multiple air quality monitoring stations in Croatia during the year 2023. The goal is to evaluate air quality levels, identify high pollution areas, and visualize temporal and categorical trends in pollution data.

## 📊 Project Structure

```
air-quality-hr-2023/
├── data/                     # Contains raw .parquet files (daily PM2.5 measurements)
├── notebooks/                # Jupyter notebook(s) with all analysis steps
├── README.md                 # Project documentation (this file)
└── .gitignore                # GitHub ignore rules
```

## 📥 Data Source

The data was downloaded in `.parquet` format from the official European Environment Agency (EEA) portal:  
🔗 [https://eeadmz1-downloads-webapp.azurewebsites.net/](https://eeadmz1-downloads-webapp.azurewebsites.net/)

Each file corresponds to a different sampling station (see `Samplingpoint` column). The raw station metadata is available via:  
🔗 [https://discomap.eea.europa.eu/App/AQViewer/index.html?fqn=Airquality_Dissem.b2g.measurements](https://discomap.eea.europa.eu/App/AQViewer/index.html?fqn=Airquality_Dissem.b2g.measurements)

To view information about a specific station, paste its ID (e.g. `HR_DOC_TYPE_D_SPO_749`) into the **"Sampling Point Id"** field on that page.

## ✅ Key Insights

- **Station `HR_DOC_TYPE_D_SPO_749` (Slavonski Brod)** recorded the highest PM2.5 levels, reaching **129 µg/m³** on 2023-12-30.
- Average PM2.5 across all stations was approximately **13.05 µg/m³**.
- Daily PM2.5 values exceeded **100 µg/m³** on several occasions – exclusively at Slavonski Brod.
- **Winter** had nearly **double** the average PM2.5 concentration compared to **Summer**:
  - Winter: **20.2**
  - Spring: **10.9**
  - Summer: **10.2**
  - Autumn: **11.5**

## 📈 Visualizations

All visualizations are embedded directly in the notebook:  
📄 [`notebooks/AirQuality_Project.ipynb`](notebooks/AirQuality_Project.ipynb)

These include:
- Air Quality Category Distribution
- Stacked Bar by Station
- PM2.5 Boxplot by Category
- Time Series by Station
- Seasonal Averages

## 🗺️ Stations with Highest PM2.5 Averages

| Sampling Point ID         | Avg PM2.5 |
|---------------------------|-----------|
| HR_DOC_TYPE_D_SPO_749     | 26.80     |
| HR_DOC_TYPE_D_SPO_795     | 17.82     |
| HR_DOC_TYPE_D_SPO_1214    | 17.82     |
| HR_DOC_TYPE_D_SPO_1028    | 14.27     |
| HR_DOC_TYPE_D_SPO_676     | 12.29     |

More station info: [EEA AQ Viewer](https://discomap.eea.europa.eu/App/AQViewer/index.html?fqn=Airquality_Dissem.b2g.measurements)

## 🧾 Requirements

- Python 3.8+
- PySpark
- Pandas
- Matplotlib
- Seaborn

## 📂 How to Run

1. Clone this repository:
    ```bash
    git clone https://github.com/MatkaMath/Air_Quality_HR_2023.git
    ```

2. Run the notebook in `notebooks/` to reproduce the full analysis.
