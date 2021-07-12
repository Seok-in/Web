# Tag의 종류2
- 리스트
  - UL ```<ul>``` : unordered list로 순서가 없는 리스트
  ```html
  <body>
      <ul>
          <li>콩나물</li>
          <li>파</li>
        </ul>
    </body>
    ```
  - OL ```<ol>``` : ordered list로 순서가 있는 리스트
    ```html
    <body>
      <ol>
          <li>콩나물</li>
          <li>파</li>
        </ol>
    </body>
    ```
    - 숫자로 표현됨.
  - DL ```<dl>``` : description list 로 용어를 설명하는 리스트
    -```<dt>``` : definition term으로 용어를 구분한다.
    -```<dd>``` : definition description으로 용어의 정의를 나타낸다.
    ```html
    <body>
        <dl>
            <dt>리플리 증후군</dt>
            <dd>허구의 세계를 ...</dd>
            <dd>허구의 세계를 ... 2</dd>
            <dt>피그말리온 효과</dt>
            <dd>허구의 세계를 ...</dd>
        </dl>
    </body>
    ```
  - 리스트의 중첩
    - ```<ol>``` 태그 내에는 ```<li>``` 태그만 올 수 있으나 ```<li>```태그내에는 자식으로 다 올 수 있다.
    ```html
    <body>
      <ol>
          <li>콩나물
              <ul>
                  <li>콩</li>
                  <li>나물</li>
              </ul>
          </li>
          <li>파</li>
        </ol>
    </body>
    ```