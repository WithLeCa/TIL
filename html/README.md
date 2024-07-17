# HTML

> #### 강의 주소
> 독학백서 기초 강의 > https://youtu.be/FV32OM3B49c?si=_2t9mLQyxIk6RTHO

### 웹 문서의 기본 구조
+ #### DOCTYPE 
    이 문서가 html문서이고 어떤 버전을 사용 하는지를 정의하는 역할로 항상 <html> 전에 선언되어야 함

+ #### html 
    html문서 전체를 감싸는 태그로 html 문법으로 작성된 웹 문서 영역

+ #### head 
    브라우저의 머리 부분 (툴바 부터 위쪽의 영역)   
    title태그를 이용해 문서의 타이틀을 작성하거나 meta태그를 사용해 문서의 설명을 작성하거나 파일 정보, 스크립트 정보 등을 작성   
    이 영역에 적힌 내용은 사용자가 직접 보는 영역이 아니라 브라우저나 검색 엔진에 전달되는 영역임

+ #### body
    브라우저 몸통 부분 (툴바 아래 본문 부분), 사용자가 직접 보게 되는 영역


### 태그와 기본 주소, 블럭, 인덱스
1. #### 태그
    + 태그 구조 : <태그이름 속성이름=”속성값”>
    + 짝을 이루는 태그 : <태그></태그>   
    ex) ```<body></body>```
    + 혼자 쓰는 태그 : </태그>가 없음   
    ex) ```<img src:””>```
    + 주석 : <!— —>
    
2. #### 이미지 태그
    + ```<img src=”경로” alt=””>```
    + 절대 경로: 고정적으로 변하지 않는 주소 ex)웹 주소
    + 상대 경로: 현재 문서를 기준으로 경로를 찾는 방법 
    현재 문서가 있는 폴더는 . 으로, 현재 문서의 부모 폴더는 .. 으로 표현

3. #### 블록 태그와 인라인 태그

    + 블록 태그 : 항상 전체 너비를 차지하는 태그 종류
    + 인라인 태그 : 자기 자신 만큼의 크기만 차지하는 태그 종류

        ```html
        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Document</title>
        </head>
        <body>
            <span>인라인</span>
            <span>인라인</span>
            <div>블록</div>
            <span>인라인</span>
        </body>
        </html>
        ```

    #### 결과 :   
        인라인 인라인   
        블록   
        인라인   

4. #### 태그 규칙

    1. 블록 태그 내부에는 블록 태그, 인라인 태그 모두 중첩 가능
    2. 인라인 태그 내부에는 인라인 태그만 중첩 가능
    3. 문단 태그 (p태그)는 블록 태그지만 인라인 태그만 중첩 가능   

   
### 제목, 문단 서식 태그   
1. #### 제목 태그   
    + 가장 큰 h1부터 가장 작은 h6까지 있다.   
    + 기본적으로 볼드 스타일이 지정   
    + 디자인적인 차이 뿐만 아니라 검색 엔진과 브라우저에서도 제목 태그를 제목으로 인식   
    ```<h1></h1>```

2. #### 문단 태그
    + 문단을 블록 형태로 나눔   
    ```<p></p>```
    + HTML에서는 엔터를 입력 해도 줄 바꿈이 되지 않음
    + 줄 바꿈 태그를 사용해야 함   
    ```(줄 끝에)<br>```
    + p태그 안에 블록 태그를 넣게 되면 p태그와 블록 태그가 분리됨 -> 적용 안됨

3. #### 볼드. 기울임, 밑줄, 인용문 태그
    + 볼드
        + b 태그와 strong 태그 모두 볼드 스타일로 텍스트가 적용됨   
        ```<b></b>``` , ```<strong></strong>```
        + strong 태그는 텍스트 스타일 뿐 아니라 중요한 텍스트라는 의미를 내포   
        -> b 태그는 일반 텍스트와 크게 다르지 않지만,    
        strong 태그는 검색 엔진이나 브라우저에서도 강조된 텍스트로 적용됨   

    + 기울임
        + i 태그와 em 태그 모두 기울임 스타일로 텍스트가 적용됨
        + 위의 strong 태그 처럼 em 태그도 중요한 텍스트라는 의미를 내포
        ```<i></i>``` , ```<em></em>```

    + 밑줄
        + ins 태그와 del 태그 모두 기울임 스타일로 텍스트가 적용됨
        + del 태그는 중요한 텍스트라는 의미를 내포
        ```<ins></ins>``` , ```<del></del>```

    + 밑줄
        + q 태그와 blockquote 태그 모두 기울임 스타일로 텍스트가 적용됨
        + q 태그는 짧은 인용문에 사용하고, blockquote 태그는 긴 인용문에 사용   
        ```<q></q>``` , ```<blockquote></blockquote>```


