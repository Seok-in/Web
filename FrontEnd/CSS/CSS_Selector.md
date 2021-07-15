# CSS 문법 -Selector
- 선택자(Selector)
  - 요소 선택자 (태그 선택자)<br>
    - 전체 선택자 : ```*{ color : yellow;}```
    - ```h1, h2, h3, h4 { color : yellow;}``` 등으로 그룹화도 가능하다.
    - ```h1, h2, h3, h4 { color : yellow; font-size : 2em;}``` 처럼 선언과도 동시에 그룹화 할 수 있다.
  - class 선택자
    - 요소에 구애 받지 않고 스타일 규칙을 적용할 수 있는 선택자
    - 클래스 선택자를 쓸 때는 맨앞에 . 을 찍어줘야한다.
    ```css
    .foo{font-size:30px;}
    <p class = "foo">... </p>
    ```
    - 다중클래스 : class 속성은 공백으로 구분하여 여러 개의 클래스 값을 넣을 수 있다.
    ```css
    .foo{font-size : 30px;}
    .bar{color : blue;}
    <p class = "foo bar">... </p>
    ```
  - id 선택자 
    - 클래스 선택자와 비슷하나 . 대신 #을 이용하여 쓴다.
    ```css
    #bar{background : yellow;}
    <p id = "bar">... </p>
    ```
    - id 속성값은 문서 내에 유일하게 사용되어야 한다.
  - 선택자의 조합
    - 요소와 클래스의 조합 : ```p.bar{...}```
    - 다중 클래스 : ```.foo.bar{...}```
    - id 와 class의 조합 : ```#foo.bar{...}```
***
- 속성선택자
  - 단순 속성으로 선택
    ```css
    p[class]{color : silver;}
    p[class][id]{text-decoration: underline;}
    ```
  - 정확한 속성값으로 선택
    ```css
    p[class="foo"]{color : silver;}
    p[id="title"]{text-decoration: underline;}
    ```
  - 부분 속성값으로 선택
    ```css
    [class~="bar"] : class 속성의 값이 공백으로 구분한 "bar" 단어가 포함되는 요소
    [class^="bar"] : class 속성의 값이 "bar"로 시작하는 요소
    [class$="bar"] : class 속성의 값이 "bar"로 끝나는 요소
    [class*="bar"] : class 속성의 값이 "bar"문자가 포함되는 요소 선택
    ```
***

- 부모 자식 관계 이해하기 
  - 부모와 자식
    - 부모요소 : 그 요소를 포함하는 가장 가까운 상위 요소로, 그 요소의 부모는 단 하나이다.
    - 자식요소 : 부모요소의 반대로 자식요소는 여러개일 수 있다.
  - 조상과 자손
    - 조상요소 : 그 요소를 포함하는 모든 요소로 부모 요소를 포함하여 여러 개일 수 있다.
    - 자손요소 : 조상요소의 반대이다.
  - 형제 : 같은 부모를 가지고 있는 요소들은 서로 형제 관계에 있다.
  ```html
    <html>
  <body>
      <div>
          <h1><span>HTML</span>: Hyper Text Markup Language</h1>
      </div>
      <p>HTML과 CSS와 JAVASCRIPT를 이용해서 멋진 웹 사이트를 제작할 수 있습니다.</p>
  </body>
  </html>
  ```
- 문서 구조 관련 선택자  
  - 자손 선택자 : ```div span{color : red ;}```
    - 아무 기호없이 그냥 공백으로 구분한다.(div의 자손인 span을 선택)
  - 자식 선택자 : ```div>h1 {color : red;}```
    - 꺽쇠 기호(>)를 이용한다. (div의 자식요소 h1을 선택)
  - 인접형제 선택자 : ```div+p{color : red;}```
    - 형제 관계이면서 바로 뒤에 인접해 있는 요소를 선택하는 선택자이다.(div의 형제요소 p 선택)