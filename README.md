# JavaScript-Basic
### 😍배운 내용을 기록하는 repository 입니다.😍

## 1. 변수와 상수
✔ let, const<br>
※ var 는 이제 쓰지 않아요 ^-^
```javascript
let a = 10; // 변할수 있는 값 (변수)
const b = 20; // 변할수 없는 값 (상수)
...
let a = 20; // a 에 새로운 20이 할당 됨
const b = 40; // error!
```

## 2. 형변환
✔ 묵시적 형변환, 명시적 형변환
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
✔ 1. 대입연산자 : 변수에 값을 넣는 행동
```javascript
let a = 1; // 1을 a 변수에 넣음! (아주 기본)
```

✔ 2. 산술연산자 : 사칙 연산이 가능<br>
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

✔ 3. 연결연산자<br>
+ "문자열" + "문자열"

✔ 4. 복합연산자 : '+=', '-=' 등
```javascript
let a = 1;

a = a + 5; // a는 6이 됨
a += 5; // a는 6이 됨 a = a + 5 와 같은 식임
```

✔ 5. 증감연산자 : ++, --
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

✔ 6. 논리연산자 : boolean 자료형
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

✔ 7. 비교연산자 : 비교하는 수식들
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

✔ 8. 타입연산자 : 어떤 타입인지 확인
+ typeof 변수
```javascript
let a = 10;
let b = "100";

console.log(typeof a); // number
console.log(typeof b); // string
```

✔ 9. null 병합 연산자 : null 이나 nudefined 를 찾아서 값을 대입
```javascript
let a = 0;
let b;

console.log(a ?? 10); // 0
console.log(b ?? 10); // 10
```
변수 `a`는 0으로 할당 되었기 때문에 Pass<br>
변수 `b`는 할당된 값이 없으므로 undefined로 10을 출력

## 4. 조건문
### if, else, else if, switch, for

✔ 1. if 문
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

✔ 2. for 문<br>
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

## 5. 함수 표현식, 화살표 함수