### 리스트 링크 태그
1. #### 리스트 태그
    + ul 태그는 순서가 없는 리스트, ol 태그는 순서가 있는 리스트를 만들 때 사용
    + 각 항목은 li 태그를 사용   
        ```html
        <ul>
            <li>1번</li>
            <li>2번</li>
            <li>3번</li>
        </ul><br>
        <ol>
            <li>1번</li>
            <li>2번</li>
            <li>3번</li>
        </ol>
        ```
        #### 결과 :   
        <ul>
            <li>1번</li>
            <li>2번</li>
            <li>3번</li>
        </ul><br>
        <ol>
            <li>1번</li>
            <li>2번</li>
            <li>3번</li>
        </ol>

2. #### 링크 태그
    + a 태그는 링크를 적용할 때 사용, 인라인 태그   
    ```<a 속성>주소 설명</a>```
    + 속성은 다음과 같다.   
        + href="이동할 주소"   
        이동할 주소를 입력
        + target=""   
        이동할 웹 페이지를 어떤 식으로 열건지 정의   
        ex)   
        _self (기본값) : 현재 페이지에서 열림   
        _blank : 새 탭 혹은 새 창에서 열림

    + id 태그를 이용하면 같은 문서 내에서도 링크를 생성할 수 있다.
    + 이동할 부분에 id 태그를 적용하면, href속성에 href="#id 태그"로 링크를 생성   
        ```html
        <ul>
            <li><a href="#first">1단원</a></li>
            <li><a href="#second">2단원</a></li>
            <li><a href="#third">3단원</a></li>
        </ul>
        <div id="first">1단원 본문</div>
        <div id="second">2단원 본문</div>
        <div id="third">3단원 본문</div>
        ```
        #### 결과 :   
        <ul>
            <li><a href="#first">1단원</a></li>
            <li><a href="#second">2단원</a></li>
            <li><a href="#third">3단원</a></li>
        </ul>
        <div id="first">1단원 본문</div>
        <div id="second">2단원 본문</div>
        <div id="third">3단원 본문</div>
       <br>

    + href="top"을 적용하면 문서의 최상단으로 이동

### 이미지, 비디오 오디오 태그
1. #### 이미지 태그
    + ```<img src="경로" alt="코멘트">```
    + alt 속성은 src의 이미지를 가져올 수 없을 때 대신 출력되는 부분이고, 웹 접근성을 향상 시킴
    + 가로 크기를 결정하는 width,    
    세로 크기를 결정하는 height,    
    툴팁을 지정하는 title,   
    로딩 방식을 지정할 수 있는 loading 속성이 있다.

2. #### 비디오 태그
     
    ```html
        <video 
        controls 
        src="경로" 
        width="가로" 
        height="세로" ></video>
    ```
    + controls로 비디오 컨트롤러 사용
    + 비디오가 자동 재생되도록 하는 autoplay, 반복 재생 하는 loop 등이 있다.

3. ####오디오 태그
    +  비디오 태그와 동일한 방식으로 사용   
    ```<audio src="경로" ></audio>```
    + 제어 속성도 동일하게 적용 가능
    

### div 태그, span 태그
1. #### div 태그와 span 태그
    + 두 태그는 여러가지 태그를 하나로 묶거나, 같은 속성을 적용시키는데 사용한다.
    + div 태그는 블록 태그, span 태그는 인라인 태그이다.
2. #### class 와 id 속성
    + css와 javascript와 함께 사용하기 위해 적용하는 속성
    + 태그에 이름을 붙일 때 사용
    + class 태그는 앞에 .을 붙혀 사용
    + class 태그는 다른 태그에 사용할 수 있고, 한 태그에 여러번 선언 가능   
    ```class="클래스1 클래스2 클래스3 ..."```
    + id 태그는 문서에서 1번만 사용 가능 (동일한 id 사용 불가),   
    한 태그에 1개의 id만 사용 가능
    + id와 class는 같이 적용 가능
    
    ex)
    ```html
    <!DOCTYPE html>
    l lang="en">
    d>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        #block1 { background-color: aqua;}
        .title {color: red;}
    </style>
    ad>
    y>
    <div id="block1">
        <h2 class="title1">타이틀 1</h2>
        <p>
            블럭 1
        </p>
    </div><br>
    <div id="block2">
        <h2 class="title1">타이틀 2</h2>
        <p>
            블럭 2
        </p>
    </div>
    dy>
    ml>
    ```

    #### 결과 : 
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
        <style>
            #block1 { background-color: aqua;}
            .title1 {color: red;}
        </style>
    </head>
    <body>
        <div id="block1">
            <h2 class="title1">타이틀 1</h2>
            <p>
                블럭 1
            </p>
        </div><br>
        <div id="block2">
            <h2 class="title2">타이틀 2</h2>
            <p>
                블럭 2
            </p>
        </div>
    </body>
    </html>

### 폼, 인풋 태그
#### 1. form 태그
+ 폼 태그 : 사용자의 데이터를 받아서 데이터를 웹 서버 등으로 전송할 때 사용하는 태그
+ input 태그로 입력 칸 생성, placeholder에 입력 칸 텍스트 입력
+ type 속성엔 text, number, tel, radio 등 적용 가능 

ex)

```html
    <form>
        <input type="text" placeholder="이름"/>
        <input type="email" placeholder="이메일"/>
        <input type="password" placeholder="비밀번호"/>
        <input type="submit" value="회원가입" />
    </form>
```   

