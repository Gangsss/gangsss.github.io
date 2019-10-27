---
layout: post
title: "python-tip"
subtitle: ""
categories: data
tags: etc
comments: true
---

## Python 공부하면서 정리해놓은 함수, 기법들

이번 글에서는 파이썬을 공부하면서 헷갈리거나 항상 찾던 것들을 정리해봤습니다.  


1.input 함수

input을 통해 나온 결과물의 자료형은 string입니다.

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/python-tip/tip1.PNG">



<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/python-tip/tip2.png">



그러므로 원하는 데이터 타입으로 변경해 줘야합니다

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/python-tip/tip3.png">

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/python-tip/4.PNG">


2.문자열 포맷팅

결과를 출력 하는데 결과물이 항상 달라지는 경우에 많이 쓰이는 문자열 포멧팅을 정리했습니다



자료형 마다 달라지는 문자열 포멧팅

%s - 문자열

%d - 정수

%f - 실수

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/python-tip/5.PNG">



%10.4f 의 뜻

실수형 자료형인데(f)

총 10칸을 이용할 거고(10)

실수형 자료형은 소숫점 자리 4개까지만(.4)

오른쪽 정렬할거야(양수/ 음수면 왼쪽 정렬)



3.replace 함수

말그대로 바꿔주는 함수입니다.

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/python-tip/6.PNG">

'-'을 ','으로 변경해 줍니다.



4.리스트 안에 있는 지 확인

in을 활용해서 리스트 안에 해당하는 것이 있는 지 확인합니다.

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/python-tip/7.PNG">


5.if 문 한줄로 쓰기(조건부 표현식)

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/python-tip/8.PNG">

한 줄로 작성이 가능하여 가독성이 좋아집니다



6.range의 step

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/python-tip/9.PNG">

range함수 안에 step을 지정해줘서 더 편리하게 쓸 수 있습니다.

다음과 같이 홀수를 출력할 때도 굳이 i를 변경해주지 않고도 출력이 가능합니다.



7.리스트 내포

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/python-tip/10.PNG">

[표현식 for 항목 in 반복 가능한 객체 if 조건]을 통해서 리스트를 생성할 수 있습니다.



8.아스키 <-> 문자

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/python-tip/11.PNG">



ord함수와 chr함수를 통해 문자를 아스키코드로, 아스키코드를 문자로 변환이 가능합니다.



9.함수에서 *args, *kwarg

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/python-tip/12.PNG">

함수에 입력할 값이 몇개인지 모를 때, *args매개변수를 통해 위와 같이 활용 할 수 있습니다.



<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/python-tip/13.PNG">

kwargs는 매개변수들을 딕셔너리 형태로 저장되며, a=b값이 key: value형태인 a:b로 저장 됩니다
