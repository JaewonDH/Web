## JavaScript 정리 (출처 :https://ko.javascript.info/)
#### 1.[자바스크립트 기본](./documnet/javascript_basic.md) 
#### 2.[자바스크립트 객체](./documnet/javascript_object.md) 


## 참조 사이트
#### 1.[온라인 코드 수행 https://replit.com/](https://replit.com/) 


## 형변환 확인 사항 
1.undefined 숫자로 형변환 시 Nan 됨  
2.null 숫자로 형변환 시 0 이됨.

## 기본 연산자
1. let value=2**5;  //2를 5번 곱함. 거듭 제곱 연산자  
2. let value=+"12"; // +를 변수에 붙이면 value는 숫자 12로 전환되어 대입됨
3. +는 문자열이 있으면 문자열로 변경 됨 ex) '1'+2="12" 
4. -는 문자열이 있으면 숫자형으로 변경하여 계산됨. ex) 6-'2' =4   '2'-6=-4
5. value++  ++가뒤에 있는 상태에서는 값을 반환 후 ++로 증가 한다 
   let a=value++; value가 1이면 value에 먼저 a값을 넣고 ++ value 값을 증가 시킨다.
