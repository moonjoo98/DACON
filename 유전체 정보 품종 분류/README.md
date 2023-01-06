# [DACON]유전체 정보 품종 분류 AI 경진대회

### TASK
- 개체와 SNP 정보를 이용하여 품종 분류 AI 모델 개발

![image](https://user-images.githubusercontent.com/103553532/210488689-d64faa38-5b42-415d-b361-4ec91b7509d2.png)

### FLOW
- 데이터 전처리 : 의미없는 일부 데이터를 전처리하고 범주형 변수를 라벨 인코딩을 진행 + AutoML 전처리
- 모델링 : AutoML libary 사용

### REVIEW

최근 머신러닝 대회를 진행하면서 직접 여러 데이터 전처리를 진행하고 모델링을 해봤지만 노력에 비해 좋은 성능을 얻기는 어려웠다.

여러 대회에서 OverSampling, pca(pca,umap,tsne), clustering, ensemble 등등 머신러닝 기법과 여러 기법들을 가져와서 사용해봤다.

하지만 상위 10%에 드는 경우는 종종 있었지만 머신러닝 task에서 5%이내로 드는것은 쉽지 않았다. 오히리 너무 많은 기법들을 적용하다보니 overfitting되는 경우가 허다했다.

그러다 이번 기회에 여러 머신러닝 대회에서 상위권에서 종종 보인 AutoML library만으로 컴피티션을 진행해보고자 했다.

이번 유전체 정보 품종 분류 대회는 데이터가 너무 적었다. 학습 데이터가 256밖에 되지 않았고 train과 test의 분포가 거의 비슷했다.

리더보드를 보면 f1-score가 1인사람들도 많은 것을 볼 수 있었다. 그래서 이번 대회에는 큰 힘을 쓰지 않고 AutoML library를 통해 성능을 비교해보고 경험해보기로 결정했다.

### 자세한 설명은 블로그 참고
https://mz-moonzoo.tistory.com/5


