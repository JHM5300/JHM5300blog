---
title: "[javascript] 리액트 첫 글"
excerpt: "자바스크립트의 최신 문법"
categories:
  - javascript
toc: true
toc_sticky: true
tags:
  - javascript
---

# 자바스크립트 문법 공부

### shorthand property names

> key와 value가 동일한 경우에는 하나로만 생략이 가능하다.

```
const obj = {
    name : name,
    age:age,
}
```

```
const obj = {
    name,
    age,
}
```

### Destructuring assignment

> 객체나 배열을 분해해서 그 값을 개별 변수에 담을 수 있게 하는 JavaScript 표현식

```javascript
const obj = {
  name: "kim",
  age: 20,
};
```

```javascript
const { name, age } = obj;
console.log(name); // kim
console.log(age); // 20
```

###Spread syntax

> 복사할때 많이 사용, `...` 을 이용해 배열이나 객체에 들어 있는 하나하나 씩을 낱개로 가져와서 복사한다.

```javascript
const item = { name: "콜라", price: 200 };
const item2 = { name: "사이다", price: 100 };
const itemList = [item, item2];

const copyItemList = [...itemList];
console.log(copyItemList); // [{name:콜라,price:200},{name:사이다,price:100}]
item.price = 150;
console.log(copyItemList); // [{name:콜라,price:150},{name:사이다,price:100}]
```

**주소 값만 복사가 되어있기 때문에 실제로 전부 다 동일한 obj를 가르키고 있음을 알자.**

### Default parameters

> 함수를 호출 할 때 아무런 인자를 전달되지 않을 때 기본인 초깃값을 지정할 수 있다.

```javascript
function defaultMessage(message = "기본 메세지") {
  console.log(message); // 기본 메세지
}
```

### Ternary Operator

> 삼항연산자를 이용해 if문을 축약할 수 있다.

```javascript

(조건문) ? (조건문이 true일때) : (조건문이 false일때)
pwdRef.value != "" ? tryLogin() : alert("비밀번호를 입력하세요.");
```

### Optional chaining

> `?.` 를 이용해 프로퍼티가 없는 줃첩 객체를 에러(TypeError) 없이 안전하게 접근할 수 있는 연산자이다.

```javascript
const user =
  { name: { first: "John", last: "Doe" } } >
  user?.name?.first > //'John'
  user?.address?.street; //undefined
```

### Nullish Coalescing Operator

> `??` 를 이용해 논리 연산자로 왼쪽 피연산자가 null이나 undefined일 때, 오른쪽 피연산자를 return한다.

```javascript
false : false, '' , 0, null, undefined
```

기본 값을 지정할 때 || 연산자를 사용하지만 이것을 사용하면 버그가 일어날 수 있다.

```javascript
{
  const name = "";
  const userName = name || "Guest";
  console.log(userName); // Guest
}
//Nullish Coalescing Operator
{
  const name = "";
  const userName = name ?? "Guest";
  console.log(userName);

  const num = 0;
  const message = num ?? "undefined";
  console.log(message); //0
}
```

출처)
<https://velog.io/@devky/TIL-Javascript-%EC%B5%9C%EC%8B%A0-%EB%AC%B8%EB%B2%95-%EC%A0%95%EB%A6%AC>
<https://developer.mozilla.org/ko/>
<https://github.com/dream-ellie/learn-javascript/tree/master/notes/es6-11>
