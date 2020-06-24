# HTML,CSS

### HTML 이란

웹페이지를 만들기 위한 언어로써 웹페이지의 구조를 잡을 수 있다.

이미지, 텍스트, 비디오, 버튼 등 웹사이트에 보여줄 내용을 구성하고 있다.

<html>, <head>, <body> 가 HTML을 구성하기 위한 최소한의 태그들이다.



### Tag(태그)

html에서 이미지 나 텍스트를 그릴려면  나 텍스트를 그릴려면 그에 맞는 태그가 필요하다.

태그는 <>로 감싸져있고 </>로  끝낼수 있다.



### element(요소)

<태그이름> 과 </끝태그> 사이 내용이 있는 구간을 요소라 한다. 끝 태그가 없는태그는 태그자체가 요소가 된다.



### **attribute(속성)**

속성은 시작태그에 위치하며 한 태그에 여러속성을 지정할 수 있다.



### HTML 의 기본구조


```
<!DOCTYPE> 
<html>
 <head>
 </head>
 <body>
 </body>
</html>
```

- `<!DOCTYPE>`

HTML태그는 아니지만 html파일의 버전을 브라우저에 알려주는 역할을 한다.

`<!DOCTYPE html>` 은 HTML5 버전을 사용한다는 뜻이다.

- `<html>`

  `<!DOCTYPE>`을 제외한 모든 html 요소들은 `<html></html>`요소로 감싸져있다.

- `<head>`

  사이트의 제목, 설명, 부가 정보, 기술적 내용 이 들어가는 부분

  ```
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>repl.it</title>
  </head>
  ```

 - `<meta charset="utf-8">`

    한글, 일본어, 중국어 가 포함된 페이지라면 utf-8 값을 인코딩해야한다.

 - `<meta name="viewport" content="width=device-width">`

    디바이스의 가로 크기가 곧 웹페이지의 가로와 같다는 의미이다, 모바일에서 웹사이트를 봐야할 경우가 있을때 추가해야되는 정보이다.

 - `<title>repl.it</title>`

    브라우저 탭에 보이는 페이지 이름,  index.html에 작성된 코드는 지금 보고 있는 웹페이지 자체의 index.html 파일이 아니라서, 수정을 해도 적용이 되지는 않는다.

- `<body>`

  화면에 보여져야할 레이아웃대로 각종 태그들이 존재한다.

  
  
  ### body 의 태그들	

- `<h1> ~ <h5>`

  heading의 줄임말로 헤드라인의 제목같은 텍스트를 보여주려할떄 사용하는 태그이다.

  `<h1>` 이 가장 크고 숫자가 높아질수록 글자크기가 작아진다. `<h5>` 까지 존재한다.

 - `<span>`

    주로 텍스트를 넣어 묶는 역할을 한다. 화면에 줄바꿈이 되지않고 한 줄로 이어져나오게 되는데

    이런 요소를 inline-element 요소 라고 한다.

  - `<p>`

    paragraph의 줄임말로 주로 텍스트를 넣는 태그이다. `<span>`과는 달리 줄바꿈이 일어난다.

  - `<a>`

    클릭하면 화면이 이동하는 기능을 가진 태그이다.

    href 속성으로 이동할 주소를 써주면 된다. target="_blank" 은 새창으로 이동하는 속성값이다.

    ```<a href="https://www.w3schools.com/tags/tag_div.asp" target="_blank">div 태그?</a>```

  - `<div>`

    division의 줄임말이며, 웹사이트의 섹션을 나눌때 사용하는 태그

    비슷한 부분끼리 그룹을 짓고

    디자인에 맞게 레이아웃을 분리

    class나 id 를 부여해 CSS 스타일을 각 영역에 입혀줄 수 있다.

### body의 속성들

하나의 태그에 여러가지의 속성을 부여할 수있다.

여러 속성을 주고 싶으면 한 칸 띄워쓰기 후 다른속성을 추가하면 된다.

- `id`

  각 태그에 이름을 주는 속성, 한 태그당 하나의 `id`밖에 주지 못한다.

  해당요소에만 넣고 싶은 디자인을 적용할때 쓰인다.

- `class`

  id 와 같이 태그에 이름을 주지만 중복이 가능하다.

  


