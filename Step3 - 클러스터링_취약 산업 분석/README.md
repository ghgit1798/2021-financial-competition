# 클러스터링을 활용한 취약 산업 분석
- 데이터: 신한카드 카드매출데이터

- 목차
1. [대분류 클러스터링](#대분류-클러스터링)
2. [코로나 전후 대분류 카드매출금액](#코로나-전후-대분류-카드매출금액)
3. [⭐인사이트 & 추후 방향](#⭐인사이트-&-추후-방향)
4. [1️⃣ 종합유통-생활서비스](#1️⃣-종합유통-생활서비스)
5. [2️⃣ 종합유통](#2️⃣-종합유통)

## 대분류 클러스터링

### Elbow chart
![image](https://user-images.githubusercontent.com/44918665/129468971-247d5ba9-fb60-4115-ad4d-46d8c8f35680.png)
- elobw chart를 기반으로 해석하면 업종대분류는 2개의 클러스터가 적당하다.

### Clustering 결과
![image](https://user-images.githubusercontent.com/44918665/129470384-fe7992b7-4bb2-4dfe-857e-a59ba50f2fdf.png)
- 0번 클러스터는 가맹점수, 매출건수가 크지만 건당,점당매출은 작은 편의점 같은 산업들이 해당된다.
- 1번 클러스터는 가맹점수, 매출건수는 작지만 건당,점당매출이 큰 유통, 전문서비스 등 음식을 제외한 산업이 해당된다.
- 0번과 1번 클러스터의 가장 큰 차이는 건당매출금액과 가맹점수이다.
- 따라서 0번 클러스터는 음식관련산업, 1번 클러스터는 그 외 산업으로 분류하였다.

1. 음식
![image](https://user-images.githubusercontent.com/44918665/129470468-7aceb944-9b51-418a-ad21-746e5912c40d.png)
- Clusert 0에 해당하는 음식산업이다.
2. 문화레저
![image](https://user-images.githubusercontent.com/44918665/129470480-70574e26-5d38-4cc8-a050-d92c348eaa9a.png)
- Cluster 1에서 매출액, 건수, 금액이 전부 작은 산업이다.
- 기준년월별로 시각화할 필요가 있다.
3. 생활서비스
![image](https://user-images.githubusercontent.com/44918665/129470543-27a96137-67b5-4a39-b4a0-048f7acb0e8d.png)
- Cluster 1에서 점당매출금액은 작으나 매출액, 건수는 상당히 높다.
4. 일반유통
![image](https://user-images.githubusercontent.com/44918665/129470589-5533610c-bf2f-481b-babd-cca007b73bb9.png)
- Cluster 1이지만 가맹점수는 큰 편, 매출액-건수-점당매출금액은 낮은편이다.
- Cluster 1로 분류된 가장 큰 이유는 **건당매출금액이 매우 크기 때문**으로 판단된다.
6. 전문서비스
![image](https://user-images.githubusercontent.com/44918665/129470702-65df39cd-330d-4a8e-b75f-3cb7406a6ec5.png)
- Cluster 1로 일반유통과 비슷하게 가맹점수-건당매출금액이 매우 크다.
- 하지만 다른 점은 카드매출금액도 매우 높은 편이며, 건당매출금액의 크기가 일반유통보다 크다.
6. 종합유통
![image](https://user-images.githubusercontent.com/44918665/129470729-78613e04-ba23-421a-a328-519ebdb7a303.png)
- Cluster 1로 분류되었으나, 카드매출금액-카드매출건수가 매우크다.
- Cluster 1로 분류된 이유는 가맹점수가 매우 작기 때문으로 판단되나 유사한 클러스터라고 보기엔 어렵다.
7. 기타
![image](https://user-images.githubusercontent.com/44918665/129470787-182c05bf-8d27-475e-8057-b00550f6821e.png)
- Cluster 1로 분류되었으나 점당매출금액만 매우 높다.
- 아마 여러가지 분류하기 애매한 산업들이 합쳐진 결과로 예상된다.
- 기타 산업에는 어떤 세부분류들이 있는지 확인이 필요하다.
![image](https://user-images.githubusercontent.com/44918665/129470823-4236d9e1-dcee-44db-9a7e-231d6ee5168e.png)
![image](https://user-images.githubusercontent.com/44918665/129470832-ca4cf7f9-cc1f-4c01-a0e9-1f91b4e00a8f.png)
- 확인해보니 기타는 주로 자사가맹점/해외사용건으로 특수한 경우로 제외하고 집계하는 것도 고려해 볼 필요가 있다.

## 코로나 전후 대분류 카드매출금액
![image](https://user-images.githubusercontent.com/44918665/129473027-18e4df63-9d8b-4cdf-8fc7-15c7a05518ac.png)
- 음식관련산업과 문화레저는 코로나 전후로 3월, 9월 모두 감소했다.
- 반면 그 외 산업들은 코로나 후 산업 9월에는 전부 매출증가했다. 

## ⭐인사이트 & 추후 방향
- 클러스터링 결과 해석
- 전문서비스 & 일반유통이 비슷한 군집으로 보임
- 생활서비스 & 종합유통이 비슷한 군집으로 보임
- 음식, 문화레저는 각각의 군집 형태
- 매출가맹점수, 신규가맹점수, 해지가맹점수는 강한 상관관계가 존재했다.
- 📌 따라서 추후 4가지 그룹을 묶어서 클러스터링 진행

## 1️⃣ 종합유통-생활서비스
- 종합유통-생활서비스 추출 후 클러스터링 결과
![image](https://user-images.githubusercontent.com/44918665/129482163-c8bbeca1-d855-483b-b7f2-51b10da51ce6.png)
### ❗문제점 발생
- Outlier가 존재하는 것으로 예측됨, 레이더 차트가 찌그러지는 문제
- 리서치 결과 Standard, MinMaxscaler는 Outlier에 민감함
- 따라서 RobustScaler 시도
![image](https://user-images.githubusercontent.com/44918665/129482296-9a51c9f9-ba61-4e5d-ba25-e4b55c5367aa.png)
- 서로 다른 두 업종이 섞여 군집 파악이 오히려 어려우므로, 다시 분리 후 시도

## 2️⃣ 종합유통
- Scaler의 경우 가독성을 위해 MinMax보다는 Robust를 사용
- MinMaxSclaer
![image](https://user-images.githubusercontent.com/44918665/129482491-1f94306c-eb14-436d-ab0b-af4e01a96c80.png)
- RobustScaler
![image](https://user-images.githubusercontent.com/44918665/129482513-4315723e-fb13-48b3-92ec-1af69fbb4361.png)


