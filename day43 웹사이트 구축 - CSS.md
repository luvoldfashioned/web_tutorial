# [[CSS]]
Cascading Style Sheets
캐스케이딩 스타일 시트
[[HTML]]  XML 등 마크업 언어를 꾸며줌

##### 왜 필요한가
[[HTML]]만 사용하여 레이아웃을 조작하다 보면 table을 사용해야하는데,
코드가 너무 장황해짐 -> 작성해야 하는 코드의 양이 많아지고 구문 오류가 발생하기 매우 쉬움

## [[Inline CSS]]
인라인 CSS
`<body stlye="background-color: blue;">`

## [[Internal CSS]]
내부 CSS
어느 한 페이지에 있는 특정 HTML 요소의 모든 인스턴스에 스타일을 구현
헤드 섹션에서 스타일 태그 추가
```html
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Yeom's Personal Site</title>

    <style>
      body {
        background-color: #dcf2f1;
      }
      hr {
        border-color: #365486;
        border-style: none;
        border-top-style: dotted;
        border-width: 6px;
        width: 10%;
      }
    </style>

  </head>
```

### [[브라우저 기본 CSS]]
이미 브라우저에 의해 적용된 default CSS가 있다
https://www.w3schools.com/cssref/css_default_values.php
![[Pasted image 20240102162633.png]]
![[Pasted image 20240102162545.png]]

### CSS 학습에서 가장 중요한 개념 중 하나
#### ==웹페이지에 존재하는 거의 모든 것은 상자(box)==
```css
  hr {
	background-color: #11235A;
	border-style: none;
  }
```
![[Pasted image 20240102163321.png]]

```css
  hr {
	background-color: #11235A;
	border-style: none;
	height: 2px;
  }
```
![[Pasted image 20240102163634.png]]


## [[external CSS]]
외부 CSS
한 곳에서 CSS 스타일을 변경하여 웹사이트 전반에 걸쳐 변경 사항을 적용하는 방법

1. css 파일 생성
![[Pasted image 20240102173735.png]]
 2. 스타일 작성![[Pasted image 20240102173915.png]]
 3. 헤더에 링크![[Pasted image 20240102174114.png]]

## [[CSS Debugging]]
chrome에서 개발자 도구(DevTools) 활용
![[Pasted image 20240102181531.png]]


### [[동일한 요소속성에 대한 CSS 규칙 우선순위]]
([[Inline CSS]])
![[Pasted image 20240102182846.png]]
([[external CSS]])
![[Pasted image 20240102182901.png]]
(결과)
![[Pasted image 20240102183115.png]]
![[Pasted image 20240102183225.png]]

[[Inline CSS]] ➡️ [[Internal CSS]] ➡️ [[external CSS]]


## [[CSS Syntax]]

##### `selector {property : value;}`

[[selector]](선택자): 기본적으로 '대상'을 의미(Who?: 어떤 대상 스타일을 바꿀 것인가)
property(속성): 'What?' h1의 무엇을 바꿀 것인가(배경색, 텍스트 색상 등)
value(값): 'How?' h1의 배경색을 어떻게 바꿀 것인가

### [[Class Selector]]
##### 클래스 속성을 사용하여 HTML 요소 구분
```html
  <img class="bacon" src="https://em-content.zobj.net/source/apple/354/bacon_1f953.png" alt="bacon_img">
  <img class="broccoli" src="https://em-content.zobj.net/source/apple/354/broccoli_1f966.png" alt="broccoli_img"
```

![[Pasted image 20240103133626.png]]
클래스 앞에 . 붙이기

### [[id Selector]]
![[Pasted image 20240103134228.png]]
![[Pasted image 20240103134208.png]]
![[Pasted image 20240103134253.png]]
tag selector보다 [[id Selector]]와 [[Class Selector]] 가 더 구체적이기 때문에 더 우선순위를 가짐

##### [[id Selector VS Class Selector]]
- 유사점: 스타일을 지정하려는 [[HTML]] 요소를 식별하는데 사용

- Id는 특정 페이지에서 단 하나만의 요소를 지정하는데 사용(고유해야 함)
- Class는 유사한 동작 또는 스타일을 갖는 모든 관련 요소들을 그룹화 가능

- 특정 id는 해당 페이지에서 한 번만 사용할 수 있다

