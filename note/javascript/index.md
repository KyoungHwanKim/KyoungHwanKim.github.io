---
layout: post
title: "JavaScript Study 1"
subtitle: "자바스크립트 스터디 1"
type: "JavaScript"
note: true
text: true
draft: true
author: "KyoungHwan Kim"
post-header: true
header-img: None
order: 2
---

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