결과:   
    <form>
        <input type="text" placeholder="이름"/>
        <input type="email" placeholder="이메일"/>
        <input type="password" placeholder="비밀번호"/>
        <input type="submit" value="회원가입" />
    </form>

#### 버튼 타입별 차이점
+ button : 기본 행동이 지정되지 않은 버튼
+ submit : 서버로 form 내용이 전송되는 버튼
+ reset : form의 내용을 모두 초기값으로 되돌리는 버튼   
<br>   

#### button 태그    
+ input 타입을 사용하지 않고도 버튼을 생성   
```<button>내용</button>```
+ submit이 기본값
+ type 속성으로 바꿀 수 있다.
+ '내용'부분에 아이콘 등을 넣을 수 있다.

#### 2. 레이블 태그
+ 사용자 인터페이스 항목에 이름을 붙여주고 연결하는 역할   
```<label for="name">이름</label>```
+ for 속성에 연결할 오브젝트의 id 입력

ex)   
```html
    <input id="man" type="radio" name="gender" />
    <label for="man">남</label>    
    <input id="woman" type="radio" name="gender" />
    <label for="woman">여</label>
```
결과:    
<input id="man" type="radio" name="gender" />
<label for="man">남</label>    
<input id="woman" type="radio" name="gender" />
<label for="woman">여</label>

#### 2. 서버에 데이터 전송
+ form 태그에 action 속성과 method 속성을 사용   
```<form action="주소" method="방식"></form>```
+ method는 어떤 방식으로 서버로 전송할 지 선택, 기본은 GET
    1. GET : 서버로부터 정보를 조회하기 위한 메소드
    2. POST : 리소스를 생성하거나 변경하기 위한 메소드

### 의미론적 태그
#### 1. 의미론적 태그의 개념
+ 과거엔 본문 영역마다 클래스 이름을 정해두었다.   
상단 영역 : ```<div class="header"></div>```   
본문 영역 : ```<div class="contents"></div>```   
하단 영역 : ```<div class="footer"></div>```   
+ HTML-5부턴 이런 부분을 의미론적 태그로 따로 제공함
+ div 태그는 브라우저나 검색 엔진이 무슨 영역인지 이해하지 못함
+ 의미론적 태그는 브라우저나 검색 엔진이 무슨 영역인지 이해함

#### 2. 의미론적 태그의 종류
+ header : 제목 영역
+ article : 본문 영역
+ footer : 하단 영역
+ nav : 네비게이션 영역

ex)   
```html

<!-- 제목 영역 -->
<header>
    <h1>제목 영역</h1>
</header>

<!-- 네비게이션 영역 -->
<nav>
    <ul>
        <li><a href="">네비게이션 1</a></li>
        <li><a href="">네비게이션 2</a></li>
        <li><a href="">네비게이션 3</a></li>
    </ul>
</nav>

<!-- 본문 영역 -->
<article>
    <p>
        본문   <br>
        본문   <br>
        본문   <br>
        본문   <br>
    </p>
</article>

<!-- 하단 영역 -->
<footer>
    <div>하단 영역</div>
</footer>
```

결과 :   
<header>
        <h1>제목 영역</h1>
    </header>
    <nav>
        <ul>
            <li><a href="">네비게이션 1</a></li>
            <li><a href="">네비게이션 2</a></li>
            <li><a href="">네비게이션 3</a></li>
        </ul>
    </nav>
    <article>
        <p>
            본문   <br>
            본문   <br>
            본문   <br>
            본문   <br>
        </p>
    </article>
    <footer>
        <div>하단 영역</div>
    </footer>

### 웹 접근성, 웹 표준, 검색 엔진 최적화
#### 1. 웹 접근성
+ 웹 사이트에서 제공하는 정보를 신체적, 환경적 조건 없이 동등하게 접근하고 이용할 수 있도록 보장하는 것
+ 웹 컨텐츠 접근성 지침을 제공 중
+ 문서에 언어 코드를 제공하거나 자막을 제공 하는 등의 방법으로 접근성을 증가시킬 수 있음

#### 2. 웹 표준
+ 웹에서 표준으로 사용 되는 기술이나 규칙
+ 구조(Markup), 표현(Style), 동작(Script)이 있음
+ 구조는 HTML, 표현은 CSS, 동작은 Javascript가 담당하도록 만드는 것을 의미
+ 웹 표준을 준수하면 다양한 플렛폼과 디바이스에 호환이 가능하고, 웹 접근성이 향상

#### 3. 검색 엔진 최적화
+ 검색 엔진은 봇이 수집한 정보를 각각의 기준과 규칙에 따라 분류함
+ 검색 엔진 최적화란 봇이 수집하고 분류한 수 많은 정보들 중에 내 웹사이트가 상위에 노출되도록 하는 것
+ HTML문서를 봇이 잘 해석하고 분류할 수 있도록 의미론적으로 분명하게 작성하는것이 핵심
+ 검색 엔진 최적화 방법
    + 웹 접근성과 웹 표준 준수   
    + ```<head>```태그에 제공되는 정보를 정확하고 간결하게 작성
    + HTML5의 의미론적 태그 활용
