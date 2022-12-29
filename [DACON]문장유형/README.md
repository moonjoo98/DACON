# [DACON] 문장 유형 분류 AI 경진대회

### TASK
- 언어가 사용되는 모든 영역에서 폭넓게 활용될 수 있는 문장 유형 분류 AI 모델 개발
![image](https://user-images.githubusercontent.com/103553532/209910863-3cf4160b-050f-4a87-b536-9bce6475e9db.png)

### FLOW
데이터 EDA 후 텍스트 전처리 진행 - 뉴스 데이터라 전처리할 것이 별로 없었음.</br>
</br>
Pretrianed 모델에 fine-tuning 진행
  - 여러 pretrained모델을 불러와서 ensemble을 진행 + freeze를 통해 미세조정
  - 성능이 높고 상관관계가 낮은 모델끼리 가중평균 ensemble 

### REVIEW
기존에 NLP에 관심이 많고 여러 한국어 언어 모델을 알고 전처리 팁을 알고 있어서 더 재밌게 진행한 공모전 이였다.</br>
</br>
여러 pretrained모델을 불렁와 ensemble을 진행하는 것이 더 좋은 결과를 보여주는 것을 확인했다.</br>
</br>
추가로 Back translation을 통해 추가 데아터셋을 구축해 활용했지만 성능 향상에 기여하지 못했는데 조금 더 손봤으면 도움이 됐을 것 같다.</br>
</br>
NLP 공모전은 거의 처음이였는데 좋은 성과를 거둘 수 있어서 재밌었고 NLP 프로젝트를 진행해보고자 하는 계기가 됐다.


