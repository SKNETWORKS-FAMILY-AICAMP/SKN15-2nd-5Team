# SKN15-2nd-5Team (전기 요금 기반 이탈 예측)

##  팀명: 

# 1. 팀 소개
| 오원장 | 권도원 | 유의정 | 조솔찬 | 홍민식 |
|--|--|--|--|--|
| @AQUAQUA5 | @dowonk120 | @Rr-EJ | @solchna | @minnnsik |
|  |
| Project Leader |  |  |  |  |

ㅇd

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
1. 계절별 요금 급등기(성수기)부담 -> 이탈 증가  
   여름(7~8월)이나 겨울(12월)처럼 수요가 몰리는 시기에 요금이 20% 이상 오르는 고객은 ‘요금 충격’을 받아
   계약 갱신을 망설이기 쉽습니다. 실제로 이 시기에 요금이 크게 오르는 그룹의 이탈률은 2025%로 가장 높게 나타    났습니다.
    
 2. 변동 단가의 불안정성 → 예측 불가능성에 대한 거부감
    고정 요금은 비교적 안정적이지만, 요금이 심하게 오르내리는 고객은 “다음 달 청구액이 얼마나 될지 모른다”는
    불안감을 느낍니다. 변동 폭이  큰 그룹의 이탈률은 평균보다 약 1.5배 높게 관찰되었으며, 이들은 주로 다른
    회사로 이동하거나 요금제를 변경하는 경향을 보였습니다.

 
 3. 이동평균으로 본 중기 방향성 → 지속 상승 시 이탈 가능성↑
    3개월 평균 요금이 꾸준히 오르는 추세를 보이면, 고객은 “앞으로도 계속 오를 것 같다”고 생각해 미리 이탈을
    결정합니다. 반면, 일시적으로 요금이 오르고 다시 내려오는 패턴을 경험한 고객은 이를 계절적 현상으로
    받아들이고  계약을 유지하는 비율이 상대적으로 높았습니다.



 <img width="659" alt="reuter-1 " src="https://github.com/user-attachments/assets/eda46139-5a46-462e-b157-9920afbfc204" />

Figure 1. Europe’s power price divide hits southeastern economies Source: Reuters. (2025, April 24). Title of article.
 
 
 
 <img width="659" alt="reuter-2" src="https://github.com/user-attachments/assets/dd27f639-fc10-49c9-af2e-0f12efbb6380" />

 Figure 2. Europe's economic woes may worsen as key power prices rise: Maguire Source: Reuters (2025 November 20). Title of article.
 
 
 
 <img width="659" alt="reuter-3" src="https://github.com/user-attachments/assets/a6f6b099-ef1e-47b5-ab7d-b09ad1539c7e" />
 Figure 3. Europe’s power price divide hits southeastern economies Source: Reuters (2025 January 7). Title of article.



## 🖐️ 프로젝트 소개





## ❤️ 기대효과

## 👤 대상 사용자



