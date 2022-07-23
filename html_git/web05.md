# TIL Day05

## web5일차

### js07_array

자바스크립트의 배열 선언

* 배열 크기를 지정하지 않아도 된다.
* 데이터형이 다른 데이터를 하나의 배열에 보관할 수 있다.

```javascript
var arr = new Array();
arr[2] = 150;
arr[10] = "홍길동"; // 가능하다.
```

`배열명.push()`  배열에 데이터 추가하기 : 마지막 값 추가 

`배열명.join(-,* 등등)`  문자 연결하기

`배열명.pop()`  마지막 데이터 삭제하기

`배열명.shift()` 오른쪽 데이터 왼쪽으로 이동하고 0번 째 값 사라짐

`배열명.unshift(값)` 값이 처음에 들어가고 오른쪽으로 이동 

**배열의 정렬**

* 오름차순
  	* 문자 오름차순  `배열명.sort()`  
  	* 숫자 오름차순  `배열명.sort(function(x,y){return x-y;})`
* 내림차순
  * 문자 내림차순 : 오름차순으로 정렬 후 역순으로 변경해야 한다.  `배열명.rever()`
  * 숫자 내림차순 `배열명.sort(function(a,b){return b-a;})`  오름차순의 반대로 설정

**Json** (javascript object notation) : 데이터 처리하기

key와 value를 가지는 구조.

```javascript
var jData = {username : "홍길동", tel:"010-8965-8963", 
			email:{
					firstemail:"goguma777@nate.com",
					secondemail:"goguma7@naver.com"
					},
			gugudan : function(dan){
							var r = "";
							for(var i=2; i<=9; i++){
								r += dan+"*"+i+"="+dan*i+"<br/>";
							}
							return r;
				}
		};  // 이런 식으로 내부에 내부로도 만들어서 사용이 가능하다.
//Json 데이터에 접근 방법 : jData.email.firstemail, jData.email.secondemail
```

 

### Js09_datetime

 `getFullYear()`  년	`getMonth()`  월	`getDate()`  일	`getHours()`  시	`getMinutes()`  분	`getSeconds()`  초	`getDay()`  요일 --> 일요일:0, 월요일:1....

### Js10_window

팝업창 띄우기 : win.open("새 창에 띄울 파일명", "창이름", "width=, height=, left=, top=")

팝업창 닫기 : win.close()

절대 좌표 이동 : win.moveTo(width, height)

상대 좌표 이동 : Win.moveBy(width, height)

### Js11_setInterval

`setInterval("호출할 함수명", 밀리초)`  설정한 시간 간격으로 호출됨

`clearInterval`  interval을 중지시킴

### login.html

### layoutStyle.css, index.html

레이아웃을 먼저 설정하여 영역을 나누기

Ul div div(하단)로 분리

자바스크립트 배열




