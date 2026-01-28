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
```

## 🚀 Key Methodology
* **1. Data Engineering:** 서울시 업종별 5개년 공공데이터를 기반으로 공간 데이터 집계 및 특성 추출(Feature Engineering). 특히 Polars 라이브러리를 활용한 고속 데이터 처리를 수행함.

* **2. Spatial Analysis:** 공간 자기상관 지수(Moran's I) 분석을 통한 업종별 상권 밀집도 및 클러스터링 패턴 평가.
* **3. Threshold Modeling:** 자기잠식이 급격히 발생하는 임계점(Threshold)을 산출하여 최적 입지 전략 모델링 구축.

## 📊 Results & Insights
💡 필요 이미지 삽입

* 핵심 요약: (((학위논문의 가이드라인 제시)))
* 시각화 결과: (((결과물 이미지 링크 삽입할 것)))
