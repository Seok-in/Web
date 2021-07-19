# CSS(Cascading Style Sheet)
- HTML(마크업 언어)를 꾸며주는 언어
- html이 웹페이지의 정보를 표현한다면 CSS는 html을 보기 좋게 디자인하는 역할
***
### CSS 문법
```h1 {color : yellow; font-size:2em;}```
- 선택자(selector) : h1
- 속성(property) : color, font-size
- 값(value) : yellow, 2em
- 선언(declaration) : color : yellow ;
- 선언부(declaration block) :```{color : yellow; font-size:2em;}```
- 규칙(rule set) : ```h1 {color : yellow; font-size:2em;}```
***
### CSS의 속성과 HTML 속성
##### 두 가지는 전혀 다르다. HTML 속성은 Attribute이고 CSS 속성은 Property 이다.
***
### CSS 주석
```/* 주석내용*/```
***
### ⭐CSS 적용방식
- Inline
  - ```<div style ="color : gray;">내용</div>```\
  - 자주 사용되지 않음
- Internal
  - ```<style> p{ color : gray;} </style>```
  - ```<head>``` 태그에 구현한다.
- External
  - 별도의 css파일을 만들어서 넣는 방식
  ```css
  p{
      color : gray;
   }
    ```
    - ```<head>``` 태그 내에 ```link rel = "stylesheet" href = "css/style.css"``` 선언하여 구성한다.
    - 관리 및 용량관리가 용이하여 자주 사용한다.
- @import
    - 성능이 별로 좋지않아 자주 쓰이지 않음