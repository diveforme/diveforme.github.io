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

현재 진행하고 있는 날씨 웹앱에서 사용중인 api제공처에서도 구글에서 제공하는 geocoding api기능을 제공한다. 굳이 구글 api켰었는데, 그거 끄고 이 사이트의 기능을 사용하려한다.

## geocoding 이란 무엇인가?
geocoding이란, 도시명 같은 이름을 사용해서 위도와 경도를 get할 수 있게 한다.

## reverse geocoding이란 무엇인가?
위도와 경도 정보로부터 도시이름이나 위치명을 알아내는 것이다. api콜은 아래와 같이 날린다.
> http://api.openweathermap.org/geo/1.0/reverse?lat={lat}&lon={lon}&limit={limit}&appid={API key}

주의할 점은, lat, lon 등을 감싸고 있는 중괄호를 반드시 없애고 값만 넣은 채 api를 날려야 한다.