- HTML 요소는 둘 이상의 Class를 가질 수 있지만 id는 특정 요소에 둘 이상을 사용할 수 없다
(class)
![[Pasted image 20240103140842.png]]
![[Pasted image 20240103140901.png]]
![[Pasted image 20240103141022.png]]

(id)
![[Pasted image 20240103141211.png]]
![[Pasted image 20240103141201.png]]

### [[pseudo-class]]
의사 클래스
![[Pasted image 20240103141725.png]]
(콜론을 달고있음)

HTML 요소의 다른 상태를 명시하기 위해 사용
ex) 텍스트나 이미지 위로 마우스를 가져다 놓은 상태와 그렇지 않은 상태에 따라 CSS가 변함
![[Pasted image 20240103142018.png]]
![[Pasted image 20240103142036.png]]
(마우스가 밖에 있을 때)
![[Pasted image 20240103142044.png]]
(마우스가 베이컨 이미지 위에 있을 때)


## [[CSS Display property]]
디스플레이 속성
#### [[block display(display property)]]
블록 요소는 기본적으로 어떤 웹 페이지의 화면 폭 전체를 차지함
따라서 다른 모든 요소가 그것의 양옆에 있지 못하도록 차단함
![[Pasted image 20240104143408.png]]

ex)블록 요소의 예
- Paragraphs(`<p>`)
- Headers(`<h1>`through`<h6>`)
- Divisions(`<div>`)
- Lists and list items(`<ol>`, `<ul>`, and `<li>`)
- Forms(`<form>`)

#### [[Inline display(display property)]]
Inline display element
heading이나 paragraph같은 [[block display]] 요소와는 다르게 높이와 폭 면에서 필요한 만큼의 공백만 차지함
![[Pasted image 20240104161630.png]]

ex)인라인 요소의 예
- Spans(`<span>`)
- Images(`<img>`)
- Anchors(`<a>`)
인라인 요소의 문제: 폭을 변경하지 못함

#### [[display property change]]
- paragraph를 inline display element로 바꾸기
```css
p {
  background-color: red;
  width: 100px;
  display: inline;
}
span {
  background-color: blue;
  width: 100px;
}
```
![[Pasted image 20240105132255.png]]

- 같은 라인을 점유할 수 있게 하면서 폭을 설정하는 방법
### [[Inline-Block(display property)]]
같은 라인 점유([[Inline display]]) + 폭 설정 가능([[block display]])
```css
p {
  background-color: red;
  width: 100px;
  display: inline-block;
}
```
![[Pasted image 20240105132628.png]]

### [[None(Display property)]]
```css
.second-p {
  display: none;
}
```
![[Pasted image 20240105134614.png]]

웹페이지에서 뭔가를 감추는 방법
1. display: none
2. visibility: hidden


### [[html요소 렌더링 규칙]]
#### 1. Content is Everything(콘텐츠가 제일이다)

[[Inline display]] element는 딱 콘텐츠만큼의 폭과 높이만을 차지
- 긴 단어가 포함된 span이 있으면 폭이 커짐
- 짧은 단어가 포함된 span이 있으면 폭이 작아짐
[[block display]] element의 높이는 콘텐츠에 의해 결정됨

따라서 콘텐츠는 ==element가 어떻게 표시되고 높이와 폭이 어떻게 될 지 결정하는 중요한 것==으로, [[CSS]]와는 무관하다

#### 2. Order Comes From Code(요소들의 순서는 html 코드를 따른다)
```html
<h1></h1>
<p></p>
<p></p>
<p></p>
<img>
```
기본적인 배치 순서는 코드가 결정한다

#### 3. Children Sit On Parents(하위 개체가 상위 개최 위에 놓인다)
![[Pasted image 20240105140355.png]]
```html
<div>
	<h1>a programmer</h1>
</div>
```
빨간색으로 된 div위에 놓인 h1
(*h1은 보는사람에게 더 가깝고 화면으로부터 멀다*)
*일종의  z축 개념 등장*

기본적으로 하위 개체는 모든 html 요소는 상위 요소의 위에 놓여있게 됨

![[Pasted image 20240105140725.png]]
```html
<div>
	<h1>a <span>pro</span>grammer</h1>
</div>
```
div➡️h1➡️span


