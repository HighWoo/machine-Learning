# machine-Learning
## 파이썬을 활용한 머신러닝/빅데이터  
  
## 1주차(2021/09/03)  
machine-Learning = 데이터를 이용해서 명시적으로 정의되지 않은 패턴을 컴퓨터로 학습하여 결과를 만들어낸다  
통계학+알고리즘+프로그램  
데이터를 보고 추리하는것이 머신러닝의 핵심  
데이터/패턴인식/컴퓨터를 활용한 계산  
현재의 머신러닝=대량의 데이터를 바탕으로 하는 딥러닝 기법을 주로 사용  
(음성인식,번역,이미지 인식에서 좋은성과)  

## 2주차(2021/09/10)  
머신러닝의 첫번째 단계 (데이터 분석)  

### 판다스의 자료구조 
시리즈:1차원 배열  
데이터프레임:2차원 배열  
  
시리즈 만들기  
방법 1(딕셔너리를 시리즈로 변환)    
판다스 내장함수 Series() 이용  
딕셔너리를 매개변수로 전달  
딕셔너리 키:시리즈의 인덱스에 대응  
딕셔너리의 각 키에 매칭되는 값:시리즈의 데이터 값으로 변환  
![image](https://user-images.githubusercontent.com/75231868/132804328-1cca4d5c-0e6e-4ddf-a9e2-65cc5df3e8d2.png)
![image](https://user-images.githubusercontent.com/75231868/132804364-46f8be63-07c7-4574-bc1c-a5c434e3b4e8.png)

  
방법 2(리스트를 시리즈로 변환)  
![image](https://user-images.githubusercontent.com/75231868/132804071-cf16218b-4d3b-4163-b2ee-51a5c711f41e.png)
![image](https://user-images.githubusercontent.com/75231868/132804088-f38542a2-e2a9-457d-b861-753753f4b1c7.png)
 
### 시리즈  
인덱스 구조:자기와 짝을 이루는 원소의 순서와 주소 저장  
  
인덱스의 종류:정수형 위치 인덱스,인덱스 이름 또는 인덱스 라벨  
![image](https://user-images.githubusercontent.com/75231868/132804539-488c9537-4606-4486-96e0-00f8bd3992c5.png)

![image](https://user-images.githubusercontent.com/75231868/132804757-2e9f83d8-2b1a-4aca-8231-c1748e3442a3.png)
![image](https://user-images.githubusercontent.com/75231868/132804777-349da836-3caa-407c-ab31-419f29fadf64.png)

원소 선택  
인덱스를 이용하여 시리즈의 원소를 선택할 수 있다  
정수형 인덱스는 대괄호 안에 숫자 입력(배열과 동일하게 0부터 시작)  
인덱스 이름 은 대괄호 안에 이름과 함께 따옴표 입력(큰 따옴표 작은따옴표 모두 사용 가능)  
![image](https://user-images.githubusercontent.com/75231868/132805350-7da763bb-2c56-4857-a1a7-6e653c26adc6.png)
![image](https://user-images.githubusercontent.com/75231868/132805393-60f5d6c7-0559-4c3f-91c6-ac7c8d11ec52.png)




