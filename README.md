HTML 연습 파일 총정리
01_hellowworld.html — 기본 HTML 뼈대
<!DOCTYPE html>

HTML5 문서라고 브라우저한테 선언하는 것. 항상 맨 첫 줄에 써야 함.
<html lang="en">

문서 전체를 감싸는 최상위 태그. lang="en"은 이 문서의 언어가 영어라는 뜻. 한국어면 lang="ko"로 써야 함.
<head>

브라우저한테 필요한 정보를 담는 곳. 화면에 직접 보이지는 않음.
<meta charset="UTF-8" />

문자 인코딩 설정. UTF-8 써야 한글이 깨지지 않음. 필수!
<meta name="viewport" content="width=device-width, initial-scale=1.0" />

모바일 화면 대응용. 화면 너비를 디바이스 너비에 맞추고, 처음 zoom은 1배율로 시작.
<title>연습하장</title>

브라우저 탭에 표시되는 제목.
<body>
  <h2>주현이 </h2>
</body>
body 안에 실제로 화면에 보이는 내용을 씀.

02_basic.html — 기본 태그들
<h1>머릿말1</h1> ~ <h6>머리말6</h6>
제목 태그. h1이 제일 크고 h6이 제일 작음. 글씨 크기뿐 아니라 중요도도 나타냄.

<p>첫번째 문장입니다.</p>
문단(paragraph) 태그. 문장 쓸 때 사용.

<a href="https://naver.com">네이버</a>
링크 태그. href에 이동할 주소 넣음. 클릭하면 그 주소로 이동.

<a href="./01_hellowworld.html">01_helloword_html</a>
외부 사이트뿐 아니라 내 컴퓨터 파일로도 링크 가능. ./는 현재 폴더를 의미함.

<img src="https://..." alt="" />
이미지 태그. src에 이미지 주소, alt에 이미지 설명 텍스트 (이미지 못 불러올 때 나옴, 스크린리더기도 읽어줌).

03_global_attribute.html — 전역 속성
전역 속성 = 거의 모든 HTML 태그에 사용 가능한 속성들

<h1 draggable="true">움직일 수 있는 태그</h1>

draggable="true" : 마우스로 끌어서 이동 가능하게 함.
<p lang="ko">대한민국</p>

lang : 특정 요소의 언어 지정. 번역이나 스크린리더에 영향 줌.
<p hidden>이 문장은 화면에 보이지 않습니다.</p>

hidden : 요소를 화면에서 숨김. 공간도 차지 안 함.
<a href="https://google.com" id="google" title="클릭하면 구글로 이동됨">구글</a>

id : 요소의 고유 이름 (중복 불가). CSS나 JS에서 이 요소를 콕 찍어서 사용할 때 씀.
title : 마우스 올리면 말풍선으로 설명이 뜸.
<label for="userId">사용자 아이디</label>
<input type="text" id="userId" />

label의 for와 input의 id를 같게 하면, 라벨 클릭해도 input이 활성화됨. 접근성에 중요!
<p spellcheck="true" contenteditable="true">This is a paraggraph</p>

spellcheck="true" : 철자 오류 밑줄 표시.
contenteditable="true" : 브라우저에서 직접 텍스트 수정 가능.
<p style="color: red; background-color: yellow">빨간색 문장입니다.</p>

style : 인라인으로 직접 CSS 스타일 적용.
<a href="" tabindex="1">네이버</a>
<a href="" tabindex="3">구글</a>
<a href="" tabindex="2">개발자의 품격</a>

tabindex : Tab 키로 이동할 순서 지정. 숫자 순서대로 이동함. (1 → 2 → 3)
04_local_attribute.html — 지역 속성
지역 속성 = 특정 태그에서만 사용 가능한 속성들

<a href="https://google.com" target="_blank">구글</a>

target="_blank" : 링크를 새 탭에서 열기. (_self는 현재 탭, 기본값)
<img src="./img/devlogo.png" width="100px" height="auto" alt="">

width, height : 이미지 크기 지정. height="auto" 하면 비율 유지하면서 너비에 맞게 자동 조절.
05_style.html — CSS 스타일 적용 방법
<style>
  /* 주석 ctrl + 슬래시 */
</style>

CSS 파일 없이 HTML 안에 스타일 쓰는 방법 = 인터널 스타일
/* */ 로 주석 작성
스타일 적용 방법 3가지:

