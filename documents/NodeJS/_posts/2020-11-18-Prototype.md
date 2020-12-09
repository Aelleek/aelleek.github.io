---
layout: article
title: Syntax - Prototype
permalink: /documents/NodeJS/Prototype
sidebar:
  nav: nodejs
aside:
    toc: false
tags: NodeJS 
---

## Prototype
<div class = "blue-div">
자바스크립트는 프로토타입 기반 객체지향 프로그래밍 언어이다.
ES2015부터 class 키워드를 지원하기 시작했으나, 문법적인 지원일뿐 자바스크립트는 여전히 프로토타입 기반의 언어이다.

 
자바스크립트에서도 다른 객체 지향(Object Oriented) 언어와 마찬가지로 객체의 원형(Prototype)을 정의한 후 그 원형에서 새로운 인스턴스 객체를 만들어 낼 수 있다.
프로토타입 객체는 데이터를 넣어 두려는 목적보다는 하나의 틀로 사용하기 위해 만든다.
프로토타입 객체를 정의하고 나면 new 연산자를 사용하여 인스턴스 객체들을 만들 수 있다.
</div>

```javascript
function Person(name, age){
    this.name = name;
    this.age = age;
}

Person.prototype.walk = function(speed){
    console.log(speed + 'km 속도로 걸어갑니다.');
}
```
<div class="blue-div">
Person 객체는 name과 age 속성을 갖는다. 그리고 이 객체에 walk 함수를 속성으로 추가하고 싶다면
Person.walk = function(){} 과 같은 형태가 아니라 Person.prototype.walk=function(){} 의 형태로 넣는다.   
Person 객체가 실제 데이터를 담기 위해 만들어진 것이 아니라 다른 인스턴스 객체를 만들기 위한 틀로 만들어졌기 때문이다.
Person 객체 안에 있는 prototype 속성에 데이터나 함수를 속성을 추가하면 실제 인스턴스 객체를 만들 때 메모리를 효율적으로 관리할 수 있다.(어떻게??) 
</div>



