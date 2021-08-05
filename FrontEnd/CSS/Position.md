# Position 속성
### 요소의 위치를 정하는 방법을 지정하는 속성
- ```position: value;```
  - static : 기본 흐름에 따라 배치되며 offset이 적용되지 않는다.
  - absolute : 부모 요소의 위치를 기준으로 offset에 따라 배치된다.
    - relative 로 속성을 가지는 부모가 기준이 되며 없을 시 body가 기준이 된다.
    - 부모요소의 border를 제외하고 padding 영역부터 기준이 된다.
  - relatvie : 자신이 원래 있어야 할 위치를 기준으로 offset에 따라 배치된다.
    - 주변 요소에 영향을 주지 않으면서 위치하게 된다.
  - fixed : 뷰포트(브라우저)를 기준으로 offset에 따라 배치된다.

# Z-Index 속성
### 요소가 겹치는 순서를 지정하는 속성
- ```z-index : value;```
  - auto : 기본값
  - number : 해당 수치로 순서 설정(음수허용)
  - position 값이 static이 아닌 경우 지정가능
  - 순서 값이 없을 경우 생성순서에 따라 쌓임
  - 부모가 z-index 값이 있을경우 부모 안에서만 의미 있음
  - 큰 값이 가장 위쪽