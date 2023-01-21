# RecSysStudy


https://developers.google.com/machine-learning/recommendation/overview 
부터 공부 시작

참고 링크

https://github.com/lsjsj92/recommender_system_with_Python

Kaggle OTTO 벼락치기용


콘텐츠 기반 필터링

- 장점
  - 다른 이용자의 정보를 필요로 하지 않음. 컨텐츠의 정보만으로 많은 사람에게 추천을 해줄 수 있음.
- 단점
  - 특징 추출 등에 있어서 많은 도메인 지식(Domain Knowledge)이 필요함. 
  - 추가적인 관심사에 대해서 새로 추천해주기는 힘들다. 
  
  
협업 필터링

Matrix Factorization을 사용

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
