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
6. ("" || "1" || "s" )  
   => 처음 부터 오른쪽으로 이동하면서 true 인값을 찾아 true이면 해당 값을 반환  
   ("" && "1" && "s" )  
   => 처음 부터 오른쪽으로 이동하면서 false를 만나면 해당 값을 반환 하고 false가 없으면 마지막의 변수 값을 반환      
7. (a ?? 1)    
   => ??는 앞에 변수 a에 null이나 undefined 확인하여 아니면 a 값을 반환 그렇지 않음면 1을 반환  
   => a ?? 1 =====> (!a==null && !a==undefined) ? a : 1  
## loop
1. 레이블을 사용하여 loop 밖으로 빠져 나올 수 있음  
아래 for문에서 break , contiune에 레이블을 넣어면 outer 선언 후 첫번 째 outer로 넘어가서 continue하거나 break 한다. 
```
outer:for(let i=0; i<10; i++){  
    for(let j=0; j<10; j++){                 
        if(i==5){  
            break outer;  
        }  
        if(j==0 || i==0){  
            continue;  
        }  
        console.log(`${i}*${j}=${i*j}`);          
    }    
}
```
## function
1. 디폴트 파라미터에 값이나 함수를 호출하여 설정 가능  
```
   function aa(name,print,age=getAge(),temp=22){

    }
```
2. 파라미터에 함수를 넣어 함수 내부에서 함수 호출 가능 
```  
   function print(data){
        console.log(data);
    }
   function showMesage(message, print){
        print(message);
    }
    showmesage("ddd",print);
```
3. 함수 표현식 가능 
```
   let print=function(message){
        console.log(message);
   }
```   
4. 화살표 함수 
아래와 같이 함수를 줄여서 표현 할 수 있다.
```
   let minus = (a,b)=> a+b;
   let printA2 = ()=> console.log();
   let printMessagea = message => console.log(message);
```   

## Object(객체) 정리
```
   const car={
       color:'',
       cost: 0,    
   }
   
```
1. 대괄호 표기법 사용 가능 
```
   car["name"]="k7";
   
```
2. delete로 객체의 property 삭제 
```
   delete car.color;
   delete car[coast];
   
```
3. in 으로 객체에 property 존재 확인.    
```
('color' in car) //존재하면 true 리턴 됨

```
4. for(item in car) 으로 item 전체 순회 가능 
```
   for(key in car){
      console.log(key); // car object의 property key 값을 반환
   }
```
5. object 객체 복사 
참조에 의한 복사 
```
  const car= {};
  const tempCar=car;  // 참조에 의한 복사 
  
```  
Object.assign() 깊은 복사  
객체 안의 객체는 복사가 안되며 for문으로 직접 복사해야 함.
자바스크립트 라이브러리 lodash의 메서드인 _.cloneDeep(obj)을 사용하면 가능
```
    const car= {
        name:"k7"
    };

    let tempCar={
        color:'red'
    };

    Object.assign(tempCar,car);
```

6. 가비지 컬렉터 사용하지 않는 object에 null 을 넣거나 참도되는 object에 null 넣어 메모리 관리를 해야 한다. 

7. Object에 함수 정의 가능 함수는 아래 처럼 3가지 타입으로 정의 가능 
```
    let people={
        name:'jaewon',
        age : 333,
        address:'',

        getName: function(){
            return this.name; // this는 object를 가리킴  user
        },

        getAge(){
            return this.age;
        },

        getAddress:()=>{
            return this.address;
        }
    }
```    
8. this 
함수에 안에서 사용 가능하며 함수에서 사용 시 객체에 포함되지 않은   
상태에서는 undefined 되며 포함될 때 this는 포함된 object가 된다.  
```
let calculator = {
    inputA:0,
    inputB:0,
    read(){
        this.inputA=+prompt("계 산할 첫번 째 입력 값",'');
        this.inputB=+prompt("계산 할 두번 째 입력 값",'');
    },
    sum(){
        return this.inputA + this.inputB;
    },
    mul(){
        return this.inputA * this.inputB;
    }
}

```
9. new 연산자와 생성자 함수
객체의 틀을 만들고 재 사용하기 사용함.  
```
function Accumulator(value){
    this.value=value;

    this.read=(value)=>{
        this.value+=value;
    }
}

let accumulator = new Accumulator(2);

accumulator.read(2);
accumulator.read(10);

console.log(accumulator.value);


// 재사용할 필요가 없는 객체를 아래와 같이 만들어 캡슐화 한다.
let userB= new function(){

}

```
10. 옵셔널 체이닝 공부해야함 ? 최근 문법 
11. Symbol  
11. 체를 원시형으로 변환하기 ?  
