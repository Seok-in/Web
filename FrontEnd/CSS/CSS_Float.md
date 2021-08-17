# CSS -Float해제
- Float의 특성
  - 요소를 보통의 흐름에서 벗어나 띄워지게 함.
  - 주변 텍스트나 인라인 요소가 주위를 감싸는 특징이 있음.

- Float의 해제
  - 부모요소의 height 부여 : 부모요소를 자식 요소의 높이값 만큼 늘려 눈속임효과를 줌.
  - 부모의 요소의 float 속성 부여 
  - overflow : hidden : 팝업창이 보이지 않음.
  - 인접 형제 요소의 clear속성 이용 : 빈태그 이용으로 번잡
  - 💡 가상요소를 이용한 clear속성 이용(가장 좋음)
    ```css
    .box_parent:after{/*after를 이용하여 인접오쇼로 구성하여 해제*/
        display:block;
        clear:both;
        content:"";
    }
    ```