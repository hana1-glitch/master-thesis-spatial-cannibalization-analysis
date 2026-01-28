# 📍 Master’s Thesis: Spatial Cannibalization Analysis
> **공간 자기상관과 Cannibalization 임계점 분석을 통한 대기업 상권 입지전략 연구**
> *(A Study on Location Strategy through Spatial Autocorrelation and Cannibalization Threshold Analysis)*

---

## 📝 Project Overview
본 연구는 서울시 공공데이터를 활용하여, 대기업의 상권 입지 전략 수립 시 발생하는 **공간 자기상관(Spatial Autocorrelation)**과 **자기잠식(Cannibalization) 효과**를 5개년 시계열 데이터로 분석합니다. 

* **Period:** 5-Year Industry-level analysis (Seoul, South Korea)
* **Key Focus:** Identifying the 'Threshold' where expansion leads to cannibalization.
* **Target:** Large enterprise strategic location decision-making.

## 🛠 Tech Stack
* **Language:** Python (Pandas/Polars), SQL
* **Analysis:** Spatial Autocorrelation (Moran's I), Regression Analysis
* **Tools:** GIS-based Spatial Analysis, PostgreSQL/BigQuery (Pipeline)

## 📂 Repository Structure
```text
├── data/       # Processed datasets & Documentation
├── sql/        # SQL pipelines for Feature Engineering & Spatial Aggregation
├── modeling/   # Scripts for Spatial Autocorrelation & Cannibalization Analysis
└── results/    # Model evaluation and Visualizations (Dashboards, Maps)
