# Daegu-Traffic-Accident-Damage-Prediction-AI-Competition
# [DACON] 대구 교통사고 피해 예측 AI 경진대회 [(Link)](https://dacon.io/competitions/official/236193/overview/description)

주최 : 산업통상자원부, 대구광역시

주관 : 한국자동차연구원, 대구디지털혁신진흥원

운영 : 데이콘

규모 : 약 2000여명 참가

---
## ✔️ 최종결과
![image](https://github.com/dorahee-ee/Daegu-Traffic-Accident-Damage-Prediction-AI-Competition/assets/102142694/79c4045f-72bd-4ecc-ab67-532231300b18)

`Public 48위, Private 98위`
인공지능 공부를 시작하고, 처음으로 공모전에 참가하였다. 딥러닝에 대한 지식이 부족했기 때문에 머신러닝을 이용하여 참여하였고, 중간중간 코드공유에 올라오는 글들을 참고하여 코드를 수정해나갔다. Public 48등, Private 98등으로, 수상을 하지는 못하였지만 처음 나간 공모전치고는 나쁘지 않은 성적이라고 생각한다.

private에서 상위권의 코드들을 보면 EDA를 통해서 데이터를 분석하는 것이 상당 부분을 차지하는 것 같다는 생각을 하였다. 다음에 또 이런 공모전에 참가하게 된다면, EDA와 전처리에 더 신경을 써야할 것 같다.

---
## 📂 DATA
- train.csv
- test.csv
- sample_submission.csv
- 대구 보안등 정보.csv
- 대구 어린이 보호 구역.csv
- 대구 주차장 정보.csv

---
## Processing

### EDA
- 새벽시간(0시 - 5시)에 ECLO가 높음을 확인하였다. -> 새벽(dawn) 변수 추가
- 주말(토, 일)에 ECLO가 높음을 확인하였다. -> 주말(weekend) 변수 추가
- 공휴일에 ECLO가 높음을 확인하였다. -> 공휴일(Holiday) 변수 추가

### Modeling
- AutoML (mljar - supervised)
- `['Random Forest', 'LightGBM', 'Xgboost', 'CatBoost']`을 앙상블하여 진행
- `Random Seed = 0`으로 고정

### Result
#### 최종선택모델
Baseline + 새벽(Dawn) : `RMSE = 3.20667`, `제출 점수 = 0.4265551988`

---
