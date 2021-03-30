# StudyMarkdown

## 4.10 표
GFM에서는 리프블록 타입이 가능한 곳에서 표를 만들수 있다.
표는 열과 헹으로 이루어진 데이터들의 집합이며, 하나의 헤더 줄과 헤더와는 분리되어있는 0개 이상의 delimeter 줄이 있다.
각 줄에는 인라인이 구문분석되고, 파이프(|)로 구분된 임의의  텍스트를 포함하는 셀로 구성된다. 가독성을 위해, 혹은 구문 분석의 모호성이 있을때 선행 및 후행 파이프도 권장된다. 파이프와 셀 내용 사이의 공간은 잘린다. 블록 레벨 요소는 테이블에 삽입되지 않는다.

구분 기호 행은 하이픈(-)과 선행 또는 후행 콜론(:) 또는 둘 다에 해당하는 셀로 구성되어 각각 왼쪽, 오른쪽 또는 가운데 정렬을 나타낸다.

`| foo | bar |  
| --- | --- |  
| baz | bim |`
는 다음처럼 나타난다.
| foo | bar |
| --- | --- |
| baz | bim |
