# TIL Day 01

## html1일차 0715(화)

### html

 -Hyper Text Markup Language 약어로 웹페이지에서 다른 페이지로 이동할 수 있는 언어

 -웹 문서의 뼈대를 만들고 웹 문서 내용을 보여주기 위한 것



### 태그

 -정보를 정의하는 것을 말 한다.

 -<태그명 속성명1 = 속성값1 속성명2 = 속성명2></태그명>순의 문법을 따른다.



### 문서 기본 구조

`<!DOCTYPE html>` 또는`<!doctype html>`   웹 브라우저에게 ‘이제부터 처리할 문서는 HTML 문서라고 알려주는 것

`<title>`문서 제목

`<head>` 브라우저에게 정보를 줌

### 여러가지 태그들

`<br> or <br/>`  줄 바꿈	  `<hn>`제목 표시  	`<p>` 텍스트 단락	 `<b> <strong>`  굵게 `<i>` 기울임		`<pre>`  문서에 입력한 그대로 보여줌		`<b>, <strong>`  진하게

`&nbsp;`  빈 칸 한 개	 `&lt;, &gt;`  < > 를 말함	 `&copy;` : ©

`s, del, strike`  취소선

`<img>`  웹 페이지에 이미지를 표시한다

​		`src` 사용할 이미지 파일 명 	`width height` 폭, 높이	`alt` 이미지가 없을 때 표시할 내용

`<a>`  링크, 파일 다운로드를 할 수 있다. 

​		`href` 주소를 가르킨다. 

​		`_blank` 새 창으로  `_self` 현재 창으로 `_parent` 부모 창으로

### 목록 만들기

`<ol>, <li>`  순서가 있는 목록  `type` 1, a, A, i, I

`<ul>, <li>`  순서가 없는 목록  `type` disk(안이 채워진 원) circle(안이 비워진 원), square

`<dl>`  dt,dd를 묶음	 `<dt>`  이름(제목) 지정	`<dd>`  값(설명) 지정

### 테이블 만들기

`<table>`  표 전체	`<caption>` 표 제목	`<th>`  제목 셀(가운데 정렬)	`<td>`  셀	`<tr>` 행

`border="1"`  표에 선 생성(table속성)	

​	**테이블 합치기**

​		`<td rowspan="합칠 셀의 개수">셀의 내용</td>` 줄을 합친다

​		`<td colspan="합칠 셀의 개수">셀의 내용</td>`  칸을 합친다

​    	합친 테이블을 잘 생각해서  `<td>` 를 작성한다.

​    

클라이언트(웹브라우저)가 웹 서버(html/css/Javascript)에

클라 -> 웹서버 -> 자바 -> MySQL -> 자바 -> 웹서버 -> 클라

Front End(뷰단) html/scc/Javascript/ Jquery/ajax - 인터프린터 언어

Back End(서버단) Java Spring Mybatis - 컴파일 언어

블럭을 잡는 것 : html 길이, 폭, 선 보이게 등 디자인 작업 : css





<!DOCTYPE html>
