# Media Query
### 미디어쿼리는 각 미디어 매체에 따라 다른 스타일을 적용할 수 있도록 하는것
### 반응형 웹사이트를 제작하기 위해 이용한다.

-```@media medaqueries{/*style rules*/```}
- 미디어 타입 : all, print, screen
- 미디어 특성 : width, orientation (prefix : min-/max-)

***
## 예시
- @media screen { ... }
    : 미디어 타입이 screen이면 적용됩니다.

- @media screen and (min-width: 768px) { ... }
    : 미디어 타입이 screen이고 width가 768px 이상이면 적용됩니다. 두 개 중 하나라도 만족하지 않으면 거짓이 됩니다.

- @media (min-width: 768px) and (max-width: 1024px) { ... }
    : and는 연결된 모든 표현식이 참이면 적용됩니다.(and 키워드는 연결된 부분이 모두 참이어야 적용이 됩니다.)

- @media (color-index)
    : 미디어 장치가 color-index를 지원하면 적용됩니다.

- @media screen and (min-width: 768px), screen and (orientation: portrait), ...
    : 쉼표로 연결된 미디어 쿼리 중 하나라도 참이면 적용됩니다.( and 키워드와 반대라고 생각하면 됩니다.)

- @media not screen and (min-width: 768px)
    : not 키워드는 하나의 media_query 전체를 부정합니다.
    : (not screen) and (min-width: 768px) 잘못된 해석!
    : not (screen and (min-width: 768px)) 올바른 해석!
    : @media not screen and (min-width: 768px), print
       첫 번째 미디어 쿼리에만 not 키워드가 적용되며, 두 번째 미디어 쿼리(print)에는 영향이 없습니다.
***
## Viewport
- 0 ~ 767px : mobile phone
- 768 ~ 1024px : tablet
- 1024px ~ : desktop

- Viewport 설정 : ```<meta name = "viewport" contetn = "뷰포트 설정값">```
  - content 설정값
    - width(height) : 뷰포트의 가로(세로) 크기를 지정(device-width(height))
    - initial-scale : 페이지가 처음 나탈 때 초기 줌 레벨 값 설정
    - user-scalable : 사용자의 확대 축소기능 설정
- 대부분의 모바일 웹사이트 뷰포트 설정<br>
```<meta name = "viewport" content="width =device-width, initial-scale=1.0">```