## 2.1 Your first JS Function (Basic grammer)
console is an Object, but bigger than what we made in last lesson, and log is one thing that's inside of console object. 
console.log is a built-in fucntion. 

function is a piece of code that you can make and use as many times as you want.

function functionName () {} <br>
the argument is inside of (). they are like variables. <Br>
we can give anything to argument(=parament,인자), and function will take it and use it.

```js
function youare(name,age,howitis){
  console.log("You're ",name,"who is",age,"years old.","you're",howitis);
}

youare("Jian",29,"pretty");

//결과값
>You're  Jian who is 29 years old. you're pretty
```
()안에 있는 argument가 외부에 있는 value를 받아와 담아둔다. (*argument는 variable(변수) 같은 것임) <br>
이후 value를 불러오면 담아둔 순서대로 출력된다.


## 2.2 More Function Fun
이름과 나이를 넣어 "Hello 이름 you are 나이 years old" 출력 하기.

```js
function sayHello(name,age){
  return ( `Hello ${name}. you are ${age} years old. `);
  }

const greetJian = sayHello("Jian",29)

console.log(greetJian)

//console 출력값
>Hello Jian. you are 29 years old. 
```

계산기 만들기
```js
//calculator 

const calculator = {
  plus : function (a, b){
    return a + b;
  },
  minus : function(a, b){
    return a - b;
  },
  devide : function(a, b){
    return a / b;
  },
  multiple : function(a, b){
    return a * b;
  },
  power : function(a, b){
    return a ** b;
  }
}

let a = 5;
let b = 5;

const plus = calculator.plus(a,b);
console.log(plus);

const minus = calculator.minus(a,b);
console.log(minus);

const devide = calculator.devide(a,b);
console.log(devide);

const multiple = calculator.multiple(a,b);
console.log(multiple);

const power = calculator.power(a,b);
console.log(power);

const result = 
 console.log(`when a=5, b=5 => plus(+):${plus}, minus(-):${minus}, devide(/):${devide}, multiple(*):${multiple}, power(**):${power} `)
 
//console 출력값
>10
0
1
25
3125
when a=5, b=5 => plus(+):10, minus(-):0, devide(/):1, multiple(*):25, power(**):3125 
   
 ```
## 2.6 - 2.7 DOM - If else - Function practice
* 색상 바로 복사하는 사이트 https://flatuicolors.com/
* 이벤트 찾을 땐 항상 MDN에서 찾아볼 것. (click, mouseenter...) <br>
 https://developer.mozilla.org/en-US/docs/Web/Events#Most_common_categories
 
title을 클릭했을 때 color가 'rgb(186, 220, 88)'이면 #686de0로 변경하고, #686de0이면 rgb(186, 220, 88)로 변경하기
```js
const title = document.querySelector("#title");

const BASE_COLOR = "rgb(186, 220, 88)";
const OTHER_COLOR = "#686de0";


function colorCheck() {
    const currentColor = title.style.color;
    if (currentColor === BASE_COLOR) {
    /*★아래의 title.style.color를 currentColor로 바꾼다면 작동하지 않음.
    currentColor는 그저 주소를 가리키는 변수일 뿐이기 때문임. (말하자면 링크같은것..?)
    */
        title.style.color = OTHER_COLOR;
    } else {
        title.style.color = BASE_COLOR;
    }
}

function clickHandle() {
    title.style.color = BASE_COLOR;
    title.addEventListener("click", colorCheck);
}

clickHandle();
```

## 2.7 
