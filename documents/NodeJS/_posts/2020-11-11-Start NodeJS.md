---
layout: article
title: NodeJS.
permalink: /documents/NodeJS/start-nodejs
sidebar:
  nav: nodejs
aside:
    toc: false
tags: NodeJS 
---

## 노드JS 란.
<div class="blue-div">
Node.js 는 Chrome V8 javascript 엔진으로 빌드된 Javascript 런타임입니다.
( 출처 - Node.js 공식 사이트.)

Node.js는 확장성 있는 네트워크 애플리케이션(특히 서버 사이드) 개발에 사용되는 소프트웨어 플랫폼이다. 작성 언어로 자바스크립트를 활용하며 Non-blocking I/O와 단일 스레드 이벤트 루프를 통한 높은 처리 성능을 가지고 있다.

내장 HTTP 서버 라이브러리를 포함하고 있어 웹 서버에서 아파치 등의 별도의 소프트웨어 없이 동작하는 것이 가능하며 이를 통해 웹 서버의 동작에 있어 더 많은 통제를 가능케 한다.

( 출처 - 위키백과 )
</div>


## 자바스크립트 런타임
<div class="blue-div">
노드는 자바스크립트 런타임이다. 런타임은 특정 언어로 만든 프로그램들을 실행할 수 있는 환경을 뜻한다.
즉, 노드는 자바스크립트 프로그램들을 실행할 수 있다.

이전에는 자바스크립트 프로그램을 웹 브라우저 위에서만 실행할 수 있었다. 
브라우저 외의 환경에서 자바스크립트를 실행하기 위한 시도가 있었지만 실행 속도 문제 때문에 이슈가 있었다.
그러다 2008년 구글이 V8 엔진을 사용한 크롬을 출시하면서 속도문제가 해결되어 라이언 달(Ryan Dahl)이 2009년 V8 엔진 기반의 노드 프로젝트를 시작했다.

노드는 V8 엔진과 더불어 libuv라는 라이브러리를 사용한다.
libuv 라이브러리는 노드의 특성인 이벤트 기반, 논 블로킹 I/O 모델을 구현하고 있다.
</div>


## 이벤트 기반
<div class="blue-div">
이벤트 기반(event-driven)이란 이벤트가 발생할 때 미리 지정해둔 작업을 수행하는 방식을 말한다.
이벤트로는 클릭이나 네트워크 요청 등이 있을 수 있다.

이벤트 기반 시스템에서는 특정 이벤트가 발생할 때 무엇을 할지 미리 등록해두어야 한다.
이를 이벤트 리스너(envent listener)에 콜백(callback) 함수를 등록한다고 표현한다.

노드도 이벤트 기반 방식으로 동작하므로, 이벤트가 발생하면 이벤트 리스너에 등록해둔 콜백 함수를 호출한다.
발생한 이벤트가 없거나 발생했던 이벤트를 다 처리하면, 노드는 다음 이벤트가 발생할 때까지 대기한다.
</div>    


## 이벤트 루프
<div class="blue-div">
이벤트 루프는 이벤트 발생 시 호출할 콜백 함수들을 관리하고, 호출된 콜백 함수의 실행 순서를 결정하는 역할을 한다. 노드가 종료될 때까지 이벤트 처리를 위한 작어비을 반복하므로 루프라고 부른다.

노드는 자바스크립트 코드의 맨 위부터 한 줄씩 실행하고, 함수 호출 부분이 있다면 호출한 함수를 호출스택(call stack)에 넣는다.    
</div>
```Javascript
function first(){
    second(); console.log("first");
}
function second(){
    third(); console.log("second");
}
function third(){
    console.log("third");
}
first();
```
<div class="blue-div">
위와 같은 자바스크립트 파일을 실행시켰을 때, first() - second() - third() 순서로 호출된다.
그리고 호출된 순서와 반대로 실행이 완료된다.
호출 스택을 그려보면 다음과 같은 형태로 스택에 함수가 쌓인다.
</div>

| third() |
| second()|
| first()|
| anonymous|

<dir class="blue-div">
anonymous 함수는 처음 실행 시의 전역 컨텍스트(global context)를 의미하고 컨텍스트는 함수가 호출되었을 때 생성되는 환경을 의미한다.
자바스크립트 코드는 실행시 기본적으로 전역 컨텍스트 안에서 돌아간다고 볼 수 있다.  

</dir>












