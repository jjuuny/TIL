# TIL Day11

## 0719 js를 이용한 ajax테스트

**ajax란?**

**비동기식**으로 웹서버와 통신을 할 수 있는 자바스크립트 라이브러리이다.

ajax를 사용하면 비동기식으로 웹서버에 데이터를 보내거나 받을 수 있다.

전체 페이지를 새로 고치지 앙ㄴㅎ아도 페이지 일부만을 위한 데이터를 위한 데이터를 로드하는 기법이다.

간단하게 정리하면 자바스크립트를 통해 서버에 데이터를 요청하는 것이다.

### js_ajax01_XMLHttpRequest

구현 : 1. 객체 생성(XMLHttpRequest())	2. 서버에서 데이터가 넘어오면 전송받을 기능을 만듦	3. 객체 열기(객체명.open('전송방식', '파일명', 'true or false'))	4.객체를 보냄(객체명.send()  실제 서버에 접속)

`readyState`  객체 처리 결과를 가지고 있다(0:초기화실패 1 : 서버 연결 2 : 요청접수 3 : 처리요청 4 :요청완료)	

```
<script>
	// ajax란 비동기식으로 웹서버와 통신을 할 수 있는 자바스크립트 라이브러리다.
	// ajax를 사용하면 비동기식으로 웹서버에 데이터를 보내거나 받을 수 있다.
	function loadDom(){
		// 비동기식으로 서버에 접속하여 abcd.txt 파일의 정보를 전송받아 ajaxResult에 내용을 변경한다.
		// XMLHttpRequest : ajax처리를 하는 자바스크립트 내장 객체
		
		// 1. 객체생성
		var xHttp = new XMLHttpRequest(); //웹 서버와 통신하는 객체를 생성한다.
		
		// 2. 서버에서 데이터 넘어오면 전송받을 기능 구현
		xHttp.onreadystatechange = function(){
			// 서버에서 정보가 오면 이벤트에 의해서 실행되는 함수
			// 전송결과 확인하는 변수
			// readyState : XMLHttpRequest의 처리결과를 가지고 있음(0: 초기화실패, 1: 서버연결, 2: 요청접수, 3: 처리요청, 4: 요청완료)
			// status : 요청 처리 상태 번호를 반환(200: 정상처리, 403: 금지, 404: 찾을 수 없음)
			// statusText : 'OK', 'Not Found'
			// responseText : 실행결과 값 -> 서버에서 전송받은 내용이 있는 변수
			
			if(this.readyState==4 && this.status==200){//정상 처리됨
				document.getElementById("ajaxResult").innerHTML = this.responseText;
			}else{// 전송실패
				document.getElementById("ajaxResult").innerHTML = "서버에서 정보를 가져오지 못했습니다";
			}
		}
		// 3. 객체열기
		xHttp.open('GET','abcd.txt', true); //('전송방식','가져올 데이터 파일명', 동기식(false)/비동기식(true))
		// 4. 객체를 보냄 : 실제서버에 접속
		xHttp.send();// 서버에 정보를 요청함
	}
</script>
</head>
<body>
<h1>자바스크립트를 이용한 ajax테스트</h1>
<button onclick="loadDom()">클릭하면 서버에서 데이터를 비동기식으로 가져옴</button>
<div id="ajaxResult" style="border:1px solid gray; height:200px;"></div>
```

### jq_ajax01_text

Load : 비동기식으로 파일을 가져오는 함수

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
<script>
	$(function(){
		$("#result>button").click(function(){
			// 서버에서 abcd.txt파일의 내용을 가져오기
			//                파일명
			$("#result").load('abcd.txt'); // load:비동기식으로 파일 가져오는 함수
		});
	});
</script>
</head>
<body>
<h1>jquery에서 ajax처리(text)</h1>
<div id="result" style="background:#ddd;">
	<button>클릭하시면 비동기식으로 text파일의 내용을 가져옴.</button>
</div>
</body>
</html>
```

### jq_ajax02_json

서버에서 json 데이터 가져오기

ajax_data.json 파일에 {"rank": {데이터들 선언}}

```
<script>
	$(function(){
		$("#ajaxBtn").on('click', function(){
			//서버에서 json데이터 가져오기
			$.ajax({
				url: 'ajax_data.json',   //서버에 접속할 대상
				dataType:'json',
				success:function(result){ // 서버에서 정상전송을 받았을 때 / result에 json데이터가 들어가있다. result는 변수기 때문에 아무거나 선언 가능
					console.log(result);
					$("#result").append("<ol type='1'>");
					$.each(result.rank,function(idx, data){
						// <li>데이터 : 내용 </li>
						$("#result>ol").append("<li>" +data.name+" : "+data.local+"</li>");
					});
					$("#result").append("</ol>")
				},
				error: function(request, status, error){ // 서버에서 전송을 받지 못했을 때
					console.log("전송실패...");
					console.log("request.code=", request.code);
					console.log('error Message=', request.responseText);
					console.log('error=', error);
				}
			});
		});
	});
</script>
</head>
<body>
<button id="ajaxBtn">클릭하면 비동기식으로 서버에서 json데이터 가져옴</button>
<div id="result"></div>
```



