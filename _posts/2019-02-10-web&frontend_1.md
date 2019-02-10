---
layout: post
title: "CS231n- 2강"
subtitle: "CS231n"
categories: development
tags: WEB
comments: false
---



[페이스북 이노베이션 랩](https://www.facebook.com/innovationlabkorea/?eid=ARCe_mN3CP7Y9TxxQsRcbv7cZx2OmjmSg78adsF3eRkCWni2eZ62CoFXYUF2p1DzX2G2kgwkw2NZ3XLn)에서 진행하는 웹 프론트엔드과정을 듣고 정리한 글입니다.



동아리에서 크롤링을 공부하다보니 html, css에 간단히 배웠는데  이번에 좋은 기회를 통해 이고잉님께 배울 수 있는 기회가 생겨 수업을 듣고 필요한 내용만 정리한 내용입니다. 



자세한 사항은 이고잉님의 [생활코딩](https://opentutorials.org/course/3084)을 참고해주세요!

---

html 태그

- <~>으로 시작해 
   
   </~>으로 끝난다.



u - underline

strong - 굵게



h1 

- 제목에 쓰는 태그
- 숫자가 늘어 남에 따라 작아진다.
<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/h1_code.png">

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/h1.png">


br 

- 줄 바꿈 하는 태그
- 대신 닫는 태그는 없다.

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/br.png">


list

- 정리해서 list화 시킬 수 없을까?
- li 태그

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/list.png">



- list가 두개로 나눠진다면 ul태그를 중간에 써준 것이 약속!
<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/u.png">




ol 태그

- 리스트처럼 정리하고 싶지만 숫자를 넣고 싶다! 
- ol태그 후 li 태그

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/ol.png">

mark up language

- 이건 list다라고 태그로 하나하나 명명해주는 언어(약속)



팀 버너스리

WEB Browser - html

WEB Server - url

htttp



웹이 웹이기 위한 태그는?



a 태그(링크)

- a 태그는 이것이 링크다 라는 것만 알려줘

- 속성이 필요하다!
- href(hypertext reference)
<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/a_href.png">




title tag


<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/title_tag.png">




meta

데이터를 설명 하는 데이터

- charset
- encoding을 맞추기 위해

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/meta.png">


head& body

메타데이터와 컨텐츠 데이터를 나누자

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/head_body.png">



img 

src에 unplash.com의 이미지를 활용해 홈페이지를 풍성하게

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/get_img.png">


---



정보와 디자인을 분리



css 등장의 이유

- html이 정보의 표현에 집중하게 한다.
- 디자인에 최적화된 css에 집중.



css를 배운다

1. 선택자(selector)를 배워 가는 과정 - targeting
2. 효과(description)를 배워가는 과정 


<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/css_basic.png">

style태그로 시작 하고 끝냄

1. li - tag 선택자 selector

   ex) li {

   ​		color : red;         - 효과(description)

   ​	}

   ​	

2. id 선택자 -단하나의 id에 해당하는 것만으로 targeting 가능

   ex) #em

   

3. classs 선택자 - grouping 하는 선택자

   ex) class = viewed



html 에서 말하는 elements는 태그다.



- box model


<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/css_box.png">



h1태그는 전체 화면을 쓴다.



border-width : 10px;    -  테두리 두께

border-style : solid;      -  테두리 종류

border-color : magenta;   - 테두리 색깔



border : 10px solid magenta - 합쳐서 쓸 수 있다.

---

이고잉님이 코딩에 대해 몇가지 말씀해주신 것



알고 있는 것도 낯설게 하는 것도 능력이다.



코드는 설계도다!

하지만 건축과 다르게 설계도를 짜면 바로 프로덕트로 나온다.

결국, 오픈소스는 제품을 주는 것!



코드한줄 써보고 확인해보고 

한자써보고 확인해보자 문제의 원인을 하나씩 풀어가자



코딩을 공부할 때, 중복을 제거하는 코딩을 해보자
