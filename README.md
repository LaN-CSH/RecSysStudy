# RecSysStudy


https://developers.google.com/machine-learning/recommendation/overview 
부터 공부 시작

참고 링크

https://github.com/lsjsj92/recommender_system_with_Python

https://www.kaggle.com/competitions/otto-recommender-system/discussion/363544

https://www.kaggle.com/code/utm529fg/otto-tuning-candidate-rerank-model-lb-0-577 - Re-rank Model

Kaggle OTTO 벼락치기용


콘텐츠 기반 필터링

특정 item을 선호하면 그와 비슷한 item도 좋아할 것. 이를 추천 item으로 선정 되게 하는 필터링.

- 장점
  - 다른 이용자의 정보를 필요로 하지 않음. 컨텐츠의 정보만으로 많은 사람에게 추천을 해줄 수 있음.
- 단점
  - 특징 추출 등에 있어서 많은 도메인 지식(Domain Knowledge)이 필요함. 
  - 추가적인 관심사에 대해서 새로 추천해주기는 힘들다. 
  
  
협업 필터링

'비슷한 유저끼리 비슷한 item을 선호할 것이다' 라는 전제의 필터링.

특정 벡터 공간에 item의 특성을 대변하는 벡터를 가지고 비교

Matrix Factorization을 사용

Embedding을 학습하게 하는 것. 특징을 따로 안뽑아도 된다.

- 장점
  - 도메인 지식 불필요.
  - 모델 덕에 다른 관심사도 추천 항목으로 뜰 수 있음.
  - 내용적 특징 추출을 필요로 하지 않음.
- 단점
  - 새로운 (user, item) 페어가 있을 때 이를 학습하기 이전이라면 embedding을 형성할 수 없음
  - Cold-start problem으로 자주 불리는 문제
  - Query/Item의 side features를 포함하기 힘들다

딥러닝 기반 추천

- Softmax 등 Embedding에 있어서 DNN 적 특성 적용 가능
