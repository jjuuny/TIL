# TIL Day04

## HTML4일차 + CSS + JS 0708

### css13_duration

overflow 속성

1. auto : 내용이 넘치면 스크롤바 생김
2. scroll : 무조건 스크롤바 생김(내용이 안 넘쳐도 생긴다)
3. hidden : 숨긴다

transition-duration: 객체의 움직임 속도	Opacity: 튜명도 (0~1사이의 값)

시멘틱 태그 

가로로 나눠지는 기준을 먼저 잡기

Js03_intro파일 받기 실행이 안 됨



### css14_media

media쿼리를 이용해 반응형 스타일 지정

디스플레이 종류 : all(모든), screen(모니터), print, tv, projection.... ex)

```+css
@media all and (min-width:320px) and (max-width:600px){
		li{background-color:yellows;}
		img{display:block;}
```



### js01_start

초기값에 의해 데이터형이 정해진다. 설정하지 않은 경우 undefined

`var` `let` `const`

var i = 12.5;	let k;	const x = 10;

* `var` i 라는 변수를 필요하면 다시 선언해도 된다.
* `let`  k는 같은 블럭에서는 한 번만 선언할 수 있다.
* `const`  x는 상수화된 변수

**자바스크립트 출력**

1. window.alert() 메소드 : 브라우저오 별개로 대화상자를 띄워 사용자에게 데이터 전달

2. HTML DOM 요소를 이용한 innerHTML 프로퍼티 : 가장 많이 사용, 내용이나 속성값 변경 가능하다.

3. document.write() 메소드 : 웹 페이지가 로딩될 때 실행되면, 웹 페이지에 가장 먼저 데이터를 출력 따라서 대부분 테스트, 디버깅 용으로 많이 사용한다.

4. console.log() 메소드 : 웹브라우저의 콘솔을 통해 데이터 출력

### js02_external, js03_intro_style

JS의 대화상자(Alert, Confirm, Prompt)

1. `Alert` 단순히 메세지를 전달하고 반환값이 없다.

2. `Confirm`  true 또는 false를 반환한다.
3. `Prompt`  사용자가 입력한 값을 받아온다.

※ self.close() / window.close() : 종료

**선언한 객체를 가져오는 법**

스타일 : document.getElementById("선언한 ID")

​				style.border, width, height 등 사용 가능

태그속성도 똑같이 변경해서 사용 가능 

### js04_function

**함수 생성하기** -> 함수는 호출하여야 실행이 된다.

```+js
// 1번
function gugudan(){
		var dan = document.getElementById("dan").value;
		if(!isNaN(dan)){ // is not a number 숫자가 아닐 때 true, 숫자일 때 false
			var r = "<ul>";
			for(var i=2; i<=9; i++){
				r += "<li>"+dan+"*"+i+"="+(dan*i)+"</li>";
			}
			r +="</ul>";
			console.log(r);
			document.getElementById("result").innerHTML = r;
		}else{
			document.getElementById("result").innerHTML = "숫자가 아닙니다.";
		}
	}
	// 2번
	var hap = function(a, b){
		var h = a + b;
		document.getElementById("result").innerHTML = h;	
	}
	// 3번
	var cha = (a, b)=>{ /*function 생락할 때 => 사용*/
		var c = a - b;
		console.log(c);
	}
```

### js05_string

length(길이), indexOf(찾을 문자열,시작 위치), search(찾을 문자열)

substr(start, length) : 시작위치부터 길이만큼 반환

substring(stare, end) : 시작위치부터 end앞까지 반 <매개변수로 잘라내고 싶은 문자열 start index, laste index 전달한다.> 

slice() : substring과 동일하지만 음수일 때 결과값이 다름

replace(찾을문자, 변경할 문자) toUpperCase(), toLowerCase() : 대문자로, 소문자로 

concat() : 문자연결 charAt() : 위치의 문자 반환 charCodeAt() : index의 유니코드 반환

### js06_math

Math.PI(), Math.pow(), Math.round(), Math.ceil(), Math.floor(), Math.random()

