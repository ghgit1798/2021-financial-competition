# 전처리 이슈 및 과정

## 📌 전처리 대상

### 1. 업종대분류
- nan값 존재
- 음식 카테고리 2개 존재 ('음식', '음식 ')

## 📌 전처리 과정

### nan값 삭제
1. 총 72개 업종대분류에서 nan값이 나타났다.
2. ![image](https://user-images.githubusercontent.com/44918665/129470037-acd80ef3-3528-429f-b7ae-e5f26d6bb1ee.png)
3. 데이터를 삭제할 지, 레이블링할 지를 결정해야 했다.
4. ![image](https://user-images.githubusercontent.com/44918665/129470084-be146b4e-0825-4336-8be9-37223d5ef8bc.png)
5. 주어진 자료로부터 특징을 파악하기도 어려웠고, 미정으로 두더라도 사용하기 어려운 데이터라고 판단하여 삭제하였다.

### 음식 카테고리 통일
1. 같은 음식을 의미하는 두 업종대분류를 통일하였다.
2. ![image](https://user-images.githubusercontent.com/44918665/129470113-792c3065-20fa-45f4-8fd5-da401c865333.png)








