# Frontend Learning Project - Codebase Analysis

---

## 1. HTML5 (HyperText Markup Language)
웹 페이지의 구조와 의미를 정의하기 위해 사용된 태그와 속성들입니다.

### 1.1 문서 구조 및 메타데이터
- `<!DOCTYPE html>`: HTML5 문서임을 브라우저에 알리는 선언.
- `<html>`: 문서의 루트(Root) 요소. `lang="en"` 속성으로 언어 설정.
- `<head>`: 문서의 메타데이터를 담는 영역.
  - `<meta charset="UTF-8">`: 문자 인코딩 설정.
  - `<meta name="viewport" ...>`: 반응형 웹을 위한 뷰포트 설정.
  - `<title>`: 브라우저 탭에 표시될 문서 제목.
  - `<link>`: 외부 리소스(CSS, 폰트 등) 연결. (`rel="stylesheet"`, `href="..."`)
  - `<style>`: 문서 내부에 CSS 코드를 직접 작성할 때 사용.
- `<body>`: 실제로 화면에 표시되는 콘텐츠 영역.

### 1.2 섹셔닝 및 그룹화 태그
- `<div>`: 순수 컨테이너. 특별한 의미 없이 구역을 나눌 때 사용 (가장 많이 사용됨).
- `<span>`: 인라인 컨테이너. 텍스트의 일부를 감싸서 스타일을 줄 때 사용.
- `<article>`: 독립적인 콘텐츠(예: 게시글 카드)를 감쌀 때 사용.
- `<ul>`, `<li>`: 순서 없는 목록(Unordered List)과 항목. (`list-style: none`으로 점 제거 후 자주 사용)
- `<h1>` ~ `<h6>`: 제목 태그. 문서의 계층 구조를 나타냄.

### 1.3 폼(Form) 및 입력 요소 (`reservation.html`)
사용자로부터 데이터를 입력받기 위해 사용된 태그들입니다.
- `<form>`: 입력 양식의 범위. `action`(데이터 전송 URL), `method`(GET/POST 전송 방식) 속성 사용.
- `<fieldset>`: 관련된 입력 요소들을 하나의 그룹으로 묶음.
- `<legend>`: fieldset 그룹의 제목(캡션).
- `<label>`: 입력 요소 이름표. 접근성 향상 및 클릭 영역 확보.
- `<input>`: 다양한 데이터 입력 필드.
  - `type="text"`: 일반 텍스트.
  - `type="password"`: 비밀번호 (마스킹 처리).
  - `type="tel"`: 전화번호 입력에 최적화.
  - `type="date"`: 날짜 선택기(Date Picker) 제공.
- `<button>`: 클릭 가능한 버튼.
  - `type="button"`: 일반 버튼(JS와 연결).
  - `type="submit"`: 폼 데이터 전송.
  - `type="reset"`: 입력 내용 초기화.

### 1.4 멀티미디어 및 링크
- `<img>`: 이미지 삽입. `src`(경로), `width`, `height` 속성 사용.
- `<a>`: 하이퍼링크. `href="#"` (임시 링크) 형태로 자주 실습.

---

## 2. CSS3 (Cascading Style Sheets)
웹 페이지의 디자인과 레이아웃을 담당하는 스타일 속성들입니다.

### 2.1 선택자 (Selectors)
CSS를 적용할 대상을 선택하는 문법입니다.
- **Type Selector**: `body`, `div`, `button` (태그 이름으로 선택).
- **Class Selector**: `.className` (HTML의 `class="..."` 속성과 매칭, 재사용 가능).
- **ID Selector**: `#idName` (HTML의 `id="..."` 속성과 매칭, 고유 요소).
- **Descendant Combinator**: `div h1` (div 안에 있는 모든 h1).
- **Child Combinator**: `div > h1` (div의 바로 아래 자식 h1).
- **Pseudo-class**: `button:hover` (마우스가 올라갔을 때 상태).
- **Grouping**: `h1, h2, h3` (여러 선택자에 같은 스타일 적용).

### 2.2 레이아웃 (Layout) 속성
- **Display**:
  - `block`: 한 줄을 다 차지함 (div, p 등).
  - `inline-block`: 내부는 block처럼 박스 모델을 가지지만, 배치는 inline처럼 옆으로 나열 (`card.css`).
  - `flex`: Flexbox 레이아웃. `justify-content`(가로 정렬), `align-items`(세로 정렬) (`mediaQuery.html`).
  - `grid`: Grid 레이아웃 (`list.css`).
- **Float**: 요소를 좌/우로 띄움 (`float: left/right`). (Layout용으로는 이제 Flex/Grid가 더 선호됨).
- **Overflow**: 내용이 넘칠 때 처리 (`overflow: hidden`).

