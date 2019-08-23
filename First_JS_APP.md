## 3.1-3.2 Making a JS Clock 

```js
const clockContainer = document.querySelector(".js-clock"), //jsscript clock을 넣어줄 div 클래스 선택(.js-clock)하여 변수로 지정
    clockTitle = clockContainer.querySelector("h1"); //ClockContainer 내의 'h1' 선택하여 변수지정.

function getTime() { //현재 시간을 나타내 줄 함수 만들기

    const date = new Date(); //오늘의 날짜, 시간 정보 얻기
    const hours = date.getHours(); //'시' 얻기
    const mins = date.getMinutes(); //'분' 얻기
    const seconds = date.getSeconds(); //'초' 얻기
    
    clockTitle.innerText = `${  //clockTitle의 텍스트 변경
        hours < 10 ? `0${hours}` : hours  //hours가 10보다 작다면 앞에 0${hours}를 리턴하고, 아니면 hours를 리턴하기.
        }:${
        mins < 10 ? `0${mins}` : mins //mins가 10보다 작다면 앞에 0${mins}를 리턴하고, 아니면 mins를 리턴하기.
        }:${
        seconds < 10 ? `0${seconds}` : seconds //seconds가 10보다 작다면 앞에 0${seconds}를 리턴하고, 아니면 seconds를 리턴하기.
        }`;
}

function init() { //init 함수 만들기
    getTime(); //getTime 함수 실행 
    setInterval(getTime, 1000); //1초마다 현재 시, 분, 초를 얻어서 업데이트 시킨다.
}

init(); //init 함수 실행
```

## 3.3-3.4 Saving the User Name

```js
const form = document.querySelector(".js-form"), //form 태그 변수만들기
    input = form.querySelector("input"), //input 태그 변수 만들기
    greeting = document.querySelector(".js-greetings"); //이름 저장하고 띄울 greeting 변수 만들기

const USER_LS = "currentUser", // Username받을 변수 만들기
    SHOWING_CN = "showing" // showing class명으로 변수 만들기

function saveName(text) {
    localStorage.setItem(USER_LS, text);
}

function handleSubmit(event) {
    event.preventDefault();
    const currentValue = input.value
    paintGreeting(currentValue);
    saveName(currentValue);
}

function askFormname() {
    form.classList.add(SHOWING_CN);
    form.addEventListener("submit", handleSubmit);
}

function paintGreeting(text) {
    form.classList.remove(SHOWING_CN);
    greeting.classList.add(SHOWING_CN);
    greeting.innerText = `Hello ${text}`;
}

function loadName() {
    const currentUser = localStorage.getItem(USER_LS);
    if (currentUser === null) {
        askFormname();
    } else {
        paintGreeting(currentUser);
    }
}

function init() {
    loadName();
}

init();
```

```css
body{
    background: #ecf0f1;
  }
  
  h1{
    color:#e67e22;
    transition: color .5s ease-in-out;
  }
  
.form,
.greetings {
  display:none;
}

.showing {
  display:block;
}
```

```html
<!DOCTYPE html>
<html>

<head>
  <title>Something</title>
  <link rel="stylesheet" href="index.css" />
</head>

<body>
  <div class="js-clock">
    <h1>00:00</h1>
  </div>
  <form class="js-form form">
    <input type="text" placeholder="What is your name?">
  </form>
  <h4 class="js-greetings greetings"></h4>

  <script src="clock.js"></script>
  <script src="greeting.js"></script>
</body>

</html>
```
