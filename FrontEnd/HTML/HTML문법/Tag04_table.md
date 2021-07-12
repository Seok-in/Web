# Tag의 종류 4
- 테이블 요소(Table)
  - 데이터 표를 나타내는 태그이다.(row 행 , column 열)
  - ```<td>```, ```<th>``` : 데이터 셀
    - td 는 하나의 행에 들어가는 데이터 셀이다.
    - th: 제목 행을 나타낼때 씀. (td보단 조금 굵음)
  - ```<tr>```: 행(table-row)
  - ```<table>``` : 표
  - ```<caption>``` : 표의 제목
  - ```<thread>``` : 제목 행을 그룹
  - ```<tfoot>``` : 바닥 행을 그룹
  - ```<colspan>``` : 셀을 가로방향으로 병합
  - ```<rowspan>``` : 셀을 세로방향으로 병합
  ```HTML
  <body>
      <table>
          <caption>Monthly Savings</caption>
          <thead>
              <tr>
                  <th>Month</th>
                  <th>Savings</th>
              </tr>
          </thead>
          <tfoot>
              <tr>
                  <td  colspan = "2">Sum</td>
              </tr>
          <tbody>
              <tr><td>January</td><<td>>$100</td></tr>
              <tr><td>February</td><<td rowspan = "2">>$80</td></tr>
              <tr><td>March</td></tr>
    ```
***
- 테이블 만들기 예제
<style>
    th, td {border : 1px solid; width : 50px; height:50px}
</style>
<table>
    <caption>Specification values</caption>
    <thead>
        <tr>
            <th rowspan = "2">Grade.</th>
            <th rowspan = "2">Point.</th> 
            <th colspan = "2">Strength.</th>
            <th rowspan = "2">Percent.</th>
        </tr>
        <tr>
            <th>kg/mm</th>
            <th>lb/in</th>
        </tr>
    </thead>
    <tfoot>
        <tr>
            <td>Soft</td>
            <td>0.45</td>
            <td>42.2</td>
            <td>60,000</td>
            <td>30</td>
        </tr>
    </tfoot>
    <tbody>
        <tr>
            <td>Hard</td>
            <td>0.45</td>
            <td>56.2</td>
            <td>80,000</td>
            <td>20</td>
        </tr>
        <tr>
            <td>Medium</td>
            <td>0.45</td>
            <td>49.2</td>
            <td>70,000</td>
            <td>25</td>
        </tr>
    </tbody>
</table>


```HTML
    <style>
        th, td {border : 1px solid; width : 50px; height:50px}
    </style>
    <table>
        <caption>Specification values</caption>
        <thead>
            <tr>
                <th rowspan = "2">Grade.</th>
                <th rowspan = "2">Point.</th> 
                <th colspan = "2">Strength.</th>
                <th rowspan = "2">Percent.</th>
            </tr>
            <tr>
                <th>kg/mm</th>
                <th>lb/in</th>
            </tr>
        </thead>
        <tfoot>
            <tr>
                <td>Soft</td>
                <td>0.45</td>
                <td>42.2</td>
                <td>60,000</td>
                <td>30</td>
            </tr>
        </tfoot>
        <tbody>
            <tr>
                <td>Hard</td>
                <td>0.45</td>
                <td>56.2</td>
                <td>80,000</td>
                <td>20</td>
            </tr>
            <tr>
                <td>Medium</td>
                <td>0.45</td>
                <td>49.2</td>
                <td>70,000</td>
                <td>25</td>
            </tr>
        </tbody>
    </table>
```
  - ❓❓❓
    - ```<colgroup>``` : 테이블에서 서식 지정을 위해 하나 이상의 열을 그룹으로 묶을 때 사용
    - ```<col>``` : 테이블 하나 이상의 열 TD에 대하여 속성 값을 정의
    - scope : 테이블의 th 또는 td 등의 해당 셀에게 사용하며 컬럼인지 행인지의 여부를 알려주는 역할. 시각 장애인용 리더기를 통해 읽어지는 경우 해당하는 속성값에 따라 어떤 순서로 읽을지 결정
    - headers : ```<td>``` 태그의 headers 속성은 해당 데이터 셀과 연관된 하나 이상의 헤더 셀을 명시