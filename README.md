# JavaScript Basic
### 😍배운 내용을 기록하는 repository 입니다.😍

## Contents
* [1. 변수와 상수](#1-변수와-상수)
* [2. 형변환](#2-형변환)
* [3. 연산자](#3-연산자)
* [4. 조건문과 반복문](#4-조건문과-반복문)
* [5. 화살표 함수](#5-화살표-함수)
* [6. 객체](#6-객체)
* [7. 배열](#7-배열)
* [8. 배열 내장 함수](#8-배열-내장-함수)
## 1. 변수와 상수
### ✔ let, const<br>
※ var 는 이제 쓰지 않아요 ^-^
```javascript
let a = 10; // 변할수 있는 값 (변수)
const b = 20; // 변할수 없는 값 (상수)
...
let a = 20; // a 에 새로운 20이 할당 됨
const b = 40; // error!
```

## 2. 형변환
### ✔ 묵시적 형변환, 명시적 형변환
```javascript
// 묵시적 형변환 예시
let a = 10;
let b = '2';

console.log(a * b); // 20 >> 자동적으로 변환시켜 곱셈을 해줌

// 명시적 형변환 예시
let c = 10;
let d = '2';

console.log(c + d); // 102
console.log(c + parseInt(d)); // 12 >> 'parseInt'로 string에서 Int로 바꿈
```

## 3. 연산자
### ✔ 1. 대입연산자 : 변수에 값을 넣는 행동
```javascript
let a = 1; // 1을 a 변수에 넣음! (아주 기본)
```

### ✔ 2. 산술연산자 : 사칙 연산이 가능<br>
+ '+' , '-' , '*' , '/'(몫) , '%'(나머지)
```javascript
let a = 2;
let b = 3;

console.log(a + b); // 5
console.log(b - a); // 1
console.log(a * b); // 6
console.log(a / b); // 0 (0.666666666~)
console.log(a % b); // 2
```

### ✔ 3. 연결연산자<br>
+ "문자열" + "문자열"

### ✔ 4. 복합연산자 : '+=', '-=' 등
```javascript
let a = 1;

a = a + 5; // a는 6이 됨
a += 5; // a는 6이 됨 a = a + 5 와 같은 식임
```

### ✔ 5. 증감연산자 : ++, --
+ '++' 은 1씩 증가<br>
+ '--' 는 1씩 감소
```javascript
let a = 10;
a++;

console.log(a); // 11
```
```javascript
let a = 10;

console.log(a++); // <후위연산> 그대로 10임 (a = 10 이 출력되고 ++ 되는거라 의미가 없다)
console.log(++a); // <전위연산> 이렇게 해주어야 11이 된다
```

### ✔ 6. 논리연산자 : boolean 자료형
```javascript
// 1. ! (not) : 반대로 바꿔버림
let a = !true;
console.log(a); // false

// 2. && (and) : 둘다 true 이여야만 true 로 나옴
let a = true;
let b = true;
let c = false;

console.log(a && b); // true and true => true
console.log(a && c); // true and false => false

// 3. || (or) : 둘중 하나만 true 여도 true 가 나옴
let a = true;
let b = false;

console.log(a || b); // true or false => true
```

### ✔ 7. 비교연산자 : 비교하는 수식들
+ '==' 는 값 자체만 비교
+ '===' 는 자료형까지 비교
```javascript
1 == "1" // true
1 === "1" // false

//++ 그외 비교연산자 활용
1 != "2" // true
1 !== "2"  // true
1 >= 2 // false
1 <= 2 // true
```

### ✔ 8. 타입연산자 : 어떤 타입인지 확인
+ typeof 변수
```javascript
let a = 10;
let b = "100";

console.log(typeof a); // number
console.log(typeof b); // string
```

### ✔ 9. null 병합 연산자 : null 이나 nudefined 를 찾아서 값을 대입
```javascript
let a = 0;
let b;

console.log(a ?? 10); // 0
console.log(b ?? 10); // 10
```
변수 `a`는 0으로 할당 되었기 때문에 Pass<br>
변수 `b`는 할당된 값이 없으므로 undefined로 10을 출력

## 4. 조건문과 반복문
### if, else, else if, switch, for

### ✔ 1. if 문
```javascript
let a = 5;

if(a > 3){
  console.log("a는 3보다 큽니다.");
  }else{
    console.log("a는 3보다 작습니다.");
    } // a는 3보다 큽니다.
```
`a`는 3보다 크기 때문에 첫번째 조건문에 적합하여 콘솔창에 "a는 3보다 큽니다." 출력
```javascript
let a = 5;

if(a > 10){
  console.log("a는 10보다 큽니다.");
  }else{
    console.log("a는 10보다 작습니다.");
    } // a는 10보다 작습니다.
```
`a`는 10보다 작기 때문에 첫번째 조건문을 지나가고 else문 으로 인해 콘솔창에 "a는 10보다 작습니다." 출력

### ✔ 2. for 문<br>
+ 예시
for(초기값, 조건문, 증감식){<br>
  // 실행할 명령 작성<br>
  }
```javascript
for(i = 0; i > 5; i ++){
  console.log(i);
  } // 0,1,2,3,4
```
i가 0부터 시작, 1씩 증가하여 5미만이 될때 까지 콘솔에 찍힘<br>
순서대로 0, 1, 2, 3, 4 까지 찍히게 됨

## 5. 화살표 함수
### ✔ 함수 선언식과 화살표 함수
```javascript
// 함수 선언식
function sum(){
  console.log("더하기 함수");
}
console.log(sum()); // "더하기 함수"

// 화살표 함수
let sum = () => {
  console.log("더하기 함수"); 
}
console.log(sum()); // "더하기 함수"
```
+ 화살표 함수는 function을 쓰지 않고 더욱 간단하게 함수 표현이 가능하다.
```javascript
// 간단하게 표현 가능
let sum = () => console.log("더하기!")
console.log(sum()); // "더하기!"

// 단순 값을 return 하는 것이라면 이렇게도 가능
let sum = () => "배고파!"
console.log(sum()); // "배고파!"
```

## 6. 객체
### ✔ 1. 객체 생성 방식
+ 여러가지 자료를 동시에 가질수 있는 비원시 데이터!
```javascript
// 객체 생성자 방식
let person = new Object();

// 객체 리터럴 방식
let person = {};

// 예시
let person = {
  name: "Croossh",
  age: 29,
  tall: 178
};
```
+ 프로퍼티라고 불리우며 문자/정수/boolean 등 어떤 자료형이 와도 상관 없다.
+ But, Key는 문자열로 작성하는 것이 일반적
### ✔ 2. 객체를 꺼내오는 방법
```javascript
let person = {
  name: "Croossh",
  age: 29,
  tall: 178
};

// 1)
console.log(person.name); // "Croossh"
// 2)
console.log(person["name"]); // "Croossh" => 함수 쓸때 유용하게 쓰임
// 예시
function getKey(key){
  return person[key];
}
console.log(getKey["name"]); // "Croossh"
```
### ✔ 3. 객체를 추가, 수정, 삭제하는 방법
#### 1) 추가
```javascript
let person = {
  name: "Croossh",
  age: 29,
  tall: 178
};

// 1.
person["location"] = "한국"
// 2.
person.location = "한국" // 점표기법으로 추가

console.log(person.location); // "한국"
```
#### 2) 수정
```javascript
let person = {
  name: "Croossh",
  age: 29,
  tall: 178
};

// 방법 1
person.name = "Croossh A"
// 방법 2
person["name"] = "Croossh A"

console.log(person.name); // "Croossh A"
```
#### 3) 삭제
```javascript
let person {
  name: "Croossh",
  age: 29,
  tall: 178
};

// 방법 1
delete person.age;
// 방법 2
delete person["age"]
```
+ But, delete로 삭제 시 실제로 메모리에서는 지워지지 않는다.<br>
+ 메모리를 계속 쓰고있기 때문에 직접 지워주거나 하단의 방법을 추천한다고 함
```javascript
person.age = null;
```
이렇게 해야 메모리에서도 지워버린다

#### 4) in
+ person 객체 안에 name 이라는 이름을 가진 프로퍼티가 있는가? (true/false)
```javascript
console.log(`name : ${"name"} in person}`); // true
```

## 7. 배열
#### 배열에는 어떤 자료형이 들어가도 상관 없다!
### ✔ 1. 배열 생성 방식
```javascript
// 배열 생성자 방식
let person = new Array();

// 배열 리터럴 방식
let person = [];

// 배열의 기본 상식
arr = [1, 2, 3, 4, 5];
// 배열의 index 순번은 0번부터 시작된다
// 즉 숫자 3은 2번 원소이다.
```
### ✔ 2. 배열 추가, 길이 확인 방법
#### 1) push : 배열의 마지막에 해당 원소를 추가함
```javascript
let arr = [1, 2, 3, 4];

arr.push(5); // 배열의 마지막에 추가!
console.log(arr); // [1, 2, 3, 4, 5]
```
#### 2) length : 총 갯수를 확인
```javascript
let arr = [1, 2, 3, 4, 5];

console.log(arr.length); // 5 
// ※주의: 원소의 마지막 번호는 0부터 시작하여 4로 끝나기에 총 갯수는 5개 이다!
```

## 8. 배열 내장 함수
#### 먼저 forEach 문을 알아보자
+ forEach()는 주어진 함수를 배열 요소 각각에 대해 실행하는 메서드이다.
```javascript
const arr = [1, 2, 3, 4];

arr.forEach(function(elm){
  console.log(elm);
}); // 1, 2, 3, 4 각각 출력

//위의 식은 아래와 같이 간략하게 표기할수 있다.
arr.forEach((elm) => {
  console.log(elm);
});
// 또는
arr.forEach((elm) => console.log(elm));
```
### ✔ 1. 새로운 값을 배열에 넣기
#### 1) push
```javascript
const arr = [1, 2, 3];
const newArr = [];

arr.forEach((elm) => {
  newArr.push(elm * 2); // 위에서 선언한 비어있는 배열에 차곡차곡 넣는다
});

console.log(newArr); // [2, 4, 6, 8]
```
#### 2) map
```javascript
const arr = [1, 2, 3, 4]

const newArr = arr.map((elm) => {  
  return elm*2; // 새로운 배열을 선언 함과 동시에 map 으로 값을 넣는다
});

console.log(newArr); // [2, 4, 6, 8]
```

### ✔ 2. 배열에 값이 있는지 확인하는 방법
#### 1) if문을 활용한 기본적인 방법
```javascript
const arr = [1, 2, 3, 4];

let number = 3;

arr.forEach((elm) => {
  if(elm === number){
    console.log(true);
  }
}); // true
```
#### 2) includes
```javascript
const arr = [1, 2, 3, 4];

let number = 3;

console.log(arr.includes(number)); // true
```
+ 이 방법은 값 뿐만 아니라 자료형까지 맞는지 확인 해준다.

### ✔ 3. 배열의 값을 찾는 방법
#### 1) indexOf
```javascript
const arr = [1, 2, 3, 4];

let number = 3;

console.log(arr.indexOf(number)); // 2
```
+ 배열안에 몇번째에 있는지 알려주는 메서드
+ 만약 찾는 값이 없다면 콘솔창에는 `-1` 이 뜨게 된다.

#### 2) findIndex
```javascript
const arr = [
  { color : "red" },
  { color : "black" },
  { color : "blue" },
  { color : "green" }
];

console.log(arr.findIndex((elm) => elm.color === "green")); // 3

// 즉,
console.log(arr.findIndex(function(elm){
  return elm.color === "green"; 
  });
); // 3
```
+ 배열안의 객체의 값을 찾아주는 메서드
+ findIndex의 파라미터로는 콜백함수를 해줘야 한다.

#### 3) find
```javascript
const arr = [
  { color : "red" },
  { color : "black" },
  { color : "blue" },
  { color : "green" }
];

const element = arr.find((elm) => {
  return elm.color === "blue";
});

console.log(element); // {color : 'blue'}
```
+ 배열안의 객채의 프로퍼티를 비교해 값을 찾아준다.

#### 4) filter
```javascript
const arr = [
  { color : "red" },
  { color : "black" },
  { color : "blue" },
  { color : "green" }
];

console.log(arr.filter((elm) => elm.color === "blue")); // {color: "blue"}
```

### ✔ 4. 배열을 자르는 방법
#### 1) slice
```javascript
const arr = [
  { color : "red" },
  { color : "black" },
  { color : "blue" },
  { color : "green" }
];

console.log(arr.slice(0, 2)); // { color : "red" }, { color : "black" }
```
+ slice의 첫번째 파라미터로는 시작지점
+ slice의 두번째 파라미터로는 끝지점
+ 0 이상 ~ 2 미만 구간을 잘라내어 새로운 배열로 리턴한다.

### ✔ 5. 배열을 연결 방법
#### 1) concat
```javascript
let arr1 = [
  { firstColor : "red" },
  { secondColor : "black" },
  { thirdColor : "blue" }
];

let arr2 = [
  { fourthColor : "green" },
  { fifthColor : "blue" }
];

console.log(arr1.concat(arr2)) // {firstColor : 'red'} 부터 {fifthColor: 'blue'}
```
※ 참고: 리엑트에서는 스프레드 연산자(...변수)를 사용하는 것이 더욱 효과적이라고 한다. 
+ 스프레드 연산자 활용 방법
```javascript
let arr1 = [
  { firstColor : "red" },
  { secondColor : "black" }
];

let arr2 = [
  { fourthColor : "green" },
  { fifthColor : "blue" }
];

const newColor = [...arr1, 'baseColor: pink', ...arr2]
console.log(newColor); // arr1 배열과 arr2 배열 사이에 baseColor : pink 가 삽입되어 출력됨
```

### ✔ 6. 배열 정렬 방법
#### 1) sort
+ 배열안의 각각 객체들을 내림차순으로 정렬시킨다
```javascript
let chars = ["나", "다", "가"];

chars.sort();
console.log(chars); // 가, 나, 다
```
+ 원본 배열의 순서를 사전순으로 정렬시켜 새로운 배열로 만든다.
+ But! 숫자의 경우는 다르다
```javascript
let num = [0, 1, 2, 10, 30, 3, 20];

num.sort();
console.log(num) // 0, 1, 10, 2, 20 , 3, 30 이 출력된다

// 숫자 정렬같은 경우에는 간단한 비교함수와 함께 사용된다
const compare = (a, b) => {
  if(a > b){
    // 크다
    return 1; // a 랑 b 랑 비교했을때 a 가 크면 a 를 뒤로 보냄
  }

  if(a < b){
    // 작다
    return -1; // a 랑 b 랑 비교했을때 a 가 작으면 a 를 앞으로 보냄
  }

   //같다
   return 0; // ㅇㅋ 다음~
};
num.sort(compare); // compare 를 sort의 매개변수로 넣어버림
console.log(num); // 0, 1, 2, 3, 10, 20, 30 으로 정상적으로 출력된다
```

### ✔ 7. 문자열 합치기
#### 1) join
```javascript
const arr = ["안녕하세요?", "화장실은", "오른쪽입니다."]

console.log(arr[0], arr[1], arr[2]) // 안녕하세요? 화장실은 오른쪽입니다.
//배열안에 객체들을 하나하나 꺼내서 나열하기는 힘들다

console.log(arr.join()); // 안녕하세요?, 화장실은, 오른쪽입니다.
console.log(arr.join(" ")); // 안녕하세요? 화장실은 오른쪽입니다.
// 이렇게 공백으로 구분자를 정해주면 자연스럽게 나열된다.
```

[🔼최상단으로 가기🔼](#javascript-basic)
