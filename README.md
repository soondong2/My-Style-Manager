# Passion King Project

![캡처](https://user-images.githubusercontent.com/100760303/198916924-dc6855ed-331a-4d86-bd60-6bf57ff47fb1.PNG)

<br>

## 서비스 내용
> ***“오늘은 어떤 옷을 입어야 하지?”***

고민하는 사람들을 위한 쉽고 간편한 코디 추천 모델 **My Style Manager**입니다.

위 서비스를 통해 기대하는 바는 다음과 같습니다.

1) 준비 시간 단축

2) 유사 제품 구매 가능

3) 패션 자신감 향상

위 서비스를 사용하는 방법은 다음과 같습니다.

- 상의 또는 하의 의류 사진을 촬영합니다.
- 촬영한 사진을 업로드시 유사한 코디 스타일을 추천해줍니다.

<br>

## Data Source
![캡처2](https://user-images.githubusercontent.com/100760303/198917890-3f67fb93-82b7-41be-bae0-cabc4739c1a4.PNG)

<br>

## 기술 내용
### AutoEncoder & **Similarity Calculation**
![Untitled](https://user-images.githubusercontent.com/100760303/198917354-c4592229-a013-40df-9931-d3b5462b2e95.png)
<br>

Encoder를 통해 데이터를 압축하여 의미 있는 Latent Feature들을 뽑아내고 Decoder를 통해 이미지를 다시 복원시킵니다. Latent Feature들을 이용해 Cosine Similarity, Euclidean Distance, Pearson Similarity 등 유사도를 구하고 가장 성능이 뛰어난 유사도를 사용해 Input 이미지와 유사한 패션 착용 이미지 Top 10을 추천합니다.
<br>

### OpenCV
Input으로 입력된 의류 이미지를 모델을 학습시킨 이미지와 같은 환경으로 만들어주기 위해 이미지에서 배경을 하얗게 만들고 의류만을 객체로 인식할 수 있도록 하였습니다.

<br>

## 결과
<img width="60%" src="https://user-images.githubusercontent.com/100760303/198918755-fa121b68-4f3c-4dfa-803b-3b2e1584e1d4.png"/>
<img width="60%" src="https://user-images.githubusercontent.com/100760303/198918798-9a7d4a5a-e9f8-4d8a-a88b-553ad8873c19.png"/>

<br>

## Streamlit
https://lion-hill-final-project-main-gyuho-h3kna3.streamlitapp.com/
