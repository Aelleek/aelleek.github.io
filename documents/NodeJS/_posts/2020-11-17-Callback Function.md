---
layout: article
title: Syntax - CallbackFunc
permalink: /documents/NodeJS/Callback Function
sidebar:
  nav: nodejs
aside:
    toc: false
tags: NodeJS 
---

## Callback Function

<div class="blue-div">
자바 스크립트의 변수에는 숫자나 문자열 같은 데이터 객체뿐만 아니라 함수도 할당할 수 있다.
변수에 함수를 할당할 수 있기 때문에 함수를 호출할 때 전달인자로 다른 함수를 보내 줄 수 있다. 

자바 스크립트는 비동기 프로그래밍 방식으로 동작한다.
그래서 함수를 실행한 후 결과 값이 반환될 때까지 기다리지 않고 다음 코드를 실행한다.
함수를 실행할 때 함수를 전달인자로 보냈다면 함수의 실행이 끝났을 때 전달인자로 보낸 함수가 실행이 되고,
그 함수를 콜백 함수라고 한다.
콜백함수는 함수가 실행되는 중간에 호출되어 상태 정보를 전달하거나 결과값을 처리하는데 사용된다.
</div>
```javascript
function add(a, b, callback){
    let result = a + b;
    callback(result)

add(10, 10, function(result){
    console.log("파라미터로 전달된 콜백 함수 호출");
    console.log(result);
});
}
```
<div class="blue-div">
위의 add() 에서 값을 반환하는 return 코드가 존재하지 않는다.
대신 반환할 값을 callback 함수로 전달하여 add()가 실행이 완료된 후 callback 함수가 실행되면서 
전달인자로 보낸 result값을 사용한다.

callback 함수의 경우 미리 정의된 함수를 전달인자로 보낼수도 있지만 위의 코드와 같이 익명 함수로 만들어서 보낼 수 있다.  
</div>

## 함수 안에서 값을 반환할 때 새로운 함수를 만들어 반환하는 방법.
<div class="blue-div">
함수를 실행했을 때 return 값으로 또 다른 함수를 반환받으면 그 함수를 그대로 실행할 수 있다.
이렇게 만들면 하나의 함수를 실행했을 때 추가적인 결과를 얻거나 또는 추가 작업을 할 수 있다.   
</div>

```javascript
function add(a, b, callback){
    let result = a+b;
    callback(result)

    var history = function(){
        return `${a} + ${b} = ${result}`;
    }
    return history
}

const add_history = add(10, 10, function(result){
    console.log("add func의 callback func 호출");
    console.log(result);
});

console.log(`결과 값으로 받은 함수 실행 결과 : ${add_history()}`);
```
```
결과값
add func의 callback func 호출
20
결과 값으로 받은 함수 실행 결과 : 10 + 10 = 20
```

<div class="blue-div">
위의 코드에서 add_history에 반환된 함수는 add() 안에서 만들어지는데 history() 안에 있는 변수들은
함수가 반환된 후에도 계속 접근해서 사용할 수 있다.
history() 안에서 count 변수를 선언하고 호출 될때마다 증가하는 코드를 넣은 후에
add_history() 함수를 여러번 호출한다면 호출할 때마다 count 변수의 값이 증가하는 것을 확인할 수 있을 것이다.

보통의 경우 add 함수의 실행이 종료되고 나면 add 함수가 메모리에 접근할 수 없는 상태가 되지만
이와 같이 함수 안에서 새로운 함수를 만들어 반환하는 경우에는 예외적으로 접근을 허용한다.
이러한 것을 클로저(Closure)라고도 부른다.
</div>


