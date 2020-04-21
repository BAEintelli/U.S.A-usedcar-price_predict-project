# U.S.A-usedcar-price_predict-project
미국 중고차 가격예측 프로젝트

### Create info
- made by : 배준영, 유호원, 조대선, 홍성현
- sapn : 2020.03.01 ~ 2020.04.18
	

## 프로젝트 개요

### 회귀 분석 동기
- 미국의 중고차 시장에 나온  매물들의 가격을 미리 예측하는 모델을 만들어 시장에 나온 자동차가 싼가격인지 비싼가격인지 직관적으로 볼 수 있게 만들기 위함.
- 프로젝트 진행하면서 중고차에 대한 인사이트를 얻어 언제 차를 처분하는것이 좋은 가격을 받을 수 있은지 확인

### 데이터 출처
- Craiglist(크레이그리스트) https://craigslist.org/: 중고 매물 구인 구직 자유주제 토론등을 다루는 커뮤니티
- kaggle(캐글) https://www.kaggle.com/austinreese/craigslist-carstrucks-data : 데이터셋 제공

## 프로세스
- EDA : 변수 특성 파악, (가격,주행거리,연식의)상관관계 파악, 주행거리 히스트그램분석
- 전처리 : vinaudit API를 활용하여 허위매물 필터링, 독립변수 선택
- 모델링: OLS (스케일링, interacrion, 유의미 변수추가, 정규화)
- 검증: ANOVA, KFold, test data를 활용 최종검증
<img src="https://myawsbuckethoward.s3.ap-northeast-2.amazonaws.com/img12.png" width="1350px">


## 회고
- Keep
    - EDA : EDA에서 가설을 세워 진행을 하였던 부분이 모델 발전에 많은 기여를함.
    - 전처리 : 자동차 이력제공 시스템을 활용하여 허위매물 제거는 현재 모델의 비약적인 향상에 이바지함.
- Problem
    - 자동차 보증수리 여부에 대한 데이터의 부재로 model5의 아이디어를 좀더 발전시키지 못함.
- Try
   - 2달에 한번씩 데이터가 업데이트 되기 때문에 데이터를 활용 모델향상 및 검증예정

