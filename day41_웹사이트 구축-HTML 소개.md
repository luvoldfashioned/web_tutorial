
### 인터넷의 작동
##### [[Internet]]
긴 전선으로 서로 다른 컴퓨터를 연결해 준 것
##### [[Server]]
365일 온라인, 웹사이트에 접속할 때마다 요청하는 데이터와 파일을 모두 가져다 줄 준비가 되어 있어야 함, 365/24 운영되는 거대한 도서관
##### [[Client]]
사용자가 인터넷에 접속해서 켜게 되는 컴퓨터

#### 인터넷 동작 원리
1. 컴퓨터에서 google.com 접속 시도
2. 브라우저에서 Internet Service Provider([[ISP]]: 인터넷 서비스 제공업체: 인터넷 접속을 하기 위해 비용을 지불하는 회사)에 메시지를 보냄
3. [[DNS]](Domain name system: 성능이 좋은 전화번호부, 서버에서 데이터베이스를 들여다보고 접속하려고 하는 웹사이트의 정확한 [[IP address]](컴퓨터에 달린 우편 주소)가 무엇인지 찾음) 서버에 메시지를 전달
4. [[DNS]] 서버가 [[IP address]]를 찾으면 브라우저로 다시 알려줌
5. [[ISP]]를 통해 해당 주소에 직접 요청
6. 요청은 Internet Backbone이라는 곳을 통해 구글 서버로 전달
   (* submarinecablemap.com: 대륙 간 해저 케이블 지도)
7. Server는 모든 파일을 Internet Backbone을 통해 다시 Client로 보내줌

### 웹사이트의 작동
#### [[Browser]]
웹사이트의 [[IP address]]를 찾아서 데이터를 받아 웹사이트를 보여주는 역할


서버에서 받은 데이트는 보통 세 가지 유형의 파일로 구성
## [[HTML]](</>) 
HyperText ==Markup== Language
웹사이트의 구조를 책임 짐, 웹사이트가 집이라면 HTML은 벽을 만드는 건축업자, 집의 구조를 설정, 따라서 이미지, 버튼, 텍스트 박스 등을 추가 가능

태그는 <로 시작하여 >로 끝남, 가운데는 사용하려는 요소의 유형 또는 태그 유형이 들어감
시작 태그를 써주면 종료도 해줘야 함

```html
<hr size="3">   # <hr>: HTML element / size='3': HTML Attribute
<h1>THE ADVENTURES OF <br>SHERLOCK HOLMES</h1>
<br>       # 줄바꿈(Self-closing tag)
<h3>by</h3> # heading 태그의 숫자가 올라갈수록 크기가 작아짐(h6까지)

<h2>SIR ARTHUR CONAN DOYLE<h2>
<hr size="3">
```

#### [[Self-closing tag]]
자체 종료 태그
`<br>` 등 종료 태그가 필요없는 태그

##### HTML element
br hr 등 사용하는 것

##### HTML Attribute
브라우저에 추가 정보를 주어 해당 HTML element에 변경 사항을 지정

![[Pasted image 20231227160538.png]]
![[Pasted image 20231227160503.png]]
![[Pasted image 20231227160441.png]]
<!--텍스트 스니펫이 meta tag 에서 본 것과 같음-->

#### HTML 주석
`<!--  a;lwkjefhn;alwkefn;lk-->`

### [[Boilerplate code]]
상용구 코드
- 수정하지 않거나 최소한의 수정만을 거쳐 여러 곳에 필수적으로 사용되는 코드
- 일반적으로 재사용할 수 있는 공동 템플릿
- 코드 템플릿과 비슷해 다른 프로젝트에서 재사용 가능

- ![[Pasted image 20231227153122.png]]
#### [[UTF-8]]
[[HTML]]5 표준 인코딩
국제 기호와 유니코드 문자 집합에 포함된 모든 단일 기호가 포함되어 있기 때문

#### [[i 태그 VS em 태그]]
`<i>` :  단순히 텍스트를 기울임체로 바꿈
`<em>` : (emphasis)강조 태그, 브라우저에 해당 태그로 둘러싸인 말들이 강조되어야 한다고 알려줌.

강조를 하려면 i보다는 em을 쓰는 습관들이기 -> 단순히 스타일에 관한 것만이 아님
<strong>HTML 코드를 작성할 땐 텍스트의 모양이나 표시 방식보다 텍스트 구조화에 신경 써야 함</strong>


## [[CSS]]({..})
웹사이트의 스타일링, 집을 짓는다면 페인트와 장식을 해주는 기술자
버튼의 색, 글꼴 등



## [[JS(Java Script)]](</>)
웹사이트가 실제로 작업이나 행동을 하게 함, 집을 짓는다면 전선을 끌어와서 전구가 켜지게 하거나 배관을 설치해 변기가 내려가게 하는 역할, 기능성이 생김







------------------------------------------
##### [[웹 개발 안내서]]
1. MDN(Mozilla Developer Network)
2. w3schools
3. devdocs.io