인라인 스타일 : 태그 안에 직접 style="..." 쓰는 것
인터널 스타일 : <style> 태그 안에 작성
익스터널 스타일 : 별도 .css 파일로 만들어서 연결 (실무에서 주로 이 방식)
<p style="font-size: 30px">큰 사이즈 글자입니다.</p>
<p style="text-align: center">가운데 정렬입니다.</p>
<p style="text-align: right">오른쪽 정렬</p>
<p style="font-weight: bold">볼드체(굵은)로 보입니다.</p>
<p style="text-decoration: underline">밑줄이 생깁니다.</p>
<p style="text-decoration: line-through">취소선 생깁니다.</p>
<p style="font-style: italic">이탤릭체로 보여집니다.</p>

속성	의미
font-size: 30px	글자 크기
text-align: center	가운데 정렬
text-align: right	오른쪽 정렬
font-weight: bold	굵은 글자
text-decoration: underline	밑줄
text-decoration: line-through	취소선
font-style: italic	이탤릭체
06_meaningful.html — 의미 있는 태그 vs 의미 없는 태그
<p style="font-weight: bold">볼드체</p>  <!-- 스타일만 있음 -->
<b>볼드체</b>                            <!-- 스타일만 있음 -->
<strong>강조하는 볼드체</strong>          <!-- 의미 있음! 스크린리더가 강하게 읽어줌 -->

b vs strong : 둘 다 굵게 보이지만 strong은 **"중요하다"**는 의미를 가짐. 스크린리더가 강조해서 읽어줌.
<i>이탤릭체</i>
<em>강조하는 이탤릭체</em>

같은 원리. em이 의미 있는 강조.
<small>작게</small>
<mark>우유</mark>               <!-- 형광펜 효과, 배경 노란색 -->
<del>3만원</del>               <!-- 취소선 - "삭제된 내용"이라는 의미 -->
<ins>노란색</ins>              <!-- 밑줄 - "추가된 내용"이라는 의미 -->
<sub>2</sub>                   <!-- 아래첨자: X₂ -->
<sup>2</sup>                   <!-- 위첨자: X² -->

<blockquote cite="출처URL">긴 인용문...</blockquote>
<q>짧은 인용</q>

blockquote : 블록 형태의 긴 인용문
q : 인라인 짧은 인용문
<abbr title="world health organization">who</abbr>

약자(abbreviation). 마우스 올리면 전체 이름이 뜸.
<address>대한민국 제주특별자치도 ...</address>

주소를 나타내는 태그. 이탤릭체로 표시됨.
<cite>절규</cite>

작품명(책, 영화, 노래 등) 나타낼 때 사용.
<div style="background-color: blue">div 태그</div>
<span style="background-color: green">span 태그</span>

div : 의미 없는 블록 컨테이너. 한 줄 전체 차지.
span : 의미 없는 인라인 컨테이너. 자기 크기만큼만 차지.
둘 다 레이아웃 잡을 때 많이 씀.
블록 요소 vs 인라인 요소:

블록 : div, h1~h6, p → 한 줄 전체 차지
인라인 : span, a, img → 자기 크기만큼만 차지
07_list.html — 목록 태그
<ul>
  <li>에스프레소</li>
  <li>아메리카노</li>
</ul>

ul (unordered list) : 순서 없는 목록. 점(•)으로 표시.
<ol>
  <li>비주얼스튜디오코드 설치</li>
  <li>node.js 설치</li>
</ol>

ol (ordered list) : 순서 있는 목록. 숫자(1, 2, 3...)로 표시.
<dl>
  <dt>html</dt>
  <dd>- 웹 페이지 개발을 위한 마크업 언어</dd>
  <dt>css</dt>
  <dd>- 웹 페이지 디자인을 위한 언어</dd>
</dl>

dl (description list) : 설명 목록
dt (define term) : 용어 정의
dd (description) : 용어 설명
08_table.html — 표(테이블)
<style>
  table, td, th {
    border: 1px solid black;
    border-collapse: collapse;
  }
  table { width: 100%; }
</style>

border-collapse: collapse : 셀 사이 테두리를 하나로 합침. 안 쓰면 이중선으로 보임.
<table>
  <thead>
    <tr>
      <th>이름</th>  <!-- 열 제목 -->
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>유재석</td>  <!-- 데이터 -->
    </tr>
  </tbody>
