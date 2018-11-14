---
layout: post
title: "면접 대비 개념 정리"
date: 2018-11-11
excerpt: "기술면접 대비 개념 정리"
tag:
- 취준
comments: true
---

contents
1. [JAVA](#java)
2. [ajax](#ajax)

- - -

# JAVA

## 자바의 특징
1. 운영체제에 독립적이다.
  - 자바 프로그램은 JVM과 통신하고, JVM이 전달 받은 프로그램을 해당 운영체제에 맞게 변환한다.  
  - JVM: Java Virtual Machine, 자바를 실행하기 위한 가상의 컴퓨터
2. __객체지향언어__
  - 자바는 객체지향개념의 특징인 __상속, 캡슐화, 다형성__ 이 잘 적용된 언어이다.
3. 자동 메모리 관리(Garbage Collection)
  - garbage collector가 자동적으로 메모리를 관리해 준다.
  - 프로그래머가 보다 프로그래밍에 집중할 수 있다.  

## 객체지향언어
- 객체지향언어(JAVA) ↔ 절차적언어(C)
- <hly>객체(=Class)간의 관계를 맺어줌으로써 유기적으로 프로그램을 구성한다.</hly>
- <hlr>코드의 재사용성이 높다.</hlr>
- <hlr>코드의 유지보수가 용이하다.</hlr>
- <hlr>코드의 중복을 최소화 한다.</hlr>

## 상속
- __상속이란 기존의 클래스를 재사용하여 새로운 클래스를 작성하는 것이다.__
- 코드의 재사용성을 높이고 코드의 중복을 제거하여 프로그램의 생산성과 유지보수에 기여한다.
- 클래스 이름 뒤에 'extends' 키워드를 사용한다.

## 오버라이딩
- __부모 클래스로부터 상속받은 메소드의 내용을 변경하는 것.__
- 메소드의 이름, 매개변수의 개수, 타입, 반환타입이 부모 클래스의 메소드와 모두 같아야 한다.

## 오버로딩
- __하나의 클래스 내에 같은 이름의 메소드를 여러 개 정의하는 것__
- 메소드 이름이 같아야 하고, 매개변수의 개수 또는 타입이 달라야 한다.
~~~java
int add(int a, int b){}
int add(inta, intb, int c){}
~~~
- 하나의 이름으로 여러 개의 메소드를 정의할 수 있기 때문에 메소드 작성이 효율적이고 직관적인 사용이 가능하다.

## 다형성
- __여러가지 형태를 가질 수 있는 능력__
- 조상 클래스 타입의 참조변수로 자손 클래스 타입의 인스턴스를 참조할 수 있다.

## 캡슐화 (정보 은닉)
- 접근 제한자를 이용해서 해당 메소드나 변수를 외부에서 접근할 수 없게 함
- 접근 제한자에 따라 정보를 숨기는 범위가 달라짐
- private → (package) → protected → public 순으로 접근제한 약해짐
- private: 해당 클래스만 접근 가능
- protected: 해당 클래스와 자손 클래스 & 동일 패키지 내에서 접근가능
- public: 어떤 클래스라도 접근 가능


- - -

# Ajax

- Asynchronous JavaScript + XML
- 대화형 웹 어플리케이션을 개발하는 방법
- 페이지의 이동 없이 화면전환이 가능하다(속도향상)

[Ajax를 사용하면 좋은 경우]  
1. 불필요한 팝업 또는 페이지 전환이 많을 때  
2. 하나의 웹 페이지 안에서 다양한 작업을 수행할 때  

[Ajax 사용 예]  
추천 검색어 - 네이버나 구글에서 검색어 입력 시 밑에 추천 검색어 뜨는 거  
회원가입 Form - 가입 조건을 충족하지 않았을 때, 창을 새로 띄우지 않고 해당페이지에 바로 메세지를 보여줌  

[단점]
JavaScript를 사용해야 해서 유지보수, 디버깅이 어렵다  

## 동기 vs 비동기
참고) [동기와 비동기의 개념과 차이](http://private.tistory.com/24)  

|     |   동기  |  비동기  |
|:----|:-------:|:--------:|
|장점 |   설계가 쉽고 직관적  | 서버로 부터 결과가 주어지는 동안 다른 작업을 수행할 수 있다.   |
|단점 | 서버로 부터 응답을 받을 동안 다른 작업을 수행 할 수 없다  | 설계가 복잡 |
{: rules="groups"}  