# JavaScript-Basic → 배운 내용 기록
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
let a = 10
let b = '2'

console.log(a*b) // 20 >> 자동적으로 변환시켜 곱셈을 해줌

// 명시적 형변환 예시
let c = 10
let d = '2'

console.log(a+b); // 102
console.log(a+parseInt(b)); // 12 >> 'parseInt'로 string에서 Int로 바꿈
```

## 3. 연산자
✔ 1. 대입연산자 : 변수에 값을 넣는 행동
```javascript
let a = 1; // 1을 a 변수에 넣음! (아주 기본)
```

✔ 2. 산술연산자 : 사칙 연산이 가능<br>
+ '+' , '-' , '*' , '/'(몫) , '%'(나머지)
```javascript
let a = 2
let b = 3

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
let a = 1

a = a + 5 // a는 6이 됨
a += 5 // a는 6이 됨 a = a + 5 와 같은 식임
```

✔ 5. 증감연산자 : ++, --
+ '++' 은 1씩 증가<br>
+ '--' 는 1씩 감소
```javascript
let a = 10;
a++;

console.log(a) // 11
//이런 경우도 있다
let a = 10;

console.log(a++) // 그대로 10임 (a = 10 이 출력되고 ++ 되는거라 의미가 없다)
console.log(++a) // 이렇게 해주어야 11이 된다
```

✔ 6. 논리연산자 : 
```javascript

```

✔ 7. 비교연산자 : 
```javascript

```

✔ 8. 타입연산자 : 
```javascript

```

✔ 9. null 병합 연산자 : 
```javascript

```
