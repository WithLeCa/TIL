# CSS

> #### 강의 주소
> 독학백서 기초 강의 > https://youtu.be/FV32OM3B49c?si=_2t9mLQyxIk6RTHO

### HTML과 CSS   
HTML에 스타일을 적용하는 방법이다.

#### 1. 인라인   
+ HTML 태그 내부에 style 속성을 사용해 직접 스타일을 지정하는 방법   
+ 짧은 예제를 작성할 때 유용하나, style이 많아지고 길어지면 가독성이 떨어지고 유지보수도 힘듬   

ex) 
```html
<h1 style="color : red">Hello World!</h1>
```
결과 : 
<h1 style="color : red">Hello World!</h1>   
   

#### 2. 인터널   
+ 스타일을 중괄호{ }로 묶어 스타일을 지정하는 방법   
+ 한 문서가 양이 많지 않은 고유한 스타일을 가질 때 사용, 인라인과 마찬가지로 가독성과 유지보수가 좋지 않음   

ex) 
```html
<style>
    h1 {
        color : red;
    }

    <h1>Hello World!</h1>   
```     

   
#### 3. 익스터널   
+ css확장자를 가진 별도의 파일에 스타일을 작성하고 HTML문서에 링크로 연결하는 방식   
+ 별도의 파일을 만들기 때문에 유지보수가 쉽고 가독성도 좋음   

```html
 <!-- head에 작성-->
<head>
    .
    .
    .
    <link rel="stylesheet" href="css문서 경로">
</head>
```   
+ rel 속성 : 문서와의 관계를 나타냄, 위에선 stylesheet로 지정
+ href 속성 : css 파일의 경로를 작성

#### 4. 주석    
```css
/* 여기에 입력 */
```   

#### 5. 기본 문법
선택자와 선언부로 구성
```css
/* h1은 선택자 */

h1 {
    /*내부는 선언부*/
    color : red;
    font-size : 20px;
}
```

+ 선언부는 중괄호 { }로 감싸져야 함
+ 각 속성은 세미콜론;으로 구분   

<br>

### 선택자
#### 1. 전체 선택자
+ HTML 내에 모든 요소에 스타일을 적용
+ 식별자는 *   

ex)   
```css
* {
    color : red;
}
```   

#### 태그 요소 선택자
+ 태그 내에 모든 요소에 스타일을 적용
+ 식별자는 태그 이름

ex) 
```css
/* h1 태그가 있는 모든 요소에 적용*/
h1 {
    color : red;
}
```   

#### ID 선택자
+ ID로 선택한 요소에 스타일을 적용
+ 식별자는 ID앞에 #
   
ex)   
```css
#red {
    color : red;
}
```   

ID태그를 이용해 적용 가능   

```html
<h1 id="red">Hello World!</h1>
```

#### Class 선택자
+ 해당 클래스를 사용하는 요소에 스타일을 적용
+ 식별자는 클래스 이름 앞에 .   

```css
.blue {
    color : blue;
}
```   

Class태그를 이용해 적용 가능   

```html
<h1 class="blue">Hello World!</h1>
```   

#### 다양한 태그에 속성 적용
,로 구분해 한번에 속성을 적용할 수 있다.   

ex)
```css
h1,     /*태그 요소 선택자*/
#red,   /*ID 선택자*/
.blue { /*Class 선택자*/
    font-size : 20px;
}
```   

#### 결합 선택자
+ 조상 요소의 한 태그 자손 요소를 선택할 때 사용
+ 띄어쓰기로 구분

```css
.first h1 { /* first 클래스 내부에 있는 모든 h1 태그에 적용 */
    color: red;
}
```

+ 클래스 내부에 있는 자손 요소만 선택할 땐 > 로 구분   

```css
.first h1 { /* first 클래스 내부에 있는 자손 요소의 h1 태그에 적용 -> 예제 참고 */
    color: red;
}
```

### 텍스트와 폰트 스타일

#### 1. 색깔
```css 
color : red; 
```   

#### 2. 정렬
```css
text-align : center;
```   
왼쪽, 오른쪽, 중앙, 양쪽 정렬중 하나로 지정 가능   

#### 3. 줄간격
```css
line-height : normal;
```   

#### 4. 선 장식
```css
text-decoration : line-through;
```
기울이기, 굵게, 취소선, 밑줄 등이 있음

#### 5. 폰트 집합
+ 같은 폰트를 사용하는 폰트를 정의
+ 속성에는 사용하려는 폰트 집합, 제네릭 집합을 지정
+ 제네릭 집합은 비슷한 모양을 가진 폰트 집합을 의미   

```css
font-family : "Times New Roman", Times, serif;
```

폰트 집합을 나열하고, 마지막에 제네릭 집합을 명시하면   
사용하려는 폰트가 없을 경우 제네릭 집합을 사용   

#### 6. 웹 폰트 적용
+ HTML의 link나 css의 @import를 이용해 적용 가능
+ HTML에선 head에 해당 폰트에서 제공하는 코드를 작성, 속성 적용도 동일하게 작성   
 -> 예제 확인
+ CSS에서도 동일하게 코드 작성, @import형태로 존재
+ 스타일 시트를 작성하는 곳에 추가되어야함