### 2.3 박스 모델 (Box Model)
- `width`, `height`: 요소의 너비와 높이.
- `margin`: 요소 바깥쪽 여백. (`margin: auto`로 중앙 정렬).
- `padding`: 요소 안쪽 여백.
- `border`: 테두리 (`border: 1px solid color`).
- `border-radius`: 테두리 둥글게 처리 (`50%`는 원형 생성).
- `box-sizing`: 패딩과 테두리를 너비에 포함할지 여부.

### 2.4 타이포그래피 및 시각 효과
- **Text**: `font-size`, `font-weight`(bold), `font-family`, `text-align`, `text-decoration`(none: 링크 밑줄 제거).
- **Color**: `color`(글자색), `background-color`(배경색).
- **Background**: `background: url(...) no-repeat cover` (배경 이미지 처리).
- **Misc**: `cursor: pointer` (마우스 오버 시 손가락 커서), `list-style: none` (리스트 불릿 제거).

### 2.5 반응형 웹 (Responsive Web)
- `@media screen and (min-width: ...)`: 화면 크기 조건에 따라 다른 CSS를 적용하는 미디어 쿼리 기술 (`mediaQuery.html`).

---

## 3. JavaScript (ES6+ & DOM)
동적인 기능 구현을 위해 사용된 프로그래밍 문법입니다.

### 3.1 변수 및 자료형 (Variables & Types)
- **`var` vs `let` vs `const`**:
  - `var`: 함수 스코프, 호이스팅 문제(잘 쓰지 않음, `scriptVar.html` 비교 실습).
  - `let`: 변수(재할당 가능), 블록 스코프.
  - `const`: 상수(재할당 불가), 블록 스코프.
- **Template Literal**: 백틱(`` ` ``)을 사용하여 문자열 내 변수 삽입 (` `${var}` `).
- **Object**: `{ key: value }` 형태.
  - **Enhanced Object Literals**: `{ key }` (키와 변수명이 같으면 축약).
- **Array**: `[1, 2, 3]` 형태. `arr.length` 등 사용.

### 3.2 연산자 및 최신 문법 (Modern Syntax)
- **Spread Operator (`...`)**: 객체나 배열의 복사 및 병합 (`const newObj = { ...oldObj }`).
- **Destructuring (구조 분해 할당)**: `const { name, age } = userObj;` (객체 속성을 변수로 추출).
- **Arrow Function (화살표 함수)**:
  - `const func = () => { ... }`
  - `this` 바인딩이 상위 스코프를 따름.

### 3.3 제어문 (Control Flow)
- **조건문**:
  - `if (조건) { ... } else { ... }`
  - `switch (값) { case 1: ... break; default: ... }` (`scriptCondition.html`).
- **반복문**:
  - `for (let i=0; i<len; i++)`: 고전적인 반복문.
  - `arr.forEach((item, idx) => ...)`: 배열 전용 순회 메서드.
  - `for (const key in obj)`: 객체의 속성 키 순회.
  - `for (const item of arr)`: 배열(Iterable)의 값 순회.

### 3.4 DOM 조작 (Document Object Model) (`scriptDom.html`)
HTML 요소를 자바스크립트로 선택하고 변경하는 기능.
- **선택**: `document.getElementById('id')`, `document.querySelector('css_selector')`.
- **내용 변경**:
  - `.textContent`: 텍스트만 변경.
  - `.innerHTML`: HTML 태그를 포함하여 변경 (보안 주의).
- **속성 변경**: `.src` (이미지 경로), `.className` (클래스 변경).
- **생성 및 추가**:
  - `document.createElement('div')`: 새 요소 생성.
  - `parent.appendChild(node)`: 부모 요소에 자식으로 추가.

### 3.5 이벤트 (Events)
- **Inline**: `<button onclick="func()">` (HTML에 직접 작성).
- **Property**: `btn.onclick = func;`
- **EventListener**: `btn.addEventListener('click', () => { ... })` (권장 방식, `scriptDomQuiz.html`).

### 3.6 비동기 통신 (Async/Await & Axios) (`scriptAxios.html`)
- **Async/Await**: 비동기 코드를 동기 코드처럼 직관적으로 작성 (`async function`, `await promise`).
- **Axios**: 브라우저용 HTTP 클라이언트 라이브러리.
  - `axios.get(url)`: GET 요청 전송.
  - `.then(res => ...)`: 성공 시 콜백.
  - `.catch(err => ...)`: 에러 처리.
- **API 연동**: `fakestoreapi.com`을 통해 실제 상품 JSON 데이터를 받아와 화면에 렌더링.

### 3.7 내장 객체 및 메서드
- **Array Methods**: `.push()`, `.filter()`, `.map()` (데이터 변환 및 가공).
- **Window/Global**: `window.alert()`, `window.prompt()`, `console.log()`.
- **Type Casting**: `parseInt()`, `Number()`.
- **Date**: `new Date()`, `.toLocaleDateString()` (시간/날짜 처리).
