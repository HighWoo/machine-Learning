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
  
### 시리즈  
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

인덱스 구조:자기와 짝을 이루는 원소의 순서와 주소 저장  
  
인덱스의 종류:정수형 위치 인덱스,인덱스 이름 또는 인덱스 라벨  
![image](https://user-images.githubusercontent.com/75231868/132804539-488c9537-4606-4486-96e0-00f8bd3992c5.png)

![image](https://user-images.githubusercontent.com/75231868/132804757-2e9f83d8-2b1a-4aca-8231-c1748e3442a3.png)
![image](https://user-images.githubusercontent.com/75231868/132804777-349da836-3caa-407c-ab31-419f29fadf64.png)

원소 선택  
인덱스를 이용하여 시리즈의 원소를 선택할 수 있다  
정수형 인덱스는 대괄호 안에 숫자 입력(배열과 동일하게 0부터 시작)  
인덱스 이름 은 대괄호 안에 이름과 함께 따옴표 입력(큰 따옴표 작은따옴표 모두 사용 가능)  
![image](https://user-images.githubusercontent.com/75231868/132805588-38b23be6-ed10-4b7e-aa5f-627504d621f2.png)
![image](https://user-images.githubusercontent.com/75231868/132805393-60f5d6c7-0559-4c3f-91c6-ac7c8d11ec52.png)  
sr['a':'b'] 하면 a부터 b까지의 값과 네임을 보여준다  
sr['a','b','c']하면 에러  
sr[['a','b','c']] 라고 해야 에러가 안나온다  

### 데이터 프레임  
![image](https://user-images.githubusercontent.com/75231868/132806015-6cb96a5c-896f-4043-8429-b641848742f0.png)

데이터 프레임 만들기  
![image](https://user-images.githubusercontent.com/75231868/132806279-a4fe4b31-0843-4dfd-b650-5f65091f4b25.png)

![image](https://user-images.githubusercontent.com/75231868/132806681-f49afad9-b41b-48c9-b8ce-cb6a7d1fcf4c.png)
![image](https://user-images.githubusercontent.com/75231868/132806698-94ef1a95-fa98-456b-8357-18d66643b140.png)

컬럼와 인덱스를 직접 지정  
![image](https://user-images.githubusercontent.com/75231868/132807158-74702cc5-0fd8-4d87-a096-3ec273d9513b.png)
![image](https://user-images.githubusercontent.com/75231868/132807171-63279d9e-c249-400b-a982-319fcaf2401e.png)
데이터를 변경하는 법  
df.index=['김준서','이예은']  
df.columns=['연령','남여','소속']  

데이터를 삭제하는 법  
- 행을 삭제할때는 axis=0 or 생략  
- 열을 삭제할때는 axis=1  
- 원본객체를 직접 변경할때는 inplace=True 추가  
  

drop() 메서드 사용  
![image](https://user-images.githubusercontent.com/75231868/132808063-2e0e8e5f-ffdd-45d9-8f80-1585c5783e6b.png)
![image](https://user-images.githubusercontent.com/75231868/132808072-04200c64-92ad-4490-ad33-44b035aecdd0.png)  
  
drop 메서드는 원본은 안사라진다 복제를 해야함  
  
원본을 삭제하려면 inplace=True 해줘야 한다  
![image](https://user-images.githubusercontent.com/75231868/132808269-34f12165-4d27-4f1e-be91-621d6e80bbee.png)
![image](https://user-images.githubusercontent.com/75231868/132808282-a110a965-8e5e-4bd2-a402-f7c8eb891306.png)

## 3주차(2021/09/18)  
데이터 프레임 원소 선택  
![image](https://user-images.githubusercontent.com/75231868/133867397-2b0a6a89-af65-41a7-96f3-58aba826aea7.png)
  
  
데이터 프레임 행 선택  
인덱서를 사용  
iLoc : 위치인덱스  
Loc : 인덱스 이름  
  
- 예제  
![image](https://user-images.githubusercontent.com/75231868/133866938-1f4c4431-a83a-4423-82a9-b8699c884c17.png)

- label1  
![image](https://user-images.githubusercontent.com/75231868/133866594-8e3b70a7-b5ae-47bc-b03b-c8cf0d8e85a2.png)
- position1  
![image](https://user-images.githubusercontent.com/75231868/133866969-4f8dfb05-c11a-4f6b-b0d7-b5748f11fa86.png)  
- position2  
![image](https://user-images.githubusercontent.com/75231868/133867026-d7ca0db8-eb83-434d-a8f3-735d7a5411eb.png)
- position3(범위값은 끝이 포함되지 않는다)  
![image](https://user-images.githubusercontent.com/75231868/133867053-0beadad0-9a2f-4bc1-9bb3-1beb585a8fd5.png)
- position3의 범위값을 0:2  
![image](https://user-images.githubusercontent.com/75231868/133867084-ce6f19f0-05b4-4d04-b094-6fdf1b3d7e5b.png)
  


데이터 프레임 열 선택  
방법1 [] 대괄호  
방법2 도트+열이름(.+열이름)  
![image](https://user-images.githubusercontent.com/75231868/133867218-df7f1105-9246-4b8c-ade4-69595c78bb30.png)  
![image](https://user-images.githubusercontent.com/75231868/133867221-4ff3cc85-4fcc-449f-a117-9be88197a282.png)  

df['수학'] 은 출력될때 열 이름이 나오지 않지만  
df[['수학']] 은 출력할 때 열 이름이 나온다  
  
데이터 프레임 다중선택  

![image](https://user-images.githubusercontent.com/75231868/133867350-8f6ff8f5-e736-4186-b763-f451bd53a734.png)
![image](https://user-images.githubusercontent.com/75231868/133867360-aa2f9f37-1968-4fa9-b944-359857c8807f.png)

데이터 프레임 원소선택  
![image](https://user-images.githubusercontent.com/75231868/133867761-4a0c9f66-0ded-43da-8108-b878b6e597d2.png)
![image](https://user-images.githubusercontent.com/75231868/133867764-b97bdc6e-f328-4953-b6d6-e92ac01cc7da.png)  
  
데이터 프레임 열 추가  
하나의 값으로 동일하게  
![image](https://user-images.githubusercontent.com/75231868/133867814-f6bdc9cb-91fc-46c8-8427-0dc87a96cf86.png)
![image](https://user-images.githubusercontent.com/75231868/133867818-4d0fe074-3dd4-4911-be95-86d280a3ce6a.png)
  
데이터 프레임 열 추가  
서로 다른 값으로  
![image](https://user-images.githubusercontent.com/75231868/133867849-16f92241-1364-4fc8-bfc3-c47308a31c2b.png)
![image](https://user-images.githubusercontent.com/75231868/133867851-707f4517-0c9e-4b52-bbd6-7b2bf829f99d.png)

데이터 프레임 행 추가  
![image](https://user-images.githubusercontent.com/75231868/133867920-6aa93993-fc34-45f0-9f6e-4d9a6367ae6d.png)
![image](https://user-images.githubusercontent.com/75231868/133867923-d19fcf88-e1c8-44e7-be2d-59b375cb08e8.png)

데이터프레임 원소 값 변경  
![image](https://user-images.githubusercontent.com/75231868/133868084-3b710ff7-4762-4fa1-88c5-2df63587ad79.png)
![image](https://user-images.githubusercontent.com/75231868/133868090-4589c241-240b-415f-b00f-327824329022.png)

데이터 프레임 행 열의 위치 바꾸기  
![image](https://user-images.githubusercontent.com/75231868/133868252-7ed96095-442e-4c54-86b1-2f24f5a6a68c.png)
![image](https://user-images.githubusercontent.com/75231868/133868257-a77d2929-4323-4879-9bdb-3e5ef394cf7a.png)
  
데이터프레임 특정 열을 행 인덱스로 설정  
![image](https://user-images.githubusercontent.com/75231868/133868296-9aa5356e-d809-46ef-8fe0-327097a9e28d.png)
  
![image](https://user-images.githubusercontent.com/75231868/133868371-efbafbbb-a7c0-49b8-853d-466fed09906d.png)
![image](https://user-images.githubusercontent.com/75231868/133868372-27af0dd3-31cb-4a0b-83e2-bde71fcd4a11.png)
  
데이터프레임 행 인덱스 재배열  
![image](https://user-images.githubusercontent.com/75231868/133868522-fa6011c2-8e3f-4c01-b072-36ff3af9ad21.png)
![image](https://user-images.githubusercontent.com/75231868/133868524-11db2bff-711a-4981-bf1e-8edc86a806d4.png)
  
데이터프레임 행 인덱스 초기화  
![image](https://user-images.githubusercontent.com/75231868/133868551-d5571176-f5b5-457b-bce0-de45b6dc1a75.png)  

데이터 프레임 행 인덱스를 기준으로 정렬  
ascending 옵션이 True 이면 오름차순 False 이면 내림차순  
![image](https://user-images.githubusercontent.com/75231868/133869058-8d4adf51-7de6-4c56-80cf-f51573057f13.png)
![image](https://user-images.githubusercontent.com/75231868/133869066-e05d2aca-076b-4a36-9430-c345b1ee373f.png)

데이터 프레임 데이터 값 기준으로 정렬  
![image](https://user-images.githubusercontent.com/75231868/133869109-7b9b6b43-acd5-42c2-ad53-5dfa38c0407e.png)
![image](https://user-images.githubusercontent.com/75231868/133869112-ac33b3ab-859d-4c75-a58b-c0689e44e3ec.png)


<hr>
## 4주차(2021/09/25)  
### 산술연산  
시리즈와 숫자의 연산  
![image](https://user-images.githubusercontent.com/75231868/134769636-ca4875d1-5af5-4063-a839-8c0e05a9217d.png)  
![image](https://user-images.githubusercontent.com/75231868/134769744-3158915b-e6a4-442b-b166-c96e8a4fe102.png)![image](https://user-images.githubusercontent.com/75231868/134769746-8068ea4f-99ab-4c3f-aba8-4160f93a4b4c.png)  

시리즈와 시리즈의 연산  
시리즈의 순서가 아닌 인덱스 값으로 계산한다(수학은 수학 영어는 영어)  
![image](https://user-images.githubusercontent.com/75231868/134769833-82d94803-2efc-4b3f-9e6f-e52b982a4bfb.png)![image](https://user-images.githubusercontent.com/75231868/134769837-0c1e18a7-3025-4ba4-b8d2-0a5972df23eb.png)  
![image](https://user-images.githubusercontent.com/75231868/134769988-814a9eb3-62b2-419c-91de-9ba05e3dbdb0.png)  

데이터프레임과 숫자의 연산  
![image](https://user-images.githubusercontent.com/75231868/134770224-0d7b3fc1-d9eb-4f07-9e66-1adb90a93cf8.png)  
![image](https://user-images.githubusercontent.com/75231868/134770444-d671ff77-b23f-442f-a0f3-95264d94fdb8.png)![image](https://user-images.githubusercontent.com/75231868/134770452-4ae623c0-1012-4dc8-90b4-64fd5adac849.png)

데이터프레임과 데이터프레임의 연산  
![image](https://user-images.githubusercontent.com/75231868/134770548-fd85be16-f1d6-4b38-ad8c-e60961eef9c9.png)![image](https://user-images.githubusercontent.com/75231868/134770554-3866c35f-cb03-428f-917e-46817601de2b.png)  

### 외부파일 읽기  
CSV파일  
![image](https://user-images.githubusercontent.com/75231868/134770994-5eebef20-8809-4d4d-bb3d-d787363ef6f2.png)  
![image](https://user-images.githubusercontent.com/75231868/134771009-19cb7d44-71f6-4d37-a127-53aeb8e89928.png)![image](https://user-images.githubusercontent.com/75231868/134771016-70272ed7-19b1-4c8f-9420-2b6c06dbec0e.png)

Excel 파일  
![image](https://user-images.githubusercontent.com/75231868/134771033-899dd533-de12-4bf5-8c4d-97ff5a3dc11b.png)
![image](https://user-images.githubusercontent.com/75231868/134771068-65713daf-fe87-4419-ae9e-b3dd4af9d10b.png)![image](https://user-images.githubusercontent.com/75231868/134771070-414185ab-91e4-4812-a7e7-94f86e69e860.png)

웹파일  
![image](https://user-images.githubusercontent.com/75231868/134771121-03c7082b-4395-4a3c-8200-45c0c3b57d40.png)
![image](https://user-images.githubusercontent.com/75231868/134771129-c44e961a-5fd3-4695-a5bc-56a3bbf8e634.png)


## 4주차(2021/10/02)  

### CSV파일로 저장  
to_csv() 메서드 사용  
### 여러개의 데이터 프레임을 excel 파일로 저장  
ExcelWriter() 메서드 사용  