## [[CSS Positioning]]
### Static(CSS Position)
정적 위치
모든 [[html]] 요소는 기본적으로 static임
단지 html 규칙을 따르고 기본 html 흐름을 유지한다는 의미
- [[CSS]] 없이 html만 있을 때
- 위치 속성을 변경하지 않았을 때

### Relative(CSS postition)
상대적 위치
선택한 요소가 ==정적이었다면 있었을 위치에 대해 상대적==으로 배치

```css
.bacon {
    background-color: gold;
    position: relative;
    /*이전 위치에서 왼쪽으로부터 30픽셀 밀기*/
    left: 30px;
}
```
![[Pasted image 20240105143612.png]]
#### ==Relative positioning을 할 때 주의할 점==
 1. 상대적 위치를 가진 요소를 이동시킬 때 화면 내 어떤 것의 위치에도 영향을 미치지 않는다.
```css
.red{
  height: 100px;
  width: 100px;
  background-color: red;
  position: relative;
  top: 50px;
}
```
![[Pasted image 20240109141808.png]]
(파란 블록을 밀지않고 겹쳐짐)

 2. 좌표 속성(coordinate property)을 변경할 때, 예를 들어 top: 50px이면
	상단으로부터 50px만큼의 margin(여백)을 주는 것이다.
	(margin)
	![[Pasted image 20240105144742.png]]


### Absolute(CSS Position)
절대적 위치
==상위 개체에 대해 상대적으로 배치==

Relative 
- 그 요소가 있었어야 할 곳에 대해 상대적
- 일종의 유령 요소를 남겨서 다른 모든 것들의 위치가 똑같이 유지
Absolute 
- 상위 요소에 여백을 추가
- 실제로 요소를 문서 흐름에서 꺼내게 되고 더 이상 문서의 자연적인 흐름의 일부로 간주되지 않게 됨
```css
.red{
  height: 100px;
  width: 100px;
  background-color: red;
  position: absolute;
  left: 200px
}
```
![[Pasted image 20240109144538.png]]

##### 상위 개체가 꼭 body일 필요는 없음
상대적 레이어를 갖고 있는 가장 가까운 상위 개체일 수도 있음
```html
  <div class="container">
    <div class="red">
    </div>
  </div>
```
```css
.container {
  position: relative;
  background-color: grey;
  width:300px;  
  height:300px;
}

.red{
  height: 100px;
  width: 100px;
  background-color: red;
  position: absolute;
  left: 200px;
}
```
![[Pasted image 20240109151956.png]]

Absolute와 Relative 조합
```css
.container {
  position: relative;
  background-color: grey;
  width:300px;  
  height:300px;
}

.red{
  height: 100px;
  width: 100px;
  background-color: red;
  position: absolute;
  right:0;
}

.blue {
  height: 100px;
  width: 100px;
  background-color: blue;
  position: absolute;
  left: 100px;
  top:0;
}

.yellow{
  height: 100px;
  width: 100px;
  background-color: yellow;
  position: absolute;
  top:0;
}
```
![[Pasted image 20240109154259.png]]

### Fixed(CSS Position)
스크롤해도 웹사이트 body에 대해 상대적으로 자리가 고정됨
```css
.yellow{
  height: 100px;
  width: 100px;
  background-color: yellow;
  position: fixed;
  top:0;
}
```
![[Pasted image 20240109155025.png]]


## 요소들을 중앙에 놓는 방법(CSS)
```css
text-align: center;
```
- 이미지 같은 인라인 블록 요소 or 모든 폭을 차지하는 블록 요소가 있을 때만 작동
- 컨테이너 또는 상위 요소 안에서 사용하면 그 안에 있는 폭이 설정되지 않은 모든 것이 중앙에 배치됨
![[Pasted image 20240109155753.png]]

h1의 폭을 10%로 지정 시
```css
h1 {
    margin-top: 0;
    width: 10%;
}
```
![[Pasted image 20240109163734.png]]
(중앙에 정렬되지 않음)

#### 해결법: margin(여백)을 이용
margin: auto ➡️ 요소가 수직 또는 수평으로 중앙에 정렬
margin: 0 auto 0 auto(=0 auto(원형속기)); ➡️ 수평 중앙에 정렬
```css
h1 {
    width: 10%;
    margin: 0 auto;
}
```
![[Pasted image 20240109164544.png]]
![[Pasted image 20240109164137.png]]



## Font Design
일반적인 웹사이트 스타일링
- Serif
	- 대부분의 브라우저에서 기본값은 Times 폰트
