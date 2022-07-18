# TIL Day02

## HTML2일차 0706 

### 이미지 삽입하기

`<img src="파일경로" alt=대체텍스트>`

### tag10_video

​	 `src`  재생할 사운드파일 

​	`controls`  컨트롤 바 표시

​	`autoplay`  자동재생

​	`loop`  숫자 상관없이 무한 반복

​	`preload`  전송이 완료 후 재생을 하라는 뜻

​	`width, height`

​	`poster` 영상 시작 전 이미지

### tag11_form

`<form method="전송방식(post or get)"  action="서버페이지 파일명">`

`size`  칸길이 	`maxlength` 입력받을 문자 수	`required`  빈 값 안됨(필드를 채워야 한다.) submit이 실행되면 서버페이지 파일로 넘겨준다.

#### input

`<form>` 태그는 전체 양식을 의미하며, 화면에 보이지 않는 추상적인 태그입니다.
실제로 사용자가 양식을 입력하기 위한 태그는 `<input>` 태그 등이 사용됩니다.

`type` 속성을 통해 종류를 나타내며, `name`을 통해 데이터의 이름, `value`를 통해 기본 값을 지정합니다.

type

- `text`: 일반 문자
- `password`: 비밀번호
- `button`: 버튼
- `submit`: 양식 제출용 버튼
- `reset`: 양식 초기화용 버튼
- `radio`: 한개만 선택할 수 있는 컴포넌트
- `checkbox`: 다수를 선택할 수 있는 컴포넌트
- `file`: 파일 업로드
- `hidden`: 사용자에게 보이지 않는 숨은 요소



```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>tag11_form</title>
</head>
<body>
<h1>클라이언트측에서 서버로 정보를 보낼준비를 한다.</h1>
<pre>
	method : 전송방식(get, post)
	action : 서버페이지 파일명
</pre>
<form method="post" action="write.jsp">
	<!-- hidden은 입력하지 않은 값을 넘기는 숨겨진 양식 -->>
	<input type="hidden" name="reNo" value="564765"/>
<!-- 
		size : 칸 길이 
		maxlentgh : 입력받을 문자 수 
		required : 이 필드를 채우시오 빈 값 안 됨
		submit이 실행되면 write.jsp로 넘겨줌
		method = post : 데이터를 숨겨서 보냄
		체크박스는 여러개 선택 가능 라디오 버튼은 한 개만 선택 가능
		checked : 전엥 체크한 것이 표시되어 보임
		select : 
 -->
	<ul>
		<li><label>아이디, 이름</label> : <input type="text" name="userid" size="30" maxlength="10"
		placeholder="아이디를 입력하세요" required/> </li>
		<li>비밀번호 : <input type="password" name="userpwd" placeholder="비밀번호를 입력하세요"/></li>
		<li>파일첨부 : <input type="file" name="filename"/></li>
		<li>체크박스 : <input type="checkbox" name="hobby" value="등산"/> 등산 
					<input type="checkbox" name="hobby" value="쇼핑" checked/> 쇼핑 
					<input type="checkbox" name="hobby" value="게임"/> 게임 
					<input type="checkbox" name="hobby" value="사이클" checked/> 사이클 
					
		</li>
		<li>라디오버튼 : <input type="radio" name="gender" value="M"/> 남
					  <input type="radio" name="gender" value="f" chcked/> 여
		</li>
		<li>관심분야 : <select name="interest" size="4" multiple>
						<option>독서</option>
						<option>영화감상</option>
						<option>달리기</option>
						<option>암벽등반</option>
						<option>인라인</option>
						<option>수영</option>			
					</select>
		</li>
		<li>
			optgroup태그 : <select>
								<optgroup label="프론트엔드">
								<option>HTML5</option>
								<option>CSS3</option>
								<option>JAVASCRIPT</option>
								<option>JQUERY</option>
								</optgroup>
								<optgroup label="백엔드">
								<option>JSP</option>
								<option>SPRING</option>
								</optgroup>
						  </select>
		</li>	
		<li>
			여러줄의 문장 : <textarea name="intro" cols="50" rows="5">dddd</textarea>
		</li>
		<li>date : <input type="date" name="date1"/></li>
		<li>datetime-local : <input type="datetime-local" name="date2"/></li>
		<li>month : <input type="month" name="date3"/></li>	
		<li>week : <input type="week" name="date4"/></li>
		<li>color : <input type="color" name="color"/></li>
		<li>number : <input type="number" name="num" min="0" max="20" step="5" value="5"/></li>
		<li>range : <input type="range" name="num2" min="1" max="11" step="2" value="3"/></li>
		<li>
			<input type="submit" value="등록"/>
			<input type="button" value="등록"/><!-- submit기능이 포함되어 있지 않다. -->
			<input type="reset" value="다시쓰기"/><!-- submit기능이 포함되어 있지 않다. -->
			
			<input type="image" src="../img/button.png"/><!-- submit기능이 포함되어 있다. -->
			<input type="reset" value="다시쓰기"/>
		</li>
	</ul>
</form>
</body>
</html>
```

### tag12_div.form

`<div>`태그는 Division의 약자로, 레이아웃을 나누는데 주로 쓰인다.

다른 태그와 다르게 특별한 기능을 갖고 있지는 않고, **가상의 레이아웃**을 설계하는데 쓰이며, 주로 CSS와 연동하여 사용한다.





​	



