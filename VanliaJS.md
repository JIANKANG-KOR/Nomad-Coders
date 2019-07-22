# About JavaScript (Why should I learn JS?)
 - JS는 웹에 쓰이는 하나뿐인 프로그래밍 언어이다.
   (백엔드는 다른 언어에 대한 옵션이 많다 ex.Python, ASP, JAVA..)
 - 이는 프론트엔드 일을 하는 장점이자 단점이다.
 - 장점: 웹사이트를 하는 사람들은 모두 같은 언어로 얘기가능.
 - 단점: 우리가 할 수 있는게 없을 때가 있다.
   바꿀수도 업데이트도 할 수 없음. 원하는 것으로 교체할 수도 없음.
  
- 이 언어가 시간을 투자할 가치가 있는 이유 : <br>
  웹이 빠르게 발전함에 따라 JS도 빠르게 발전한다. 덕분에 막강해지고 영향력이 커지고 있다.<br>
 ->  JS가 가능한 개발자들은 할 수 있는 일이 점점 더 늘어난다.<br>
  웹사이트, 웹 앱, 모바일 어플리케이션, 비디오 게임, 네이티브 어플리케이션, 데스크톱 앱 등 다양한 것들을 만들 수 있다.<br>
  
- VS Code 혹은 ATOM을 사용하고 있다면 JS로 만들어진 Desktop application을 사용있는 것이다.

- 프론트엔드에서 JS를 쓰는 이유는 다른 언어로 교체되지 않았기 떄문이다.<br>
  모든 컴퓨터는 브라우저가 있고 브라우저는 JS로 돌아간다.<br>
  그러므로 모든 컴퓨터에는 JS가 깔려있다는 것. 모든 컴퓨터가 이 언어를 이해한다.
  
- JS는 영향력이 많은 언어이다. 따라서 어떤걸 함에 있어서 선택범위가 넓어질 수 있다.<br>
  이와 반대로, 유명하지 않은 언어를 선택하면 선택범위가 좁아진다. (ex. Ruby)
 
 
- 얼마나 영향력이 있는지 살펴보자 (Javascript를 이용해서 만든 예시들)
     
   1. Nomad Movies  
   https://play.google.com/store/apps/details?id=co.nomadcoders.nomadmovies&hl=ko
   
   2. world draw
   https://worlddraw.withgoogle.com/
   
   3. Impact JS
   https://impactjs.com/
   
 - What is the ECMASCript? Vanila JS?
 > JS는 언어, ECMAScript는 Specification(설명문), VanilaJS는 화장하지않은 날 것의 JS를 일컫는다.
  - Library나 Framwork는 메이크업, 화장같은 존재. JS를 더 예쁘게 만들어준다. 
    바닐라 자바스크립트를 쓰는게 능숙해질때 다음으로 넘어가자. 
    - why? -> JS에 진짜 JS에 재능있는 사람을 찾을 수가 없다. 
    리액트나 Jquery를 아는 사람들, Library를 다룰 줄 알거나 Framwork에 대한 전문가들은 찾기 쉽다.
    이런 사람들은 Framework에서만 전문가다. 실제 필드에서는 실력발휘를 못한다. 
    Vanila JS를 더 잘하게 되고 이해하게 되면 리액트와 같은 다른 언어를 시작할 때도 아무런 문제가 없을 것임.
    바닐라JS를 배우게 되면 다른 언어를 배울 때의 '컨셉'을 알게 된다. 이 컨셉은 다른 언어에서도 일맥상통한다.
    예를 들면 Function, Variable, 조건, 이벤트, Class, Objects, Array.. 등과 같은 것들.
  
 ## How to apply JS in HTML 
 
 ```html
<!DOCTYPE html>
<html>
  <head>
    <title>something</title>
    <link rel="stylesheet" href="index.css"/>
  </head>
  <body>
    <h1>This works!</h1>
    <script src="index.js"></script> 
   <!-- 바디의 제일 마지막에 <script> 태그를 넣는다. src를 건 상태로 script 태그 안에 코드를 작성해도 작동가능하다.-->
  </body>
</html>
```

