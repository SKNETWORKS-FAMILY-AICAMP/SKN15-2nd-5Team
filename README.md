# SKN15-2nd-5Team

# 1. 팀 소개
 오원장
 권도원
 유의정
 조솔찬
 홍민식



# 2. 프로젝트 기간
###  25년 07월 10일 (목요일) ~ 25년 07월 11일 (금요일) 


# 3. 프로젝트 개요
- 목적: 이 프로젝트의 궁극적 목적은 PowerCo 고객 이탈(Churn) 예측을 통해 회사의 매출 손실을 최소화하고, 
  효율적인 고객 유지(Retention) 전략을 수립하기 위함입니다.
- 데이터 출처: [Kaggle - PowerCo dataset Prediction]
(https://www.kaggle.com/datasets/naiborhujosua/energy-industry)
- 데이터 구성: 총 42개 컬럼, (16,096명 최근 12개월 전력 소비량, 서비스시작일,서비스 종료일, 이탈여부 등)


## 📕 프로젝트명


## ✅ 프로젝트 배경 및 목적

 <img width="767" alt="reuter-1 " src="https://github.com/user-attachments/assets/eda46139-5a46-462e-b157-9920afbfc204" />
 <img width="659" alt="reuter-2" src="https://github.com/user-attachments/assets/dd27f639-fc10-49c9-af2e-0f12efbb6380" />
 <img width="666" alt="reuter-3" src="https://github.com/user-attachments/assets/a6f6b099-ef1e-47b5-ab7d-b09ad1539c7e" />




## 🖐️ 프로젝트 소개
1. 계절별 요금 급등기(성수기)부담 -> 이탈 증가  
     여름철 냉방 수요(7~8월),  겨울철 난방 수요(12월)에 전기·가스 요금이 크게 오르는 구간이 있어요.
    이런 시기에 요금 상승폭(pct_change)이 
    평균 대비 20% 이상인 고객들은, 일시적 ‘요금 충격’을 경험하면서 계약 갱신을 망설이기 쉽습니다.
    
    특히 여름 냉방용·겨울 난방용 전기 비중이 높은 고객(계절성 더미 변수 m_7, m_1 값이 큰 군집)의 
    이탈율이 **20~25%**로 가장 높게 나왔습니다.
    
 2. 변동 단가의 불안정성 → 예측 불가능성에 대한 거부감
고정 단가(price_p1_fix)는 매월 비슷하지만, 변동 단가(price_p1_var)가 심하게 출렁이는 고객은 ‘다음 달 얼마나 내야 할지 모르겠다’는 불안감을 느낍니다.
  변동성(var_std) 상위 10%에 든 고객들의 이탈율이 약 1.5배 정도 높게 관찰되었고, 이 군집이 바로 “계약 변경”이나 “타사 이동”을 선택하는 경향이 강했습니다.
 
 3. 이동평균으로 본 중기 방향성 → 지속 상승 시 이탈 가능성↑
  3개월 이동평균(fix_ma_3)이 꾸준히 상승 곡선을 그릴 때, 고객은 ‘요금이 계속 오를 것 같다’고 판단해 미리 이탈을 결정합니다.
  반면 계절성 급등 후 하락 패턴(peak-and-drop)이 뚜렷한 고객은 “일시적 성수기”로 받아들이고 유지하는 비율이 상대적으로 높았습니다.




## ❤️ 기대효과

## 👤 대상 사용자



# 4. 기술 스택
### AI & 데이터 처리


[](https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white)![](https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white)![](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)![](https://img.shields.io/badge/scikitlearn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)



### 머신러닝 모델
![](https://img.shields.io/badge/RandomForest-00B050?style=for-the-badge)![](https://img.shields.io/badge/DecisionTree-228B22?style=for-the-badge)![](https://img.shields.io/badge/XGBoost-EC0000?style=for-the-badge&logo=xgboost&logoColor=white)![](https://img.shields.io/badge/LightGBM-3C3C3C?style=for-the-badge&logo=lightgbm&logoColor=white) ![](https://img.shields.io/badge/CatBoost-FFCC00?style=for-the-badge)

![](https://img.shields.io/badge/SGDClassifier-006699?style=for-the-badge)![](https://img.shields.io/badge/Logistic%20Regression-1E90FF?style=for-the-badge)![](https://img.shields.io/badge/SVM-8A2BE2?style=for-the-badge)![](https://img.shields.io/badge/KNN-FF69B4?style=for-th e-badge)![](https://img.shields.io/badge/MLP-800080?style=for-the-badge)![]

### 버전 관리 및 협업

![](https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white) ![](https://img.shields.io/badge/discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)





# 5. 수행결과(분석 및 예측 결과)



# 6. 한 줄 회고

