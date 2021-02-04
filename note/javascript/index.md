---
layout: post
title: "JavaScript Study 1"
subtitle: "자바스크립트 스터디 1"
type: "JavaScript"
note: true
text: true
draft: false
author: "KyoungHwan Kim"
post-header: true
header-img: None
order: 2
---

#### 생활코딩 JavaScript 강좌 OT ~ 비교 까지의 정리본.

### 간단한 코드 작성과 실행

자바스크립트는 브라우저 뿐만 아니라 서버를 포함한 여러 환경에서 동작함.

메모장에 아래의 코드를 입력한 뒤 확장자명 html로 저장. 인코딩 타입은 UTF-8.

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
    </head>
    <body>
        <script>
            alert('Hello world');
        </script>
    </body>
</html>
```

해당 html 파일을 실행시켰을 때, 경고창이 뜨면 성공.

### 숫자

자바스크립트에서 숫자를 표현할 때에는, 큰 따옴표나 작은 따옴표를 붙이지 않고 숫자만 입력하면 된다. 파이썬과 비슷하다.

```javascript
alert(1 + 1); // 2
alert(1.2 + 1.3); // 2.5
alert(2 * 5); // 10
alert(6 / 2); // 3
```

좀 더 복잡한 연산은 Math 클래스를 통해 연산할 수 있다.

```javascript
alert(Math.pow(3, 2)); // 9, 3의 2승
alert(Math.round(10.6)); // 11, 10.6을 반올림
alert(Math.ceil(10.2)); // 11, 10.2를 올림
alert(Math.floor(10.6)); // 10, 10.6을 내림
alert(Math.sqrt(9)); // 3, 3의 제곱근
alert(Math.random()); // 0부터 1.0 사이의 랜덤한 숫자
```

### 문자

자바스크립트에서 문자를 표현할 때에는, 큰 따옴표 혹은 작은 따옴표로 감싸줘야 한다. 큰 따옴표로 시작했다면 큰 따옴표로 끝내야 하고, 작은 따옴표로 시작했다면 작은 따옴표로 끝내야 한다.

```javascript
alert("Hello World");
alert('Hello World');
```

숫자를 따옴표로 감쌌을 때에도 문자가 된다.

```javascript
alert(typeof "1"); // 결과 : string
alert(typeof 1); // 결과 : number
```

만약 따옴표 문자를 표현하고 싶다면, `\`와 따옴표를 같이 입력해 주면 된다.

```javascript
alert("kyounghwan's javascript"); // syntax error
alert("kyounghwan\'s javascript"); // kyounghwan's javascript
```

이런 식으로 입력해야 하는 문자들이 몇 가지 있는데, 이를 "이스케이프 시퀀스"라고 한다.

여러 줄에 걸쳐 표시하고 싶다면, `\n`을 입력해 주면 된다.

```javascript
alert("안녕하세요.\n자바스크립트입니다.");
```

문자들도 숫자와 마찬자기로 연산을 진행할 수 있는데, 문자와 문자를 더할 때에는 `+`로 더해준다.

```javascript
alert("Hello" + " World."); // Hello World.
```

문자의 길이를 구할 때에는, 문자 뒤에 `.length`를 붙여 준다.

```javascript
alert("Hello World.".length); // 결과 : 12
```

### 변수

변수는 문자나 숫자 같은 값을 담는 컨테이너 역할을 한다. 변수에 담겨진 값은 연산할 때 사용할 수 있고, 언제든지 바꿀 수 있다.

자바스크립트에서 변수를 선언하려면 `var`로 시작하고 변수명을 지정해주면 된다.

```javascript
var a = 1;
alert(a); // 결과 : 1
aleart(a + 1); // 결과 : 2

var a = 2;
alert(a); // 결과 : 2
alert(a + 1); // 결과 : 3

var a = "Hello";
alert(a + " World."); // 결과 : Hello World.

var a = "Hello", b = "World";
alert(a); // 결과 : Hello
alert(b); // 결과 : World
```

### 비교

비교 연산자를 통해 주어진 값들이 같은지, 다른지, 큰지 등을 판단할 수 있다. 비교의 결과는 `true` or `false`이다.

#### ==

두 값이 같은지 판단하는 연산자이다. 서로의 값이 같다면 `true`를 반환하고, 다르다면 `false`를 반환한다.

```javascript
alert(1 == 2) // false
alert(1 == 1) // true
alert("one" == "two") // false 
alert("one" == "one") // true
```

#### ===

앞서 설명한 `==` 연산자와 유사하지만, 이 연산자는 해당 값의 자료형까지 일치해야 `true`를 반환한다. 그 이외에는 `false`를 반환한다.

```javascript
alert(1 == '1'); // true
alert(1 === '1'); // false
```

`==` 연산자 보다는 `===` 연산자를 사용하는 것을 강력히 권한다고 한다.

```javascript
alert(null == undefined); // true
alert(null === undefined); // false
alert(true == 1); // true
alert(true === 1); // false
alert(true == '1'); // true
alert(true === '1'); // false
 
alert(0 === -0); // true
alert(NaN === NaN); // false
```

#### !=

프로그래밍에서 `!`는 부정을 의미한다. 따라서 서로 다른 값인지 확인하는 연산자이다. `==` 연산자와 정반대의 결과를 보여준다.

```javascript
alert(1 != 2); // true
alert(1 != 1); // false
alert("one" != "two"); // true
alert("one" != "one"); // false
```

`!=` 연산자가 있다면 `!==` 연산자도 있다. 설명은 생략...

#### >, >=, <, <=

다양한 비교 연산자이다. 수학에서의 의미와 같으니 설명은 생략...

```javascript
alert(10 > 20); // false
alert(10 > 1); // true
alert(10 > 10); // false

alert(10 >= 20); // false
alert(10 >= 1); // true
alert(10 >= 10); // true
```