---
title: "asmrplayer"
date: 2019-08-26 08:26:28 -0400
categories: dev
---
##
---
###Intro
- 캡스톤 team project
- repository [asmrplayer]
- Barcode + STT 인식 Refrigerator Manager 앱
- 4 people(2018.3.1 ~ 6.8)
---
###Program Stacks
- Raspberry Pi
- Apache
- PHP
- MySQL
- SQLite
- JAVA(Android)
- kakao plus friend API
---
###Implementation
##### Web
- Raspberry Pi + 우분투(Apache + PHP + MySQL) APMSetup 웹 서버 구축
- PHP + MySQL + kakao plus friend API : 간단한 카카오봇
- PHP + MySQL : 앱 데이터 웹 서버에 백업

##### App
######상품등록
- Zxing Library : Barcode 인식
- JSoup Library : beepscan 웹 페이지 바코드 정보 파싱
- STT Library : 음성 인식

######냉장고(메인)
- StickyGridHeader Library + SQLite : 메인 화면 구성
- RequestHttpURLConnection + AsyncTask : 냉장고 정보 웹 서버와 통신
- 조건 정렬 및 레시피 검색
- 유통기한 Notification

######장바구니
- ListView + SQLite : 장바구니 화면 구성
- RequestHttpURLConnection + AsyncTask : 장바구니 정보 웹 서버와 통신

######기타
- 안드로이드 로그인
---
###My part
- 장바구니 전체
- 냉장고(메인) : StickyGridHeader Library + SQLite : 메인 화면 구성
- Zxing Library : Barcode 인식
- JSoup Library : beepscan 웹 페이지 바코드 정보 파싱
//- Apache HTTP Client : 웹 서버와 통신(ver1) >> 나중에 변경
- RequestHttpURLConnection + AsyncTask : 웹 서버와 통신(ver2)
- PHP + MySQL + kakao plus friend API : 간단한 카카오봇
- PHP + MySQL : 앱 데이터 웹 서버에 백업

[asmrplayer]: https://github.com/blackjayH/asmr-player/
