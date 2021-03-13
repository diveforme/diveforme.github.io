---
layout: single
title:  "Reverse geocoding으로 도시 이름 가져오기"
cartegory:
    - Web
tags:
    - Javascript    
---

> <https://openweathermap.org/api/geocoding-api#reverse>

## 도시 이름 받아오기

현재 진행하고 있는 날씨 웹앱에서 사용중인 api제공처에서도 구글에서 제공하는 것과 비슷한 geocoding api기능을 제공한다. 굳이 구글 api켰었는데, 그거 끄고 이 사이트의 무료 기능을 사용하려한다.

## geocoding 이란 무엇인가?
geocoding이란, 도시명 같은 이름을 사용해서 위도와 경도를 get할 수 있게 한다.

## reverse geocoding이란 무엇인가?
위도와 경도 정보로부터 도시이름이나 위치명을 알아내는 것이다. api콜은 아래와 같이 날린다.
> http://api.openweathermap.org/geo/1.0/reverse?lat={lat}&lon={lon}&limit={limit}&appid={API key}

주의할 점은, lat, lon 등을 감싸고 있는 중괄호를 반드시 없애고 값만 넣은 채 api를 날려야 한다.

➕ 21-03-14 ~~화이트데이~~

이 오픈 웨더맵의 api 날릴때마다 값이 계속 바뀐다.. 날릴때마다 반포본동, 용산구, 서울, 광명 등등 뜨는 위치 리스트들이 계속 바뀐다. 공식문서에 나와있는대로 limit 옵션을 주어 5개의 위치를 받아오도록 했는데, 그렇다고 또 한개로 limit을 주면 반포본동 나온다. 뭐지진짜.

어제 테스트 했을 때 서울이 나와서 되는줄 알았더만, 계속 요청해서 값을 확인해보면 값이 매번 바뀌었다.

빠르게 버리고 안정적인 구글의 geocoding api를 사용한 결과, 현재 내 위치인 `대한민국 서울특별시 동작구`를 안정적으로 받아오는 결과를 확인할 수 있었다. 

역시 무료에는 한계가 있나봄
