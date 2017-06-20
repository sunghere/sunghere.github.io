---
layout: post
title : "자바스크립트 inner html 태그안 function안에 실제값넣기"
tags: 
  - javascript
---

## inner html로 넣어주는 문자의 태그안에서 javascript의 변수를 동적으로 변경하여 넣어주고싶을 때가 있을것이다.

그러나 많이 마주치게되는 문제가 있다.

> uncaught reference error "변수명" is not defined 

위와 같은 오류가 콘솔에 찍히게되는데 이렇게 발생하는 오류는 보통 아래와 같다.

```javascript

inner_text += "<button type='button'' onclick='myfunction("+value+")'>";


```

value 값이 변수로 인식되어 버려 해당 문제가 발생 한다.

### 해당문제를 해결해주려면 코드를 아래와 같이 수정하여 주면 정상 작동된다.

```javascript
inner_text += "<a href='#' onclick='myfunction("+value+")'>";
inner_text = inner_text.replace(/#{value1}/gi, '"' + value + '"');

```