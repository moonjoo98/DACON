# [DACON]감귤 착과량 예측

![image](https://user-images.githubusercontent.com/103553532/209908373-601a1c12-1692-4860-9f07-58a66ffc059d.png)

### TASK
- 감귤나무의 나무 생육 상태, 엽록소 및 새순 정보로부터 감귤 착과량을 회귀 예측

### FLOW
- 2차 자료를 통한 사전조사 진행 (감귤 나무 엽록소 새순 정보)</br>
- 데이터 EDA 후 Features engineering 진행 + train data Oversampling
  - 데이터셋이 부족해서 학습이 어려울 것이라 생각해 성능 향상을 위해 Oversampling 진행(smogn)
  - Feature importance를 확인해본 결과 불필요한 변수가 많이 있어 Feature sampling 진행 (boruta shap, shap, percentile(ridge, ngboost)</br>
- modeling (ensemble)
  - 부스팅 계열의 모델의 성능이 더 좋을 것이라 예상해 catboost, lgbm, ngboost로 모델링 진행
  - 성능이 높고 상관관계가 낮은 모델끼리 ensemble
### REVIEW
위의 과정을 통해 public score 2위로 마무리했지만 private score에서 41위로 overfitting이 발생했다.</br>
ngboost가 가장 최근에 나온 부스팅 모델이고 당장 성능이 잘 나와서 사용했지만 이 task에선 overfitting이 발생했다. (파라미터 튜닝 부족 + 모델의 특징 예상)</br>
overfitting 방지를 위해 oversampling을 진행했지만 부족했고 데이터 분포도 좀 더 비슷하게 맞추는게 좋았을 것 같다.</br>
데이터가 부족해 cv를 진행하지 않았는데 overfitting방지를 위해 public score에 너무 집착하지 않는 것이 좋을 것 같다.

### LB
Public - 2nd
Private - 41th(16%)
