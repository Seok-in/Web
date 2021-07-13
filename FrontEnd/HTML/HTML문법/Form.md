# 폼 관련 요소(Form)
### 서버에 데이터를 전달하기 위한 요소를 폼(Form) 요소 라고 한다.
- Input 요소
  - 대표적인 폼 요소로, 다양한 type 속성으로 여러 종료의 입력 양식으로 나타난다.
  - ```<input type = "...">``` 방식으로 쓴다.
    - ```<input type = "text" placeholder = "">``` :  간단한 텍스트를 입력할 때 사용을 하며 placeholder라는 속성은 입력전에 미리 화면에 노출하는 값이다.
    - ```<input type = "password">``` : 암호와 같이 공개할 수 없는 내용을 입력할 때 사용한다.
    - ```<input type = "radio" name = "gender">``` : 라디오버튼을 만들 때 사용한다.(중복X) name이라는 속성을 통해서 같은항목으로 묶어 중복이 안되게 할 수 있다.
    - ```<input type = "checkbox" name ="hobby">``` :체크박스를 만들 때 사용한다.(중복O)     
    - ```<input type = "file">``` : <input type = "file"> 처럼 쓰이고 파일을 서버에 올릴 때 사용한다.
  - Input Button 타입
    - ```<input type = "submit">``` : <input type = "submit"> 으로 form의 값을 전송
    - ```<input type = "reset">```: <input type = "reset"> 으로 값 초기화
    - ```<input type = "image" src="" alt="" width="" height="">```: <input type = "image"> 으로 submit과 동일
    - ```<input type= "button">```: <input type= "button"> 으로 아무 기능없는 버튼
    - value 속성을 이용해서 보여주는 내용을 표시해줄 수 있다.
***
- Select 요소
  - 선택 목록상자(콤보박스)의 양식을 갖는다.
  - 몇 개의 선택지를 리스트 형태로 노출하고 그중 하나를 선택할 수 있게하는 태그(multiple 속성을 이용하면 다중 선택도 가능)
  - ```<option>```을 자식으로 가지며 option에는 selected를 통해 먼저 표시되는 값을 checked 할 수 있다.
  - 예시) <select>
             <option>서울</option>
             <option>경기</option>
             <option selected>강원</option>
         </select>
   ```html
   <select>
       <option>서울</option>
       <option>경기</option>
       <option selected>강원</option>
  </select>
  ```
  ***
- TextArea 요소
    - 여러 줄의 텍스트 입력상자이다.
    - 텍스트 상자의 크기를 조절하는 rows, cols 속성이 있다.
      - cols : 가로 크기를 조절하는 속성(영문기준으로 글자 수)
      - rows : 세로 크기를 조절하는 속성
    - 예시)<textarea cols="30" rows ="5" placeholder = "예시"></textarea>
    - ```<textarea cols="30" rows ="5" placeholder = "예시"></textarea>```
***
- Button 요소
  - 사용자가 클릭 가능한 버튼이다.
  - <button type = "button">버튼예시</button> ```<button type = "">버튼예시</button>```
  - type 속성에는 submit, reset, button 과 같은 기능을 가진다.
  - 빈 태그가 아니여서 내용을 안에 직접 넣을 수 있으므로 좀 더 자유로운 스타일 표현이 가능하다.
***
- Label 요소
  - form 요소의 이름과 form 요소를 명시적으로 연결시켜주기 위해 사용한다.
  - 웹접근성 향상에 도움이 된다.(필수적)<br>
  ```<label for="userid">아이디</label>:<input type="text" id="userid"```
  - form 요소의 id 속성값과 label의 for 속성 값을 같게 적어주어야한다.
  - label 클릭 시에 해당 form 요소를 클릭한 것처럼 동작한다.
***
- Fieldset, Legend 요소
  - ```<filedset>``` : 여러 개의 폼 요소를 그룹화하여 구조적으로 만들기 위해 사용
  - ```<legend>``` : 폼 요소의 제목으로 ```<fieldset>```요소 내부에 작성
***
- form 요소
  - 폼 데이터를 그룹화하여 서버에 전송한다.
  - action : 폼데이터를 처리하기 위한 서버의 주소
  - method: 데이터를 전송하는 방식을 지정(get, post)
    - get : 데이터가 전송될 때 주소창에 파라미터 형태로 붙어 데이터가 노출됨
    - post : 데이터가 전송될 때 데이터가 노출되지 않는다.