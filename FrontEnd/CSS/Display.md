# DISPLAY
### 요소의 rendering box 유형을 결정
- ```display:value;```
  - block : 한 줄 전체를 해당하게 되는 요소로 렌더링
  - inline : 각각의 요소가 자동으로 위치가 맞춰져 해당되는 렌더링
  - inline-block : block의 속성을 가지나 inline 처럼 배치가 됨.
- inline 은 width height 값을 할당하지 못하고, margin padding border 가 좌우에만 적용이 된다.
- inline의 개행은 4px의 여백을 가지게 된다.
***
- ```visibility:value;```
  - visible : 기본값
  - hidden : 공간은 차지하나 화면에는 표시되지 않음(vs. ```display : none```)
  - collaapse : 셀 간의 경계를 무시하고 숨김
***
- ```float : value;```
  - none : 기본값
  - left/right : 좌 우측으로 float 시킴
  - float는 부모기준으로 (left/right)에 따라 띄워지게한다.
  - 주변 텍스트나 인라인 요소가 주위를 감싸게되는 특징이 있다.
  - float로 속성을 주면 display 속성이 block으로 변하게 된다.
- ```clear : value;``` : 요소를 floating 된 요소의 영향에서 벗어나게 한다.
  - none : 기본값
  - left/right/both : 왼쪽/오른쪽/양쪽 float 요소의 영향에서 벗어남
  - display : block 인 요소만 가능하다.