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
<hr> -* Horizontal Rule
```
> > 단락을 구분하지 않고 줄 바꿈
```
<br> -* Break
```
