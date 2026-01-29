# 📍 Master’s Thesis: Spatial Cannibalization Analysis
> **공간 자기상관과 Cannibalization 임계점 분석을 통한 대기업 상권 입지전략 연구**
> *(A Study on Location Strategy through Spatial Autocorrelation and Cannibalization Threshold Analysis)*

---

## 📝 Project Overview
본 연구는 서울시 공공데이터를 활용하여, 상권 내 **공간 자기상관(Spatial Autocorrelation)**과 과밀 상권의 **자기잠식(Cannibalization) 임계점**을 산출하여 대기업의 최적 입지 전략을 제안합니다. 

* **Period:** 5-Year Industry-level analysis (Seoul, South Korea)
* **Key Focus:** Identifying the 'Threshold' where expansion leads to cannibalization.
* **Target:** Large enterprise strategic location decision-making.

## 🔥 Key Technical Accomplishments (Dunamu Focus)
1. **고성능 데이터 파이프라인 구축 (Engineering)**
* **Polars 기반 고속 처리:** 20GB 이상의 대규모 생활인구 및 상권 데이터를 처리하기 위해 Pandas 대비 약 5~10배 빠른 Polars를 도입. Lazy API를 활용한 쿼리 최적화로 메모리 효율 극대화.
* **데이터 모듈화:** 스파게티 코드를 지양하고 전처리(src/data_loader.py)와 분석(src/spatial_analysis.py) 로직을 분리하여 재사용 가능한 라이브러리 형태로 구축.
2. **공간 통계 및 임계점 모델링 (Analysis)**
* **공간 자기상관 분석:** Global/Local Moran's I를 활용하여 상권 활성도의 공간적 군집 패턴(Hot-spot) 정량화.
* **Threshold 모델링:** 특정 지역 내 점포 밀도가 증가함에 따라 매출 증가율이 둔화되거나 하락하는 **자기잠식 임계점(Cannibalization Threshold)**을 수학적으로 도출.

## 🛠 Tech Stack
* **Language:** Python (Pandas/Polars), SQL
* **Analysis:** Spatial Autocorrelation (Moran's I), Regression Analysis
* **Tools:** GIS-based Spatial Analysis, PostgreSQL/BigQuery (Pipeline)

## 📂 Repository Structure
```text
├── src/               # 재사용 가능한 핵심 모듈 (Python Scripts)
│   ├── data_loader.py # Polars 기반 고속 데이터 로드 및 전처리
│   └── spatial_stats.py # Moran's I 및 LISA 통계 계산 로직
├── notebooks/         # 단계별 분석 프로세스 (Experimentation)
│   ├── 01_Preprocessing.ipynb # 데이터 정제 및 Parquet 변환
│   ├── 02_Spatial_Analysis.ipynb # 공간 통계 모델링 및 시각화
│   └── 03_Strategy_Mapping.ipynb # 전략 도출 및 비즈니스 가이드라인
├── results/           # 분석 결과물 및 리포트
│   └── figures/       # LISA Cluster Map, 전략 지도 이미지
└── requirements.txt   # 의존성 관리
```

## 🚀 Key Methodology
1. **Data Engineering:** 서울시 업종별 5개년 공공데이터를 기반으로 공간 데이터 집계 및 특성 추출(Feature Engineering). 특히 Polars 라이브러리를 활용한 고속 데이터 처리를 수행함. 
2. **Spatial Analysis:** 공간 자기상관 지수(Moran's I, LISA) 분석을 통한 업종별 상권 밀집도 및 클러스터링 패턴 평가.
* **Global Moran's I 지수 산출**
공간적 인접성에 따른 상권 활성도의 자기상관성을 측정하여 전체적인 상권 밀집 패턴을 파악합니다.$$I = \frac{N}{S_0} \frac{\sum_i \sum_j w_{ij} z_i z_j}{\sum_i z_i^2}$$
* **LISA (Local Indicators of Spatial Association)**
행정동 단위의 핫스팟(High-High)과 콜드스팟(Low-Low)을 분류하여 지역별 입지 특성을 세분화합니다.
4. **Threshold Modeling:** 자기잠식이 급격히 발생하는 임계점(Threshold)을 산출하여 최적 입지 전략 모델링 구축.

## 📊 Results & Insights
💡**핵심 분석 결과**
* **자기잠식 임계점 도출:**
상권 내 인접 점포 간의 거리가 $X$m 이내로 좁혀질 때, 신규 출점이 기존 점포 매출의 $Y$%를 잠식함을 증명.
* **6단계 입지 전략 수립:**
LISA 분석 결과와 매출 변화율을 결합하여 Core Growth(핵심성장), Cannibalization Risk(자기잠식위험), Monitor(관찰) 등의 전략 레이블을 서울시 전역 행정동에 매핑.

## 📈 시각화 결과물
LISA Cluster Map,Strategy Priority Map
(실제 결과 이미지를 해당 경로에 업로드 후 연결하세요),