</table>

태그	의미
table	표 전체
thead	제목 행들 묶음
tbody	데이터 행들 묶음
tfoot	합계 등 마지막 행 묶음
tr	행(가로줄)
th	열 제목 셀 (굵게, 가운데 정렬)
td	데이터 셀
<td rowspan="3">1학년</td>

rowspan="3" : 세로로 3칸 합치기
<td colspan="2">합계</td>

colspan="2" : 가로로 2칸 합치기
09_from_element.html — 폼 입력 요소들
<input type="checkbox" name="chk_lang" id="chk_html" />

체크박스 : 여러 개 선택 가능. 같은 name으로 묶음.
<input type="radio" name="rdo_lang" id="rdo_html" />

라디오버튼 : 같은 name 그룹에서 하나만 선택 가능.
<input type="color" id="favoriteColor" />
<input type="date" id="bornDate" />
<input type="datetime-local" id="arrivalDateTime" />
<input type="email" id="email" />
<input type="file" id="attachment" />
<input type="hidden" name="email" value="john@gmail.com" />
<input type="image" src="./img/devlogo.png" />
<input type="month" id="yearmonth" />
<input type="number" min="0" max="100" />
<input type="password" id="userpass" />
<input type="tel" pattern="^010-\d{4}-\d{4}$" />
<input type="text" id="general" />
<input type="time" id="visitTime" />
<input type="url" />
<input type="week" id="weekplan" />
<input type="search" id="searchkeyword" />

type	역할
color	색상 선택기
date	날짜 선택기
datetime-local	날짜+시간 선택기
email	이메일 형식 검사
file	파일 첨부
hidden	화면에 안 보이는 값 (개발자용)
image	이미지 버튼
month	년월 선택기
number	숫자 입력 (min/max 가능)
password	입력 내용 숨김
tel	전화번호 (pattern으로 형식 검사)
text	일반 텍스트
time	시간 선택기
url	URL 형식 검사
week	주차 선택기
search	검색창 (X 지우기 버튼 생김)
10_input_attribute.html — input 속성들
<input type="text" value="abc" />

value : 미리 입력된 값
<input type="text" value="ABC" readonly />

readonly : 읽기 전용. 수정 불가, 서버에는 전송됨.
<input type="text" value="abc" disabled />

disabled : 비활성화. 수정 불가, 서버에 전송 안 됨.
<input type="text" maxlength="6" />

maxlength : 최대 입력 글자 수 제한.
<input type="tel" placeholder="하이픈(-) 없이 숫자만 입력하세요" />

placeholder : 입력 전에 보이는 힌트 텍스트. 입력하면 사라짐.
<input type="text" required autocomplete="on" autofocus="on" />

required : 필수 입력 (비우면 제출 안 됨)
autocomplete="on" : 이전에 입력했던 값 자동 완성 제안
autofocus : 페이지 로드되면 이 입력창이 자동으로 포커스됨 (바로 타이핑 가능)
11_form_other.html — 기타 폼 요소들
<select name="" id="" multiple>
  <option value="02">서울</option>
  <option value="051">부산</option>
</select>

select : 드롭다운 선택. multiple 속성 있으면 여러 개 선택 가능 (Ctrl+클릭).
option의 value : 실제로 서버에 전송되는 값.
<textarea style="width: 100%" rows="10"></textarea>

여러 줄 텍스트 입력창. rows로 줄 수 지정.
<fieldset>
  <legend>학력정보</legend>
  <input type="text" />
</fieldset>

fieldset : 관련된 입력들을 박스로 묶음.
legend : 그 박스의 제목.
<input list="browsers" />
<datalist id="browsers">
  <option value="chrome">chrome</option>
  <option value="firefox">firefox</option>
</datalist>

datalist : 텍스트 입력하면서 추천 목록이 나오는 자동완성. input의 list와 datalist의 id를 같게 연결.
12_form.html — form 태그와 GET/POST
<form action="전송할 서버주소" method="get" target="_self" novalidate>

속성	의미
action	데이터 보낼 서버 주소
method	전송 방식 (get / post)
target	어느 창에서 응답받을지
novalidate	form 안 input들의 유효성 검사 건너뜀
GET vs POST:

GET	POST
데이터 위치	URL에 붙어서 감 (?name=주현)	숨겨서 전송
보안	취약 (URL에 노출)	상대적으로 안전
크기 제한	있음	없음
언제 씀	검색, 페이지 공유	로그인, 회원가입
<button type="submit">저장</button>

