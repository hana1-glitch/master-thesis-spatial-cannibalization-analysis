# 📍 Master's Thesis: Spatial Cannibalization Analysis

> **공간 자기상관과 Cannibalization 임계점 분석을 통한 대기업 상권 입지전략 연구**
> *(A Study on Location Strategy through Spatial Autocorrelation and Cannibalization Threshold Analysis)*
>> 본 저장소는 **석사 학위 논문 연구**를 위해 수행된 데이터 분석 전 과정을 담고 있습니다. 

* 서울시 5개년 시계열 데이터를 바탕으로 상권 밀집도에 따른 자기잠식 효과를 통계적으로 입증하고, 이를 활용한 기업 입지 전략 모델을 제안합니다.


## 📝 Project Overview

* **목적:** 대기업의 무분별한 상권 확장이 기존 점포 및 인근 상권에 미치는 **공간적 자기잠식(Spatial Cannibalization)** 효과 규명
* **데이터:** 서울시 5개년 공공데이터 (점포정보, 추정매출, 생활인구 등 약 20GB 규모)
* **핵심 지표:** Moran's I 및 LISA를 활용한 공간적 군집 패턴 및 자기상관성 분석


## 🚀 Key Methodology (Research Focus)

본 코드는 학술적 연구의 재현성을 위해 **실제 논문 분석에 사용된 원본 코드**을 포함하고 있습니다.

### 1. **Spatial Autocorrelation Analysis:**
* **Global Moran's I:** 서울시 전체 상권의 공간적 밀집 패턴 정량화
* **LISA (Local Moran's I):** 행정동 단위 핫스팟(High-High) 및 콜드스팟(Low-Low) 분류
### 2. **Threshold Modeling:**
* 점포 간 거리와 매출 변화율의 상관관계를 분석하여 **자기잠식 임계점(Threshold)** 산출
### 3. **Strategic Location Labeling:**
* 분석 결과를 바탕으로 **6단계 입지 전략(Core Growth, Cannibalization Risk 등)** 도출 및 매핑


## 🛠 Tech Stack

* **Language:** Python (Pandas/Polars), SQL
* **Analysis:** Spatial Autocorrelation (Moran's I), Regression Analysis
* **Tools:** GIS-based Spatial Analysis, PostgreSQL/BigQuery (Pipeline)


## 📂 Repository Structure

* `/notebooks`: 실험 및 통계 분석 과정이 담긴 원본 Jupyter Notebooks
* `/results`: LISA Cluster Map 및 최종 입지 전략 시각화 결과물
* `/data`: 분석 가이드라인을 위한 샘플 데이터셋


## 📈 Statistical Insights

본 연구의 통계적 기반이 되는 Global Moran's I 핵심 수식입니다.

$$I = \frac{N}{S_0} \frac{\sum_{i=1}^N \sum_{j=1}^N w_{ij}(x_i - \bar{x})(x_j - \bar{x})}{\sum_{i=1}^N (x_i - \bar{x})^2}$$

**Variables:**
* $N$: 분석 대상 행정동의 총 개수
* $w_{ij}$: 공간 가중치 행렬(Spatial Weights Matrix)의 원소
* $x_i, x_j$: 각 행정동의 상권 활성도 지표
* $\bar{x}$: 지표의 전체 평균
* $S_0$: 모든 공간 가중치의 합 ($\sum_i \sum_j w_{ij}$)

*(Global Moran's I를 통해 공간적 의존성 검정 수행)*

