# JavaScript Basic
### π λ°°μ΄ λ΄μ©μ κΈ°λ‘νλ repository μλλ€. π

## πββοΈContents
* [1. λ³μμ μμ](#1-λ³μμ-μμ)
* [2. νλ³ν](#2-νλ³ν)
* [3. μ°μ°μ](#3-μ°μ°μ)
* [4. μ‘°κ±΄λ¬Έκ³Ό λ°λ³΅λ¬Έ](#4-μ‘°κ±΄λ¬Έκ³Ό-λ°λ³΅λ¬Έ)
* [5. νμ΄ν ν¨μ](#5-νμ΄ν-ν¨μ)
* [6. κ°μ²΄](#6-κ°μ²΄)
* [7. λ°°μ΄](#7-λ°°μ΄)
* [8. λ°°μ΄ λ΄μ₯ ν¨μ](#8-λ°°μ΄-λ΄μ₯-ν¨μ)
## 1. λ³μμ μμ
### β let, const
β» var λ μ΄μ  μ°μ§ μμμ ^-^
```javascript
let a = 10; // λ³ν μ μλ κ° (λ³μ)
const b = 20; // λ³ν μ μλ κ° (μμ)
...
let a = 20; // a μ μλ‘μ΄ 20μ΄ ν λΉ λ¨
const b = 40; // error!
```

## 2. νλ³ν
### β λ¬΅μμ  νλ³ν, λͺμμ  νλ³ν
```javascript
// λ¬΅μμ  νλ³ν μμ
let a = 10;
let b = '2';

console.log(a * b); // 20 >> μλμ μΌλ‘ λ³νμμΌ κ³±μμ ν΄μ€

// λͺμμ  νλ³ν μμ
let c = 10;
let d = '2';

console.log(c + d); // 102
console.log(c + parseInt(d)); // 12 >> 'parseInt'λ‘ stringμμ Intλ‘ λ°κΏ
```

## 3. μ°μ°μ
### β 1. λμμ°μ°μ : λ³μμ κ°μ λ£λ νλ
```javascript
let a = 1; // 1μ a λ³μμ λ£μ! (μμ£Ό κΈ°λ³Έ)
```

### β 2. μ°μ μ°μ°μ : μ¬μΉ μ°μ°μ΄ κ°λ₯<br>
+ '+' , '-' , '*' , '/'(λͺ«) , '%'(λλ¨Έμ§)
```javascript
let a = 2;
let b = 3;

console.log(a + b); // 5
console.log(b - a); // 1
console.log(a * b); // 6
console.log(a / b); // 0 (0.666666666~)
console.log(a % b); // 2
```

### β 3. μ°κ²°μ°μ°μ<br>
+ "λ¬Έμμ΄" + "λ¬Έμμ΄"

### β 4. λ³΅ν©μ°μ°μ : '+=', '-=' λ±
```javascript
let a = 1;

a = a + 5; // aλ 6μ΄ λ¨
a += 5; // aλ 6μ΄ λ¨ a = a + 5 μ κ°μ μμ
```

### β 5. μ¦κ°μ°μ°μ : ++, --
+ '++' μ 1μ© μ¦κ°<br>
+ '--' λ 1μ© κ°μ
```javascript
let a = 10;
a++;

console.log(a); // 11
```
```javascript
let a = 10;

console.log(a++); // <νμμ°μ°> κ·Έλλ‘ 10μ (a = 10 μ΄ μΆλ ₯λκ³  ++ λλκ±°λΌ μλ―Έκ° μλ€)
console.log(++a); // <μ μμ°μ°> μ΄λ κ² ν΄μ£Όμ΄μΌ 11μ΄ λλ€
```

### β 6. λΌλ¦¬μ°μ°μ : boolean μλ£ν
```javascript
// 1. ! (not) : λ°λλ‘ λ°κΏλ²λ¦Ό
let a = !true;
console.log(a); // false

// 2. && (and) : λλ€ true μ΄μ¬μΌλ§ true λ‘ λμ΄
let a = true;
let b = true;
let c = false;

console.log(a && b); // true and true => true
console.log(a && c); // true and false => false

// 3. || (or) : λμ€ νλλ§ true μ¬λ true κ° λμ΄
let a = true;
let b = false;

console.log(a || b); // true or false => true
```

### β 7. λΉκ΅μ°μ°μ : λΉκ΅νλ μμλ€
+ '==' λ κ° μμ²΄λ§ λΉκ΅
+ '===' λ μλ£νκΉμ§ λΉκ΅
```javascript
1 == "1" // true
1 === "1" // false

//++ κ·ΈμΈ λΉκ΅μ°μ°μ νμ©
1 != "2" // true
1 !== "2"  // true
1 >= 2 // false
1 <= 2 // true
```

### β 8. νμμ°μ°μ : μ΄λ€ νμμΈμ§ νμΈ
+ typeof λ³μ
```javascript
let a = 10;
let b = "100";

console.log(typeof a); // number
console.log(typeof b); // string
```

### β 9. null λ³ν© μ°μ°μ : null μ΄λ nudefined λ₯Ό μ°Ύμμ κ°μ λμ
```javascript
let a = 0;
let b;

console.log(a ?? 10); // 0
console.log(b ?? 10); // 10
```
λ³μ `a`λ 0μΌλ‘ ν λΉ λμκΈ° λλ¬Έμ Pass<br>
λ³μ `b`λ ν λΉλ κ°μ΄ μμΌλ―λ‘ undefinedλ‘ 10μ μΆλ ₯

## 4. μ‘°κ±΄λ¬Έκ³Ό λ°λ³΅λ¬Έ
### if, else, else if, switch, for

### β 1. if λ¬Έ
```javascript
let a = 5;

if(a > 3){
  console.log("aλ 3λ³΄λ€ ν½λλ€.");
  }else{
    console.log("aλ 3λ³΄λ€ μμ΅λλ€.");
    } // aλ 3λ³΄λ€ ν½λλ€.
```
`a`λ 3λ³΄λ€ ν¬κΈ° λλ¬Έμ μ²«λ²μ§Έ μ‘°κ±΄λ¬Έμ μ ν©νμ¬ μ½μμ°½μ "aλ 3λ³΄λ€ ν½λλ€." μΆλ ₯
```javascript
let a = 5;

if(a > 10){
  console.log("aλ 10λ³΄λ€ ν½λλ€.");
  }else{
    console.log("aλ 10λ³΄λ€ μμ΅λλ€.");
    } // aλ 10λ³΄λ€ μμ΅λλ€.
```
`a`λ 10λ³΄λ€ μκΈ° λλ¬Έμ μ²«λ²μ§Έ μ‘°κ±΄λ¬Έμ μ§λκ°κ³  elseλ¬Έ μΌλ‘ μΈν΄ μ½μμ°½μ "aλ 10λ³΄λ€ μμ΅λλ€." μΆλ ₯

### β 2. for λ¬Έ
+ μμ
for(μ΄κΈ°κ°, μ‘°κ±΄λ¬Έ, μ¦κ°μ){<br>
  // μ€νν  λͺλ Ή μμ±<br>
  }
```javascript
for(i = 0; i > 5; i ++){
  console.log(i);
  } // 0,1,2,3,4
```
iκ° 0λΆν° μμ, 1μ© μ¦κ°νμ¬ 5λ―Έλ§μ΄ λ λ κΉμ§ μ½μμ μ°ν<br>
μμλλ‘ 0, 1, 2, 3, 4 κΉμ§ μ°νκ² λ¨

### β 3. switch λ¬Έ
+ case μμμ λ§λ μ‘°κ±΄μ μ°Ύμμ μ€νν΄μ€λ€!
```javascript
const day = 3;
  swtich (day) = {

    case 1:
      console.log("Monday");
      break; // νμμ΄λ€ κ·Έλ μ§μμΌλ©΄ λ°μΌλ‘ μ­ μ€ννλ€

    case 2:
      console.log("Tuesday");
      break;

    case 3:
      console.log("Wednesday");
      break;

    case 4:
      console.log("Thursday");
      break;

    case 5:
      console.log("Friday");
      break;

    case 6:
    case 7:
      console.log("Weekend!")
      break;

    defaulf: // μΌμΉνλκ² μμλ μΆλ ₯νλ λΆλΆ!
        console.log("I don't know what are you saying")

// μμ λ³μ day λ 3μ΄λ―λ‘ Wednesdayκ° μΆλ ₯λλ€!
```

## 5. νμ΄ν ν¨μ
### β ν¨μ μ μΈμκ³Ό νμ΄ν ν¨μ
```javascript
// ν¨μ μ μΈμ
function sum(){
  console.log("λνκΈ° ν¨μ");
}
console.log(sum()); // "λνκΈ° ν¨μ"

// νμ΄ν ν¨μ
let sum = () => {
  console.log("λνκΈ° ν¨μ"); 
}
console.log(sum()); // "λνκΈ° ν¨μ"
```
+ νμ΄ν ν¨μλ functionμ μ°μ§ μκ³  λμ± κ°λ¨νκ² ν¨μ ννμ΄ κ°λ₯νλ€.
```javascript
// κ°λ¨νκ² νν κ°λ₯
let sum = () => console.log("λνκΈ°!")
console.log(sum()); // "λνκΈ°!"

// λ¨μ κ°μ return νλ κ²μ΄λΌλ©΄ μ΄λ κ²λ κ°λ₯
let sum = () => "λ°°κ³ ν!"
console.log(sum()); // "λ°°κ³ ν!"
```

## 6. κ°μ²΄
### β 1. κ°μ²΄ μμ± λ°©μ
+ μ¬λ¬κ°μ§ μλ£λ₯Ό λμμ κ°μ§μ μλ λΉμμ λ°μ΄ν°!
```javascript
// κ°μ²΄ μμ±μ λ°©μ
let person = new Object();

// κ°μ²΄ λ¦¬ν°λ΄ λ°©μ
let person = {};

// μμ
let person = {
  name: "Croossh",
  age: 29,
  tall: 178
};
```
+ νλ‘νΌν°λΌκ³  λΆλ¦¬μ°λ©° λ¬Έμ/μ μ/boolean λ± μ΄λ€ μλ£νμ΄ μλ μκ΄ μλ€.
+ But, Keyλ λ¬Έμμ΄λ‘ μμ±νλ κ²μ΄ μΌλ°μ 
### β 2. κ°μ²΄λ₯Ό κΊΌλ΄μ€λ λ°©λ²
```javascript
let person = {
  name: "Croossh",
  age: 29,
  tall: 178
};

// 1)
console.log(person.name); // "Croossh"
// 2)
console.log(person["name"]); // "Croossh" => ν¨μ μΈλ μ μ©νκ² μ°μ
// μμ
function getKey(key){
  return person[key];
}
console.log(getKey["name"]); // "Croossh"
```
### β 3. κ°μ²΄λ₯Ό μΆκ°, μμ , μ­μ νλ λ°©λ²
#### 1) μΆκ°
```javascript
let person = {
  name: "Croossh",
  age: 29,
  tall: 178
};

// 1.
person["location"] = "νκ΅­"
// 2.
person.location = "νκ΅­" // μ νκΈ°λ²μΌλ‘ μΆκ°

console.log(person.location); // "νκ΅­"
```
#### 2) μμ 
```javascript
let person = {
  name: "Croossh",
  age: 29,
  tall: 178
};

// λ°©λ² 1
person.name = "Croossh A"
// λ°©λ² 2
person["name"] = "Croossh A"

console.log(person.name); // "Croossh A"
```
#### 3) μ­μ 
```javascript
let person {
  name: "Croossh",
  age: 29,
  tall: 178
};

// λ°©λ² 1
delete person.age;
// λ°©λ² 2
delete person["age"]
```
+ But, deleteλ‘ μ­μ  μ μ€μ λ‘ λ©λͺ¨λ¦¬μμλ μ§μμ§μ§ μλλ€.<br>
+ λ©λͺ¨λ¦¬λ₯Ό κ³μ μ°κ³ μκΈ° λλ¬Έμ μ§μ  μ§μμ£Όκ±°λ νλ¨μ λ°©λ²μ μΆμ²νλ€κ³  ν¨
```javascript
person.age = null;
```
μ΄λ κ² ν΄μΌ λ©λͺ¨λ¦¬μμλ μ§μλ²λ¦°λ€

#### 4) in
+ person κ°μ²΄ μμ name μ΄λΌλ μ΄λ¦μ κ°μ§ νλ‘νΌν°κ° μλκ°? (true/false)
```javascript
console.log(`name : ${"name"} in person}`); // true
```

## 7. λ°°μ΄
#### λ°°μ΄μλ μ΄λ€ μλ£νμ΄ λ€μ΄κ°λ μκ΄ μλ€!
### β 1. λ°°μ΄ μμ± λ°©μ
```javascript
// λ°°μ΄ μμ±μ λ°©μ
let person = new Array();

// λ°°μ΄ λ¦¬ν°λ΄ λ°©μ
let person = [];

// λ°°μ΄μ κΈ°λ³Έ μμ
arr = [1, 2, 3, 4, 5];
// λ°°μ΄μ index μλ²μ 0λ²λΆν° μμλλ€
// μ¦ μ«μ 3μ 2λ² μμμ΄λ€.
```
+ μΆκ°λ‘, λ°°μ΄μ constλ‘ μ μΈνμ¬λ λ°°μ΄μμ μμλ€μ μμ ν  μ μλ€! (λΉμμνμμ΄λΌ κ°λ₯νλ€)
### β 2. λ°°μ΄ μΆκ°, μ­μ , κΈΈμ΄ νμΈ λ°©λ²
#### 1) push : λ°°μ΄μ λ§μ§λ§μ ν΄λΉ μμλ₯Ό μΆκ°ν¨
```javascript
let arr = [1, 2, 3, 4];

arr.push(5); // λ°°μ΄μ λ§μ§λ§μ μΆκ°!
console.log(arr); // [1, 2, 3, 4, 5]
```

#### 2) pop : λ°°μ΄μ λ§μ§λ§μ ν΄λΉ μμλ₯Ό μ­μ ν¨
```javascript
let arr = [1, 2, 3, 4];

arr.pop(); // λ°°μ΄μ λ§μ§λ§ μμ μ­μ !
console.log(arr); // [1, 2, 3]
```

#### 3) shift/unshift : λ°°μ΄μ μμ μμλ₯Ό μ­μ /μΆκ°ν¨
```javascript
let arr = [1, 2, 3, 4];

arr.shtif(); // λ°°μ΄μ μ²«λ²μ§Έ μμ μ­μ !
console.log(arr); // [2, 3, 4]

arr.unshift(0); // λ°°μ΄μ μ²«λ²μ§Έμ ν΄λΉ μμ μΆκ°
console.log(arr); // [0, 2, 3, 4]

```

#### 4) length : μ΄ κ°―μλ₯Ό νμΈ
```javascript
let arr = [1, 2, 3, 4, 5];

console.log(arr.length); // 5 
// β»μ£Όμ: μμμ λ§μ§λ§ λ²νΈλ 0λΆν° μμνμ¬ 4λ‘ λλκΈ°μ μ΄ κ°―μλ 5κ° μ΄λ€!
```

## 8. λ°°μ΄ λ΄μ₯ ν¨μ
#### λ¨Όμ  forEach λ¬Έμ μμλ³΄μ
+ forEach()λ μ£Όμ΄μ§ ν¨μλ₯Ό λ°°μ΄ μμ κ°κ°μ λν΄ μ€ννλ λ©μλμ΄λ€.
```javascript
const arr = [1, 2, 3, 4];

arr.forEach(function(elm){
  console.log(elm);
}); // 1, 2, 3, 4 κ°κ° μΆλ ₯

//μμ μμ μλμ κ°μ΄ κ°λ΅νκ² νκΈ°ν μ μλ€.
arr.forEach((elm) => {
  console.log(elm);
});
// λλ
arr.forEach((elm) => console.log(elm));
```
### β 1. μλ‘μ΄ κ°μ λ°°μ΄μ λ£κΈ°
#### 1) push μμ©
```javascript
const arr = [1, 2, 3];
const newArr = [];

arr.forEach((elm) => {
  newArr.push(elm * 2); // μμμ μ μΈν λΉμ΄μλ λ°°μ΄μ μ°¨κ³‘μ°¨κ³‘ λ£λλ€
});

console.log(newArr); // [2, 4, 6, 8]
```
#### 2) map
```javascript
const arr = [1, 2, 3, 4]

const newArr = arr.map((elm) => {  
  return elm*2; // μλ‘μ΄ λ°°μ΄μ μ μΈ ν¨κ³Ό λμμ map μΌλ‘ κ°μ λ£λλ€
});

console.log(newArr); // [2, 4, 6, 8]
```

### β 2. λ°°μ΄μ κ°μ΄ μλμ§ νμΈνλ λ°©λ²
#### 1) ifλ¬Έμ νμ©ν κΈ°λ³Έμ μΈ λ°©λ²
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
+ μ΄ λ°©λ²μ κ° λΏλ§ μλλΌ μλ£νκΉμ§ λ§λμ§ νμΈ ν΄μ€λ€.

### β 3. λ°°μ΄μ κ°μ μ°Ύλ λ°©λ²
#### 1) indexOf
```javascript
const arr = [1, 2, 3, 4];

let number = 3;

console.log(arr.indexOf(number)); // 2
```
+ λ°°μ΄μμ λͺλ²μ§Έμ μλμ§ μλ €μ£Όλ λ©μλ
+ λ§μ½ μ°Ύλ κ°μ΄ μλ€λ©΄ μ½μμ°½μλ `-1` μ΄ λ¨κ² λλ€.

#### 2) findIndex
```javascript
const arr = [
  { color : "red" },
  { color : "black" },
  { color : "blue" },
  { color : "green" }
];

console.log(arr.findIndex((elm) => elm.color === "green")); // 3

// μ¦,
console.log(arr.findIndex(function(elm){
  return elm.color === "green"; 
  });
); // 3
```
+ λ°°μ΄μμ κ°μ²΄μ κ°μ μ°Ύμμ£Όλ λ©μλ
+ findIndexμ νλΌλ―Έν°λ‘λ μ½λ°±ν¨μλ₯Ό ν΄μ€μΌ νλ€.

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
+ λ°°μ΄μμ κ°μ±μ νλ‘νΌν°λ₯Ό λΉκ΅ν΄ κ°μ μ°Ύμμ€λ€.

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

### β 4. λ°°μ΄μ μλ₯΄λ λ°©λ²
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
+ sliceμ μ²«λ²μ§Έ νλΌλ―Έν°λ‘λ μμμ§μ 
+ sliceμ λλ²μ§Έ νλΌλ―Έν°λ‘λ λμ§μ 
+ 0 μ΄μ ~ 2 λ―Έλ§ κ΅¬κ°μ μλΌλ΄μ΄ μλ‘μ΄ λ°°μ΄λ‘ λ¦¬ν΄νλ€.

#### 2) splice
```javascript
let colors = [ "red", "blue", "green", "yellow", "black", "white" ]

colors.splice(2) // [ "green", "yellow", "black", "white" ] 2λ²λΆν° λκΉμ§ νμ(sliceμ λμΌ)
colors.slice(1,3) // [ "blue", "green", "yellow" ] 1λ²λΆν° 3κ°κΉμ§ νμ
```
+ sliceμ λ§μ΄ λΉμ·νλ μ½κ°μ μ°¨μ΄κ° μλ€! μ‘°μ¬!

### β 5. λ°°μ΄μ μ°κ²° λ°©λ²
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

console.log(arr1.concat(arr2)) // {firstColor : 'red'} λΆν° {fifthColor: 'blue'}
```
β» μ°Έκ³ : λ¦¬μνΈμμλ μ€νλ λ μ°μ°μ(...λ³μ)λ₯Ό μ¬μ©νλ κ²μ΄ λμ± ν¨κ³Όμ μ΄λΌκ³  νλ€. 
+ μ€νλ λ μ°μ°μ νμ© λ°©λ²
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
console.log(newColor); // arr1 λ°°μ΄κ³Ό arr2 λ°°μ΄ μ¬μ΄μ baseColor : pink κ° μ½μλμ΄ μΆλ ₯λ¨
```

### β 6. λ°°μ΄ μ λ ¬ λ°©λ²
#### 1) sort
+ λ°°μ΄μμ κ°κ° κ°μ²΄λ€μ λ΄λ¦Όμ°¨μμΌλ‘ μ λ ¬μν¨λ€
```javascript
let chars = ["λ", "λ€", "κ°"];

chars.sort();
console.log(chars); // κ°, λ, λ€
```
+ μλ³Έ λ°°μ΄μ μμλ₯Ό μ¬μ μμΌλ‘ μ λ ¬μμΌ μλ‘μ΄ λ°°μ΄λ‘ λ§λ λ€.
+ But! μ«μμ κ²½μ°λ λ€λ₯΄λ€
```javascript
let num = [0, 1, 2, 10, 30, 3, 20];

num.sort();
console.log(num) // 0, 1, 10, 2, 20 , 3, 30 μ΄ μΆλ ₯λλ€

// μ«μ μ λ ¬κ°μ κ²½μ°μλ κ°λ¨ν λΉκ΅ν¨μμ ν¨κ» μ¬μ©λλ€
const compare = (a, b) => {
  if(a > b){
    // ν¬λ€
    return 1; // a λ b λ λΉκ΅νμλ a κ° ν¬λ©΄ a λ₯Ό λ€λ‘ λ³΄λ
  }

  if(a < b){
    // μλ€
    return -1; // a λ b λ λΉκ΅νμλ a κ° μμΌλ©΄ a λ₯Ό μμΌλ‘ λ³΄λ
  }

   //κ°λ€
   return 0; // γγ λ€μ~
};
num.sort(compare); // compare λ₯Ό sortμ λ§€κ°λ³μλ‘ λ£μ΄λ²λ¦Ό
console.log(num); // 0, 1, 2, 3, 10, 20, 30 μΌλ‘ μ μμ μΌλ‘ μΆλ ₯λλ€
```

#### 2) reverse
+ λ°°μ΄μ μμλ₯Ό λ€μ§μ΄ μμ΄λ²λ¦°λ€! (feat. νκ΄΄λ©μλ)
```javascript
let num = [ "1", "2", "3", "4" ]

num.reverse() // [ "4", "3", "2", "1" ]
```  

### β 7. λ¬Έμμ΄ ν©μΉκΈ°
#### 1) join
```javascript
const arr = ["μλνμΈμ?", "νμ₯μ€μ", "μ€λ₯Έμͺ½μλλ€."]

console.log(arr[0], arr[1], arr[2]) // μλνμΈμ? νμ₯μ€μ μ€λ₯Έμͺ½μλλ€.
//λ°°μ΄μμ κ°μ²΄λ€μ νλνλ κΊΌλ΄μ λμ΄νκΈ°λ νλ€λ€

console.log(arr.join()); // μλνμΈμ?, νμ₯μ€μ, μ€λ₯Έμͺ½μλλ€.
console.log(arr.join(" ")); // μλνμΈμ? νμ₯μ€μ μ€λ₯Έμͺ½μλλ€.
// μ΄λ κ² κ³΅λ°±μΌλ‘ κ΅¬λΆμλ₯Ό μ ν΄μ£Όλ©΄ μμ°μ€λ½κ² λμ΄λλ€.
```

[πΌμ΅μλ¨μΌλ‘ κ°κΈ°πΌ](#javascript-basic)
