# U.S.A-usedcar-price_predict-project
미국 중고차 가격예측 프로젝트

# Create info
- made by : 배준영, 유호원, 조대선, 홍성현
- sapn : 2020.03.01 ~ 2020.04.18
# Goal
- "Craiglist(미국판 중고나라)"의 약 51만건의 미국 중고차 정보를 활용한 가격 예

# Technical Skills
- Python, Scikit-learn, pandas, numpy

# 회귀 분석 동기
- 미국의 중고차 시장에 나온  매물들의 가격을 미리 예측하는 모델을 만들어 시장에 나온 자동차가 싼가격인지 비싼가격인지 직관적으로 볼 수 있게 만들기 위함.
- 프로젝트 진행하면서 중고차에 대한 인사이트를 얻어 언제 차를 처분하는것이 좋은 가격을 받을 수 있은지 확인

# 데이터 출처
- Craiglist(크레이그리스트) https://craigslist.org/: 중고 매물 구인 구직 자유주제 토론등을 다루는 커뮤니티
- kaggle(캐글) https://www.kaggle.com/austinreese/craigslist-carstrucks-data : 데이터셋 제공

# Workprocess 
<img src="https://myawsbuckethoward.3.ap-northeast-2.amazonaws.com/img12.png" width="1350px">
측
# Issue
- 데이터 특성상 허위 및 광고성 매물로 인한 주행거리, 연식등의 이상치들이 다수 존재
- 따라서 이상치 탐색 및 제거가 중요

# Issue solving
- vin(차고유번호)를 활용한 이상치 탐색 작업 
- https://www.vinaudit.com/ 에서 제공하는 api를 이용하여 허위 매물 탐색 및 이력 조회
- 위 api는 미국 정부기관에서 관리하는 데이터베이스를 기반으로 제작, 신뢰도가 높음

# Result
- R2-square 약 0.88달성
<img src="https://github.com/BAEintelli/U.S.A-usedcar-price_predict-project/blob/master/img/result.png">


- 가설 검증
	- 가설 1: 미국의 중고차도 한국과 마찬가지로 약 5만Km를 기준으로 가격이 급격히 떨어질 것이다.

	- 데이터에서 가장 많은 매물일 2012년식 포드 F-150 FX4 차량은 주행거리 3만 마일(약 4만8천 km) 지점에서 가격이 급격히 하락

	- 가설 2: 미국은 가 주별로 가격의 차이가 있을 것이다.
	- 포드 F-150 FX4 차량의 워싱턴 주와 코네티컷 주의 차량 가격의 차는 약 1만불




# 회고
- Keep
    - EDA : EDA에서 가설을 세워 진행을 하였던 부분이 모델 발전에 많은 기여를함.
    - 전처리 : 자동차 이력제공 시스템을 활용하여 허위매물 제거는 현재 모델의 비약적인 향상에 이바지함.
- Problem
    - 자동차 보증수리 여부에 대한 데이터의 부재로 model5의 아이디어를 좀더 발전시키지 못함.



