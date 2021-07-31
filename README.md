# HTML, CSS, JS basic



## HTML

> HTML:Hyper Text Markup Language - 마크업(표시) 언어
> 
> 웹페이지의 구조를 표시
> 
> 웹페이지의 콘텐츠를 표시


### HTML Element

> Elements : 요소 -의미적
> 
> tag : 태그 - 기술적
> 
> 문법(Syntax)
> 
> > <>로 감싸줌
> > 
> > 소문자로만 사용
> > 
> > 시작태그와 종료태그 세트로 구성됨
```
<tagname>contents</tagname>
```
> > 
> > 예외) 시작태그만 존재하는 경우: 빈 태그(Empty Element)
> > 
> > 포함관계(Nested)
```
<body>
  <div>
    text
  </div>
</body>
```


### HTML Attribute

> Attribute : 자질, 속성
> 
> > * 참고- CSS는 Property
> 
> HTML 요소의 부가 정보
> 
> 문법
> 
> > 속성이름 = "속성값"
```
<a href="http://www.naver.com">naver</a>
```


### Anatomy of an HTML document

```
<!DOCTYPE html>                   - 1
<html>                            - 2
  <head>                          - 3
    <meta charset="utf-8">        - 4
    <title>My test page</title>   - 5
  </head>
  <body>                          - 6
    <p>This is my page</p>
  </body>
</html>
```

1- 웹 문서의 버젼 : HTML5

2- HTML 문서의 가장 바깥쪽 요소

3- 웹 문서의 설명하는 정보가 담기는 영역 요소(실콘텐츠 X)

4- 웹 문서의 정보 표시 태그

5- 웹 문서의 제목을 표시하는 요소

6- 웹 문서의 콘텐츠 요소들이 담기는 영역 요소

### HTML 페이지에서 표시하는 콘텐츠

> 텍스트 콘텐츠
> 
> 멀티미디어 콘텐츠(임베디드 콘텐츠)
> 
> > 이미지
> > 
> > 비디오
> > 
> > 오디오



### HTML Fundamental Elements


#### header tag(제목 태그)

> h(Heading)
>
> h1 ~ h6
> 
> 제목 기준 분류를 표시
> 
> h1이 가장 큰 제목

```
<h1>Head 1</h1>
<h2>Head 2</h2>
<h3>Head 3</h3>
<h4>Head 4</h4>
<h5>Head 5</h5>
<h6>Head 6</h6>
```


#### paragraph tag(단락 태그)

> p(Paragraph): 단락
>
> 단락을 표시
```
<p>콘텐츠</p>
```
> > 단락과 단락사이를 구분하는 수평선
```
<hr>              - Horizontal Rule
```
> > 단락을 구분하지 않고 줄 바꿈
```
<br>              - Break
```


#### list tag(리스트 태그)

> li(List Item): 목록 항목
> 
> ol(Ordered List): 순서가 있는 리스트
> 
> ul(Unordered List): 순서가 없는 리스트
```
<ul>
  <li>HTML</li>
  <li>CSS</li>
</ul>

<ol>
  <li>HTML</li>
  <li>CSS</li>
</ol>
```
> 포함관계(nested)로 구성된 목록
> 
> 코딩 할때 밖에서 안쪽 방향 순서로!
> 
> > - html
> > 
> >   - html4
> >   
> >   - html5
> >   
> > - css
> > 
> >   - css2
> >   
> >   - css3
```
<ul>
  <li>
  HTML
    <ul>
      <li>HTML4</li>
      <li>HTML5</li>
    </ul>
  </li>
  <li>
  CSS
    <ul>
      <li>CSS2</li>
      <li>CSS3</li>
    </ul>
  </li>
</ul>
```

> dl(Description List): 설명 목록

```
<dl>
  <dt>HTML</dt>              - (dt: Description Title)
  <dd>표준 마크업 언어</dd>   - (dd: Description Data)
</dl>

```
> ***
> 
> * advanced text formatting
> 
>   - 있다는 것만 알기
>   
>   - 모질라 [link](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting)
>   
> ***
> 


#### Hyperlink

