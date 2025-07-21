# SKN15-2nd-5Team (전기 요금 기반 이탈 예측)

####  팀명: 오원장과 아이들

## 팀 소개
| 오원장 | 권도원 | 유의정 | 조솔찬 | 홍민식 |
|--|--|--|--|--|
| @AQUAQUA5 | @dowonk120 | @Rr-EJ | @solchna | @minnnsik |
|  |


## 프로젝트 기간 🏆
###  25년 07월 10일 (목요일) ~ 25년 07월 11일 (금요일) 

## ✅ 프로젝트 배경 및 목적

파워코(PowerCo)는 BCG의 클라이언트로, 중소기업(SME)과 주거 고객에게 가스와 전기를 공급하는 에너지 회사입니다.  
최근 유럽 시장의 전력 자유화(Power Liberalization)와 가격 경쟁 심화로, 특히 SME 고객층에서 고객 이탈(Churn)률이 증가하고 있습니다.

<img width="659" alt="reuter-1" src="https://github.com/user-attachments/assets/eda46139-5a46-462e-b157-9920afbfc204" />


### 프로젝트 목표

- 고객의 계약, 이용 패턴, 요금, 마진, 마케팅 이력 등 다양한 특성과 이탈 간 관계를 데이터 기반으로 분석  
- 고객 이탈 확률(Churn Probability)을 예측하는 분류 모델 개발  
- 예측 결과를 활용해 효과적인 마케팅 전략(예: 할인 캠페인 타겟팅) 수립에 필요한 인사이트 도출


 
## 기술 스택
### AI & 데이터 처리

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
[](https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white)![](https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white)![](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)![](https://img.shields.io/badge/scikitlearn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)



### 머신러닝 모델
![](https://img.shields.io/badge/RandomForest-00B050?style=for-the-badge)![](https://img.shields.io/badge/DecisionTree-228B22?style=for-the-badge)![](https://img.shields.io/badge/XGBoost-EC0000?style=for-the-badge&logo=xgboost&logoColor=white)![](https://img.shields.io/badge/LightGBM-3C3C3C?style=for-the-badge&logo=lightgbm&logoColor=white) ![](https://img.shields.io/badge/CatBoost-FFCC00?style=for-the-badge)

![](https://img.shields.io/badge/SGDClassifier-006699?style=for-the-badge)![](https://img.shields.io/badge/Logistic%20Regression-1E90FF?style=for-the-badge)![](https://img.shields.io/badge/SVM-8A2BE2?style=for-the-badge)

### 버전 관리 및 협업

![](https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white) ![](https://img.shields.io/badge/discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)

## 1. 데이터셋 소개

본 프로젝트에서는 **Kaggle PowerCo 고객 이탈 예측** 데이터셋을 활용하였습니다.  
이 데이터는 유럽 지역 SME(중소기업)와 주거용 고객을 대상으로 전기·가스를 공급하는 PowerCo사의 실제 거래 및 이탈 이력 데이터를 기반으로 합니다.

PowerCo는 전력 시장 자유화, 가격 민감도 증가 등 환경 변화로 인해 고객 이탈(Churn) 가능성이 높아진 상황에서,  
이탈 예측 모델링을 통해 "이탈 위험 고객"에게 20% 할인 등 차별적 마케팅 전략을 적용할지 판단하고자 합니다.

데이터셋은 다음 세 개의 주요 파일로 구성되어 있습니다.

- **ml_case_training_data.csv**  
    - 고객 기본 정보가 담긴 메인 파일

- **ml_case_training_hist_data.csv**  
    - 고객별 월별 계약 가격 정보(변동단가·고정단가 포함) 제공  

- **ml_case_training_output.csv**  
    - 타겟 변수 

## 2. 변수 소개


### 2.1 Train_data (고객별 프로필·예측 정보)

| 컬럼명                    | 데이터 타입       | 설명                             | 카디널리티 | 결측 비율 | 결측 처리 방식              |
|--------------------------|------------------|---------------------------------|-----------:|---------:|---------------------------|
| id                       | object           | 고객 고유 식별자                 |     16 096 |     0.00% | n/a                       |
| channel_sales            | object           | 가입 영업 채널 코드              |          7 |    26.21% | fillna("new category")    |
| activity_new             | object           | 회사 활동 카테고리               |        419 |    59.30% | review & merge categories |
| campaign_disc_ele        | float64          | 마지막 가입 전기 캠페인 코드     |          1 |   100.00% | drop                      |
| cons_12m                 | int64            | 최근 12개월간 전기 사용량        |       2 342 |     0.00% | n/a                       |
| cons_gas_12m             | int64            | 최근 12개월간 가스 사용량        |       1 820 |     0.00% | n/a                       |
| cons_last_month          | int64            | 직전 월 전기 사용량              |       1 200 |     0.00% | n/a                       |
| imp_cons                 | float64          | 현재 청구된 사용량               |       3 150 |     0.22% | n/a                       |
| forecast_cons            | float64          | 다음 달 예상 전기 사용량         |       3 210 |    21.10% | n/a                       |
| forecast_cons_12m        | float64          | 다음 12개월 예상 전기 사용량     |       2 450 |     0.00% | n/a                       |
| forecast_cons_year       | int64            | 연간 예상 전기 사용량            |       2 460 |     0.00% | n/a                       |
| forecast_price_energy_p1 | float64          | 1구간 예상 에너지 단가           |         120 |     0.00% | n/a                       |
| forecast_price_energy_p2 | float64          | 2구간 예상 에너지 단가           |           1 |    70.00% | n/a                       |
| forecast_price_pow_p1    | float64          | 1구간 예상 전력 단가             |         134 |     0.00% | n/a                       |
| margin_gross_pow_ele     | float64          | 전력 가입 총 마진                |       4 181 |     0.08% | n/a                       |
| margin_net_pow_ele       | float64          | 전력 가입 순마진                 |       4 181 |     0.08% | n/a                       |
| net_margin               | float64          | 전체 순마진                      |       4 181 |     0.09% | n/a                       |
| nb_prod_act              | int64            | 활성화된 상품·서비스 개수        |          11 |     0.00% | n/a                       |
| num_years_antig          | int64            | 고객 가입 경과 연수              |          15 |     0.00% | n/a                       |
| origin_up                | object           | 최초 가입 전기 캠페인 코드       |          15 |     0.54% | most_frequent            |
| date_activ               | datetime64[ns]   | 계약 활성화 날짜                 |            – |     0.00% | n/a (NaT 유지)           |
| date_first_activ         | datetime64[ns]   | 고객 첫 계약 시작일              |            – |    78.21% | drop                      |
| date_modif_prod          | datetime64[ns]   | 상품 마지막 수정일               |            – |     0.98% | bfill                     |
| date_renewal             | datetime64[ns]   | 다음 계약 갱신일                 |            – |     0.25% | bfill                     |
| date_end                 | datetime64[ns]   | 계약 종료 등록일                 |            – |     0.01% | bfill                     |

---

### 2.2 Hist_data (월별 소비·단가 시계열)

| 컬럼명        | 데이터 타입       | 설명                   | 카디널리티 | 결측 비율 | 결측 처리 방식 |
|--------------|------------------|-----------------------|-----------:|---------:|---------------|
| id           | object           | 고객 고유 식별자       |     16 096 |     0.00% | n/a           |
| price_date   | datetime64[ns]   | 청구 기준일            |          12 |     0.00% | n/a           |
| price_p1_var | float64          | 1구간 가변 에너지 단가 |          12 |     0.00% | n/a           |
| price_p2_var | float64          | 2구간 가변 에너지 단가 |          10 |     0.00% | n/a           |
| price_p3_var | float64          | 3구간 가변 에너지 단가 |           8 |     0.00% | n/a           |
| price_p1_fix | float64          | 1구간 고정 전력 단가   |          12 |     0.00% | n/a           |
| price_p2_fix | float64          | 2구간 고정 전력 단가   |          10 |     0.00% | n/a           |
| price_p3_fix | float64          | 3구간 고정 전력 단가   |           6 |     0.00% | n/a           |

---

### 2.3 Output_data (타깃)

| 컬럼명 | 데이터 타입 | 설명                          | 카디널리티 | 결측 비율 | 결측 처리 방식 |
|-------|-------------|-------------------------------|-----------:|---------:|---------------|
| id    | object      | 고객 고유 식별자              |     16 096 |     0.00% | n/a           |
| churn | int64       | 이탈 여부 (0 = 유지, 1 = 이탈) |           2 |     0.00% | n/a           |


## 3. 분포 소개

**범주형 데이터**
| 변수명                                                                                               | 의미                    | 고유값 수 (Unique) | 분석 인사이트 요약                 |
| ------------------------------------------------------------------------------------------------- | --------------------- | -------------- | -------------------------- |
| `activity_new`, `date_active`, `date_end`, `date_first_active`, `date_modif_prod`, `date_renewal` | 고객 활동 및 관련 날짜 정보      | 매우 많음 (다수)     | 고유값이 많아 타겟과의 직접 연관성 분석 어려움 |
| `channel_sales`                                                                                   | 고객 가입 경로              | 7개             | 특정 경로에서 가입하거나 이탈한 고객이 많음   |
| `has_gas`                                                                                         | 전기 외에 가스 서비스 가입 여부    | 2개 (`0`, `1`)  | 전기만 가입한 고객 수가 더 많음         |
| `origin_up`                                                                                       | 최초 가입 시 사용한 전기 캠페인 코드 | 5개             | 이탈과 비이탈 간 차이 분석 가능         |

  
![](https://www.kaggleusercontent.com/kf/249884298/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..S7ubOFvyJyMZbwlZyRkbYw.rKits_cfq7UmIIemmdoI85UdOMV5Zlxvo2FAMU7hi6RGRmMSse_gGdZbCcEpJo2zxBiFCsHhDRoWgq_VgUNVmWss2Y9CSVIfYwLjK10S51b05N0AhVmRegTxnhag92aJqEm6L65CQoZAMj4hK5Xs8UgARWnXA8UcMKGn-az7oGpnyvAFF8vT_vBBEnRTI5dUTO7xlrFMgvzPqYq8nFhz2CxQSuA00BBOLkU48AnGNvx5BkBVFkahaKF63_wZTh9SouiBfaKJTOAzUtDRiXqRwXU_D5cXt2xJQoj4GmDL2RIJjaXhK9yfVPu-ikNw_EsFy9_kDk1q8sju5QJgSC-x19CJhM85bOwwoOpMwqZlx13np6F7s5AgL92MQx5GU9U4PsujDMcyJeAqEmZP54Y3eL8GZvLYOFUZ1J0VsESMyPsvZkpjKLswcutLaYKc6JaabgbQH5f_RlGl-kPSoyHarF20FieJGWndmW2UDZWAzUhBLPCRMwszykfpeNbuBAeGrsVOPeFTpIu3PfJ-VADsWSNcCnAcVQAc6xhH-ELe4JqB1GsJDFHzbWUTaMh4NNFwoaLJ7njX02IOBldYbSfGhM2fSGugHxPRzegegQuFWJXD7Ag2uSclDmxC8Q7CX7nY.9o16I9Wd-RUalkoscYB-RQ/__results___files/__results___16_0.png)


- **수치형 데이터**

| 변수명                  | 의미                            | 분석 인사이트 요약                            |
| -------------------- | ------------------------------- | ----------------------------------------- |
| `cons_last_month`    | 고객의 **최근 한 달 전기 사용량**           | 이탈 직전 소비량이 적은 고객이 많아, **행동 변화 감지에 효과적**   |
| `cons_12m`           | 고객의 **최근 12개월간 전기 총사용량**        | 연간 사용량이 적은 고객에서 이탈률 높음. **소규모 사용자 이탈 경향** |
| `nb_prod_act`        | 고객이 **현재 사용 중인 상품 개수**          | 상품 수가 적을수록 이탈률이 높음. **충성도 및 관여도 반영**      |
| `net_margin`         | 고객으로부터 얻는 **총 순마진** | 손해 고객에서 이탈률 높음. **고객 수익성과 이탈 연결**         |
| `margin_net_pow_ele` | 전기 공급을 통한 **전력 가입 순마진**           | 수익이 적을수록 이탈 가능성 높음. **가격 민감도 있는 고객 특성**   |
| `num_years_antig`    | 고객이 **가입한 이후 경과한 연수**           | 가입 기간이 짧을수록 이탈률 높음. **신규 고객 리스크** 파악 가능   |

  
![](https://www.kaggleusercontent.com/kf/249884298/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..S7ubOFvyJyMZbwlZyRkbYw.rKits_cfq7UmIIemmdoI85UdOMV5Zlxvo2FAMU7hi6RGRmMSse_gGdZbCcEpJo2zxBiFCsHhDRoWgq_VgUNVmWss2Y9CSVIfYwLjK10S51b05N0AhVmRegTxnhag92aJqEm6L65CQoZAMj4hK5Xs8UgARWnXA8UcMKGn-az7oGpnyvAFF8vT_vBBEnRTI5dUTO7xlrFMgvzPqYq8nFhz2CxQSuA00BBOLkU48AnGNvx5BkBVFkahaKF63_wZTh9SouiBfaKJTOAzUtDRiXqRwXU_D5cXt2xJQoj4GmDL2RIJjaXhK9yfVPu-ikNw_EsFy9_kDk1q8sju5QJgSC-x19CJhM85bOwwoOpMwqZlx13np6F7s5AgL92MQx5GU9U4PsujDMcyJeAqEmZP54Y3eL8GZvLYOFUZ1J0VsESMyPsvZkpjKLswcutLaYKc6JaabgbQH5f_RlGl-kPSoyHarF20FieJGWndmW2UDZWAzUhBLPCRMwszykfpeNbuBAeGrsVOPeFTpIu3PfJ-VADsWSNcCnAcVQAc6xhH-ELe4JqB1GsJDFHzbWUTaMh4NNFwoaLJ7njX02IOBldYbSfGhM2fSGugHxPRzegegQuFWJXD7Ag2uSclDmxC8Q7CX7nY.9o16I9Wd-RUalkoscYB-RQ/__results___files/__results___18_0.png)

- **타겟 (이탈 / 비이탈)**
    - 타겟 데이터 분포 9:1로 불균형 심함
      
![](https://www.kaggleusercontent.com/kf/249884298/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..S7ubOFvyJyMZbwlZyRkbYw.rKits_cfq7UmIIemmdoI85UdOMV5Zlxvo2FAMU7hi6RGRmMSse_gGdZbCcEpJo2zxBiFCsHhDRoWgq_VgUNVmWss2Y9CSVIfYwLjK10S51b05N0AhVmRegTxnhag92aJqEm6L65CQoZAMj4hK5Xs8UgARWnXA8UcMKGn-az7oGpnyvAFF8vT_vBBEnRTI5dUTO7xlrFMgvzPqYq8nFhz2CxQSuA00BBOLkU48AnGNvx5BkBVFkahaKF63_wZTh9SouiBfaKJTOAzUtDRiXqRwXU_D5cXt2xJQoj4GmDL2RIJjaXhK9yfVPu-ikNw_EsFy9_kDk1q8sju5QJgSC-x19CJhM85bOwwoOpMwqZlx13np6F7s5AgL92MQx5GU9U4PsujDMcyJeAqEmZP54Y3eL8GZvLYOFUZ1J0VsESMyPsvZkpjKLswcutLaYKc6JaabgbQH5f_RlGl-kPSoyHarF20FieJGWndmW2UDZWAzUhBLPCRMwszykfpeNbuBAeGrsVOPeFTpIu3PfJ-VADsWSNcCnAcVQAc6xhH-ELe4JqB1GsJDFHzbWUTaMh4NNFwoaLJ7njX02IOBldYbSfGhM2fSGugHxPRzegegQuFWJXD7Ag2uSclDmxC8Q7CX7nY.9o16I9Wd-RUalkoscYB-RQ/__results___files/__results___20_0.png)


## 4. 기존 사례
| No. | Dataset      | Description                                                     | EDA 요약                                                                                                    | Model                                      | Accuracy | Precision | Recall  | F1-score | Reference                                                                                         |
|-----|-------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------|----------|-----------|---------|----------|---------------------------------------------------------------------------------------------------|
| 1   | PowerCo     | 다양한 전처리 및 이탈률 분석 적용                                | 결측치 처리<br>이탈률 시각화<br>이상치 절대값 변환<br>데이터 타입 변환 및 클린 데이터셋 구축                  | xgb.XGBClassifier                          | 0.981368 | 0.998939  | 0.808022|          | [Link](https://www.kaggle.com/code/iamarjunchandra/powerco-business-problem-from-bcg-consulting)  |
| 2   | Telco Churn | 통신사 고객 이탈 여부 예측                                      | 결측치/이상치/중복 제거<br>인코딩 및 시각화<br>계약 유형·요금 분석<br>SMOTE 적용                             | Random Forest<br>SVM, KNN (Best), AdaBoost | 0.898    | 0.650     | 0.0426  |          |                                                                                                   |
| 3   | CoE         | 다른 코드 기반, 최신 기법 적용                                  | 파생 변수 생성<br>PCA·로그 변환<br>상관관계 분석 및 정제                                                    | Random Forest<br>Naive Bayes, SVM          | 0.950    |           | 0.91    | 0.93     |                                                                                                   |
| 4   | Bank Churn  | 은행 신용카드 고객 이탈 분석<br>이번 달 이탈 여부(churn) 예측   | 결측치 제거·인코딩<br>분포 시각화(연령, 카드 등급, 상품 수, 한도, 잔고 등)<br>상관관계 히트맵<br>이탈 특성 비교<br>K-Means 군집 분석 및 시각화 | Random Forest<br>AdaBoost<br>SVM           | 0.9091   | 0.9091    | 0.9087  | 0.9087   |                                                                                                   |

## 5. 지표 설정
이탈할 것으로 예측되는 고객에게 20퍼센트 할인을 하여 이탈을 막는 것이 목표이다.  
사용시 이윤이 큰 모델이 가장 좋은 모델이다. 따라서 평가지표는 다음과 같다.

r = 고객 1명당 마케팅으로 인한 매출 증가량  
c = 고객 1명당 마케팅 비용



$$
\frac{\text{모델의 예측에 따른 이윤}}{\text{정확하게 예측 시 이윤}} = 
\frac{{r \times (이탈예측\,중\,실제이탈\,수) - c \times (이탈예측 \,수)}}{{( r-c )\times(실제이탈\,수)}}
$$


$$
\frac{TP \times r  - ( TP + FP ) \times c}{(TP+FN)(r - c)}
$$ 

$$
= Recall + \frac{1}{(r - c)} ( Recall- \frac{Recall}{Precision}) \ 
$$


$$
이때,  \frac{1}{(r - c)} \approx 0 이니
$$
$$
= Recall + \frac{1}{(r - c)} ( Recall- \frac{Recall}{Precision}) \approx Recall
$$



따라서 Recall이 높은 모델을 목표로 진행한다.

## 6. 전처리

결측치 70% 이상 칼럼 제거  
고객 회사 활동, 고객이 가입한 캠페인 칼럼은 오브젝트 형이므로 결측치를 새로운 카테고리로 분류한다.   

카테고리를 원핫 인코딩하면 카테고리간의 유사성을 고려하지 못한다.  
이를테면   
```관광업```과 ```머신러닝 사업``` 간의 거리 = ```머신러닝 사업```과 ```딥러닝 사업```간의 거리  
로 인식하게 된다.  
따라서 카테고리는 단어의 유사성을 반영하는 워드 임베딩을 시도.
카테고리가 코드로 저장되어있어 실패. 

날짜를 정수로 변환  

date_end 칼럼의 결측치 : ```계약시작일``` + ```평균 계약기간```으로 설정
```
이탈 = clean[clean['churn'] == 1]
유지 = clean[clean['churn'] == 0]

m = int((유지["date_end"] - 유지["date_activ"]).mean())
mask = clean["date_end"].isna()
clean.loc[mask, "date_end"] = clean.loc[mask, "date_activ"] + m
```
날짜 칼럼들은 데이터 제약 조건이 있다.  
예를들어 계약 시작일은 반드시 계약 종료일보다 빨라야한다.  
이러한 데이터 제약조건을 만족하면서 결측치를 채운다.  

이 데이터셋의 조건은
> date_activ, date_renewal <= date_end

날짜형 칼럼만 살펴본다.
|   | date_activ | date_end | date_modif_prod | date_renewal |
|---|------------|----------|-----------------|--------------|
| 0 | 4694       | 6154     | 4694            | 5791         |
| 1 | 4914       | 6010     | <NA>            | 5652         |
| 2 | 3520       | 6086     | 3520            | 5721         |
| 3 | 3758       | 5950     | 3758            | 5585         |
| 4 | 3741       | 5933     | 3741            | 5568         |

date_activ와 date_modif_prod가 같은 데이터들이 간혹 있다.
```
#비이탈자들의 date_modif_prod - date_activ
lt_0 = clean[clean["churn"]==0]["date_modif_prod"] - clean[clean["churn"]==0]["date_activ"]
print(f"비이탈자 소요시간 0의 비율: {(lt_0== 0).sum() / lt_0.shape[0]:.4f}")

#이탈자들의 date_modif_prod - date_activ
lt_1 = clean[clean["churn"]==1]["date_modif_prod"] - clean[clean["churn"]==1]["date_activ"]
print(f"이탈자 소요시간 0의 비율: {(lt_1== 0).sum() / lt_1.shape[0]:.4f}")
```
비이탈자 소요시간 0의 비율: 0.5034   
이탈자 소요시간 0의 비율: 0.4301
상품 수정까지의 소요시간이 7%p 차이나는 것을 확인

이를 고려하여 결측치를 채운다.
```
#이것을 고려하여 결측치를 채움
import numpy as np
lt_0_rat = 0.5034
lt_0_mean = 1432

lt_1_rat = 0.4301
lt_1_mean = 1266

#비이탈자에서 0의 비율만큼 0 할당 
mask = clean['date_modif_prod'].isna() & (clean['churn'] == 0)
na_idx = clean[mask].index
n_total = len(na_idx)
n_zero = int(n_total * lt_0_rat)
zero_idx = np.random.choice(na_idx, size=n_zero, replace=False)
clean.loc[zero_idx, 'date_modif_prod'] = 0

#비이탈자에서 나머지는 date_activ+평균으로 할당
mask = clean["date_modif_prod"].isna() & (clean["churn"] == 0)
clean.loc[mask, "date_modif_prod"] = clean.loc[mask, "date_activ"] + lt_0_mean


#이탈자에서 0의 비율만큼 0 할당 
mask = clean['date_modif_prod'].isna() & (clean['churn'] == 1)
na_idx = clean[mask].index
n_total = len(na_idx)
n_zero = int(n_total * lt_1_rat)
zero_idx = np.random.choice(na_idx, size=n_zero, replace=False)
clean.loc[zero_idx, 'date_modif_prod'] = 0

#비이탈자에서 나머지는 date_activ+평균으로 할당
mask = clean["date_modif_prod"].isna() & (clean["churn"] == 1)
clean.loc[mask, "date_modif_prod"] = clean.loc[mask, "date_activ"] + lt_1_mean
```

date_renewal은 특별한 특성이 없으니 데이터 조건을 만족하게끔 결측치 완성

데이터 조건 : ```date_activ, date_renewal <= date_end```
dr = (1- (dr-de / de-da)mean) *de
```
mean = ((clean["date_renewal"] - clean["date_end"]) / (clean["date_end"] - clean["date_activ"])).mean()
mask = clean["date_renewal"].isna()
clean.loc[mask, "date_renewal"] = ((1 - mean) * clean.loc[mask, "date_end"]).astype(int)
```

## 7. 데이터 증강 후 모델별 성능 비교

SMOTE으로 데이터를 증강한다.

```
TransformerWrapper(exclude=None, include=None, transformer=FixImbalancer(estimator=SMOTE(k_neighbors=5, random_state=42, sampling_strategy='auto')))
```
KNN, K=5 사용

| Description                 | Value            |
|:----------------------------|:-----------------|
| Session id                  | 42               |
| Target                      | churn            |
| Target type                 | Binary           |
| Original data shape         | (193002, 29)     |
| Transformed data shape      | (301351, 40)     |
| Transformed train set shape | (243450, 40)     |
| Transformed test set shape  | (57901, 40)      |
| Numeric features            | 24               |
| Categorical features        | 4                |
| Preprocess                  | True             |
| Imputation type             | simple           |
| Numeric imputation          | mean             |
| Categorical imputation      | mode             |
| Maximum one-hot encoding    | 25               |
| Encoding method             | None             |
| Fix imbalance               | True             |
| Fix imbalance method        | SMOTE            |
| Fold Generator              | StratifiedKFold  |
| Fold Number                 | 10               |
| Log Experiment              | False            |
| Experiment Name             | clf-default-name |
| USI                         | cbd6             |

최종 학습 데이터의 형태는 위와 같다.
XGBoost, CatBoost, LightGBM을 포함한 16종의 머신러닝의 성능을 비교한다.

| Model               | Accuracy |   AUC  | Recall | Precision |   F1   | Kappa  |  MCC   | TT (Sec) |
|:--------------------|---------:|-------:|-------:|----------:|-------:|-------:|-------:|---------:|
| KNN                 | 0.9996   | 1.0000 | 1.0000 | 0.9961    | 0.9980 | 0.9978 | 0.9978 |   3.386  |
| Random Forest       | 0.9999   | 1.0000 | 0.9993 | 0.9999    | 0.9988 | 0.9998 | 0.9996 |   6.533  |
| Extra Trees         | 0.9998   | 1.0000 | 0.9981 | 0.9999    | 0.9990 | 0.9989 | 0.9989 |   7.581  |
| Decision Tree       | 0.9985   | 0.9961 | 0.9931 | 0.9916    | 0.9924 | 0.9915 | 0.9915 |   1.033  |
| CatBoost            | 0.9941   | 0.9992 | 0.9822 | 0.9594    | 0.9707 | 0.9674 | 0.9675 |  44.064  |
| XGBoost             | 0.9649   | 0.9887 | 0.9132 | 0.7736    | 0.8375 | 0.8180 | 0.8216 |   1.647  |
| Dummy Classifier    | 0.9010   | 0.5000 | 0.0000 | 0.0000    | 0.0000 | 0.0000 | 0.0000 |   0.656  |
| LightGBM            | 0.8880   | 0.9285 | 0.7693 | 0.4608    | 0.5763 | 0.5164 | 0.5390 | 117.068  |
| Gradient Boosting   | 0.7546   | 0.7797 | 0.6388 | 0.2318    | 0.3401 | 0.2280 | 0.2723 |  10.997  |
| AdaBoost            | 0.6875   | 0.7233 | 0.6255 | 0.1836    | 0.2839 | 0.1544 | 0.2021 |   3.075  |
| LDA                 | 0.6108   | 0.6777 | 0.6426 | 0.1524    | 0.2464 | 0.1028 | 0.1514 |   1.468  |
| Ridge Classifier    | 0.6106   | 0.6777 | 0.6429 | 0.1524    | 0.2464 | 0.1028 | 0.1514 |   0.411  |
| SVM (Linear)        | 0.5563   | 0.5565 | 0.4962 | 0.1376    | 0.1653 | 0.0314 | 0.0470 |   1.827  |
| Logistic Regression | 0.5548   | 0.6182 | 0.6238 | 0.1315    | 0.2172 | 0.0641 | 0.1023 |   6.559  |
| Naive Bayes         | 0.2164   | 0.6026 | 0.9234 | 0.1054    | 0.1892 | 0.0140 | 0.0548 |   0.384  |
| QDA                 | 0.1449   | 0.5936 | 0.9863 | 0.1026    | 0.1859 | 0.0080 | 0.0557 |   1.069  |

autoML을 사용했다.

#### 07.21 추가
성능이 비정상적으로 높다.
전처리된 ml_case_training_data와 날짜별 가격변화를 담은 ml_case_training_hist_data 테이블을 merge하였는데,
이렇게 merge된 데이터가 트레이닝과 테스트셋에서 제대로 나뉘지 않은 것 같다.


## 8. 결과물을 이용한 마케팅의 가치 평가

### 📊 그래프 해석: 전반적인 구조

중요도 상위 3개:

1. **origin_up**...(원핫 인코딩) : 처음 가입한 전기 캠페인

2. **margin_net_pow_ele** : 전력 가입 순마진

3. **cons_last_month** :직전 월 소비량



**👉 즉, 상위 몇 개 feature가 전체 모델에 비해 상대적으로 더 많이 사용되거나 중요**

=======
$$
\frac{\text{예측 이윤}}{\text{정확하게 예측시 이윤}} = 
\frac{\text{실제이탈자 수 * 매출 - 총 마케팅비용 }}{\text{실제 이탈자 수 * (매출-마케팅비용)}}
$$


$$
\frac{TP * r  - ( TP + FP ) * c}{TP(r - c)}
$$ 

$$
= 1 - \frac{FP * c}  {TP(r - c)} \approx Recall
$$

따라서 Recall이 높은 모델을 목표로 진행한다.

## 6. EDA

결측치 70% 이상 칼럼 제거  
고객 회사 활동, 고객이 가입한 캠페인 칼럼은 오브젝트 형이므로 결측치를 새로운 카테고리로 분류한다.   

카테고리를 원핫 인코딩하면 카테고리간의 유사성을 고려하지 못한다.  
이를테면   
```관광업```과 ```머신러닝 사업``` 간의 거리 = ```머신러닝 사업```과 ```딥러닝 사업```간의 거리  
로 인식하게 된다.  
따라서 카테고리는 단어의 유사성을 반영하느 워드 임베딩한다.  

날짜를 정수로 변환  

date_end 칼럼의 결측치 : ```계약시작일``` + ```평균 계약기간```으로 설정
```
이탈 = clean[clean['churn'] == 1]
유지 = clean[clean['churn'] == 0]

m = int((유지["date_end"] - 유지["date_activ"]).mean())
mask = clean["date_end"].isna()
clean.loc[mask, "date_end"] = clean.loc[mask, "date_activ"] + m
```
날짜 칼럼들은 데이터 제약 조건이 있다.  
예를들어 계약 시작일은 반드시 계약 종료일보다 빨라야한다.  
이러한 데이터 제약조건을 만족하면서 결측치를 채운다.  

이 데이터셋의 조건은
> date_activ, date_renewal <= date_end

날짜형 칼럼만 살펴본다.
|   | date_activ | date_end | date_modif_prod | date_renewal |
|---|------------|----------|-----------------|--------------|
| 0 | 4694       | 6154     | 4694            | 5791         |
| 1 | 4914       | 6010     | <NA>            | 5652         |
| 2 | 3520       | 6086     | 3520            | 5721         |
| 3 | 3758       | 5950     | 3758            | 5585         |
| 4 | 3741       | 5933     | 3741            | 5568         |

date_activ와 date_modif_prod가 같은 데이터들이 간혹 있다.
```
#비이탈자들의 date_modif_prod - date_activ
lt_0 = clean[clean["churn"]==0]["date_modif_prod"] - clean[clean["churn"]==0]["date_activ"]
print(f"비이탈자 소요시간 0의 비율: {(lt_0== 0).sum() / lt_0.shape[0]:.4f}")

#이탈자들의 date_modif_prod - date_activ
lt_1 = clean[clean["churn"]==1]["date_modif_prod"] - clean[clean["churn"]==1]["date_activ"]
print(f"이탈자 소요시간 0의 비율: {(lt_1== 0).sum() / lt_1.shape[0]:.4f}")
```
비이탈자 소요시간 0의 비율: 0.5034   
이탈자 소요시간 0의 비율: 0.4301
상품 수정까지의 소요시간이 7%p 차이나는 것을 확인

이를 고려하여 결측치를 채운다.
```
#이것을 고려하여 결측치를 채움
import numpy as np
lt_0_rat = 0.5034
lt_0_mean = 1432

lt_1_rat = 0.4301
lt_1_mean = 1266

#비이탈자에서 0의 비율만큼 0 할당 
mask = clean['date_modif_prod'].isna() & (clean['churn'] == 0)
na_idx = clean[mask].index
n_total = len(na_idx)
n_zero = int(n_total * lt_0_rat)
zero_idx = np.random.choice(na_idx, size=n_zero, replace=False)
clean.loc[zero_idx, 'date_modif_prod'] = 0

#비이탈자에서 나머지는 date_activ+평균으로 할당
mask = clean["date_modif_prod"].isna() & (clean["churn"] == 0)
clean.loc[mask, "date_modif_prod"] = clean.loc[mask, "date_activ"] + lt_0_mean


#이탈자에서 0의 비율만큼 0 할당 
mask = clean['date_modif_prod'].isna() & (clean['churn'] == 1)
na_idx = clean[mask].index
n_total = len(na_idx)
n_zero = int(n_total * lt_1_rat)
zero_idx = np.random.choice(na_idx, size=n_zero, replace=False)
clean.loc[zero_idx, 'date_modif_prod'] = 0

#비이탈자에서 나머지는 date_activ+평균으로 할당
mask = clean["date_modif_prod"].isna() & (clean["churn"] == 1)
clean.loc[mask, "date_modif_prod"] = clean.loc[mask, "date_activ"] + lt_1_mean
```

date_renewal은 특별한 특성이 없으니 데이터 조건을 만족하게끔 결측치 완성

데이터 조건 : ```date_activ, date_renewal <= date_end```
dr = (1- (dr-de / de-da)mean) *de
```
mean = ((clean["date_renewal"] - clean["date_end"]) / (clean["date_end"] - clean["date_activ"])).mean()
mask = clean["date_renewal"].isna()
clean.loc[mask, "date_renewal"] = ((1 - mean) * clean.loc[mask, "date_end"]).astype(int)
```

## 7. 데이터 증강 후 모델별 성능 비교

SMOTE으로 데이터를 증강한다.

```
TransformerWrapper(exclude=None, include=None, transformer=FixImbalancer(estimator=SMOTE(k_neighbors=5, random_state=42, sampling_strategy='auto')))
```
KNN, K=5 사용

| Description                 | Value            |
|:----------------------------|:-----------------|
| Session id                  | 42               |
| Target                      | churn            |
| Target type                 | Binary           |
| Original data shape         | (193002, 29)     |
| Transformed data shape      | (301351, 40)     |
| Transformed train set shape | (243450, 40)     |
| Transformed test set shape  | (57901, 40)      |
| Numeric features            | 24               |
| Categorical features        | 4                |
| Preprocess                  | True             |
| Imputation type             | simple           |
| Numeric imputation          | mean             |
| Categorical imputation      | mode             |
| Maximum one-hot encoding    | 25               |
| Encoding method             | None             |
| Fix imbalance               | True             |
| Fix imbalance method        | SMOTE            |
| Fold Generator              | StratifiedKFold  |
| Fold Number                 | 10               |
| Log Experiment              | False            |
| Experiment Name             | clf-default-name |
| USI                         | cbd6             |

최종 학습 데이터의 형태는 위와 같다.
XGBoost, CatBoost, LightGBM을 포함한 16종의 머신러닝의 성능을 비교한다.

| Model               | Accuracy |   AUC  | Recall | Precision |   F1   | Kappa  |  MCC   | TT (Sec) |
|:--------------------|---------:|-------:|-------:|----------:|-------:|-------:|-------:|---------:|
| KNN                 | 0.9996   | 1.0000 | 1.0000 | 0.9961    | 0.9980 | 0.9978 | 0.9978 |   3.386  |
| Random Forest       | 0.9999   | 1.0000 | 0.9993 | 0.9999    | 0.9988 | 0.9998 | 0.9996 |   6.533  |
| Extra Trees         | 0.9998   | 1.0000 | 0.9981 | 0.9999    | 0.9990 | 0.9989 | 0.9989 |   7.581  |
| Decision Tree       | 0.9985   | 0.9961 | 0.9931 | 0.9916    | 0.9924 | 0.9915 | 0.9915 |   1.033  |
| CatBoost            | 0.9941   | 0.9992 | 0.9822 | 0.9594    | 0.9707 | 0.9674 | 0.9675 |  44.064  |
| XGBoost             | 0.9649   | 0.9887 | 0.9132 | 0.7736    | 0.8375 | 0.8180 | 0.8216 |   1.647  |
| Dummy Classifier    | 0.9010   | 0.5000 | 0.0000 | 0.0000    | 0.0000 | 0.0000 | 0.0000 |   0.656  |
| LightGBM            | 0.8880   | 0.9285 | 0.7693 | 0.4608    | 0.5763 | 0.5164 | 0.5390 | 117.068  |
| Gradient Boosting   | 0.7546   | 0.7797 | 0.6388 | 0.2318    | 0.3401 | 0.2280 | 0.2723 |  10.997  |
| AdaBoost            | 0.6875   | 0.7233 | 0.6255 | 0.1836    | 0.2839 | 0.1544 | 0.2021 |   3.075  |
| LDA                 | 0.6108   | 0.6777 | 0.6426 | 0.1524    | 0.2464 | 0.1028 | 0.1514 |   1.468  |
| Ridge Classifier    | 0.6106   | 0.6777 | 0.6429 | 0.1524    | 0.2464 | 0.1028 | 0.1514 |   0.411  |
| SVM (Linear)        | 0.5563   | 0.5565 | 0.4962 | 0.1376    | 0.1653 | 0.0314 | 0.0470 |   1.827  |
| Logistic Regression | 0.5548   | 0.6182 | 0.6238 | 0.1315    | 0.2172 | 0.0641 | 0.1023 |   6.559  |
| Naive Bayes         | 0.2164   | 0.6026 | 0.9234 | 0.1054    | 0.1892 | 0.0140 | 0.0548 |   0.384  |
| QDA                 | 0.1449   | 0.5936 | 0.9863 | 0.1026    | 0.1859 | 0.0080 | 0.0557 |   1.069  |

autoML을 사용했다.



## 8. 결과물을 이용한 마케팅의 가치 평가

### 📊 그래프 해석: 전반적인 구조

중요도 상위 3개:

1. **origin_up**...(원핫 인코딩) : 처음 가입한 전기 캠페인

2. **margin_net_pow_ele** : 전력 가입 순마진

3. **cons_last_month** :직전 월 소비량



**👉 즉, 상위 몇 개 feature가 전체 모델에 비해 상대적으로 더 많이 사용되거나 중요**

>>>>>>> p2/main



> origin_up...(원핫 인코딩) : 처음 가입한 전기 캠페인<br>

![스크린샷 2025-07-11 15.49.40.png](attachment:85930c09-30cd-43a4-9f29-7c0c45cba886.png)

**👉 3개 변수들만 이탈 -> 해당 경로로 유입된 고객들에게만 추가 할인 혹은 나머지 두개의 경로로 가입하도록 유도**



> 2. margin_net_pow_ele : 전력 가입 순마진<br>

![스크린샷 2025-07-11 15.50.04.png](attachment:42455153-7525-4f52-961d-1fa2169150a8.png)



**👉 1구간 고객(고마진 고객) 들의 이탈 비율 높음 : 이탈 안되도록 관리 전략 시급. 맞춤형 혜택 제공**

**👉 5구간 고객(저마진 고객) 들의 이탈 비율 낮음 : 이유 파악 필요. 혜택 과잉 여부 분석, 가격 인상 고려**


> 3. cons_last_month : 직전 월 소비량<br>

![스크린샷 2025-07-11 15.50.25.png](attachment:abd289d3-f124-4c3b-ac4c-f82b552ac139.png)


**👉 사용량 많은 고객 → 이탈 거의 없음 → 우수 고객 or 고정 사용자층 : 맞춤 혜택 유지, 이탈 방지 우선 대상**

**👉 사용량 적은 고객 → 이탈 많음 → 전환 준비, 만족도 낮음, 또는 단기 고객 가능성 : 타겟 리마케팅 or 미끼 상품 제안 고려**



 **‼️추가 주의 사항**

![image.png](attachment:61d4f135-3ee7-4aaf-8213-3e613fb4ec6d.png)

**👉 할인 캠페인 시 discount level 5~10 구간은 피하도록 권고**