## 변수 생성방법

1. 기본변수 
``` javascript
  var testA="AAA";
  var testB=1;
  let testC=11111;
  let testD="AAA";
```
2. 상수 
``` javascript
  const TEST=111;
```    

## 엄격모드 적용 방법
``` javascript
  "use strict";
```

## 자료형
1. 문자형

   >큰따옴표: "Hello"  
   작은따옴표: 'Hello'  
   역 따옴표(백틱, backtick): `Hello`  
``` javascript
  let str = "Hello";
  let str2 = 'Single quotes are ok too';
  let phrase = `can embed another ${str}`;
```
2. 숫자형
``` javascript
  let value = 1;
  let value_point = 1.222;
  
```

3. BigInt 
   >아주 끈 숫자를 사용할 때만 사용하는 자료형 
   끝에 'n'이 붙으면 BigInt형 자료입니다.  
   BigInt를 지원하는 않는 브라우저가 있으며 지원하는 브라우저는 다음과 같음 (Firefox, Chrome, Edge)
    
``` javascript 
  let value = 123455555n;    
```
4. NaN
``` javascript
  console.log("숫자가 아님" / 2 );. // 말이 되지 않는 수식 계산 시 NaN 자료형을 반환
```
5. Infinity 
``` javascript
  console.log(Infinity); // 무한데 자료형 어느 숫자든 0으로 나누면 무한대를 얻을 수 있습니다.
```
6. null,undefined
``` javascript
  let test;
  console.log(test); <= 아무 값도 없을 경우 null이 아닌 undefined 값이 표시된다.
  test=null;
  console.log(test); <= 변수에 null 값을 적용할 경우만 변수 값이 null이 된다.
```
7. typeof 연산자
``` javascript
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
``` javascript
  let value=true;
  console.log(typeof value);
  value= String(value);
  console.log(typeof value); // value 는 "true"
```
2. 숫자 형변환 
``` javascript
  let value="7"/"2";
  console.log(value); // 숫자 자료형으로 변환 됨 3
  console.log(typeof value); // number

  value="123 "; 
  value=Number(value); // 문자열에 숫자만있으면 수자형으로 변환 가능 공백도 제거 됨.
  console.log(value); // 숫자 자료형으로 변환 됨 123
  console.log(typeof value); // number
```

## 객체 생성방법
ㅇ


## 객체 생성방법
ㅇ


## 객체 생성방법
ㅇ


## 객체 생성방법
ㅇ

