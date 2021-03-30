# GFM의 기능중 확장된 것들을 정리해두었다.

## 4.10 표
GFM에서는 리프블록 타입이 가능한 곳에서 표를 만들수 있다.<br>
표는 열과 헹으로 이루어진 데이터들의 집합이며, 하나의 헤더 줄과 헤더와는 분리되어있는 0개 이상의 delimeter 줄이 있다.<br>
각 줄에는 인라인이 구문분석되고, 파이프(|)로 구분된 임의의  텍스트를 포함하는 셀로 구성된다. 가독성을 위해, 혹은 구문 분석의 모호성이 있을때 선행 및 후행 파이프도 권장된다. <br>파이프와 셀 내용 사이의 공간은 잘린다. 블록 레벨 요소는 테이블에 삽입되지 않는다.<br>

구분 기호 행은 하이픈(-)과 선행 또는 후행 콜론(:) 또는 둘 다에 해당하는 셀로 구성되어 각각 왼쪽, 오른쪽 또는 가운데 정렬을 나타낸다.

`| foo | bar |` <br>
`| --- | --- |` <br>
`| baz | bim |` <br>
는 다음처럼 나타난다.
| foo | bar |
| --- | --- |
| baz | bim |<br>



한 열의 셀은 길이가 일치할 필요는 없지만, 가독성을 위해서 맞춰주는 것이 좋다.<br>
`| abc | defghi |`<br>
`:-: | -----------:`<br>
`bar | baz`<br>


| abc | defghi |
:-: | -----------:
bar | baz


파이프를 셀에 넣으려면 백슬래시를 파이프 앞에 두면 된다.
다음의 예시는 <br>
`| f\|oo  |`<br>
`| ------ |`<br>
`| b `\|` az |`<br>
`| b **\|** im |`<br>
이렇게 나타난다.<br>
| f\|oo  |
| ------ |
| b `\|` az |
| b **\|** im |


## 5.3 체크박스
GFM에서는 체크박스를 이용하여 동적 상호작용을 할 수 있도록 해준다. (즉, 체크 표시/해제 를 가능하게 해준다.)<br>
`- [ ] foo` <br>
`- [x] bar` <br>
는 다음과 같이 나타난다.<br>
- [ ] foo <br>
- [x] bar <br>

## 6.5 취소선
GFM은 취소선기능을 지원한다.<br>
글자의 앞뒤로 물결표를 넣어 쓰면 된다.<br>
다음 문장처럼 나온다.<br>
~~나무위키에서 자주 보던 기능이다.~~<br>

새로운 단락이 생기면 취소선이 끊기게 된다.

## 6.9 오토링크
깃허브에서는 유효한 도메인에 대해 url을 자동으로 만들어준다. <br>
이메일도 마찬가지로 자동으로 링크가 생성된다.<br>
이때 이메일과 도메인은 각각의 규칙에 의해 인식된다.<br>
https://tempnixk.tistory.com/<br>
chm49@naver.com<br>

## 6.11 Raw HTML 허용 안함.
GFM에서는 HTML 출력을 렌더링할때, 태그를 필터링한다.
<title> <br>
<textarea> <br>
<style> <br>
<xmp> <br>
<iframe> <br>
<noembed> <br>
<noframes> <br>
<script> <br>
<plaintext> <br>
위의 HTML 태그들은 필터링 되어 GFM고유의 방식으로 렌더링된다. <
다른 태그들은 필터링되지 않는다.
