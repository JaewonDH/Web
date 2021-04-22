
출처 :https://ko.javascript.info/ 개인공부 정리 
## 변수 생성방법

1. 기본변수 
```
  var testA="AAA";
  var testB=1;
  let testC=11111;
  let testD="AAA";
```
2. 상수 
```
  const TEST=111;
```    

## 엄격모드 적용 방법
```
  "use strict";
```

## 자료형
1. 문자형

   >큰따옴표: "Hello"  
   작은따옴표: 'Hello'  
   역 따옴표(백틱, backtick): `Hello`  
```
  let str = "Hello";
  let str2 = 'Single quotes are ok too';
  let phrase = `can embed another ${str}`;
```
2. NaN
```
  console.log("숫자가 아님" / 2 );. // 말이 되지 않는 수식 계산 시 NaN 자료형을 반환
```
3. Infinity 
```
  console.log(Infinity); // 무한데 자료형 어느 숫자든 0으로 나누면 무한대를 얻을 수 있습니다.
```
4. null,undefined
```
  let test;
  console.log(test); <= 아무 값도 없을 경우 null이 아닌 undefined 값이 표시된다.
  test=null;
  console.log(test); <= 변수에 null 값을 적용할 경우만 변수 값이 null이 된다.
```
5. typeof 연산자
```
  typeof undefined // "undefined"

  typeof 0 // "number"

  typeof 10n // "bigint"

  typeof true // "boolean"

  typeof "foo" // "string"

  typeof Symbol("id") // "symbol"

  typeof Math // "object"  (1)

  typeof null // "object"  (2)

  typeof alert // "function"  (3)
```
## 형변환
1.  문자 형변환
```
  let value=true;
  console.log(typeof value);
  value= String(value);
  console.log(typeof value);
```
2. 숫자 형변환 
```
  let value=true;
  console.log(typeof value);
  value= String(value);
  console.log(typeof value);
```

## 객체 생성방법
ㅇ


## 객체 생성방법
ㅇ


## 객체 생성방법
ㅇ


## 객체 생성방법
ㅇ
