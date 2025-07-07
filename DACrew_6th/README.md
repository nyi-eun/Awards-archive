<h2 align='center'> 신용카드 사용자 연체 예측 모델링 </h2>  
<h3 align='center'> [DACON] 서포터즈 DACrew 6기 </h3>  
<h4 align='center'> (2023.07. ~ 2023.08.)  
<br/> 
  
![Aqua Lines](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/aqua.png)  

&nbsp;


## 1. 주최 기관

- 주최: DACON
- 참가 대상: 1명부터 최대 5명까지 가능

<br/>

## 2. 대회 기간

- 활동 기간: 2023.7.8 ~ 2023.8.31
- 1차 평가: 2023.9.1 ~ 2023.9.8
- 2차 평가: 2023.9.9 ~ 2023.9.15
- 수상자 발표: 2023.9.19
  
<br/>


## 3. 과정

**Stage 0. Intro**
1. 소개
2. 배경 및 목적


**Stage 1. 데이터 살펴보기**
1. 데이터 불러오기
2. 데이터 확인하기
3. 결과 해석


**Stage 2. EDA**
1) gender (성별)
2) car (차 소유 여부)
3) Reality (부동산 소유 여부)
4) Child_num (자녀수)
5) income_total (연간 소득)
6) income_type (소득 분류)
7) edu_type (교육 수준)
8) family_type (결혼 여부)
9) house_type (생활 방식)
10) DAYS_BIRTH (출생일)
11) DAYS_EMPLOYED (업무 시작일)
12) FLAG_MOBIL (핸드폰 소유 여부)
13) work_phone (업무용 전화 소유 여부)
14) phone (전화 소유 여부)
15) email_이메일 소유 여부)
16) occyp_type (직업 종류)
17) family_size (가족 구성원 수)
18) begin_month (신용카드 발급 월)
19) credit (신용카드 등급)
20) 추가 EDA (histogram)


**Stage 3. Data Preprocessing**    
1. 결측치 처리
2. 이상치 처리


**Stage 4. Feature Engineering**
1. 의미 없는 Feature 제거
2. DAYS_EMPLOYED
3. DAYS_BIRTH, begin_month, DAYS_EMPLOYED
4. Feature 추가
5. Scaling, Encoding

   
**Stage 5. Modeling**    
1. 모델 기초 지식  
2. Linear 모델  
3. Tree 기반 모델  
4. Boosting 기반 모델  

   
**Stage 6. Tuning & Ensemble**
1. Tuning  
1-1. CatBoostClassifier  
1-1-1. Feature importance  
1-1-2. submission 파일 제작  
1-2. XGBClassifier  
1-2-1. Feature importance  
1-2-2. submission 파일 제작  
1-3. 추가) RandomForestClassifier  
1-3-1. Feature importance  
1-3-2. submission 파일 제작
   
3. Ensemble  
2-1. 가중평균 앙상블
마무리

## 4. 자료      
https://dacon.io/competitions/official/236116/codeshare/8768?page=1&dtype=random  

![236116-1-463470_page-0001 (1)](https://github.com/Ji-eun-Kim/DACrew_6th/assets/124686375/06cb9af0-8162-4c02-9001-14a1d30aa8cc)  
