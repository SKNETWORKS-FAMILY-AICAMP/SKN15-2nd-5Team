# SKN15-2nd-5Team (전기 요금 기반 이탈 예측)

##  팀명: 오원장과 아이들

# 1. 팀 소개
| 오원장 | 권도원 | 유의정 | 조솔찬 | 홍민식 |
|--|--|--|--|--|
| @AQUAQUA5 | @dowonk120 | @Rr-EJ | @solchna | @minnnsik |
|  |
| Project Leader |  |  |  |  |



# 2. 프로젝트 기간 🏆
###  25년 07월 10일 (목요일) ~ 25년 07월 11일 (금요일) 



# 3. 프로젝트 개요 💡
- 목적: 이 프로젝트의 궁극적 목적은 PowerCo 고객 이탈(Churn) 예측을 통해 회사의 매출 손실을 최소화하고, 
  효율적인 고객 유지(Retention) 전략을 수립하기 위함입니다.
- 데이터 출처: [Kaggle - PowerCo dataset Prediction]
(https://www.kaggle.com/datasets/naiborhujosua/energy-industry)
- 데이터 구성: 총 42개 컬럼, (16,096명 최근 12개월 전력 소비량, 서비스시작일,서비스 종료일, 이탈여부 등)


##  프로젝트명


## ✅ 프로젝트 배경 및 목적

파워코(PowerCo)는 BCG의 클라이언트로, 중소기업(SME)과 주거 고객에게 가스와 전기를 공급하는 에너지 회사입니다.  
최근 유럽 시장의 전력 자유화(Power Liberalization)와 가격 경쟁 심화로, 특히 SME 고객층에서 고객 이탈(Churn)률이 증가하고 있습니다.

<img width="659" alt="reuter-1" src="https://github.com/user-attachments/assets/eda46139-5a46-462e-b157-9920afbfc204" />

*Figure 1. Europe’s power price divide hits southeastern economies (Reuters, 2025년 4월 24일)*

### 주요 배경 현황

- **계절별 요금 급등기(성수기) 부담에 따른 이탈 증가**  
  여름·겨울 수요 집중 시기에 요금이 20% 이상 급등하는 고객은 ‘요금 충격’으로 계약 갱신을 주저하며,  
  이 시기 급등 그룹의 이탈률은 20~25%로 가장 높게 나타납니다.

- **변동 단가 불안정성에 따른 예측 불가능성 거부감**  
  요금 변동 폭이 큰 고객은 다음 달 청구액 불확실성에 불안감을 느끼며,  
  평균 대비 약 1.5배 높은 이탈률을 보입니다. 이들은 주로 타사 이동 또는 요금제 변경을 선택합니다.

- **3개월 이동평균 요금 상승 추세와 이탈 가능성**  
  지속적인 요금 상승 추세는 고객의 이탈 결정을 촉진합니다.  
  반면, 일시적 상승 후 요금이 하락하는 고객은 이를 계절적 현상으로 인지해 계약 유지율이 높습니다.


이탈의 핵심 원인 중 하나로 **고객의 가격 민감도**가 지목됩니다.  
요금 급등과 변동성 높은 요금 구조가 고객 불만과 이탈을 유발하는 주요 요인으로 분석되며,  
파워코는 이탈 위험 고객에게 20% 할인 등 맞춤형 마케팅을 제공해 고객 유지율을 높이고자 합니다.


### 프로젝트 목표

- 고객의 계약, 이용 패턴, 요금, 마진, 마케팅 이력 등 다양한 특성과 이탈 간 관계를 데이터 기반으로 분석  
- 고객 이탈 확률(Churn Probability)을 예측하는 분류 모델 개발  
- 예측 결과를 활용해 효과적인 마케팅 전략(예: 할인 캠페인 타겟팅) 수립에 필요한 인사이트 도출


 
# 4. 기술 스택
### AI & 데이터 처리

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
[](https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white)![](https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white)![](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)![](https://img.shields.io/badge/scikitlearn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)



### 머신러닝 모델
![](https://img.shields.io/badge/RandomForest-00B050?style=for-the-badge)![](https://img.shields.io/badge/DecisionTree-228B22?style=for-the-badge)![](https://img.shields.io/badge/XGBoost-EC0000?style=for-the-badge&logo=xgboost&logoColor=white)![](https://img.shields.io/badge/LightGBM-3C3C3C?style=for-the-badge&logo=lightgbm&logoColor=white) ![](https://img.shields.io/badge/CatBoost-FFCC00?style=for-the-badge)

![](https://img.shields.io/badge/SGDClassifier-006699?style=for-the-badge)![](https://img.shields.io/badge/Logistic%20Regression-1E90FF?style=for-the-badge)![](https://img.shields.io/badge/SVM-8A2BE2?style=for-the-badge)

### 버전 관리 및 협업

![](https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white) ![](https://img.shields.io/badge/discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)



# 5. 데이터셋 소개

본 프로젝트에서는 **Kaggle PowerCo 고객 이탈 예측** 데이터셋을 활용하였습니다.  
이 데이터는 유럽 지역 SME(중소기업)와 주거용 고객을 대상으로 전기·가스를 공급하는 PowerCo사의 실제 거래 및 이탈 이력 데이터를 기반으로 합니다.

PowerCo는 전력 시장 자유화, 가격 민감도 증가 등 환경 변화로 인해 고객 이탈(Churn) 가능성이 높아진 상황에서,  
이탈 예측 모델링을 통해 "이탈 위험 고객"에게 20% 할인 등 차별적 마케팅 전략을 적용할지 판단하고자 합니다.

데이터셋은 다음 세 개의 주요 파일로 구성되어 있습니다.

- **ml_case_training_data.csv**  
    - 고객 기본 정보, 계약, 사용량, 예상 요금, 마진, 마케팅 이력 등 다양한 변수(32개 컬럼) 포함  
    - 예: 고객ID, 업종코드, 채널, 연간/월간 소비량, 계약일·종료일·갱신일, 전기/가스 이용여부, 예상 매출·마진, 제품 수, 순마진 등  

- **ml_case_training_hist_data.csv**  
    - 고객별 월별 계약 가격 정보(변동단가·고정단가 포함) 제공  
    - 예: 고객ID, 가격적용월, 기간별 변동/고정 단가 등  

- **ml_case_training_output.csv**  
    - 타겟 변수인 고객 이탈 여부(3개월 이내 이탈: 1, 유지: 0) 포함  

세 파일 모두 고객 고유 ID(`id`)를 기준으로 연결되며,  
고객별 이탈 여부 및 월별 가격 정보까지 결합해 분석에 활용합니다.


이 데이터셋을 통해  
- 고객의 이용 패턴, 가격, 마진, 마케팅 이력 등 다양한 특성과 이탈 간 관계를 분석하고,  
- 고객 이탈 확률(Churn Probability)을 예측하는 모델을 개발하며,  
- 예측 결과를 바탕으로 맞춤형 마케팅 전략 수립에 필요한 인사이트 도출을 목표로 합니다.


# 6. 주요 변수 소개 

PowerCo 프로젝트의 원본 데이터는 크게 **Train_data**, **Hist_data**, **Output_data** 세 부분으로 구성됩니다.  
아래 표는 핵심 컬럼별 데이터 타입·설명과 함께 “카디널리티(고유값 개수), 결측 비율(%), 결측 처리 방식”을 정리한 것입니다.

---

### 6.1 Train_data (고객별 프로필·예측 정보)

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

### 6.2 Hist_data (월별 소비·단가 시계열)

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

### 6.3 Output_data (타깃)

| 컬럼명 | 데이터 타입 | 설명                          | 카디널리티 | 결측 비율 | 결측 처리 방식 |
|-------|-------------|-------------------------------|-----------:|---------:|---------------|
| id    | object      | 고객 고유 식별자              |     16 096 |     0.00% | n/a           |
| churn | int64       | 이탈 여부 (0 = 유지, 1 = 이탈) |           2 |     0.00% | n/a           |

이 세 테이블을 고객 id 기준으로 결합해, 과거 소비·요금 패턴과 프로필 정보를 바탕으로 고객 이탈(churn)을 예측하는 것이 본 프로젝트의 핵심 목표입니다.





# 7. 분포 소개

- **범주형 데이터**


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

# 8. 같거나 비슷한 데이터셋의 기존 사례와 정확도 소개
<table border="1" cellspacing="0" cellpadding="8" style="border-collapse: collapse; width: 100%; font-family: Arial, sans-serif;">
  <thead style="background-color: #f2f2f2;">
    <tr>
      <th>No.</th>
      <th>데이터셋</th>
      <th>설명</th>
      <th>EDA 요약</th>
      <th>모델</th>
      <th>성능</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td><strong>PowerCo</strong></td>
      <td>전체 고객 중 약 10% 이탈<br>채널·상품·가입기간별 분석</td>
      <td>- 결측치 다수 컬럼 제거, 나머지는 bfill/최빈값 처리<br>- 이상치 및 음수값 처리<br>- 타입 정제, 클린 데이터 구축</td>
      <td>XGBClassifier<br>RandomForest</td>
      <td>
        Accuracy: <strong>0.981</strong><br>
        Precision: <strong>0.9989</strong><br>
        Recall: <strong>0.8080</strong>
      </td>
    </tr>
    <tr>
      <td>2</td>
      <td><strong>Bank Churn (1)</strong></td>
      <td>신용카드 고객 이탈 여부 예측</td>
      <td>- 결측치 처리, 비수치형 인코딩<br>- 분포/이탈률 시각화<br>- 군집 분석, 상관관계 시각화</td>
      <td>Random Forest<br>AdaBoost<br>SVM</td>
      <td>(EDA 중심, 모델 성능 미기재)</td>
    </tr>
    <tr>
      <td>3</td>
      <td><strong>Bank Churn (2)</strong></td>
      <td>신용카드 고객 이탈 여부 예측</td>
      <td>- 결측치 처리<br>- 클래스 불균형 SMOTE 적용<br>- 분포 시각화 및 인코딩 수행</td>
      <td>H2O GBM<br>LightGBM, XGBoost<br>로지스틱 회귀 등</td>
      <td>(AUC 기준 성능 우수)</td>
    </tr>
    <tr>
      <td>4</td>
      <td><strong>Bank Churn (3)</strong></td>
      <td>신용카드 고객 이탈 여부 예측</td>
      <td>- 전처리 파이프라인 구성<br>- 클러스터링 후 피처 추가<br>- PCA 기반 차원 축소</td>
      <td>CatBoost, XGBoost<br>LightGBM (앙상블)</td>
      <td>(정량적 성능 미기재)</td>
    </tr>
    <tr>
      <td>5</td>
      <td><strong>Telco Churn</strong></td>
      <td>통신사 고객 이탈 여부 예측</td>
      <td>- 결측치/이상치/중복 제거<br>- 인코딩 및 시각화<br>- 계약 유형, 요금 분석, SMOTE 적용</td>
      <td>Random Forest<br>SVM, KNN (Best), AdaBoost 등</td>
      <td>
        Accuracy: <strong>0.898</strong><br>
        Precision: 0.650<br>
        Recall: 0.0426
      </td>
    </tr>
    <tr>
      <td>6</td>
      <td><strong>PowerCo (다른 소스)</strong></td>
      <td>다른 코드 기반, 최신 기법 적용</td>
      <td>- 파생 변수 생성<br>- PCA 및 로그 변환<br>- 상관관계 분석 및 정제</td>
      <td>Random Forest<br>Naive Bayes, SVM</td>
      <td>
        Accuracy: <strong>0.950</strong><br>
        Recall: <strong>0.91</strong><br>
        F2-score: <strong>0.93</strong>
      </td>
    </tr>
  </tbody>
</table> 


# 9. 탐색적 데이터 분석 (EDA) 피처 엔지니어링 📂🧹

---

## 9.1 결측치 & 이상치 점검

- **결측치 매트릭스**  
  ![](./plots/missing_matrix.png)  
  - `activity_new`, `campaign_disc_ele` 등 주요 범주형 변수에 50% 이상 결측  
  - `date_first_activ` 약 78% 결측 → 분석 제외 혹은 별도 처리 필요  

- **수치형 분포 살펴보기**  
  - `cons_12m` 히스토그램 & 박스플롯  
    - 우측 꼬리(long tail) 분포, 상위 1% 이상치 확인  
  - `imp_cons`·`forecast_cons` 박스플롯  
    - 소수점 분포 및 극단치 시각화  

- **범주형 빈도 분석**  
  ![](./plots/channel_sales_count.png)  
  - `channel_sales` 상위 3개(online, branch, phone) 합계 약 70%  
  - 기타 채널 병합(“other”) 고려  

- **상관관계 히트맵**  
  ![](./plots/corr_heatmap.png)  
  - `cons_12m` ↔ `forecast_cons_12m` 상관도 0.85 (예측치 신뢰도 검증)  
  - 가격 단가 변수와 churn 간 상관도 거의 없음  


## 9.2 계절성 & 날짜 기반 피처

| 피처명                   | 설명                                                        |
|-------------------------|-------------------------------------------------------------|
| `month_sin`, `month_cos` | 월을 순환형(sinusoidal)으로 인코딩 → 계절별 churn 패턴 포착    |
| `days_since_renewal`    | 오늘 기준 갱신 후 경과 일수                                  |
| `days_to_end`           | 오늘 기준 계약 종료까지 남은 일수                            |

---

## 9.3 변동성 & 추세 피처

| 피처명                     | 설명                                                       |
|---------------------------|------------------------------------------------------------|
| `price_var_std`           | 3구간 가변 단가(`price_p1_var`~`price_p3_var`) 표준편차 → 요금 변동성 |
| `price_fix_std`           | 3구간 고정 단가(`price_p1_fix`~`price_p3_fix`) 표준편차 → 고정 단가 변동성 |
| `cons_3m_ma`, `cons_6m_ma` | 최근 3·6개월 사용량 이동평균 → 중기 소비 추세 반영         |

---

## 9.4 요금 충격 & 상호작용 피처

- **`bill_pct_change`**  
  ```text
  (imp_cons − forecast_base_bill_ele) / forecast_base_bill_ele


# 10.오토ml을 통한 여러 모델의 성능 비교 
<table class="model-metrics">
  <thead>
    <tr>
      <th>Model</th>
      <th>Accuracy</th>
      <th>AUC</th>
      <th>Recall</th>
      <th>Precision</th>
      <th>F1</th>
      <th>Kappa</th>
      <th>MCC</th>
      <th>TT (Sec)</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Random Forest</td><td>0.9999</td><td>1.0000</td><td>0.9993</td><td>0.9999</td><td>0.9996</td><td>0.9996</td><td>0.9996</td><td>6.533</td></tr>
    <tr><td>Extra Trees</td><td>0.9998</td><td>1.0000</td><td>0.9981</td><td>0.9999</td><td>0.9990</td><td>0.9989</td><td>0.9989</td><td>7.581</td></tr>
    <tr><td>KNN</td><td>0.9996</td><td>1.0000</td><td>1.0000</td><td>0.9961</td><td>0.9980</td><td>0.9978</td><td>0.9978</td><td>3.386</td></tr>
    <tr><td>Decision Tree</td><td>0.9985</td><td>0.9961</td><td>0.9931</td><td>0.9916</td><td>0.9924</td><td>0.9915</td><td>0.9915</td><td>1.033</td></tr>
    <tr><td>CatBoost</td><td>0.9941</td><td>0.9992</td><td>0.9822</td><td>0.9594</td><td>0.9707</td><td>0.9674</td><td>0.9675</td><td>44.064</td></tr>
    <tr><td>XGBoost</td><td>0.9649</td><td>0.9887</td><td>0.9132</td><td>0.7736</td><td>0.8375</td><td>0.8180</td><td>0.8216</td><td>1.647</td></tr>
    <tr><td>Dummy Classifier</td><td>0.9010</td><td>0.5000</td><td>0.0000</td><td>0.0000</td><td>0.0000</td><td>0.0000</td><td>0.0000</td><td>0.656</td></tr>
    <tr><td>LightGBM</td><td>0.8880</td><td>0.9285</td><td>0.7693</td><td>0.4608</td><td>0.5763</td><td>0.5164</td><td>0.5390</td><td>117.068</td></tr>
    <tr><td>Gradient Boosting</td><td>0.7546</td><td>0.7797</td><td>0.6388</td><td>0.2318</td><td>0.3401</td><td>0.2280</td><td>0.2723</td><td>10.997</td></tr>
    <tr><td>AdaBoost</td><td>0.6875</td><td>0.7233</td><td>0.6255</td><td>0.1836</td><td>0.2839</td><td>0.1544</td><td>0.2021</td><td>3.075</td></tr>
    <tr><td>LDA</td><td>0.6108</td><td>0.6777</td><td>0.6426</td><td>0.1524</td><td>0.2464</td><td>0.1028</td><td>0.1514</td><td>1.468</td></tr>
    <tr><td>Ridge Classifier</td><td>0.6106</td><td>0.6777</td><td>0.6429</td><td>0.1524</td><td>0.2464</td><td>0.1028</td><td>0.1514</td><td>0.411</td></tr>
    <tr><td>SVM (Linear)</td><td>0.5563</td><td>0.5565</td><td>0.4962</td><td>0.1376</td><td>0.1653</td><td>0.0314</td><td>0.0470</td><td>1.827</td></tr>
    <tr><td>Logistic Regression</td><td>0.5548</td><td>0.6182</td><td>0.6238</td><td>0.1315</td><td>0.2172</td><td>0.0641</td><td>0.1023</td><td>6.559</td></tr>
    <tr><td>Naive Bayes</td><td>0.2164</td><td>0.6026</td><td>0.9234</td><td>0.1054</td><td>0.1892</td><td>0.0140</td><td>0.0548</td><td>0.384</td></tr>
    <tr><td>QDA</td><td>0.1449</td><td>0.5936</td><td>0.9863</td><td>0.1026</td><td>0.1859</td><td>0.0080</td><td>0.0557</td><td>1.069</td></tr>
  </tbody>
</table>



# 8. 머신러닝 모델링 🤖📈



# 9. 수행결과(분석 및 예측 결과) 🧪

<h3 style="color:#2C3E50; text-align:center; font-size: 1.2em;">  ⚡️ PowerCo hist_data 데이터 셋 설명  </h3>
<table style="width:100%; border-collapse: collapse; margin: 15px 0; font-family: 'NanumGothic', sans-serif; font-size: 0.85em;">       


            







---

## 📈 성능 시각화

### 1) 전체 모델 Recall 비교  

<img width="1384" height="584" alt="Model Performance Recall Emphasized " src="https://github.com/user-attachments/assets/b47833ad-c047-470c-afc4-67af69e852e2" />

---

### 2) Top 10 모델 Recall 순위  
<img width="984" height="584" alt="TOP 10 model Recall compare " src="https://github.com/user-attachments/assets/86b4a06f-0101-4c55-b142-ac1fb11c11f6" />

---

### 3) XGBoost Feature Importance  
<img width="989" height="790" alt="XGBoost Feature importance" src="https://github.com/user-attachments/assets/a919684d-42b5-43e2-87fb-ffaa064bca94" />


---



### ✨ 핵심 인사이트

- **Recall 개선 효과**  
  - 개선 전 XGBoost는 Recall 0.81 → “이탈 고객 19% 놓침”  
  - 개선 후 KNN 등은 Recall 0.99 이상 → “거의 모든 이탈 고객 포착”  
- **Precision–Recall 균형**  
  - F1-Score가 0.89 → 0.99로 상승  
  - “거짓 경보(FP)는 소폭 증가하더라도, 놓치는 이탈(FN)을 크게 줄였다”  
- **ROC-AUC 완전 개선**  
  - 다양한 앙상블 모델들이 1.00 근접 → 임계값 전반 성능 탁월  





# 10. 🪞 한 줄 회고 🧠💬

> 🧹 **오원장**: ""
>  
> 🤖 **권도원**: ""
> 
> 💻 **유의정**: ""
> 
> 📊 **조솔찬**: ""
>
> 🐵 **홍민식**: ""
> 

