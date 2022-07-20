# TIL Day03

## HTML3일차 + CSS 0707

### css(Cascade Style Sheet)

1. Inline : 태그에 직접 스타일 적용
2. Intername : `<style>`이용해 스타일시트 모아놓은 스타일
3. external : 외부스타일 시트, 스타일시트만 있는 코드 존재.

`<style>` 기본구조 : 

선택자 {속성:속성값;} 

**태그선택자**  : span, b, strong

**아이디선택자** : `#`으로 호출

**클래스선택자** : `.`으로 호출

**그룹선택자** 한 번에 여러 개 적으면 됨.

### css연결(link사용)

link로 css를 연결해준다. 속성은 3개(rel(고정), href, type)

`<link rel="stylesheet"; href="연결할 css파일"; type="text/css">`

#### a태그의 상태에 따른 스타일시트 적용하기

`text-decoration(a의 속성)`

​		linethrough : 취소선	underline : 밑줄	overline : 윗줄	none : 선 없음

​				**기본으로 밑줄이 쳐져 있어서 취소선을 많이 사용한다. 깔끔해보임**

a:link{} : 링크상태일 때 	a:visted{} : 방문했을 때	a:hover : 마우스를 오버햇을 때	a:active 마우스를 누른 상태일 때



**background **

`background-image` 화면전체가 그림으로 채워짐	`background-color:rgb(,,)` 색상	 

`background-position`70%, left, center 등 가능



**font**

`font-size` 글자크기(기본:16px)	`font-family` 글꼴	`font-color` 글자색	

​		글자 크기를 1.5em처럼 표기해 배수로도 사용 많이 한다.



**border**

`border-style` 선모양(solid(실선), dotted(점선), double(이중선), none, groove(홈))

`border-color` RBG, color명

`border-width` 선의 두께 px

추가적인 내용 :  margin은 기준의 외부	/	padding은 기준의내부

** 기본적으로 top, right, bottom, left가 그룹화 되어있다.

​		즉, 바로 사용 가능하며 두 개를 쓸 경우 맞은 편끼리 적용이 된다.(기본적으로 top부터 시계방향으로 		진행)

**list**

`list-style-type:none` 점 없애기

`float:left` li들 좌우 정렬

`text-align:center` 내용 가운데 정렬

`line-height` 위 아래 정렬

### css07_attr

속성선택자 : 원하는 속성만 선택해서 적용

=, 	`$=` 특정값으로 끝나는 태그 선택, 	`^=` 특정값으로 시작되는 태그 선택, 	`*=` 특정값이 포함된 태그 선택

### css08_child

- 자손 선택자		>
- 후손 선택자        #main>ul>li>h2 or #main>h2 중간 생략 가능
- 동위 선택자 
  - 선택자A + 선택자B : 선택자 A의 바로 다음의 B를 선택한다.
  - 선택자A ~ 선택자B : 선택자 A의 다음에 있는 모든 B를 선택한다.

- 상태 선택자
  - focus : 커서가 컴포넌트에 들어갈 때
  - checked : 체크가 될 때
  - readonly: 읽기만 가능
  - disabled : 비활성화된 컴포넌트에 스타일 적용
  - enabled : 활성화된 컴포넌트에 적용

### css10_structure

구조선택자

	- nth-child(2n) : 짝수 번 째
	- nth-child(2n+1) : 홀수 번 째

**html 속성(선택불가능하게 설정할 때)**

oncontextmenu 마우스 오른쪽 사용 불가능

oneselectstart 드래그 시작이 불가능 

ondragend 드래그 종료 불가능

텍스트 스타일

- first-letter : 첫 번 째 문자에 대한 스타일
- first-line : 첫 번 째 줄에 대한 스타일
- Selection : 선택영역에 대한 스타일(드래그)

### css12_visibility

visility 속성 : 선택된 객체를 보여주거나 숨길 수가 있다. 숨기더라도 공간을 유지하고 있다.

`visible`  생김 / `hidden`  숨김  ex)  #d1{visibility:visible;}

display 속성 : 선택된 객체를 보여주거나 숨길 수가 있다. 숨김 상태에서 공간을 반납한다.

`block` 	`none`

position 속성

`absolute` 자기가 원래 있던 공간을 빠져나옴

`relative`  원래 공간을 차지하고 있다

`static`  좌표가 안 된다

`fixed` 고정 left, top, bottom, right
