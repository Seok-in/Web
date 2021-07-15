# 콘텐츠 모델(Content Models)
### HTML5 에는 요소들이 가지고 있는 성격에 따라 요소의 종류를 정의하는 규칙들이 있다. 요소는 이 규칙들을 준수해야 하며, 반드시 HTML 권고안을 따라야한다. 이런 규칙에 대해 비슷한 성격의 요소들끼리 그룹화한 것이 콘텐츠 모델이며, 각각의 요소들은 하나 또는 여러 개의 콘텐츠 모델에 속하게 된다.
***
- Metadata : ```base, link, meta, noscript, script, style, title (Head 태그 내 포함)```
  - 콘텐츠의 style, script 를 설정하거나 다른 문서와의 관계 등의 정보를 포함하는 요소
- Flow : ``` a, abbr, address,map>area, article, aside,audio, b, bdo, blockquote,br, button,
canvas, cite, code, datalist, del, details, dfn, div, dl, em, embed,
fieldset, figure, footer, form, h1 ~ h6, header, hgroup, hr, i, iframe, img,
 input, ins, kbd, keygen, label, map, mark, math, menu, meter, nav, noscript, object, ol,
output, p, pre, progress, q, ruby, samp, script, section, select, small, span, strong,
style[scoped], sub, sup, svg, table, textarea, time, ul, var, video, wbr ```

    - Flow에는 문서의 자연스러운 흐름에 의해 배치되는 요소들이 포함된다.
    - Metadata에 해당하는 일부 태그들만 Flow에서 제외되며 요소 대부분이 Flow에 포함 된다.

- Sectioning : ```article, aside, nav, section```
  - 문서의 구조와 관련된 요소들이 포함되며 문서의 구조, 아웃라인에 영향을 주게 된다.
- Heading : ```h1,h2,h3,h4,h5,h6```
  - 각 Section의 header를 정의하는 heading 태그가 포함된다.
- Phrasing :```a, abbr, map>area, audio, b, bdo, br, button, canvas, cite, code, datalist, del, dfn, em, embed,
 i, iframe, img, input, ins, kbd, keygen, label, map, mark, math, meter, noscript, object, output,
 progress, q, ruby, samp, script, select, small, span, strong, sub, sup, svg, textarea, time,
var, video, wbr```
    - 문서의 텍스트 또는 텍스트를 꾸며주는 문단 내부 레벨로 사용되는 요소들이 포함.
- Embedded : ```audio, canvas, embed, iframe, img, math, object, svg, video```
  - 외부 콘텐츠를 포함하는 요소들이 포함되며 오디오나 비디오 이미지 등의 멀티미디어 관련요소들이 해당된다.
- Interactive : ``` a, audio[controls], button, details, embed, iframe, img[usemap], input, keygen, label, menu,
object[usemap], select, textarea, video[controls] ```
    - 사용자와 상호작용을 하는 요소들이 포함되며 form 요소들이 이에 해당된다.