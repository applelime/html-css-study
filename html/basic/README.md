# HTML 기초 태그 정리
### 제목(Headings) - h1~h6
제목을 표시할 때 사용하는 태그

### 문단(Paragraph) - p
하나의 문단을 나타내는 태그

### 강조(Emphasis) - em, strong
중요한 요소이거나 강조하고 싶은 요소일 때 em이나 strong 태그를 사용  
단순히 기울임이나 볼드를 위해 사용하면 안 된다!  
단순 볼드만 필요한 경우에는 b태그를 사용하자.

### 줄바꿈(Break) - br
텍스트 안에 줄바꿈 필요한 경우 사용.  
문단 사이 여백을 두기 위한 용도로는 br대신 p로 감싼 후 css로 여백을 조절하자.

### 링크(Anchor) - a
href특성을 통해 다른 페이지나 같은 페이지 내의 위치, 이메일 등 URL연결하여 다른 위치로 이동  
자주 사용하는 속성 - `target="_blank"` 새창에서 열기

### 이미지(Image) - img
이미지를 삽입할 때 사용하는 태그  
alt 속성 (alternative text. 대체 텍스트)도 웬만하면 뻬먹지말고 넣어주도록 하자.

### 리스트(Lists) - ul, ol, li
순서가 중요한 경우 ol(ordered list). 즉 항목의 순서를 바꿨을 때 의미가 바뀐다면 ol을 사용하자.  
순서가 중요하지 않은 경우 ul(unordered list)  

자식으로는 li(list item) 태그를 사용해야 함.

### 정의 리스트(Description List) - dl, dt, dd, dfn
용어를 정의하거나, key-value 쌍을 표시할 때 사용  

dt (Description Term) - 용어, Key값  
dd (Description Data) - 설명, Value값  
dfn (Definition) - 정의  

여러개의 용어와 1개의 정의 (2개 이상의 dt와 1개의 dd),  
1개의 용어와 여러 개의 정의 (1개의 dt와 2개 이상의 dd)도 허용한다.  
dt, dd 쌍을 div로 감싸는 것도 가능하다.

### 인용(Quotations) - blockquote, q, cite
blockquote는 긴 인용문을 표시할 때 사용한다.  
q는 짧은 인용문을 표시할 때 사용  
출처 url은 cite 속성으로, 출처 텍스트는 cite 태그로 표시  

### 그룹핑 - div, span
둘 다 아무런 동작을 하지 않으며, 그룹을 나누거나 css로 꾸미기 위해 사용한다.  
div는 블록 레벨 요소로 블록을 만들기 때문에 큰 덩어리를 묶는데 자주 사용하고,  
span은 인라인 요소로 텍스트 중간에 사용해도 문단이 끊기지 않아  
보통 텍스트 안에서 일부만 그룹핑하거나 할 때 자주 사용한다.

### 테이블(Table) - table, tr, td, th, thead, tbody
thead, tbody는 테이블 내에서 컬럼 헤드와 본문을 구분할 때 사용한다.  
tr(table rows)은 가로 줄,  
td(table data)는 실제 데이터(세로 줄),  
th(table head)는 제목인 데이터의 경우 td 대신에 사용한다.  
th에는 scope속성을 사용하여 행의 제목인지, 열의 제목인지 표시한다. (`scope="col"`)

열을 합치는 경우(가로방향) - td에 `colspan="6"`  
행을 합치는 경우(세로방향) - td에 `rowspan="2"`

### 양식 - form, input, button, textarea, ..
form은 정보를 제출하기 위한 컨트롤을 포함하는 문서 구획  
action은 보통 api의 주소, method는 특성에 따라 get이나 post를 사용한다.  

input은 입력하는 양식에 사용한다. text, radio, checkbox 등...  
button은 클릭 가능한 버튼을 만든다. type이 submit인 경우 양식을 제출한다.  
textarea는 멀티라인 텍스트 컨트롤이 필요할 때 사용한다.  
select는 옵션 메뉴를 제공하는 컨트롤,  
label은 양식에 이름을 붙이는 태그로 for속성에 id를 넣으면 된다.

### 약어(Abbreviation) - abbr
title 속성으로 전체 뜻이나 설명을 제공

### 서식 지정 텍스트(Preformatted text) - pre
미리 서식을 지정한 텍스트로 html에 작성한 내용을 그대로 표시

### 멀티미디어 - audio, video
음악 audio, 동영상 video

## 그 외에도 태그가 너무 많다.
기타 태그 및 상세 내용은 아래 사이트에서 확인하자.  
<https://developer.mozilla.org/ko/docs/Web/HTML/Element>  