### 이미지

- **`<img>` 태그로 이미지넣기**

  html에서 이미지를 삽입할 수 있다.

  ```
  <img alt="HTML" src="https://www.w3schools.com/whatis/img_js.png">
  ```

  - alt: 이미지가 뜨지 않았을때 이미지대신 보여줄 텍스트이다.
  - src: 이미지 파일경로 or 이미지 url 주소

  이미지의 크기를 조절할땐 CSS에서 하는것이 유지보수에 좋다.

  ```
  img {
    width: 150px;
  }
  ```

  이런식으로 CSS에서 가로값만 지정해주어도 가로의 150px에 맞춰서 세로도 알맞게 줄어든다.

- **backgruond-image로 이미지 넣기**
  html에서 `<img>` 태그로 이미지를 생성하는 방법 말고 다른방법이 더 있다.

  태그가 아닌 CSS에서 이미지를 생성하여도 이미지를 삽입할 수 있다.

  html에 섹션을 나누어 준다.

  ```
  <div class="bg-img"></div>
  ```

  그후

  ```
  .bg-img {
    background-color: yellow;
    background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/1280px-HTML5_logo_and_wordmark.svg.png");
  }
  ```

  `bg-img`클래스 안에 배경이미지를 추가해서 이미지를 삽입하는 방식이다.

  - background-color 로 배경색을 추가 한다 이는 `div`의 크기를 직관적으로 확인 하기 위해 넣는다
  - background-image 로 배경 이미지를 추가

  그후  `div`의 크기 를 할당하고 배경이미지의 크기를 지정해줘야한다.

  ```
  .bg-img {
    height: 300px;
    width: 300px;
    background-size: 100%;
  }
  ```

  - height:  div의 세로값을 지정
  - width: div의 가로값을 지정
  - background-size: 배경이미지의 크기조정 100% 값을 입력하면 `div`공간안에 배경이미지가 꽉차게 들어간다.

  그리고나서 공간의 크기를 확인하기 위해 넣은  `background-color: yellow;`를 삭제하면 이미지 삽입이 완료된다.



### Display

(inline, inline-block, block)

display 속성은 그 값에 따라서 웹페이지를 보고 있는 사용자에게 특정 요소를 어떻게 보여줄지 결정된다.

- **block**: 이 요소 바로 옆(좌우측)에 다른 요소를 붙여넣을 수 없다 대표적인 태그로는 p 태그와 form 태그 header 태그 footer 태그 section 태그등이 있다.

  ```
  <header>, <footer>, <p>, <li>, <table>, <div>, <h1>
  ```

  

- **inline:** 요소는 요소끼리 서로 한 줄에, 바로 옆에 위치할 수 있다 대표적으로 span 태그와 a 태그가 있다.

  ```
  <span>, <a>, <img>
  ```

 - **inline-block:** display 속성이 inline-block으로 지정된 엘리먼트는 기본적으로 inline 엘리먼트처럼 전후 줄바꿈 없이 한 줄에 다른 엘리먼트들과 나란히 배치된다. 하지만 inline 엘리먼트에서 불가능하던 width와 height 속성 지정 및 margin과 padding 속성의 상하 간격 지정이 가능하다.

block요소의 성질을 가진 `<p>`태그도 css를 사용하여 inline 스타일을 바꾸면 `<span>`과 똑같은 디자인이 된다.

```
.inline-p {
  display: inline-block;
}
```

이런식으로 `inline-p`클래스안의 `<p>`태그의 스타일을 바꿀수 있다.

반대로 inline요소를 block으로 바꾸게 할수도 있다.

```
.block-span {
  display: block;
}
```

이렇게 `.block-span` 클래스 안의 `<span>`의 스타일 을 block으로 바꾸었다.

- **none**

  해당영역이 보이지 않게 한다.

  ```
  .hide{
  	display: none;
  }
  ```

  자바 스크립트와 많이 쓰인다. 원래는 해당영역이 display: none; 으로 보이지않다가, 텍스트를 입력하는 순간 자바스크립트를 활용해 다른클래스로 교체하는걸 구현할수 있다.

### 레이아웃

