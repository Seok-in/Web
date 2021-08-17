# CSS - IR
### IR(Image Replacement) : 이미지를 볼 수 없는 사용자에게 적절한 대체 텍스트를 제공하는 것.
##### <img> 태그의 alt 속성값으로 표현하기에 대체 텍스트가 너무 길거나, CSS Background 속성을 사용하여 처리한 의미있는 이미지일 경우, 마크업으로 대체 텍스트를 제공한다.
- 여러가지 방식이 있으나 가장 좋은 방식은 아래와 같다.
  - 하나의 클래스로 숨김텍스트 지정
```HTML
<span class = "blind">숨김 텍스트</span>
```

```CSS
.blind{
    position : absolute;

    width : 1px;
    height : 1px;

    clip:rect(0 0 0 0);
    margin:-1px;
    overflow : hidden;
}
```
#### clip:rect(top right bottom left); : position 속성 값이 absolute/fixed인 요소에 네개의 지정한 좌표로 요소를 잘라내는 속성이다.