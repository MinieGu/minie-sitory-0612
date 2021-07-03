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
> > * 참고- CSS는 Property
> 
> HTML 요소의 부가 정보
> 
> 문법
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
> 멀티미디어 콘텐츠(임베디드 콘텐츠)
> > 이미지
> > 비디오
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
> 코딩 할때 밖에서 안쪽 방향 순서로!
> > - html
> >   - html4
> >   - html5
> > - css
> >   - css2
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
> * advanced text formatting
>   - 있다는 것만 알기
>   - 모질라 [link](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting)
> ***


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

# HW
> dbut.com 에 들어가서 맘에 드는 사이트, 페이지 선정. 영역 구분 분석 해보기

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


##CSS

### 기본 개념

> 선택자는 스타일을 지정할 HTML요소를 가리킵니다.
> 
> 선언 블록에는 세미콜론으로 구분 된 하나 이상의 선언이 포함됩니다.
> 
> 여러 CSS 선언은 세미 콜론으로 구분하고 선언 블록은 중괄호로 묶습니다.

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

*강사님 페이지

코드펜 [link](https://codepen.io/ministori-yonsei)

깃 [link](https://github.com/ministori-yonsei/green_weekend_06)

> # to be continued...