type="submit" : 폼 데이터를 action 주소로 전송.
13_iframe.html — 페이지 안에 다른 페이지 삽입
<iframe src="./13_iframe_contnet.html" id="ifram" frameborder="0"></iframe>

iframe : HTML 페이지 안에 다른 HTML 페이지를 끼워 넣기.
frameborder="0" : 테두리 없앰.
<a href="javascript:goToMenu('./13_iframe_contnet.html')">menu1</a>

<script>
  function goToMenu(path) {
    document.getElementById('ifram').src = path;
  }
</script>

메뉴 클릭 시 iframe의 src를 바꿔서 내용만 교체하는 방식.
<a href="https://naver.com" target="_top">Naver</a>

iframe 안에서 target="_top" 하면 iframe 안이 아니라 최상위 브라우저 창 전체로 이동.
14_video.html — 비디오
<video
  src="./mp4"
  width="320px"
  controls
  autoplay
  muted
  loop
  poster="./img/devlogo.png"
></video>

속성	의미
controls	재생/멈춤/볼륨 UI 표시
autoplay	자동 재생
muted	음소거 (autoplay 쓰려면 muted도 같이 써야 대부분 브라우저에서 작동)
loop	반복 재생
poster	재생 전 보여줄 썸네일 이미지
<track src="./media/bootcamp.ko.vtt" kind="subtitles" srclang="ko" label="한국어" />

자막 파일 연결. vtt 형식 사용.
15_audio.html — 오디오
<audio src="./media/mp3" controls></audio>

비디오랑 거의 같음. controls 쓰면 재생바 생김.
preload 속성:

auto : 미리 다운로드 (중요한 영상, 바로 재생해야 할 때)
metadata : 영상 길이 정보만 미리 가져옴
none : 아무것도 미리 안 함 (서버 트래픽 아끼고 싶을 때)
16_image_map.html — 이미지 맵
<img src="./img/ikea.png" usemap="#image-map">

<map name="image-map">
  <area href="https://..." coords="859,785,40" shape="circle" target="_blank" />
</map>

이미지의 특정 영역을 클릭하면 링크로 이동.
shape="circle" : 원형 영역. coords="x,y,반지름"
shape="rect" : 사각형. coords="x1,y1,x2,y2"
usemap과 map의 name을 #이름으로 연결.
17_semantic.html vs 17_semanticdiv.html — 시멘틱 태그
두 파일은 같은 레이아웃인데, 하나는 의미 있는 태그, 하나는 div만 사용.

semantic 버전:

<header>헤더</header>
<nav>메뉴들</nav>
<main>
  <section>
    <article>아티클1</article>
    <article>아티클2</article>
  </section>
</main>
<footer>footer</footer>

div 버전:

<div>헤더</div>
<div>메뉴들</div>
<div>
  <div>
    <div>아티클1</div>
    <div>아티클2</div>
  </div>
</div>
<div>footer</div>

결과는 똑같이 보이지만 시멘틱 태그를 써야 하는 이유:

이유	설명
SEO(검색 최적화)	구글 같은 검색엔진이 구조를 이해함
접근성	스크린리더가 내비게이션, 헤더 등 인식
가독성	코드 보는 사람이 구조 파악 쉬움
태그	의미
header	페이지/섹션의 머릿말
nav	메뉴 내비게이션
main	페이지의 주요 내용
section	주제별 묶음
article	독립적인 콘텐츠
footer	페이지 하단 정보
aside	사이드바
문제내서 맞추기.html — 복습 종합 문제
앞에서 배운 걸 직접 써본 파일. 잘 쓴 것들:

target="_blank" 새탭 링크
draggable="true" 드래그 가능
hidden 숨김 처리
ul / ol / dl 목록
rowspan / colspan 셀 합치기
tfoot으로 합계 행 처리
q 태그에 인라인 스타일로 꾸미기
신경 써볼 부분:

<dl>
  <ul>  <!-- dl 안에 ul은 올바른 구조가 아님. dl 안에는 dt, dd만 써야 함 -->
    <dt>...</dt>
    <dd><li>...</li></dd>  <!-- dd 안에 li도 잘못된 구조 -->
  </ul>
</dl>

dl 안에는 dt와 dd만 써야 함.
