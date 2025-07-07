<h2 align="center"> 클래식 공연 활성화를 위한 예술의 전당 콘서트홀의 효과적 가격 모델 수립 </h2>
<h3 align="center"> [과학기술정보통신부/NIA] 2023 빅콘테스트 정형데이터분석분야 어드밴스드리그 </h3>
<h4 align='center'> (2023.08. ~ 2023.11.) </h4>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/aqua.png)


<br/>

## 1. 배경 및 목적  
- 예술의 전당의 **고객만족도, 공공성, 수익성** 증진을 위한 **좌석 재분할**에 따른 효과적 가격 모델 수립
- 좌석 등급과 가격에 관하여 공연장과 기획사가 참고할 수 있는 **보편적인 기준안**을 제공
- **고객만족도, 수익성, 공공성을 충족**하는 효과적인 **좌석 그룹핑 방법 및 가격 모델**을 제안

<br/>

## 2. 주최 기관 및 참가 분야

- 주최 : 과학기술정보통신부, NIA 한국지능정보사회진흥원  
- 주관 : 예술의 전당을 비롯한 25개의 기관
- 후원 : KBD빅데이터포럼
- 분야 : 정형데이터 분석 분야
- 리그 : 어드밴스드 리그

<br/>

## 3. 대회 기간

- 참가접수기간: 2023.7.31~2023.9.15
- 데이터 공개: 2023.8.7
- 사전점검: 2023.9.4~2023.9.5
- 제출 마감: 2023.9.27
- 서류심사 결과발표: 2023.11.3
- PT 발표심사: 2023.11.13~2023.11.22
- PT 발표 심사결과: 2023.11.28
- 컨퍼런스 및 시상: 2023.12.13

<br/>