[레이아웃 참고 사이트](https://www.w3schools.com/html/html5_semantic_elements.asp)

- **magin** 값에 auto를 준다면

  먼저 div를 html로 할당 한후 

  ```
  div{
  	background-clor: yellow;
  	margin-bottom: 20px;
  	width: 150px;
  }
  ```

  위와 같이 block 요소일떄 width 값을 주면 더이상 늘어나지 않는다.

  이 때 margin을 suto로 설정하면 가로중앙에 오게 할수 있다.

  ```
  div{
  	margin: 20px auto;
  }
  ```

  위,아래는 20px  왼,오른쪽은 auto 값을 주었다

  이렇게되면 div는 150px의 만큼의 넓이를 차지하고 좌우의 나머지 공간은 균등하게 배분되어 여백을 갖게 된다.

### list

- `<ul>`,`<ol>`,`<li>`

  - **ol**

    순서 있는 목록 만들기 

    ```
    <ol>
    	<li>list1</li>
    	<li>list2</li>
    	<li>list3</li>
    </ol>
    ```

    `<ol>`은 목록에 숫자를 달아준다. `<li>`로 목록을 만든뒤 `<ol>`로 감싸주면 된다.

  - **ul**

    순서 없는 목록 만들기

    ```
    <ul>
    	<li>list1</li>
    	<li>list2</li>
    	<li>list3</li>
    </ul>
    ```

    `<ol>`과 마찬가지로`<li>`을 만든후`<ul>`으로 감싸준다. 

  아무 스타일도 넣고 싶지 않다고`<li>` 태그만 사용하면 안되며 항상 `<ul>`,`<ol>`로 감싸야한다.

  하지만 CSS로 없애는게 가능하다.

  ```
  ul {
   list-style: none;
  }
  ```

  을 입력하면 사라지게 되며 검정색 줄을 넣고싶을땐

  ```
  ul {
   list-style: none;
   border-left: 3px solid black;
  }
  ```

  와 같이 세로줄을 넣을수도있다. 그리고 나서

  ```
  ul {
   list-style: none;
   border-left: 3px solid black;
   padding: 15px;
  }
  li{
  	padding-bottom: 10px;
  }
  li:last-child {
     padding-bottom: 0;
  }
  li:nth-child(odd) {
    background: red;
  }
  
  li:nth-child(even) {
    background: blue;
  }
  ```

  와 같이 입맛대로 내용을 추가 할수 있다.

  `li:nth-child(odd)`은 `<li>`의 홀수를 디자인하고 `li:nth-child(even)`은 짝수를 디자인한다.

  `li:last-child`은 `<li>`의 맨마지막을 디자인한다.

### Table

- **테이블의 구성**

  ```
  <table>
      <tr>
        <td>Row 1, column 1</td>
        <td>Row 1, column 2</td>
      </tr>
      <tr>
        <td>Row 2, column 1</td>
        <td>Row 2, column 2</td>
      </tr>
    </table>
  ```

  - `<table>`

    테이블의 시작과 끝을 알리는 태그 테이블의; 내용은 `<table>` 태그로 감싸져 있어야한다.

  - `<tr>`

    한행을 시작할때 쓰이는 태그 `<td>`를 감싸준다

  - `<td>`

    행에 열을 추가할떄 쓰이는 태그 이다.

  선의 디자인은 CSS를 이용하는게 바람직하다. 테이블은 html에서 만들어진다.

- `<th>`

  table heading의 줄임말으로 `<td>`의 대신에 넣을수있다.  열과 행의 제목을 추가 할때 쓰인다.

  `<th>`를 사용하면 가운데 정렬이 되고, 글씨 두께가 두꺼워진다.

  ```
  <table>
    <tr>
      <th>Dog</th>
      <th>Cat</th>
    </tr>
    <tr>
      <td>Canine</td>
      <td>Feline</td>
    </tr>
    <tr>
      <td>Bark</td>
      <td>Meow</td>
    </tr>
    <tr>
      <td>Puppy</td>
      <td>Kitten</td>
    </tr>
  </table>
  ```

- **테이블에 선 추가하기**

  ```
  th, td {
    border: 1px solid black; 
  }
  ```

  table에 `<th>`와`<td>`의 선을 1px, 실선, 검정으로 만든다.

- **colspan, rowspan**

  - **colspan**

    열을 병합한다.

    ```
    <table>
    	<tr>
    		<th colspan="2">병합</th>
    	</tr>
    	<tr>
    		<td></td>
    		<td></td>
    	</tr>
    </table>
    ```

    `colspan="2"`는 열을 2개를 병합한다는 것이다.

  - **rowspan**

    행을 병합한다.

    ```
    <table>
    	<tr>
    		<th colspan="2">병합</th>
    		<td></td>
    	</tr>
    	<tr>
    		<td></td>
    	</tr>
    </table>
    ```

    `rowspan="2"`는 행을 2개를 병합한다는 것이다.

### Input

```
<input type="text" placeholder="ID"> 
<input type="password" placeholder="비밀번호"> 
<input type="number" placeholder="학번">
```

- **Input의 타입**

  - type="text"

    텍스트를 입력하는 속성, 대부분의 input type은 text이다.

    어느텍스트나 입력할 수 있고 주로 이름, id, 주소, 닉네임 등을 입력 받을 때 사용한다

  - type="password"

    text와 비슷한 속성이지만 뭔가를 입력하면 까만원이 나와서 보이지않게 처리한다.

    화면에서는 안보여도 자바스크립트를 이용하면 무슨값을 입력했는지 가져올수 있다

  - type="number"

    숫자만 입력할 수 있다

  - placeholder

    도움말을 넣어주는 기능이다 실제 input에 입력되어있는 텍스트가 아니다

- `<textarea>`

```
<textarea>소개:</textarea>
```

` <textarea>`는 input보다는 더 긴 텍스트를 입력받고 싶을 때나 보통 짧은 방명록이나 댓글을 입력할 때 사용한다.

> textarea에 "소개:"라고 보이는 것은 placeholder가 아니라 텍스트이다.
> input은 시작태그, 끝태그로 구성되지 않는다. 하나의 태그가 하나의 요소이다.
> textarea처럼 input에도 미리 값을 세팅해놓고 싶을 때 value라는 attribute를 사용한다.

- **inline element**

  input, textarea, button은 모두 inline element라서 한 줄에 나온다

  block으로 바꾸고 싶을때 주로`<div>` 감싼 후

  ```
  div{
  	display: block;
  	}
  ```

  div의 속성을 block으로 바꾸면 된다

- **input width**

  input과 textarea의 가로가 모두 제각각일떄 통일 시켜보자 여러 방법이 있다.

  1. input, textarea에 같은 width 값을 부여한다.
2. 부모에 width를 주고 input, textarea의 width는 100%로 설정한다

1번 방법보단 2번방법이 유지보수에 적합하므로 2번 방법을 써보자

  ```
  <body>
  <div class="survey-container">
      <div class="input-wrap>
        <input type="text" placeholder="ID"> 
      </div>
      내용
    </div>
  </body>
  ```

  

  ```
  .survey-container {
    width: 200px;
    margin: 100px auto;
  }
  input, textarea {
    width: 100%;
  }
  ```

  이렇게 하면 `survey-container`클래스가 가운데 정렬이 되고 input이 `survey-container`안에 채워진다

```
	input[type="text"]::placeholder {
  color: red;
}
```

이런식으로 input안에 placeholder의 색상을 바꿀수도 있다.

```
button {
  padding: 5px 10px;
  border-radius: 5px;
  
}
```

` border-radius`는 선모서리를 둥글게 만드는 기능이다 

```
button:hover {
	cursor: pointer;
	opacity: 0.8;
}
```

`cursor: pointer;`는 마우스를 올렸을때 커서모양이 바뀌는 기능

`opacity: 0.8;`는 마우스를 올렸을떄 색상이 연해지는 효과가 있다.

### CSS (Cascading Style Sheets)

CSS 의 역할은 html의 태그 들에게 디자인을 입혀주는 역할을 한다.

html이 정보를 조직화 하는 구조를 제공한다면, CSS는 HTML의 구조를 아름다워보이도록 스타일을 입힌다.

### CSS 적용

CSS를 작성한 후 html에 적용하는 방법은 3가지가 있다.

1. **인라인 스타일**

   html 태그 style 속성에 직접 작성 하는 방법

   빠르고 편하지만 유지보수가 좋지않고 가독성이 떨어진다.

2.  **style 태그 **

   html 파일내에 css 를 작성 하는 방법

   `<style>` 태그를 생성하고 그안에 css를 작성하는 방법이다.

   이 방법도 편하고 빠르지만 기능적으로 html와 디자인이 분리되지 않았기 떄문에 유지보수에 적합하지않다.

3.  **css 파일에 작성**

   1,2번과 달리 같은 파일에 css를 작성하지않고  html 파일과 css 파일을 분리하여 따로 작성하는 방법

   유지보수가 가장 적합하지만 빠르고 편하지 않다.

    html파일에서 어느 css파일이 쓰였는지 브라우저에 알려야 하므로, 링크를 해주는 태그를 추가해야 한다.

   ```
   <link href="index.css" rel="stylesheet" type="text/css" />
   ```

   - **link**

     link태그로 사용할 css파일을 링크해줍니다.

   - **href** 

     href 속성에 css 파일 경로를 작성합니다.

   - **type** 

     link태그로 연결되는 파일이 어떤 것인지 알려줍니다. 여기서 css file을 연결하므로 type값은 항상 "text/css"입니다.

   - **rel** 

     rel은 HTML file과 CSS file과의 관계를 설명하는 속성입니다. css파일을 링크할 때는 항상 "stylesheet"값을 대입해줍니다.



### font style

- **font family**

  폰트 스타일을 지정하는 속성

  ``` #title {
   #title{
   font-family: Georgia, "Times New Roman", Times, serif;
 }
  ```

  브라우저가 Georgia 라는 폰트를 지원해주면 Georgia 폰트를 적용한다 는 뜻이다.
  
  만약 Georgia 폰트가 지원되지 않으면 "Times New Roman"을 이것도 없다면 Times 을 
  
  이것도 없다면 serif 폰트를 사용하겠단 뜻이다.
  
  "Times New Roman" 만 ""(쌍따옴표)가 감싸져 있는데 폰트 이름에 띄어쓰기가 있다면 ""(쌍따옴표)를 사용해야한다.
  
  현재는 id가 title인 요소에만 폰트를 지정했다. 폰트를 직접 지정하지 않으면 브라우저에서 기본적으로 적당한폰트를 지정한다.
  
- **font size**

  ``` .big-size-font{
.big-size-font{
  	fint-size: 50px;
  }
  ```
  
  `.big-size-font` 클래스에 50px의 폰트크게를 지정했다, 폰트 크기 단위는 'px', 'em', 'pt' 등 여러가지가 있다.

- **font weight**

  글씨의 두께를 조절하는 속성

  ```
  .bold-font{
  	font-weight: bold;
  }
  ```

  `.bold-font`클래스에 글자 굵기 `bold`를 지정했다.

  `font-weight`는 normal, bold,100,200,... 900 등의 값이 지정 될 수 있다.

  400과 narmal은 같은두께이며, 700과 bold는 같은 두께이다.

- **font style**

  ```
  a{
   font-style: italic;
  }
  ```

  `a`태그에 이텔릭체를 지정했다.

  font-style 이라는 속성으로 쉽게 글씨 스타일을 바꿀 수있다.

  italic 값을 지정하면 *이텔릭체*로 변하게된다.

- **color**

  ```
  .pink{
  	color: pink;
  }
  .yellow{
  	color: yellow;
  }
  ```

  `.pink`클래스에 `pink`색을 `.yellow` 클래스에 `yellow`색을 지정했다

  색을 지정할수 있는 방법에는 어려가지가 있다.

  - **hex 색상코드**: 여섯자리로 표현 - #eb4639 
  - **rgb 값**: 빨강,초록,파랑으로 표현 - rgb(235,70,57)

  - **hsl** : 색상, 채도, 명도로 표현 -hsl(4,82%,57%)

  원하는 색상을 찾고싶다면 구글에 "[color picker](https://htmlcolorcodes.com/color-picker/)","[color picker hex color](https://www.google.com/search?q=color+picker+hex+color&oq=color+picker+hex+color&aqs=chrome..69i57.1805j0j7&sourceid=chrome&ie=UTF-8)" 를 검색하거나

  hex 표현에서 rgb 표현으로 바꾸고 싶다면 "[color hex to rgb](https://www.rapidtables.com/convert/color/hex-to-rgb.html)" 를 검색하면 된다.



### 텍스트정렬

텍스트 정렬에는 왼쪽정렬, 가운데 정렬, 오른쪽정렬이 있다.

- **text-align**

  left, center, right 값을 이용해 정렬 할수 있다.

  ```
  .center{
  	text-align: center;
  }
  ```

  `.center`클래스에 가운데 정렬을 했다.

  `span`태그와 같은 `inline-element`  태그들은 차지하는 영역은 "span안에서의 오른쪽정렬" 밖에 되지않는다

- **indent**

  css로 들여쓰기를 하는 방법이다.

  html에서는 스페이스를 아무리 추가 해도 하나의 스페이스밖에 입력되지않는다. 그럴때 `&nbsp;` 코드를 넣어주면 스페이스로 인식이 되서 추가로 스페이스를 넣을 수 있다.

  또한 `indent`를 사용할수 있다.

  ```
  .js-description {
    text-indent: 50px;
  }
  ```

  `.js-description`  클래스에 들여쓰기 `50px`를 적용하는 방법이다.



### Magin과 Padding

![magin, padding](https://media.vlpt.us/images/offdutybyblo/post/0b641b81-dbb6-42f3-828a-e55cec9329e2/image.png)

- 주황색은 margin 영역 : 위, 오른쪽, 아래, 왼쪽에 모두 50px
- 노란색은 border 영역 : 보더의 두께는 5px, 테두리 부분이다
- 초록색은 padding 영역 : 위, 오른쪽, 아래, 왼쪽 모두 50px
- 요소의 가로는 273px, 세로는 90px

padding은 border내에서 생기는 영역이다. 273px 라는 가로값은 padding영역이 합쳐진 가로 길이이다.

margin 은 border 외부에서 생기는 여백이다.

magin까지 합쳐진 가로길이는 273 + 50(왼쪽 magin) + 50 (오른쪽 margin) = 373 이다.

순수 내용(파란색영역)은 padding과 border를 제외한 길이이다.

순수내용의 가로길이는 273 - 50(왼쪽 padding) - 50(오른쪽 padding) - 5(왼쪽border) - 5(오른쪽 border) = 163 이다. 

css는 다음과 같다.

```
p.example{
	width: 273px;
	height: 90px;
	margon: 50px;
	border: 5px solid black;
	padding: 50px;
}
```

- **margin**

  `magin: 50px;` 을 풀어쓰면 다음과 같이된다.

  ```
  margin: 50px 50px 50px 50px;
  ```

  순서대로 위, 오른쪽, 아래, 왼쪽의 여백값이다.

  ```
  margin: 50px 50px;
  ```

  만약 이렇게 2번값 만 입력하게 되면 첫번째가 위,아래 두번째가 왼,오른쪽이 된다.

  여기서 한번더 풀어쓰면 이렇게 된다.

  ```
   margin-top: 50px;
   margin-right: 50px;
   margin-bottom: 50px;
   margin-left: 50px;
  ```

  각각 개별로 여백값을 지정 할수 있다.

- **padding**

  패딩도 풀어쓰면 다음과 같다

  ```
  padding: 50px 50px 50px 50px;
  ```

  패딩은 border 안쪽 여백을 설정하며 사용법은 마진과 다르지않다.

- **border**

  ```
  border: 5px solid black;
  ```

  두께(5px) 선스타일(solid) 선색깔(black); 을 지정해줘야 한다. border는 마진과 달리 순서는 중요하지않다.

  하지만 전 세계적으로 약속된 coding convenrion(코딩 규칙)에 따라 순서를 맞춰주는 것이 좋다.

  선스타일 종류

  - dotted
  - dashed
  - solid
  - double
  - groove
  - ridge
  - inset
  - outset

  이중에 거의 solid만 사용하지만 다른 스타일도 사용할 경우가 있으니 있다는 정도만 알아두면 된다.

  선도 각 방향마다 다양하게 스타일을 줄수 있다.

  ```
  blockquote{
  	border-top: 4px double red;
  	border-right: 2px solid #666666;
  	border-bottom: 6px dashed darkviolet;
  	border-left: 1px dotted #00ee44;
  }
  ```

  또한 `border-bottom`속성으로 글자의 밑줄처럼 만들어 커스텀마이징을 할수있다.

  원래 밑줄을 치는 속성은 ` text-decoration: underline;`이지만 커스텀마이징이 되지 않는다

  

  

### 상속(Inheritance), 그룹(Grouping)

- **상속(Inheritance)**

상속은 css가 가진 특성이다. 스타일이 상속되어 자식에게도 같은 스타일을 적용 할수 있다.

```
body{
	color: red;
	font-size: 14px;
}
```

이렇게`body`태그에 글자색과 크기를 설정해놓으면

아무런 설정을 하지않은 `<p>`태그와 `<blockquote>`태그 또한 `body`태그의 스타일 을 상속받는다.

원하지 않은 결과라면 본인의 태그의속성을 다시 설정하면 된다.

- **그룹(Grouping)**

  한번에 각기 다른 클래스, 태그에 같은 스타일을 적용하고 싶을때는

  CSS에 `,`을 넣어 스타일을 한번꺼번 지정하면 된다.

  ```
  .what-is-blockquote, span {
    color: green;
  }
  ```

  

### CSS selector

class 나 id가 selector일때 태그와 결합할 수 있다.

```
p.p-tag {
  color: gray;
}
```

`p`태그 이면서 동시에 `p-tag` 클래스가 된다.

```
p#third-line {
  text-decoration: underline;
}
```

`p`태그 이면서 동시에 `third-line`  id가 된다.

또한 `class`안의 태그만 지정해서 속성을 부여할 수 있다.

```
.pre span{
	background-color: yellow;
}
```

`pre`클래스 안의 `span`태그를 지정한다. 중간에 스페이스바를 넣으면 하위 태그를 찾아간다.

길게도 작성할수 있다. 예를들어

```
<div class="pre">
  <span>이건 노란색 배경이고</span>
</div>
<div class="main">
  <span>이건 아님!</span>
</div>
<span class="pre">이것도 아님</span>
<div>
  <p class="pre">
    <span>이건 적용됩니다! 노란색배경!</span>
  </p>
</div>
```

이런 html 예제가 있다면

```
.a div .b .pre span {
  background-color: yellow;
}
```

`a` 클래스 안에 `div`태그 안에 `b`클래스만에 `pre`클랫스 안에 `span`태그 에만 적용할 수있다.



### CSS Specificity

CSS selector의  우선순위에 대해 배워보자

```
p {
  font-size: 30px;
}
.p-tag {
  font-size: 15px;
}
```

만약 `p`태그 안에 `p-tag`가 있다고 가정해보자 font-size가 중복되어도

브라우저 30px과 15px중에 브라우저는 15px를 표현한다. 그이유는 우선순위에대한 점수계산이 이루어지기 때문이다.

- **inline styling**(13줄에 style 요소로 직접): 1000점
- **id**: 100점
- **class**: 10점
- **tag**: 1점

코드를 짜는동안 일일히 점수 계산은 힘드니

**tag** <<<<< **class** <<<< **id** <<<<<< **inline css** 이런 개념정도만 알아두자

### Position

레이아웃을 배치하거나 객체를 원하는 위치에 놓을수 있는 기능

- **static** (기본값) : 위치를 지정하지 않을 때 사용한다.

- **relative**

  위치를 계산할때 static의 원래 위치부터 계산한다. CSS를 활용해 top,bottom,left,right 로 위치를 조정할수 있다.

  ![](https://storage.googleapis.com/replit/images/1554040139571_639805e8a49b96e6f9aebb66611d974b.pn)

  ```
  .relative {
    position: relative;
  }
  .top-20 {
    top: -20px;
    left: 30px;
  }
  ```

  div.relative.top-20은 위로 20px 이동하고, 왼쪽에서 30px만큼 떨어진다.

  마이너스 값을 주면 아래로 떨어지지 않고, 위로 올라가게 된다.

  

- **absolute**

  원래 위치와 상관없이 위치를 지정할 수 있다. 단, 가장 가까운 상위 요소를 기준으로 위치가 결정 된다.

  부모 중에 position이 relative, fixed, absolute 하나라도 있으면 그 부모에 대해 절대적으로 움직이게된다.

  CSS를 활용해 top,bottom,left,right 로 위치를 조정할수 있다.

  

- **fixed**: 원래 위치와 상관없이 위치를 지정할 수 있다. 하지만 상위 요소에 영향을 받지 않기 때문에 화면이 바뀌더라도 고정된 위치를

  ​			설정 할 수 있다.   브라우저 화면의 상대 위치를 기준으로 위치가 결정된다. CSS를 활용해 top,bottom,left,right 로 위치를

  ​            조정할수 있다.





### Float 

주로 이미지 주변에 텍스트를 감싸기 위해 만들어진 프로퍼티이다. 정렬을 위해 만들어졌다. 각 객체를 오른쪽과 왼쪽에 정렬하여 문서에 배치할때 쓰인다.

- **none**: 띄우지 않음
- **left**: 왼쪽부터 시작한 후 입력값의 자리를 할당 받는다. 
- **right**: 오른쪽부터 시작한 후 입력값의 자리를 할당 받는다.
- **initial**: 기본값으로 설정함
- **inherit**: 부모 요소로 부터 상속함

```
.b{
	float: left;
	width: 200px;
}
```

`b`클래스를 div로 만들었다고 가정하고 위에 코드는`b`클래스가 화면왼쪽에 200px할당을 받았다는 뜻이다

**float 문제 해결**

>float을 해결하려면 clear라는 속성이 필요합니다. 
>
>float 요소 옆에 채워지는 요소들에게 적용하는 프로퍼티입니다.
>
>해결방법은 여러개가 있지만 그 중 몇 개만 소개해드려요.
>
>**해결방법1.** 
>
>바깥 div(.wecode-box) 마지막에 아무태그나 넣고 clear 속성을 적용합니다.
>
>이 기법을 사용할 때에는 HTML코드를 더 입력해야 하는 부담이 있습니다.
>
>**해결방법2.**
>
>주로 많이 사용하는 방법인데 바깥 div(.wecode-box)에 overflow: hidden; 을 주는 것입니다. 
>
>**해결방법3.**
>
>바깥 div(.wecode-box)를 float시킵니다.
>
>그러면 자식의 float 높이를 인지하여 그만큼 높이를 차지하게 됩니다.
>
>하지만 이것도 문제가 있죠, float이 되어버려 block 요소의 성질이 없어지게 됩니다. 이러면 width를 100% 추가하거나 해야합니다.

### **Clear**

float 속성 때문에 객체가 다음줄로 넘어가지 않을때 사용한다. clear 속성이 지정된 영역 이후로는 더 이상 float가 작동하지 않는다.

- **none**: 기본 값
- **float** : left 속성을 해제한다.
- **right**: right 속성을 해제한다.
- **both**: left, right 속성을 둘 다 해제한다.



### media Query

media query란 Responsive Web 을 구현하는 CSS technique 이다

if문과 비슷하게 특정조건에서 어떤 CSS를 적용하라는 규칙을 줄수있다

@media 라는 문법을 사용한다.

```
@media only screen and (max-width: 480px) {  
  body {  
    font-size: 12px;  
  } 
}
```

480px 보다 작은 화면에서 body의 폰트크기를 12px로 바꾸겠다는 뜻이다.

>1. @media — 이 키워드는 media 쿼리를 시작하겠다는 의미입니다. 
>2. only screen — 어떤 디바이스에서 적용하는지 알려줍니다. 예를 들면 프린트를 하고싶을 때 적용하려면 only print라고 작성하면 됩니다. screen이라고 할 경우 어떤 디바이스에 상관없이, 화면에 보이는 스크린이기만 하면 전부 적용됩니다.
>3. and (max-width : 480px) — 이건 media feature라고 불리는 부분입니다. 어느 조건에 아래의 css를 적용할지 작성해줘야 합니다.



---

#### 레이아웃 참고사이트들

http://ko.learnlayout.com/

https://poiemaweb.com/css3-layout

https://poiemaweb.com/css3-box-model