# 4. 기술 스택
### AI & 데이터 처리

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
[](https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white)![](https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white)![](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)![](https://img.shields.io/badge/scikitlearn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)



### 머신러닝 모델
![](https://img.shields.io/badge/RandomForest-00B050?style=for-the-badge)![](https://img.shields.io/badge/DecisionTree-228B22?style=for-the-badge)![](https://img.shields.io/badge/XGBoost-EC0000?style=for-the-badge&logo=xgboost&logoColor=white)![](https://img.shields.io/badge/LightGBM-3C3C3C?style=for-the-badge&logo=lightgbm&logoColor=white) ![](https://img.shields.io/badge/CatBoost-FFCC00?style=for-the-badge)

![](https://img.shields.io/badge/SGDClassifier-006699?style=for-the-badge)![](https://img.shields.io/badge/Logistic%20Regression-1E90FF?style=for-the-badge)![](https://img.shields.io/badge/SVM-8A2BE2?style=for-the-badge)

### 버전 관리 및 협업

![](https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white) ![](https://img.shields.io/badge/discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)




# 5. 데이터 설명 🧐 

# 6. 데이터 분석 및 전처리 📂🧹


# 7. EDA(탐색적 데이터 분석)** 📊🔍



# 8. 머신러닝 모델링 🤖📈



# 9. 수행결과(분석 및 예측 결과) 🧪

<h3 style="color:#2C3E50; text-align:center; font-size: 1.2em;">  ⚡️ PowerCo hist_data 데이터 셋 설명  </h3>
<table style="width:100%; border-collapse: collapse; margin: 15px 0; font-family: 'NanumGothic', sans-serif; font-size: 0.85em;">       


| 결측 유무 | 칼럼명           | 의미                     | 타입      | 단위         |
|---------:|-----------------|-------------------------|-----------|--------- |
|        0 | price_date      | 청구 기준일              | object    | –        |
|     1359 | price_p1_var    | 1구간 에너지 단가        | float64   | €/kWh   |
|     1359 | price_p2_var    | 2구간 에너지 단가        | float64   | €/kWh   |
|     1359 | price_p3_var    | 3구간 에너지 단가        | float64   | €/kWh   |
|     1359 | price_p1_fix    | 1구간 전력 고정 단가     | float64   | €/kWh   |
|     1359 | price_p2_fix    | 2구간 전력 고정 단가     | float64   | €/kWh   |
|     1359 | price_p3_fix    | 3구간 전력 고정 단가     | float64   | €/kWh   |
|        0 | cons_12m        | 최근 12개월 전기 사용량  | int64     | kWh       |
|        0 | cons_gas_12m    | 최근 12개월 가스 사용량  | int64     | m³        |
|        0 | cons_last_month | 직전 월 전기 사용량      | int64     | kWh       |

            





<h3 style="color:#2C3E50; text-align:center; font-size: 1.2em;">📊 PowerCo 데이터셋 결측치 분석</h3>
<div style="overflow-x:auto;">
<table style="width:100%; border-collapse: collapse; margin: 15px 0; font-family: 'NanumGothic', sans-serif; font-size: 0.85em;">
    <thead>
        <tr style="background-color:#E0F2F7; color:#2C3E50;">
            <th style="padding: 7px; border: 1px solid #ddd; text-align: center;">결측<br>유무</th>
            <th style="padding: 7px; border: 1px solid #ddd; text-align: left;">칼럼명</th>
            <th style="padding: 7px; border: 1px solid #ddd; text-align: left;">의미</th>
            <th style="padding: 7px; border: 1px solid #ddd; text-align: left;">타입</th>
            <th style="padding: 7px; border: 1px solid #ddd; text-align: left;">단위</th>
            <th style="padding: 7px; border: 1px solid #ddd; text-align: center;">결측치<br>비율</th>
            <th style="padding: 7px; border: 1px solid #ddd; text-align: center;">카디널리티</th>
            <th style="padding: 7px; border: 1px solid #ddd; text-align: left;">해결 방안</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd; font-weight:bold;">activity_new</td>
            <td style="padding: 5px; border: 1px solid #ddd;">회사 활동 카테고리</td>
            <td style="padding: 5px; border: 1px solid #ddd;">object</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; background-color:#FFEBEE;">59.30%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">4</td>
            <td style="padding: 5px; border: 1px solid #ddd;">새 카테고리</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd; font-weight:bold;">campaign_disc_ele</td>
            <td style="padding: 5px; border: 1px solid #ddd;">고객이 마지막으로 가입한 전기 캠페인 코드</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; background-color:#F8D7DA;">100.00%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd; color:blue;">드랍</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd; font-weight:bold;">channel_sales</td>
            <td style="padding: 5px; border: 1px solid #ddd;">영업 채널 코드</td>
            <td style="padding: 5px; border: 1px solid #ddd;">object</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; background-color:#FFEBEE;">26.21%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">7</td>
            <td style="padding: 5px; border: 1px solid #ddd;">새 카테고리</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">X</td>
            <td style="padding: 5px; border: 1px solid #ddd;">cons_12m</td>
            <td style="padding: 5px; border: 1px solid #ddd;">최근 12개월간 전기 사용량</td>
            <td style="padding: 5px; border: 1px solid #ddd;">int64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.00%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">X</td>
            <td style="padding: 5px; border: 1px solid #ddd;">cons_gas_12m</td>
            <td style="padding: 5px; border: 1px solid #ddd;">최근 12개월간 가스 사용량</td>
            <td style="padding: 5px; border: 1px solid #ddd;">int64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.00%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">X</td>
            <td style="padding: 5px; border: 1px solid #ddd;">cons_last_month</td>
            <td style="padding: 5px; border: 1px solid #ddd;">지난달 전기 사용량</td>
            <td style="padding: 5px; border: 1px solid #ddd;">int64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.00%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">X</td>
            <td style="padding: 5px; border: 1px solid #ddd;">date_activ</td>
            <td style="padding: 5px; border: 1px solid #ddd;">계약 활성화 날짜</td>
            <td style="padding: 5px; border: 1px solid #ddd;">object</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.00%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd;">date_end</td>
            <td style="padding: 5px; border: 1px solid #ddd;">계약 종료 등록일</td>
            <td style="padding: 5px; border: 1px solid #ddd;">object</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.01%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd; font-weight:bold;">date_first_activ</td>
            <td style="padding: 5px; border: 1px solid #ddd;">고객의 첫 계약 시작일</td>
            <td style="padding: 5px; border: 1px solid #ddd;">object</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; background-color:#F8D7DA;">78.21%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd; color:blue;">드랍</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd;">date_modif_prod</td>
            <td style="padding: 5px; border: 1px solid #ddd;">상품 마지막 수정일</td>
            <td style="padding: 5px; border: 1px solid #ddd;">object</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.98%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd;">date_renewal</td>
            <td style="padding: 5px; border: 1px solid #ddd;">다음 계약 갱신일</td>
            <td style="padding: 5px; border: 1px solid #ddd;">object</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.25%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd; font-weight:bold;">forecast_base_bill_ele</td>
            <td style="padding: 5px; border: 1px solid #ddd;">다음 달 예상 전기 요금 기준</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; background-color:#F8D7DA;">78.21%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd; color:blue;">드랍</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd; font-weight:bold;">forecast_base_bill_year</td>
            <td style="padding: 5px; border: 1px solid #ddd;">연간 예상 전기 요금 기준</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; background-color:#F8D7DA;">78.21%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd; color:blue;">드랍</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd; font-weight:bold;">forecast_bill_12m</td>
            <td style="padding: 5px; border: 1px solid #ddd;">12개월 예상 전기 요금 기준</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; background-color:#F8D7DA;">78.21%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd; color:blue;">드랍</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd; font-weight:bold;">forecast_cons</td>
            <td style="padding: 5px; border: 1px solid #ddd;">다음 달 예상 전기 사용량</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; background-color:#F8D7DA;">78.21%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd; color:blue;">드랍</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">X</td>
            <td style="padding: 5px; border: 1px solid #ddd;">forecast_cons_12m</td>
            <td style="padding: 5px; border: 1px solid #ddd;">다음 12개월 예상 전기 사용량</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.00%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">X</td>
            <td style="padding: 5px; border: 1px solid #ddd;">forecast_cons_year</td>
            <td style="padding: 5px; border: 1px solid #ddd;">연간 예상 전기 사용량</td>
            <td style="padding: 5px; border: 1px solid #ddd;">int64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.00%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd;">forecast_discount_energy</td>
            <td style="padding: 5px; border: 1px solid #ddd;">예상되는 반복 할인 금액</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.78%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">X</td>
            <td style="padding: 5px; border: 1px solid #ddd;">forecast_meter_rent_12m</td>
            <td style="padding: 5px; border: 1px solid #ddd;">다음 12개월 미터기 임대료 예상 금액</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.00%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd;">forecast_price_energy_p1</td>
            <td style="padding: 5px; border: 1px solid #ddd;">1구간 예상 에너지 단가</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.78%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd;">forecast_price_energy_p2</td>
            <td style="padding: 5px; border: 1px solid #ddd;">2구간 예상 에너지 단가</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.78%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd;">forecast_price_pow_p1</td>
            <td style="padding: 5px; border: 1px solid #ddd;">1구간 예상 전력 단가</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.78%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">X</td>
            <td style="padding: 5px; border: 1px solid #ddd;">has_gas</td>
            <td style="padding: 5px; border: 1px solid #ddd;">고객이 가스도 사용하는지 여부</td>
            <td style="padding: 5px; border: 1px solid #ddd;">object</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.00%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">2</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">X</td>
            <td style="padding: 5px; border: 1px solid #ddd;">imp_cons</td>
            <td style="padding: 5px; border: 1px solid #ddd;">현재 결제된 사용량</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.00%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd;">margin_gross_pow_ele</td>
            <td style="padding: 5px; border: 1px solid #ddd;">전력 가입 총 마진</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.08%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd;">margin_net_pow_ele</td>
            <td style="padding: 5px; border: 1px solid #ddd;">전력 가입 순마진</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.08%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">X</td>
            <td style="padding: 5px; border: 1px solid #ddd;">nb_prod_act</td>
            <td style="padding: 5px; border: 1px solid #ddd;">활성화된 상품 및 서비스 개수</td>
            <td style="padding: 5px; border: 1px solid #ddd;">int64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.00%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">11</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd;">net_margin</td>
            <td style="padding: 5px; border: 1px solid #ddd;">총 순마진</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.09%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">X</td>
            <td style="padding: 5px; border: 1px solid #ddd;">num_years_antig</td>
            <td style="padding: 5px; border: 1px solid #ddd;">고객의 가입 경과 연수</td>
            <td style="padding: 5px; border: 1px solid #ddd;">int64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.00%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">15</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd;">origin_up</td>
            <td style="padding: 5px; border: 1px solid #ddd;">고객이 처음 가입한 전기 캠페인 코드</td>
            <td style="padding: 5px; border: 1px solid #ddd;">object</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.54%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">5</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
        <tr>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center; color:red;">O</td>
            <td style="padding: 5px; border: 1px solid #ddd;">pow_max</td>
            <td style="padding: 5px; border: 1px solid #ddd;">가입된 최대 전력</td>
            <td style="padding: 5px; border: 1px solid #ddd;">float64</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">0.02%</td>
            <td style="padding: 5px; border: 1px solid #ddd; text-align: center;">-</td>
            <td style="padding: 5px; border: 1px solid #ddd;">-</td>
        </tr>
    </tbody>
</table>
</div>
<img width="3200" height="4977" alt="Image" src="https://github.com/user-attachments/assets/df6b609b-5a16-4515-9281-adcbe6f5e3fe" />

# 5. 타당한 평가지표 설명

## 🎯 모델 성능 비교: 개선 전·후

아래 표는 **개선 전**에 XGBoost 단일 모델만 사용했을 때와, **개선 후** 다양한 알고리즘·불균형 처리(SMOTE) 적용 이후의 핵심 지표를 한눈에 비교한 내용입니다.  

---

### 📊 주요 평가지표

| 단계       | 모델                          | Accuracy | Precision | Recall  | F1-Score | ROC-AUC |
|-----------|------------------------------|---------:|----------:|--------:|---------:|--------:|
| **개선 전**  | XGBoost                      |   0.9819 |    0.9995 | 0.8134 |   0.8967 |    0.87* |
| **개선 후**  | KNN (K Neighbors Classifier)  |   0.9996 |    0.9964 | 0.9998 |   0.9981 |    1.0000 |
|             | Extra Trees Classifier        |   0.9990 |    0.9996 | 0.9899 |   0.9947 |    1.0000 |
|             | Random Forest Classifier      |   0.9981 |    0.9998 | 0.9812 |   0.9904 |    1.0000 |
|             | Decision Tree Classifier      |   0.9970 |    0.9842 | 0.9850 |   0.9846 |    0.9917 |
|             | LightGBM                      |   0.8835 |    0.4434 | 0.6936 |   0.5410 |    0.9086 |
|             | Gradient Boosting Classifier  |   0.7515 |    0.2163 | 0.5752 |   0.3144 |    0.7452 |
|             | AdaBoost Classifier           |   0.6684 |    0.1661 | 0.5840 |   0.2585 |    0.6825 |

> **\*** ROC-AUC (개선 전 XGBoost): 예시 값(0.87) 입력  
> **Bold** 단계 구분과 **컬러 배경**(Kaggle에서는 지원되는 범위 내)로 강조하세요.

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