## 4. 과정     
![2023-12-30 153136](https://github.com/Ji-eun-Kim/Toy_project/assets/124686375/ff0ef75f-c9cf-4fdc-9f0c-84ec92989bb6)  
해당 대회는 클래식 공연 활성화를 위한 예술의 전당 콘서트홀의 효과적 가격 모델을 수립하는 것으로, 본 팀은 예술의 전당의 **고객만족도, 공공성, 수익성 증진** 에 초점을 맞춰 장르에 따른 좌석 재분할 및 효과적 가격 모델 수립을 진행하였다.  
활용 데이터로는 **예술의 전당에서 제공한 데이터**와 외부 데이터 **1.공연예술통합전산망 오픈 API** 와 **2.공공데이터포털 예술의 전당 공연 및 전시 입장객 데이터 현황** 로, **총 3가지의 데이터**를 본 분석에 사용하였다.   
우선, **탐색적 데이터 분석**을 통해 **장르가 좌석 등급과 등급에 따른 가격에
중요한 기준이 된다** 라는 인사이트를 도출하여 본 인사이트를 가설로 세웠고, **장르를 기준**으로 좌석 분류 클러스터링을 진행하였다. 

![2023-12-30 162830](https://github.com/Ji-eun-Kim/DnA-Visualization-competition/assets/124686375/e2beb2fc-6ea6-4f62-8605-cf6762b7e2f6)|![화면 캡처 2023-12-30 163046](https://github.com/Ji-eun-Kim/DnA-Visualization-competition/assets/124686375/ef716c9e-c069-433b-add7-37b76d80d295)
---|---|

기존 좌석 체계에서는 **좌석 등급의 다양성의 부족**, **좌석 분배 기준의 불명확성**이라는 문제점이 존재해, 좌석 클러스터링을 통해 **좌석 등급의 개수의 증진**, **장르에 따른 좌석 선호도** 를 목표로 하여 클러스터링을 통해 문제를 해결하고자 하였다. 클러스터링의 경우, **FINCH method**와 **K-means** 두 가지로 실험하였는데, **FINCH method**는 결과 해석이 매우 어려워 채택하지 않았다. 따라서 **K-means**를 채택하였고, 총 6개의 파생변수로 클러스터링을 진행하였다.   
**Elbow method**의 결과에 따라, 교향곡과 독주는 기존 5개에서 7개의 군집으로, 나머지 장르는 6개의 군집으로 군집의 개수가 결정되었다. 클러스터링 결과 중, 재분류한 좌석 등급의 영역이 겹치는 경우에는 **통계적 유사성**이 높은 군집으로 좌석을 재배치하여 **좌석 보정**을 진행하였다.  

![화면 캡처 2023-12-30 163330](https://github.com/Ji-eun-Kim/DnA-Visualization-competition/assets/124686375/9aeb87d3-bcb3-4f7e-8c8f-735b8bb70985)|![2023-12-30 162726](https://github.com/Ji-eun-Kim/DnA-Visualization-competition/assets/124686375/58705b43-2122-4eec-a633-5834caeb6a4e)
---|---|

앞선 군집화 과정을 통해 도출한 좌석 등급의 가격안을 **검증**하고자, 모델링도 진행하였다. **클러스터링을 통해 도출된 가격**이 본 팀이 중요하게 생각하는 가치인 **공공성, 수익성, 고객만족도를 잘 반영하고 있는지**를 모델링을 통해 **검증**하고자 하였다. 분석을 통해 공공성, 수익성, 고객만족도 측면에서의 변수를 생성하였고, **총 16가지의 변수**를 본 모델링에 활용하였다.   
사용한 모델은 트리 계열 모델 3종류(**DecisionTree, ExtraTree, RandomForest**), 부스팅 계열 모델 3종류(**LGBM, GBM, AdaBoost**)이며, 평가지표는 **RMSE, MAPE, MAE, R2** 네 가지를 사용해 실험을 진행하였고, **다양한 모델에서 공통적으로 준수한 성능이 도출** 되었다는 점에서 **군집 별 평균 원가**를 가격으로 사용하는 것에 대한 타당성을 입증하였다.   
추가적으로, 문제 데이터에서는 확인할 수 없었던 다른 요인들도 최종 가격에 고려하는 것을 **제안**하였다. 새로 제안한 **가격 보정 식(P_pred=P(제시한 티켓 가격)xV(변동 요인)** 을 통해 **가격 변동성**을 고려하였고, 해당 방법론을 적용한다면, 보다 객관화된 최종 가격을 확보할 수 있을 것이라는 인사이트 결과 또한 제공하였다.  


<br/>


## 5. 결과  및 기대 효과

[클러스터링을 통해 도출된 장르별 티켓 가격]    

<img width="366" alt="KakaoTalk_20231230_172456169" src="https://github.com/Ji-eun-Kim/DnA-Visualization-competition/assets/124686375/3ba45d46-e5d3-4188-8a96-6d93bb6cacf4">

[독주] 기존좌석 1층 / 좌석 재분할 후 1층
<img width="1300" alt="기존좌석 1층" src="https://github.com/Ji-eun-Kim/Toy_project/assets/124686375/842681c5-0b0e-40be-ae0c-b4fbe87e3052">| ![독주_변경후](https://github.com/Ji-eun-Kim/Toy_project/assets/124686375/bb801521-2ad3-4925-82fe-733f5783deb7)
---|---|

[독주] 기존좌석 2층 / 좌석 재분할 후 2층
<img width="1500" alt="교향곡_기존_2층" src="https://github.com/Ji-eun-Kim/Toy_project/assets/124686375/98dca2f7-494d-44ec-b814-8eb985a9f71b">| ![독주_변경후_2층](https://github.com/Ji-eun-Kim/Toy_project/assets/124686375/f1bf8597-ddab-452f-a485-b3e4611fab38)
---|---|

-----

[교향곡] 기존좌석 1층 / 좌석 재분할 후 1층
<img width="1300" alt="기존좌석 교향곡 1층" src="https://github.com/Ji-eun-Kim/Toy_project/assets/124686375/048e37f9-f5cb-485e-9e62-6ba1afd62797">| ![교향곡_변경후_1층](https://github.com/Ji-eun-Kim/Toy_project/assets/124686375/4c34be1d-bda8-4f4a-b6cd-88ef35a58bc7) 
---|---|

[교향곡] 기존좌석 2층 / 좌석 재분할 후 2층
<img width="1500" alt="교향곡_기존_2층" src="https://github.com/Ji-eun-Kim/Toy_project/assets/124686375/11fe315d-634a-4731-ad22-35547cb16824">| ![교향곡_변경후_2층](https://github.com/Ji-eun-Kim/Toy_project/assets/124686375/1d5b56d6-07e9-4466-b95c-00ba43ed9db2)
---|---|

<br/>

- 고객에게 객관적이고 투명한 가격 산정 근거 제시
- 대용량의 데이터로 고도화된 군집 분석을 통한 타겟 할인 정책 제시 가능
- 다양한 계층의 고객 수요 증가
- 클래식 공연의 활성화
- 데이터의 증가, 모델의 성능 향상이라는 긍정적인 결과 도출

<br/>

## 6. 팀원 및 담당 역할
<팀원>

- 전공생 4명

<br/>

<담당 역할>

- 예술의 전당 고객 데이터 탐색적 데이터 분석 및 전처리 수행
- Clustering을 위한 유의미한 파생 변수 생성
- FINCH Method Clustering, K-means을 활용한 군집화
- LGBM, RandomForest 모델 학습 및 실험 진행

<br/>

## 7. 자료  
https://www.bigcontest.or.kr/

<img width="557" alt="11" src="https://github.com/Ji-eun-Kim/Toy_project/assets/124686375/5f87e0f4-72f7-4b85-935a-5d07ef394954">   
<br/>

- 발표 영상   
https://www.youtube.com/@bigcontest/videos    

- 증빙 자료       
https://www.imaeil.com/page/view/2023121413152830691

![KakaoTalk_20231230_144717289](https://github.com/Ji-eun-Kim/Toy_project/assets/124686375/1d2635c7-ea99-4450-a265-9aab54ff659b) | ![KakaoTalk_20231230_145117752](https://github.com/Ji-eun-Kim/Toy_project/assets/124686375/d28cd795-e6a1-4910-9c52-e9ecdfea63c6)
---|---|



<br/>

