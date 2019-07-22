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
```js
function sayHello(name,age){
  return ( `Hello ${name} you are ${age} years old. `);
  }

const greetJian = sayHello("Jian",29)

console.log(greetJian)

//결과값
>Hello Jian you are 29 years old. 
```