> url(Uniform Resource Location): 웹에서 사용하는 주소(영문)
> 
> > IP(Internet Protocol) Addresss: 숫자로 된 주소
> > 
> > 도메인 주소 ex)www.naver.com
> > 
> Hyperlink: url을 사용하여 다른 페이지로 연결
> 
> a(anchor): hyperlink. 해당 url로 닻을 놓음
> 
> 속성(attribute): href(Hypertext Reference)와 함께 사용해야한다. 연결되는 웹 문서의 url
```
<a href="http://www.naver.com">네이버로 이동</a>
```
> bookmarks
> 
> >외부페이지 연결이 아닌 같은 페이지에서 특정 위치로 이동할 수 있게 해주는 기능
> >
> >도착 지점에 id attribute를 사용하여 이름을 지정
```
<h2 id="t4"> 타이틀 4 </h2>
<a href="#t4"> 링크 </a>
```


### Table Element

> 기본 사용 태그: table, thead, tbody, tr, th, td
> 
> 열 제목: thead(Table Head), th(table heading)
> 
> 표 내용: tbodya(Table Body), td(table data)
> 
> 행: tr(table row)
> 
> 테이블 생성 어플리케이션 [link](https://www.tablesgenerator.com/)


### Image Element

> tag: img
> 
> Attribute
> 
> > src(source): 이미지 위치, 파일명
> > 
> > alt(alternate): 대체 텍스트(스크린 리더를 위해, 이미지 로딩 실패시 대체 수단으로)

```
<img src="image.jpg" alt="대체 텍스트">
```


### Video Element

> 비디오 및 오디오 콘텐츠는 용량이 크기 때문에 서버에 저장을 해서 콘텐츠를 제공하면 많은 트래픽이 발생할 수 있음.
> 
> 트레픽 과부하를 해결하기 위해서 유튜브 서비스를 사용하기도 함
> 
> Attribute
> 
> > controls: 컨트롤 버튼 표시
> > 
> > autoplay: 자동재생(*muted와 같이 사용해야함)
> > 
> > muted: 음소거
> > 
> > loop: 반복 재생

```
<video autoplay muted loop>
  <source src ="url주소" type="video/mp4">
</video>
```


### Youtube

> 비디오 콘텐츠 제공시 서버의 트레픽 과부하를 해결할 수 있는 방법중의 하나
> 
> tip! 올릴때 일부 공개로 하면 페이지 방문자만 보기 가능. 유튜브 검색에 걸리지 않음
> 
> 유튜브 매개변수 [link](https://developers.google.com/youtube/player_parameters?hl=ko)
> 
> > controls: 1, 0
> > 
> > autoplay: 1, 0
> > 
> > mute: 1, 0
> > 
> > loop: 1, 0
> > 
> > 유의: src="" 내부에 넣어야 하며 autoplay와 mute / loop와 playlist는 같이 써야 활용 가능하다.
```
<iframe id="iframe1" src="https://www.youtube.com/embed/유튜브 동영상 id?controls=0&amp;showinfo=0&amp;autoplay=1&amp;mute=1&amp;loop=1&amp;playlist=유튜브 동영상 id" frameborder="0" allowfullscreen "></iframe>
```


> 텍스트는 HTML 문서에 직접 입력되는 콘텐츠
> 
> 이미지와 동영상, 오디오 콘텐츠는 외부에서 만들어지는 콘텐츠
> 
> 이미지, 동영상, 오디오는 직접 입력하는 것이 아니고 외부 파일을 삽입하는 형태. => 임베드(embed) 콘텐츠


### form 요소

> 웹페이지에서 사용자 입력을 받을 사용하는 요소

```
<input type="text"> : 일반 텍스트
<input type="password"> : 비밀번호

<input type="button" value="확인">
<button type="button">확인</button>

```

## HTML Content Model


> 카테고리 [link](https://codepen.io/MinieGu/pen/jOBJjgx)

### 시멘틱 요소

> 비 의미적 요소
> 
> > Container Element(단순 영역 구분 요소)
> >
> > > div(Division/Divide):
> > 
> > > span:
> 
> 의미요소
>
> > HTML5 이후로 구조를 표시하는 의미적 요소로 변경됨
>
> > 
```
  <article> <aside> <details> <figcaption> <figure> <footer> <header> <main> <mark> <nav> <section> <summary> <time>
```
> > aside: 부차적인
> >  
> > article: 독립적인 요소(기사)
> > 
> > section: 문서의 섹션(영역)
> >  
> > article 과 section: 어디가 어디로 포함 관계가 되는지 상관 없음. 개발, 기획 단계에서 규칙을 정하면 됨.
> > 
> > * 코딩 컨벤션 / 스타일 가이드
> >  
> > figcaption(이미지 캡션) / figure(이미지): 다이어그램, 이미지를 감싸주는 영역
> > 
> > main: 헤더, 네비, 푸터를 제외한 영역


## 구조

*참고: 원페이지 [link](https://onepagelove.com/)

> GNB(Global Navigation Bar): 원뎁스 메뉴(1depth menu)
> 
> LNB(Local Navigation Bar): 원뎁스 안의 로컬 페이지내의 메뉴
> 
> UTIL MENU(Utility Menu): 로그인등의 기능메뉴
> 
> 구조는 의미적 요소와 디자인 요소를 동시에 고려해야 한다

*프리 템플릿 사이트: freebiesbug [link](https://freebiesbug.com/psd-freebies/website-template/)

*온라인 포토샵 편집 사이트: photpea [link](https://www.photopea.com/)


### Block, Inline

> 모든 element는 각각의 고유 영역을 가지고 있음
> 
> block element, Inline Element 구분은 이들 영역의 화면 표시 방식에 따른 구분
> 
> > block element는 줄 바꿈이 되어 표시된다. -block element 영역의 가로 너비가 부모요소에 100% 채워짐
> > (** 포함하는 요소: 부모요소, 포함되는 요소: 자식요소)
> > 
> > block element에는 위, 아래 여백을 적용할 수 있음
> > 
> > inline element는 같은 줄에 나란히 표시 -inline element 영역의 가로 너비가 콘텐츠 크기만큼만 정해짐
> > 
> > inline elment는 위, 아래 여백을 적용할 수 없음


### Parent Element(부모요소), Child Element(자식요소)

> 포함 관계에서 포함하는 요소가 부모요소, 보함되는 요소가 자식요소
> 
> 직계 포함 관계에서만 부모요소 자식요소라 이야기 함
> 
> 직계가 아닌 포함관계에서는 조상요소(Ancestor Elements), 자손요소(Descendant Element) 라고 함



## CSS


### 기본 개념

> 선택자는 스타일을 지정할 HTML요소를 가리킵니다.
> 
> 선언 블록에는 세미콜론으로 구분 된 하나 이상의 선언이 포함됩니다.
> 
> 여러 CSS 선언은 세미 콜론으로 구분하고 선언 블록은 중괄호로 묶습니다.


### 작성 방법

> External CSS: 파일을 분리하는 방식
> 
> Internal CSS: 같은HTML 문서내에 head 태그 영역에 style 태그를 사용하여 입력
> 
> Inline CSS: 시작태그에 style attribute를 사용해서 입력=> javascript에서 CSS를 제어할때 사용


### naming할 때 표기 방식

> id/class naming, 변수/함수/클래스 naming, 파일/폴더 naming
> 
> 표기 방식을 사용하는 이유
> 
> > naming 할 때 두 단어 이상으로 구성되는 경우 단어와 단어 사이를 구분하기 위해 사용
> > 
> > 단어의 시작부분에 첫글자를 대문자로 변경하거나 특수기호를 사용
> > 
> 표기방식 종류
> 
> > snake case: gnb_depht1 => 파일/폴더
> > 
> > kebab case: gnb-depth1 => id/class
> > 
> > camel case: gnbDepth1 => javascript의 변수/함수
> > 
> > pascal case: GnbDepth1 => javascript의 클래스


### OOCSS(Object Oriented CSS)

> HTML Element를 대상화 시키는 과정에서 Element 하나하나를 모두 객체화 시키는 이론
>
> HTML Element 모두 각각 id, class attribute를 사용해서 이름을 지정해줌 


### 구문(Syntax)

```
h1{color:blue; font-size:12px;}
```
> [Selector] [Declaration Block]
> Selector {[declaration]; [declaration];}
> Selector { [Property]: [Value]; [Property]: [Value];}
> 
> 선택자(Selector):
> 
> 선언(Declaration):


### id, class

> HTML element에 특정 이름을 사용할 때 id, class attribute를 사용해서 이름을 붙여줄수 있음.
> 
> id는 동일한 이름이 사용된 HTML element가 여러개이면 논리적 오류가 발생
> 
> id는 HTML 문서내에서 고유해야함
> 
> class는 동일한 이름이 여러개의 element에 사용되어서 공통 디자인 요소나 공통 기능을 적용할 수 있음.
> 
> id는 주로 서버에서 불러오는 데이터를 표시하는 위치에 고유하게 사용 => 백엔드 개발에서 주로 사용
> 
> class는 주로 css 스타일 적용, javascript인터랙션 적용할 때 사용 => 프론트엔드 개발에서 주로 사용
> 
> id는 하나의 HTML Element에 대해서 하나의 이름만 존재, HTML 문서내에서 고유해야 함.
> 
> class는 하나의 HTML Element에 대해서 여러개의 이름을 지정할 수 있고, HTML 문서내에서 공통 사용 가능함.


* 주석 단축키: cmd+/ (되돌리기도 마찬가지)


### web color

> color mode
>
> 가산혼합(빛의혼합) : RGB 컬러모드
>
> 표현할 수 있는 색의 개수
>
> > 1byte = 8bit = 256개(0~255)
> >
> > RGB => 3byte => 24bit 트루컬러 : 16777216가지 색
>
> 색 표현 코드값
>
> > 16진수(hex code) : #AABA01
> > 
> > 10진수 : (255, 255, 255)
>
> CSS 사용법
> 
```
color:#2abd51;
color:rgb(42, 189, 81);
color:rgba(42, 189, 81, 0.5);
```
>
> 투명도를 의미하는 용어
> 
> > transparent : 투명한
> > 
> > alpha : 추가 채널
> > 
> > opacity : 불투명도


### text CSS

> color: color name
> 
> text-align: center / left / right / justify
> 
> vertical-align: baseline / text-top / text-bottom / sub / super
> 
> test-decoration: overline / line-through / underline / none
> 
> text-transform: uppercase / lowercase / capitalize
> 
> text-indent(들여쓰기): px
> 
> letter-spacing(자간): px 
> 
> line-height(행간): px / 배수(0.8 1.6 등등)
> 
> word-spacing:
> 
> white-space: nowarp
> 
> text-shadow: 가로 세로 색상 블러


### font CSS

> font-family: "Times New Roman", Times, serif;
> 
> > 순서대로 대체 폰트를 찾음
> > 
> > sans-serif, serif, monospace, cursive, fantasy 5개의 기본 폰트는 font-family사용시 종류에 맞게 항상 끝에 기본으로 사용됨
> > 
> 웹사이트에서 사용하는 폰트는 웹폰트(서버에 폰트 파일을 저장해서 사용)로 하용하는 데, 업로드된 파일을 직접 사용하는 경우, 웹폰트 서비스를 사용하는 경우 2가지가 있음
> 
> > 대표적인 웹폰트 서비스: 구글 폰트, 눈누
> 
> font-size:
> 
> font-style: italic
> 
> font-weight: bold / 500
> 
> > 폰트 굵기가 다양한 경우 숫자로 굵기를 표현


### Box Model

> 구성요소
> 
> > width/height: 너비/높이
> > 
> > padding: 안쪽 여백
> > 
> > border: 테두리
> > 
> > margin: 바깥 여백


### width/height

> width: 너비/가로길이
> 
> height: 높이/세로길이
> 
> auto: 기본값
> 
> > block: 너비: 부모요소를 기준으로 채워짐 / 높이: 콘텐츠(자식요소)를 기준으로 맞춰짐
> > 
> > inline: 너비/높이가 콘텐츠(자식요소)에 맞춰짐


### padding

>안쪽 여백
>
>padding-top:
>
>padding-right:
>
>padding-bottom:
>
>padding-left:
>
>padding: 10px 20px 30px 40px(top right bottom left)
>
>padding: 10px 20px 30px(top right/left bottom)
>
>padding: 10px 20px (top/bottom right/left)
>
>padding: 10px (top/right/bottom/left)


### margin

>바깥쪽 여백
>
>padding과 사용법이 같음
>
>margin collapse
>
> > 위 요소의 margin-bottom과 아래 요소에 margin-top이 중첩될경우 둘중 숫자가 큰 마진만 적용된다.
> > 
> > 위아래 양쪽으로 margin을 적용하는 것보다 한쪽을 기준으로 적용하는 것이 더 좋음


### border

> border: 1px solid red;(=> 4방향 모두 적용)
> 
> border-top: 1px solid red;
> 
> border-right: 1px solid red;
> 
> border-bottom: 1px solid red;
> 
> border-left: 1px solid red;

### 가로배치

> ※ inline 요소는 박스 모델이 제대로 적용되지 않기 때문에 레이아웃 구성 요소로 사용하기 어렵다. ※ block 요소를 레이아웃 구성 요소로 사용함 => 세로 배치는 기본 구성
>
> 가로 배치 기법
>
> > float
> >
> > flex
> >
> > grid

#### float

> left, right 값을 사용해서 가로 배치 left, right는 부모요소를 기준으로 방향성을 표현
> 
> 일반적으로 왼쪽을 기준으로 순서대로 배치할 때 left만 사용해서 배치
> 
> float은 박스가 띄워지는 현상이 있기 때문에 인접해 있는 박스의 배치가 깨질수 있음
>
> > float 박스를 부모요소로 감싸서 인접해 있는 박스와 float 박스를 감싸고 있는 부모요소와의 관계로 만들어줌
> > 
> > float 박스를 감싸는 부모요소는 높이가 0이 될수 있기 때문에 그것을 clear 할수 있는 비어있는 자식요소를 넣어줌
```
HTML
<div class="float-container>
  <div class="float-box>text</div>
  <div class="float-box>text</div>
  <div class="clearfix"></div>
</div>

CSS
.float-box{
  float:left;
}
.clearfix{
  clear:both;
}
```


### display 속성

> 요소의 기본속성을 변형하지 않고 화면에 표시되는 속성을 변형 block, inline, inline-block

```
div{
  display:inline;
}
=> 원래 block 속성인 div를 inline 속성으로 화면에 표시
```

> inline-block: inline의 속성(한줄에 나란히 표시)과 block의 속성(박스모델 적용)을 모두 표시
>
> none: 주로 자바스크립트와 함께 활용되며 숨기고 나타낼때 사용


### 이미지 표현 방법

> 콘텐츠로 표현
> 
> > img tag
>  
> 디자인 요소로 표현
> 
> > backgroun-image
> 
> ID(Image Replacement: 이미지 대체) 기법
> 
> > HTML Element에는 텍스트로 표시
> > 
> > 화면(브라우저)에 표시할때는 이미지로 표현
```
html
  <a href="" class="facebook">facebook</a>
  
css
  .facebook{
    display: block;
    text-indent: -99999px;
    width: 8px;
    height: 14px;
    background: url(url주소);
  }
```


### background

> background-color
> 
> background-image
> 
> background-repeat
> 
> > repeat-x(가로만 반복) / repeat-y(세로만 반복) / no-repeat(반복없음)
> > 
> bcakground-position
> 
> > left, center, right / top, center, bottom : 키워드
> > 
> > px 좌표 표시
```
div{
  background-position:left top;(앞:가로방향/뒤:세로방향)
  background-position:100px 200px;(앞:가로방향/뒤:세로방향)
}
```
> background-attachment
> 
> > 배경 이미지를 고정
> 
> background 축약 표현
```
background:#fff;
background:url(image.jpg);
```


### position

> 엘리먼트들의 위치를 지정
> 
> > relative: 인라인에서 위치를 차지하며 그 위치에서 지정한 간격을 띄워 나타남.
> > 
> > absolute: 화면 전체를 두고 지정한 위치에 나타남
```
html
  <div class="absolute">This div element has position: absolute; 123</div>
  <div class="relative">This div element has position: relative;
    <div class="absolute">This div element has position: absolute; 456</div>
  </div>

css
  div.relative {
    position: relative;
    width: 400px;
    border: 3px solid #73AD21;
    top: 20px;
    left: 50px;
  } 

  div.absolute {
    position: absolute;
    top: 0px;
    left: 0;
    width: 200px;
    height: 100px;
    border: 3px solid #73AD21;
    background: rgba(0, 128, 0, 0.3);
  }

```


### Pseudo(수도 클래스)

> class
> 
> > 문법(Syntax): ':' 를 사용
> > 
```
a:link {
  color: #FF0000;
}

/* visited link */
a:visited {
  color: #00FF00;
}

/* mouse over link */
a:hover {
  color: #FF00FF;
}

/* selected link */
a:active {
  color: #0000FF;
}

/* tooltip */
p {
  display: none;
  background-color: yellow;
  padding: 20px;
}

div:hover p {
  display: block;
}

```
> > 종류
> > 
> > > :first-child - 첫 자식요소에만 적용
> > > 
> > > :first-of-type - 첫 요소에만 적용
> > > 
> > > ::nth-of-type(n) - n에 입력한 순번에만 적용
>
> 
> element
> 
> > 문법(Syntax): '::' 를 사용
> > 
```
h1::after {
  content: url(smiley.gif);
}
```
> > 종류
> > 
> > > ::after - 앞에 적용
> > > 
> > > ::before - 뒤에 적용
> > > 
> > > ::first-letter - 첫 글자에 적용
> > > 
> > > ::firet-line - 첫 줄에 적용
> > > 
> > > ::marker - ul, li 등 리스트에 적용 
> > > 
> > > ::selection - 드래그시 적용


### Flexbox

> Parent Element(Container)
> 
> > Properties
> > 
> > > flex-direction: column; column-reverse; row; row-reverse;
> > > 
> > > flex-wrap: wrap; nowrap; wrap-reverse;
> > > 
> > > flex-flow: row wrap; 
> > > 
> > > justify-content: 넓이 - center;붙어서 가운데 / flex-start;부모의 왼쪽 끝 / flex-end;부모의 오른쪽 끝 / space-around;양쪽으로 패딩 / space-between;간격에 패딩
> > > 
> > > align-items: 높이 - center; flex-start; flex-end; stretch; baseline;
> > > 
> > > align-content: space-between; space-around; stretch; center; flex-start; flex-end;
> > > 
> > > perfect centering
```
.flex-container {
  display: flex;
  height: 300px;
  justify-content: center;
  align-items: center;
}
```
> * 참고
> 
> float right: 순서도 오른쪽 부터
> 
> flex-end: 순서 그대로 부모요소의 오른쪽 끝에 붙음
>
> Child Elements (Items)
> 
> > Properties
> > 
> > > order: 숫자로 순서 값
> > > 
> > > flex-grow: 도합 10 숫자로 비율대로 늘어남
> > > 
> > > flex-shrink: 0을 입력하면 그 자식만 줄어들지 않음
> > > 
> > > flex-basis: 해당 픽셀 값까지만 늘어나고 더이상 늘지 않음
> > > 
> > > flex: not growable (0), not shrinkable (0), 해당 픽셀값
```
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="flex: 0 0 200px">3</div>
  <div>4</div>
</div>
```
> > > 
> > > align-self: flex-start/flex-end/center
> > > 
>  반응형 예시
> >
```
.flex-container {
  display: flex;
  flex-direction: row;
}

/* Responsive layout - makes a one column layout instead of a two-column layout */
@media (max-width: 800px) {
  .flex-container {
    flex-direction: column;
  }
}

///

.flex-container {
  display: flex;
  flex-wrap: wrap;
}

.flex-item-left {
  flex: 50%;
}

.flex-item-right {
  flex: 50%;
}

/* Responsive layout - makes a one column layout instead of a two-column layout */
@media (max-width: 800px) {
  .flex-item-right, .flex-item-left {
    flex: 100%;
  }
}

```
> 
> Flex Gallery [link](https://www.w3schools.com/css/tryit.asp?filename=trycss3_flexbox_image_gallery)



## 반응형 웹


### OSMU(One Source Multi Use)

> > One Source: HTML
> > 
> > Multi Use: CSS, Javascript


### 변경점(break point)

> > 기준 해상도를 설정하고 범위 구간으로 설정
> 
> @media
```
@media 디바이스 and (구간 해상도){
  디바이스 스타일
}

@media screen and (max-width:300px){}
@media screen and (min-width:300px){}

// 독립된 구간으로 설정
@media screen and (min-width:360px) and (max-width:700px){
  /* 스마트 폰 CSS */
}
@media screen and (min-width:701px) and (max-width:1920px){
  /* PC CSS */
}

// 포함된 구간을 설정 <- 웹/모바일 css를 그대로 활용할 수 있음으로 선호 

/* PC CSS */

@media screen and (max-width:700px){
  /* 스마트폰 CSS */
}
```

### 뷰포트

> 뷰포트를 메타 테그에 포함시켜야 한다.
```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```



> 본인 해상도 및 뷰포트 확인 사이트 [link](mydevice.io)
> 



## JavaScript


### DOM

### Event
> 상황 변화에 따라 발생되는 신호
>
> Event 발생
> 
> > Event 감지 : 종류, 상황
> > 
> > 감지한 Event에 맞는 기능,동작 실행
> > 
> Event 종류
> 
> > Mouse Event : click, mouse over, mouse out
> > 
> > Keyboard Event : Key 입력
> > 
> Event 감지 함수
> 
> > javascript : addEventListener()
> > 
> > jquery : on()

함수 : 익명함수 정리



*강사님 페이지

코드펜 [link](https://codepen.io/ministori-yonsei)

깃 [link](https://github.com/ministori-yonsei/green_weekend_06)

> # to be continued...