## 변수 선언 방법
(* 변수를 선언할 때 기본으로 const를 쓰고 필요할 때까지 let 쓰지 말 것. 진짜 필요할 때만 let 쓰기)
 - var : 동일한 이름으로 변수 선언이 가능하여, 이전에 선언한 변수임을 잊어버리고 같은 이름으로 선언할 위험이 있다. 
 (안전장치가 없어 권장X) 에러가 뜨지 않는다.

 - let : var와 유사하지만, 중복된 변수 선언을 막아준다. (권장)
 ```js
let a = 221;
let b = a - 5;
a = 4
console.log(b,a);
```
> 결과값: 216 4

```js
let a = 221;
let b = a - 5;
let a = 4
console.log(b,a);
```
> 결과값: SyntaxError: Identifier 'a' has already been declared
    at /data/web_hosting_1/five-nine/HotpinkEnviousFlatassembler/index.js:3:5
 
 - const: let과 유사하지만 변수를 절대 바꾸지 않을 경우 사용. 
 
 ```js
const a = 221;
let b = a - 5;
a = 4
console.log(b,a);
```
> 결과값: TypeError: Assignment to constant variable.
    at /data/web_hosting_1/five-nine/HotpinkEnviousFlatassembler/index.js:3:3
   
```js
const a = 221;
let b = a - 5;
const a = 4
console.log(b,a);
```
> 결과값: SyntaxError: Identifier 'a' has already been declared
    at /data/web_hosting_1/five-nine/HotpinkEnviousFlatassembler/index.js:3:7

## Data types on JS

// for comments
/* for multi-ilne comments */


String (" "): 텍스트를 묶어줘
```js
/* String
const what = "Nicolas";
*/
```
Boolean: true = 1 / false = 0
```js
/*Boolean 
const wat = true;
*/
```

Number: 말 그대로 숫자
```js
/*Number
const wat = 666;
*/
```

Float: float하는 숫자. 소수점이 있는 숫자.
```js
/*Float (소숫점 숫자)
const wat = 55.1;
*/
```

## Organizing Data 
 1. Array: 여러 String을 하나로 묶는 것. 리스트라 생각해. (ex 월화수목금토일) 
Array 월-일을 한줄씩 const로 정해줄 필요 없이 array 사용 
```js
const daysOfWeek = ["Mon","Tue","Wed","Thu","Fri","Sat","Sun"];
const something="Something"

console.log(daysOfWeek[2],something);

>결과값: Wed Something

//추후 label 값 재지정할 수 있어 (const로 변수 지정해도 수정가능)//
const daysOfWeek[0] = "Unknown"


/*[] 안에 텍스트, true/false, numbers, floats 사용가능
console.log 내의 Array []안에 숫자를 써주면 해당하는 순서의 값을 출력.
컴퓨터는 숫자를 0부터 세는 점에 주의*/
```

 2. Object: Object는 value에 이름을 줄 수 있다. (리스트를 만들땐 Array를 사용)
하지만 예를들어, Array로 내 개인정보를 저장하려면 (이름, 나이, 성별 등)
내가 원하는 방식으로 정보가 저장되지 않아
 - **Object는 각 데이터에 label이 가능해

```js
const jianInfo = {
  name: "Jian",
  age: 29,
  gender: "Female",
  isPretty: true,
  favMovies: [
    { title: "Pasasite", janre: "Mysterious", actor: "Song Kang HO" },
    { title: "Mr.nobody", janre: "Drama", actor: "IDK" },
    { title: "Weplash", janre: "Thriller", actor: "IDK" },
    { title: "District9", janre: "Fantasy", actor: "IDK" },
  ],
  favFood: [
    //***Array 안에 object 넣을 수 있어//
    {
      name: "Kimchi", fatty: false,
    },
    {
      name: "Cheeseburger", fatty: true
    }
  ]
}

console.log(jianInfo.gender);

//favFood array 안에 있는 object의 name찾기 
console.log(jianInfo.favFood[0].name)
console.log(jianInfo.favMovies[0].actor);

//추후 label 값 재지정할 수 있어 (const로 변수 지정해도 수정가능)//
jianInfo.favFood[0].name = "Salad"

```
- [그래머 기억할 것들] : <br>',' 콤마 빼먹지 말 것, " " 쿼테이션 까먹지 말고 닫아