- Sans-serif
	- 대부분의 브라우저에서 기본값은 Arial 폰
![[Pasted image 20240109173631.png]]
monospace: 텍스트 안의 모든 문자가 동일한 폭을 차지
![[Pasted image 20240109174026.png]]

#### 구체적인 폰트 지정
```css
font-family: verdana, sans-serif;
```
![[Pasted image 20240109175858.png]]


#### CSS Web Safe Fonts
##### 만약 브라우저 또는 사용자의 운영체계에 폰트가 미설치돼있다면
➡️ 시스템 내 아무 sans-serif 폰트나 기본값으로 사용됨
 
web safe fonts : 대부분의 운영체계가 정확하게 렌더링할 수 있는 폰트 계열

실제로는 100퍼센트 완벽한 웹 세이프 폰트는 없음

#### CSS Font Stack
https://www.cssfontstack.com/
폰트와 운영체계별로 그것을 설치한 사용자의 비율이 어떤지 나열
![[Pasted image 20240109183100.png]]

![[Pasted image 20240109183436.png]]
운영체제 간 사용률의 차이가 많이나는 폰트

#### CSS fallback stack
```css
   font-family: "Helvetica Neue",Helvetica,Arial,sans-serif
```
Helvetica Neue➡️Helvetica➡️Arial➡️sans-serif
구체적인 것에서 덜 구체적인 것으로, 설치 여부와는 무관하게 대략적으로 유사한 서체와 유사한 느낌을 유지

#### CSS Font embedding
1. google fonts 에서 font 추가
https://fonts.google.com/
2. 링크 복사후 html 상단에 붙여넣기
![[Pasted image 20240109190454.png]]
(만일 사용자가 해당 폰트를 설치하지 않았거나 시스템에 캐시로 저장되어 있지 않다면 브라우저가 링크 위치로 데려가 폰트를 잡게 함)


###### Lorem ipsum
콘텐츠가 아직 없을 때 텍스트 단락을 넣는 데 사용


## CSS 동적 사이즈

정적 사이즈
```css
h1 {
    font-size: 90px;
    margin-top: 0;
    font-family: 'Sacramento', cursive;
}
```
![[Pasted image 20240110123233.png]]
폰트 사이즈가 90px로 설정되어 있어 브라우저에서 기본 폰트 사이즈를 변경해도 h1의 폰트 사이즈는 변하지 않음

#### 동적 사이즈를 만드는 법
 ==16px = 100% = 1em==
- percentage
```css
h1 {
    font-size: 562.5%x;
    margin-top: 0;
    font-family: 'Sacramento', cursive;
}
```
- em(대문자 M 폭의 n배)
```css
h1 {
    font-size: 5.625em;
    margin-top: 0;
    font-family: 'Sacramento', cursive;
}
```

#### 동적 사이즈 상속
```css
body {
    margin: 0;
    text-align:center;
    font-family: 'Merriweather', serif;
    font-size:2em;
}

h1 {
    font-size: 5.625em;
    margin-top: 0;
    font-family: 'Sacramento', cursive;
}
```
![[Pasted image 20240110125020.png]]
(h1 크기가 엄청 커짐)

퍼센티지나 em을 사용 시 그 값이 상속되기 때문에
==상위 개체에서 받은 것에서 추가됨==

위의 코드는 상위개체에서 이미 2em이 적용된 상태에서 5.625가 추가 된 것

#### 해결법: CSS3의 rem(root em)
폰트 사이즈에 관한 모든 상위 설정을 무시하고 루트에 대해 상대적으로 설정

## CSS float
이미지가 텍스트의 왼쪽에 떠 있게 하거나 텍스트가 둘러싸게 할 수 있음
```css
.computer-img {
    width: 25%;
    float:left;
}
```
![[Pasted image 20240110143259.png]]

가장 널리 사용되면서도 ==남용되는== CSS 속성
특이한 경우가 아주 많음
필요한 경우에만 사용하고 포지셔닝에 사용하지 말기

## CSS Clear
제목만 이미지를 둘러싸면서 이미지의 오른쪽에 있게 하기
```css
.code-skill-description {
    clear: left;
}
```
![[Pasted image 20240110145252.png]]

floating을 방지하는 것과 비슷
기본값 거동을 하지 못하게 막기

