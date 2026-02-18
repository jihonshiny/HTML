#  HTML 연습 정리

> 처음부터 하나하나 직접 연습한 HTML 파일들 정리본

---

## 목차

- [01 Hello World - 기본 뼈대](#01-hello-world---기본-뼈대)
- [02 Basic - 기본 태그](#02-basic---기본-태그)
- [03 Global Attribute - 전역 속성](#03-global-attribute---전역-속성)
- [04 Local Attribute - 지역 속성](#04-local-attribute---지역-속성)
- [05 Style - CSS 적용 방법](#05-style---css-적용-방법)
- [06 Meaningful - 의미 있는 태그](#06-meaningful---의미-있는-태그)
- [07 List - 목록 태그](#07-list---목록-태그)
- [08 Table - 표](#08-table---표)
- [09 Form Element - 폼 입력 요소](#09-form-element---폼-입력-요소)
- [10 Input Attribute - input 속성](#10-input-attribute---input-속성)
- [11 Form Other - 기타 폼 요소](#11-form-other---기타-폼-요소)
- [12 Form - GET / POST](#12-form---get--post)
- [13 iframe - 페이지 안에 페이지 삽입](#13-iframe---페이지-안에-페이지-삽입)
- [14 Video - 비디오](#14-video---비디오)
- [15 Audio - 오디오](#15-audio---오디오)
- [16 Image Map - 이미지 맵](#16-image-map---이미지-맵)
- [17 Semantic - 시멘틱 태그](#17-semantic---시멘틱-태그)
- [문제내서 맞추기 - 종합 복습](#문제내서-맞추기---종합-복습)

---

## 01 Hello World - 기본 뼈대

HTML 파일을 처음 만들 때 항상 들어가야 하는 기본 구조

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>연습하장</title>
  </head>
  <body>
    <h2>주현이</h2>
  </body>
</html>
```

| 코드 | 설명 |
|------|------|
| `<!DOCTYPE html>` | HTML5 문서라고 브라우저에 선언. **항상 맨 첫 줄** |
| `<html lang="en">` | 문서 전체를 감싸는 최상위 태그. 한국어면 `lang="ko"` |
| `<head>` | 브라우저에 필요한 정보를 담는 곳. 화면에 안 보임 |
| `<meta charset="UTF-8">` | 문자 인코딩 설정. **이거 없으면 한글 깨짐. 필수!** |
| `<meta name="viewport">` | 모바일 화면 대응. 디바이스 너비에 맞추고 zoom 1배율 시작 |
| `<title>` | 브라우저 탭에 표시되는 제목 |
| `<body>` | 실제로 화면에 보이는 내용을 여기에 작성 |

---

## 02 Basic - 기본 태그

```html
<!-- 제목 태그: h1이 제일 크고 h6이 제일 작음 -->
<h1>머릿말1</h1>
<h2>머릿말2</h2>
<h3>머릿말3</h3>
<h4>머릿말4</h4>
<h5>머릿말5</h5>
<h6>머릿말6</h6>

<!-- 문단 태그 -->
<p>첫번째 문장입니다.</p>

<!-- 링크 태그 -->
<a href="https://naver.com">네이버</a>

<!-- 현재 폴더 내 파일로 링크 -->
<a href="./01_hellowworld.html">01_helloword_html</a>

<!-- 이미지 태그 -->
<img src="이미지주소" alt="이미지 설명" />
```

| 태그 | 설명 |
|------|------|
| `<h1> ~ <h6>` | 제목 태그. 숫자가 클수록 작아짐. 크기뿐 아니라 **중요도**도 나타냄 |
| `<p>` | 문단(paragraph). 문장 쓸 때 사용 |
| `<a href="">` | 링크. `href`에 이동할 주소 입력 |
| `./파일명` | `./`는 현재 폴더를 의미. 내 파일로도 링크 가능 |
| `<img src="" alt="">` | 이미지. `alt`는 이미지 못 불러올 때 대체 텍스트, 스크린리더도 읽어줌 |

---

## 03 Global Attribute - 전역 속성

> **전역 속성** = 거의 모든 HTML 태그에 사용 가능한 속성들

```html
<!-- 드래그 가능 -->
<h1 draggable="true">움직일 수 있는 태그</h1>

<!-- 언어 지정 -->
<p lang="ko">대한민국</p>

<!-- 화면에서 숨기기 -->
<p hidden>이 문장은 화면에 보이지 않습니다.</p>

<!-- id, title -->
<a href="https://google.com" id="google" title="클릭하면 구글로 이동됨">구글</a>

<!-- label + input 연결 -->
<label for="userId">사용자 아이디</label>
<input type="text" id="userId" />

<!-- 직접 수정 가능 + 철자 검사 -->
<p spellcheck="true" contenteditable="true">This is a paraggraph</p>

<!-- 인라인 스타일 -->
<p style="color: red; background-color: yellow">빨간색 문장입니다.</p>

<!-- Tab 이동 순서 지정 -->
<a href="" tabindex="1">네이버</a>
<a href="" tabindex="3">구글</a>
<a href="" tabindex="2">개발자의 품격</a>
```

| 속성 | 설명 |
|------|------|
| `draggable="true"` | 마우스로 끌어서 이동 가능 |
| `lang="ko"` | 요소의 언어 지정. 번역, 스크린리더에 영향 |
| `hidden` | 요소 숨김. 공간도 차지 안 함 |
| `id` | 요소의 고유 이름. **중복 불가**. CSS/JS에서 특정 요소 선택할 때 사용 |
| `title` | 마우스 올리면 말풍선 설명 표시 |
| `for` / `id` 연결 | 라벨 클릭해도 input 활성화됨. **접근성에 중요!** |
| `spellcheck="true"` | 철자 오류에 밑줄 표시 |
| `contenteditable="true"` | 브라우저에서 직접 텍스트 수정 가능 |
| `style` | 인라인으로 CSS 스타일 직접 적용 |
| `tabindex` | Tab 키 이동 순서 지정. 숫자 순서대로 이동 (1→2→3) |

---

## 04 Local Attribute - 지역 속성

> **지역 속성** = 특정 태그에서만 사용 가능한 속성들

```html
<!-- 새 탭으로 열기 -->
<a href="https://google.com" target="_blank">구글</a>

<!-- 이미지 크기 지정 -->
<img src="./img/devlogo.png" width="100px" height="auto" alt="" />
```

| 속성 | 설명 |
|------|------|
| `target="_blank"` | 링크를 **새 탭**에서 열기. `_self`는 현재 탭 (기본값) |
| `width` / `height` | 이미지 크기 지정. `height="auto"` 하면 비율 유지하면서 너비에 맞게 자동 조절 |

---

## 05 Style - CSS 적용 방법

### CSS 적용 방법 3가지

| 방법 | 위치 | 특징 |
|------|------|------|
| **인라인 스타일** | 태그 안에 직접 `style="..."` | 우선순위 높음. 유지보수 어려움 |
| **인터널 스타일** | `<style>` 태그 안에 작성 | HTML 파일 내부에 CSS 작성 |
| **익스터널 스타일** | 별도 `.css` 파일 연결 | **실무에서 주로 사용** |

```html
<!-- 인라인 스타일 예시 -->
<p style="font-size: 30px">큰 사이즈 글자입니다.</p>
<p style="text-align: center">가운데 정렬입니다.</p>
<p style="text-align: right">오른쪽 정렬</p>
<p style="font-weight: bold">볼드체(굵은)로 보입니다.</p>
<p style="text-decoration: underline">밑줄이 생깁니다.</p>
<p style="text-decoration: line-through">취소선 생깁니다.</p>
<p style="font-style: italic">이탤릭체로 보여집니다.</p>
```

| 속성 | 의미 |
|------|------|
| `font-size: 30px` | 글자 크기 |
| `text-align: center` | 가운데 정렬 |
| `text-align: right` | 오른쪽 정렬 |
| `font-weight: bold` | 굵은 글자 |
| `text-decoration: underline` | 밑줄 |
| `text-decoration: line-through` | 취소선 |
| `font-style: italic` | 이탤릭체 |

---

## 06 Meaningful - 의미 있는 태그

### b vs strong / i vs em

```html
<!-- 보이는 건 같지만 의미가 다름 -->
<b>볼드체</b>                  <!-- 스타일만, 의미 없음 -->
<strong>강조하는 볼드체</strong> <!-- "중요하다"는 의미. 스크린리더가 강하게 읽어줌 -->

<i>이탤릭체</i>                <!-- 스타일만, 의미 없음 -->
<em>강조하는 이탤릭체</em>     <!-- "강조"라는 의미 -->
```

### 기타 의미 태그

```html
<small>작게</small>
<mark>형광펜 효과</mark>            <!-- 배경 노란색 -->
<del>3만원</del>                    <!-- 취소선 - "삭제된 내용" 의미 -->
<ins>추가된 내용</ins>              <!-- 밑줄 - "추가된 내용" 의미 -->
<sub>아래첨자</sub>                 <!-- X₂ -->
<sup>위첨자</sup>                   <!-- X² -->

<!-- 인용 -->
<blockquote cite="출처URL">긴 인용문</blockquote>
<q>짧은 인용</q>

<!-- 약자: 마우스 올리면 전체 이름 표시 -->
<abbr title="World Health Organization">WHO</abbr>

<!-- 주소 -->
<address>대한민국 제주특별자치도...</address>

<!-- 작품명 -->
<cite>절규</cite>
```

### div vs span

```html
<div style="background-color: blue">div 태그 - 블록 요소</div>
<span style="background-color: green">span 태그 - 인라인 요소</span>
```

| 태그 | 종류 | 특징 |
|------|------|------|
| `div` | 블록 요소 | 한 줄 전체 차지. 레이아웃 잡을 때 사용 |
| `span` | 인라인 요소 | 자기 크기만큼만 차지. 텍스트 일부 꾸밀 때 사용 |

> **블록 요소**: `div`, `h1~h6`, `p` → 한 줄 전체 차지  
> **인라인 요소**: `span`, `a`, `img` → 자기 크기만큼만 차지

---

## 07 List - 목록 태그

```html
<!-- 순서 없는 목록 (점으로 표시) -->
<ul>
  <li>에스프레소</li>
  <li>아메리카노</li>
  <li>카페라떼</li>
</ul>

<!-- 순서 있는 목록 (숫자로 표시) -->
<ol>
  <li>비주얼스튜디오코드 설치</li>
  <li>node.js 설치</li>
  <li>git 설치</li>
</ol>

<!-- 설명 목록 -->
<dl>
  <dt>html</dt>
  <dd>웹 페이지 개발을 위한 마크업 언어</dd>
  <dt>css</dt>
  <dd>웹 페이지 디자인을 위한 언어</dd>
  <dt>javascript</dt>
  <dd>웹 페이지 동작 처리를 위한 언어</dd>
</dl>
```

| 태그 | 설명 |
|------|------|
| `<ul>` | 순서 없는 목록. 점(•)으로 표시 |
| `<ol>` | 순서 있는 목록. 숫자(1, 2, 3...)로 표시 |
| `<li>` | 목록의 각 항목 |
| `<dl>` | 설명 목록 전체 |
| `<dt>` | 용어 (define term) |
| `<dd>` | 용어 설명 (description) |

---

## 08 Table - 표

```html
<style>
  table, td, th {
    border: 1px solid black;
    border-collapse: collapse; /* 이중선 → 단일선으로 합침 */
  }
  table { width: 100%; }
</style>

<!-- 기본 표 구조 -->
<table>
  <thead>
    <tr>
      <th>이름</th>
      <th>나이</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>유재석</td>
      <td>52</td>
    </tr>
  </tbody>
</table>

<!-- 세로 셀 합치기: rowspan -->
<td rowspan="3">1학년</td>

<!-- 가로 셀 합치기: colspan -->
<td colspan="2">합계</td>
```

| 태그 | 설명 |
|------|------|
| `<table>` | 표 전체 |
| `<thead>` | 제목 행들 묶음 |
| `<tbody>` | 데이터 행들 묶음 |
| `<tfoot>` | 합계 등 마지막 행 묶음 |
| `<tr>` | 행 (가로줄) |
| `<th>` | 열 제목 셀. 굵게 + 가운데 정렬 자동 적용 |
| `<td>` | 데이터 셀 |
| `rowspan="n"` | 세로로 n칸 합치기 |
| `colspan="n"` | 가로로 n칸 합치기 |

---

## 09 Form Element - 폼 입력 요소

```html
<!-- 체크박스: 여러 개 선택 가능 -->
<input type="checkbox" name="chk_lang" id="chk_html" />

<!-- 라디오버튼: 같은 name 그룹에서 하나만 선택 -->
<input type="radio" name="rdo_lang" id="rdo_html" />

<!-- 색상 선택 -->
<input type="color" id="favoriteColor" />

<!-- 날짜 선택 -->
<input type="date" id="bornDate" />

<!-- 날짜 + 시간 -->
<input type="datetime-local" id="arrivalDateTime" />

<!-- 이메일 형식 검사 -->
<input type="email" id="email" />

<!-- 파일 첨부 -->
<input type="file" id="attachment" />

<!-- 화면에 안 보이는 값 (개발자용) -->
<input type="hidden" name="email" value="john@gmail.com" />

<!-- 이미지 버튼 -->
<input type="image" src="./img/devlogo.png" />

<!-- 년월 선택 -->
<input type="month" id="yearmonth" />

<!-- 숫자 입력 (범위 제한 가능) -->
<input type="number" min="0" max="100" />

<!-- 입력 내용 숨김 -->
<input type="password" id="userpass" />

<!-- 전화번호 (정규식으로 형식 검사) -->
<input type="tel" pattern="^010-\d{4}-\d{4}$" />

<!-- 일반 텍스트 -->
<input type="text" id="general" />

<!-- 시간 선택 -->
<input type="time" id="visitTime" />

<!-- URL 형식 검사 -->
<input type="url" />

<!-- 주차 선택 -->
<input type="week" id="weekplan" />

<!-- 검색창 (X 지우기 버튼 자동 생성) -->
<input type="search" id="searchkeyword" />
```

| type | 역할 |
|------|------|
| `checkbox` | 여러 개 선택 가능 |
| `radio` | 같은 name 그룹에서 하나만 선택 |
| `color` | 색상 선택기 |
| `date` | 날짜 선택기 |
| `datetime-local` | 날짜 + 시간 선택기 |
| `email` | 이메일 형식 자동 검사 |
| `file` | 파일 첨부 |
| `hidden` | 화면에 안 보이는 값 전송용 |
| `image` | 이미지 버튼 |
| `month` | 년월 선택기 |
| `number` | 숫자 입력. `min` / `max` 가능 |
| `password` | 입력 내용 숨김 |
| `tel` | 전화번호. `pattern`으로 형식 검사 |
| `text` | 일반 텍스트 |
| `time` | 시간 선택기 |
| `url` | URL 형식 자동 검사 |
| `week` | 주차 선택기 |
| `search` | 검색창. X 버튼 자동 생성 |

---

## 10 Input Attribute - input 속성

```html
<!-- 미리 입력된 값 -->
<input type="text" value="abc" />

<!-- 읽기 전용: 수정 불가, 서버에는 전송됨 -->
<input type="text" value="ABC" readonly />

<!-- 비활성화: 수정 불가, 서버에 전송 안 됨 -->
<input type="text" value="abc" disabled />

<!-- 최대 입력 글자 수 제한 -->
<input type="text" maxlength="6" />

<!-- 입력 전 힌트 텍스트 (입력하면 사라짐) -->
<input type="tel" placeholder="하이픈(-) 없이 숫자만 입력하세요" />

<!-- 필수 입력 + 자동완성 + 자동 포커스 -->
<input type="text" required autocomplete="on" autofocus />
```

| 속성 | 설명 |
|------|------|
| `value` | 미리 입력된 기본값 |
| `readonly` | 읽기 전용. 수정 불가. **서버에는 전송됨** |
| `disabled` | 비활성화. 수정 불가. **서버에 전송 안 됨** |
| `maxlength` | 최대 입력 글자 수 제한 |
| `placeholder` | 입력 전 힌트 텍스트. 입력 시작하면 사라짐 |
| `required` | 필수 입력. 비우면 폼 제출 안 됨 |
| `autocomplete="on"` | 이전에 입력했던 값 자동 완성 제안 |
| `autofocus` | 페이지 로드 시 자동으로 이 input에 포커스 |

---

## 11 Form Other - 기타 폼 요소

```html
<!-- 드롭다운 선택. multiple이면 여러 개 선택 가능 (Ctrl+클릭) -->
<select name="" id="" multiple>
  <option value="02">서울</option>
  <option value="051">부산</option>
  <option value="064">제주</option>
</select>

<!-- 여러 줄 텍스트 입력 -->
<textarea style="width: 100%" rows="10"></textarea>

<!-- 관련 입력들을 박스로 묶기 -->
<fieldset>
  <legend>학력정보</legend>
  <input type="text" />
</fieldset>

<!-- 자동완성 추천 목록 -->
<input list="browsers" />
<datalist id="browsers">
  <option value="chrome">chrome</option>
  <option value="firefox">firefox</option>
  <option value="safari">safari</option>
</datalist>
```

| 태그/속성 | 설명 |
|---------|------|
| `<select>` | 드롭다운 선택 |
| `multiple` | 여러 개 선택 가능 (Ctrl+클릭) |
| `<option value="">` | `value`가 실제로 서버에 전송되는 값 |
| `<textarea rows="n">` | 여러 줄 텍스트 입력. `rows`로 줄 수 지정 |
| `<fieldset>` | 관련 입력 요소들을 박스로 묶기 |
| `<legend>` | fieldset 박스의 제목 |
| `<datalist>` | 타이핑 시 자동완성 추천 목록. `input`의 `list`와 `datalist`의 `id`를 같게 연결 |

---

## 12 Form - GET / POST

```html
<form action="전송할 서버주소" method="get" target="_self" novalidate>
  <input type="text" name="username" />
  <button type="submit">저장</button>
</form>
```

| 속성 | 설명 |
|------|------|
| `action` | 데이터를 보낼 서버 주소 |
| `method` | 전송 방식 (`get` / `post`) |
| `target` | 응답을 받을 창 (`_self` / `_blank`) |
| `novalidate` | form 안 input들의 유효성 검사 건너뜀 |

### GET vs POST

| | GET | POST |
|--|-----|------|
| 데이터 위치 | URL에 붙어서 감 (`?name=주현`) | 숨겨서 전송 |
| 보안 | URL에 노출되어 취약 | 상대적으로 안전 |
| 크기 제한 | 있음 | 없음 |
| 사용 예시 | 검색, 페이지 공유 | 로그인, 회원가입 |

---

## 13 iframe - 페이지 안에 페이지 삽입

```html
<!-- iframe으로 다른 HTML 파일 삽입 -->
<iframe src="./13_iframe_contnet.html" id="ifram" frameborder="0"></iframe>

<!-- 메뉴 클릭 시 iframe 내용만 교체 -->
<a href="javascript:goToMenu('./13_iframe_contnet.html')">menu1</a>
<a href="javascript:goToMenu('./13_iframe_content2.html')">menu2</a>

<script>
  function goToMenu(path) {
    document.getElementById('ifram').src = path;
  }
</script>

<!-- iframe 안에서 최상위 브라우저 창 전체로 이동 -->
<a href="https://naver.com" target="_top">Naver</a>
```

| 속성/값 | 설명 |
|---------|------|
| `src` | 삽입할 페이지 주소 |
| `frameborder="0"` | 테두리 없애기 |
| `target="_top"` | iframe 안이 아닌 최상위 창 전체로 이동 |

> `id`로 iframe을 잡고 JS로 `src`를 바꾸면 페이지 이동 없이 내용만 교체 가능

---

## 14 Video - 비디오

```html
<video
  src="./media/video.mp4"
  width="320px"
  controls
  autoplay
  muted
  loop
  poster="./img/devlogo.png"
>
  <!-- 자막 파일 연결 -->
  <track
    src="./media/bootcamp.ko.vtt"
    kind="subtitles"
    srclang="ko"
    label="한국어"
  />
</video>
```

| 속성 | 설명 |
|------|------|
| `controls` | 재생 / 멈춤 / 볼륨 UI 표시 |
| `autoplay` | 자동 재생 |
| `muted` | 음소거. **autoplay 쓰려면 muted도 같이 써야 대부분 브라우저에서 작동** |
| `loop` | 반복 재생 |
| `poster` | 재생 전 보여줄 썸네일 이미지 |
| `<track>` | 자막 파일 연결. `.vtt` 형식 사용 |

---

## 15 Audio - 오디오

```html
<audio src="./media/audio.mp3" controls></audio>
```

### preload 속성

| 값 | 설명 |
|----|------|
| `auto` | 미리 다운로드. 중요한 미디어, 바로 재생해야 할 때 |
| `metadata` | 미디어 길이 정보만 미리 가져옴 |
| `none` | 아무것도 미리 안 함. 서버 트래픽 아끼고 싶을 때 |

> video 태그와 속성이 거의 동일. `controls` 붙이면 재생바 생김

---

## 16 Image Map - 이미지 맵

```html
<!-- 이미지에 클릭 가능한 영역 지정 -->
<img src="./img/ikea.png" usemap="#image-map" />

<map name="image-map">
  <!-- 원형 영역: coords="중심x, 중심y, 반지름" -->
  <area
    href="https://연결할주소.com"
    coords="859,785,40"
    shape="circle"
    target="_blank"
  />

  <!-- 사각형 영역: coords="x1,y1,x2,y2" -->
  <area
    href="https://연결할주소.com"
    coords="100,100,300,300"
    shape="rect"
    target="_blank"
  />
</map>
```

| 속성/태그 | 설명 |
|---------|------|
| `usemap="#이름"` | img와 map을 `#이름`으로 연결 |
| `shape="circle"` | 원형 영역. `coords="x, y, 반지름"` |
| `shape="rect"` | 사각형 영역. `coords="x1, y1, x2, y2"` |
| `shape="poly"` | 다각형 영역. 꼭짓점 좌표들을 순서대로 나열 |

---

## 17 Semantic - 시멘틱 태그

두 파일은 **보이는 결과가 같지만 코드 의미가 다름**

###  div로만 만든 버전 (17_semanticdiv.html)

```html
<div>헤더</div>
<div>메뉴들</div>
<div>
  <div>
    <div>아티클1</div>
    <div>아티클2</div>
  </div>
</div>
<div>footer</div>
```

### 시멘틱 태그로 만든 버전 (17_semantic.html)

```html
<header>헤더</header>
<nav>메뉴들</nav>
<main>
  <section>
    <article>아티클1</article>
    <article>아티클2</article>
  </section>
</main>
<footer>footer</footer>
```

### 시멘틱 태그를 써야 하는 이유

| 이유 | 설명 |
|------|------|
| **SEO** | 구글 같은 검색엔진이 페이지 구조를 이해함 |
| **접근성** | 스크린리더가 header, nav, main 등을 인식하고 읽어줌 |
| **가독성** | 코드 보는 사람이 구조를 바로 파악할 수 있음 |

### 주요 시멘틱 태그

| 태그 | 의미 |
|------|------|
| `<header>` | 페이지 / 섹션의 머릿말 |
| `<nav>` | 메뉴 내비게이션 |
| `<main>` | 페이지의 핵심 콘텐츠 |
| `<section>` | 주제별 묶음 |
| `<article>` | 독립적인 콘텐츠 (블로그 글, 뉴스 기사 등) |
| `<aside>` | 사이드바 (부가 정보) |
| `<footer>` | 페이지 하단 정보 |

---

## 전체 요약

| 파일 | 핵심 내용 |
|------|---------|
| 01_hellowworld | HTML 기본 뼈대 구조 |
| 02_basic | 제목, 문단, 링크, 이미지 |
| 03_global_attribute | 전역 속성 (draggable, hidden, id, tabindex 등) |
| 04_local_attribute | 지역 속성 (target, width, height) |
| 05_style | CSS 적용 방법 3가지 + 주요 스타일 속성 |
| 06_meaningful | 의미 있는 태그 (strong, em, mark, del 등) |
| 07_list | ul, ol, dl 목록 태그 |
| 08_table | table, rowspan, colspan |
| 09_from_element | input type 종류 전체 |
| 10_input_attribute | input 속성 (readonly, disabled, required 등) |
| 11_form_other | select, textarea, fieldset, datalist |
| 12_form | form의 GET / POST 방식 |
| 13_iframe | iframe으로 페이지 삽입 + JS로 내용 교체 |
| 14_video | video 태그 + 자막 |
| 15_audio | audio 태그 + preload |
| 16_image_map | 이미지 특정 영역에 링크 연결 |
| 17_semantic | 시멘틱 태그 vs div 비교 |
| 문제내서 맞추기 | 종합 복습 실습 |
