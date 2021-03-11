---
layout: single
title:  "자바스크립트 문법"
cartegory: 
    - TIL
---

# True False 체크하기
```javascript
console.log(0 == false); // T
console.log(0 === false); // F
console.log(''== false); // T
console.log(''===false); // F
console.log(null == undefined); // T
console.log(null === undefined); // F
```

# 메모리에 자바스크립트변수가 할당되는 법
원시타입(Primitive : number,string..etc)변수의 경우 메모리에 값이 저장된다.

오브젝트 타입의 변수는 오브젝트 데이터전체를 메모리에 올려놓지 않는다. 오브젝트가 무거울 경우 메모리에 부담을 주기 떄문이다. 메모리에는 레퍼런스가 저장되며, 이 레퍼런스가 오브젝트를 가리키는 형태로 저장된다.

```javascript
const person = {name: 'robin', age:23};
person.age = 24;
console.log(person.age);
```

# 자바스크립트의 변수 선언
자바스크립트에서 변수를 선언할 때는 `let`과 `const`를 쓴다.
let의 경우 값이 나중에 값을 바꾸고 싶을 때 사용하며, const는 절대 수정되지 않을 상수 값을 할당할 떄 쓴다. const를 사용하여 값을 할당하면, 이 값은 절대 다른 값으로 바뀔 수 없다.

# 바닐라 자바스크립트를 모던하게 쓰는 간편한 방법
.js파일의 가장 상단에 ` "use strict;" `라는 문장을 삽입한다. 이 문장을 명시함으로써 바닐라 자바스크립트에서 코드를 모던하게 쓸 수 있게 해준다.
