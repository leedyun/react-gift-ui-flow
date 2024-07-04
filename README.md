# 카카오 테크 캠퍼스 - 프론트엔드 카카오 선물하기 편

[🔗 link](https://edu.nextstep.camp/s/hazAC9xa)

## Week 1. 1단계 - 프로젝트 세팅

[🔗 link](https://edu.nextstep.camp/s/hazAC9xa/ls/QzgHvzRM)

## Week 1. 2단계 - Storybook을 사용하여 재사용 가능한 컴포넌트 구현

[🔗 link](https://edu.nextstep.camp/s/hazAC9xa/ls/4wYFPW1K)

## Week 2. 1단계 - 페이지 만들기

[🔗 link](https://edu.nextstep.camp/s/hazAC9xa/ls/QzV1ncxk)

# Gift Shop Project

## 1단계. 구현할 기능 목록

### 1. 공통 컴포넌트

- [o] Header, Footer 구현

### 2. 메인 페이지 (`/`)

- [o] Theme 카테고리 섹션 구현 - 각 카테고리 아이템을 클릭하면 해당 테마 페이지로 이동
- [o] 실시간 급상승 선물 랭킹 섹션 구현 - 현재 인기 있는 선물 랭킹을 표시
- [o] 필터 기능 - 사용자가 특정 조건에 따라 선물 필터링
- [o] 상품 목록
  - 초기에는 6개의 상품만 표시됩니다.
  - "더보기" 버튼을 클릭하면 더 많은 상품이 표시
  - "접기" 버튼을 클릭하면 다시 6개의 상품만 표시

### 3. 테마 페이지 (`/theme/:themeKey`)

- [o] Header 섹션
  - themeKey에 따라 label, title, description, backgroundColor가 달라지는 재사용 가능한 Header 컴포넌트를 구현
- [o] 상품 목록 섹션

### 4. 로그인 페이지 (`/login`)

- [o] 로그인 폼 - 사용자가 ID와 PW를 입력할 수 있는 입력 필드

### 5. 나의 페이지 (`/my-account`)

- [o] 로그아웃 버튼
  - 로그아웃 시, 메인 페이지로 리다이렉트합니다.

## 2단계. 구현할 기능 목록

### 1. 로그인 페이지

- [o] ID와 PW 입력 시 직전 페이지로 Redirect
- [o] ID와 PW 입력 시 ID를 sessionStorage에 저장
- [o] 모든 페이지 진입 시 로그인 여부 판단 로직 구현
- [o] 내 계정을 로그인 하지 않은 경우 로그인 버튼 추가

## 2. 내 계정 페이지

- [o] 내 계정 페이지는 로그인 한 유저만 접근 가능
- [o] 내 계정 페이지에서 로그아웃 가능

## 3단계. 2주차 질문

- 질문 1. CRA 기반의 SPA프로젝트에서 React Router를 사용하지 않는다면 어떤 문제가 발생하나요?

  - URL에 따라 컴포넌트를 변경하며 페이지 전환을 수동으로 관리해야하는 불편함이 생김
  - 브라우저의 뒤로 가기, 앞으로 가기 등의 히스토리 구현 어려움
  - 각 페이지별로 구분되는 URL이 없으면, SEO 최적화가 어려움

- 질문 2. 리액트 Context 나 Redux는 언제 사용하면 좋을까요? (로그인을 제외한 예시와 이유를 함께 적어주세요.)

  - Context API 사용 : 테마 설정(모든 컴포넌트에서 테모 정보에 접근하기 위해), 다국어 지원(언어 설정을 Context에 저장하고 사용)
  - Redux 사용 : 여러 컴포넌트에 걸쳐 복잡한 상태 업데이트가 필요할 때, 상태 업데이트 추적이 필요할 때

- 질문 3. Local Storage, Session Storage 와 Cookies의 차이가 무엇이며 각각 어떨때 사용하면 좋을까요?
  - Local Storage
    1. 브라우저를 닫아도 데이터 유지
    2. 데이터는 사용자가 명시적으로 클리어하지 않는 한 계속 저장
    3. 최대 5MB
    4. 장기간 유지해야하는 데이터(사용자 설정, 장바구니 정보 등)
  - Session Storage
    1. 브라우저 탭이 열러 있는 동안만 데이터 유지
    2. 최대 5MB
    3. 한 세션 동안 필요한 데이터(폼 작성 중 임시 데이터 등)
  - Cookies
    1. 만료 날짜가 정해진 데이터 조각 저장. HTTP 요청 시 서버로 자동 전송
    2. 최대 4KB
    3. 주로 사용자 인증, 세션 관리 등 사용
    4. 사용자 로그인 상태 유지나 정보를 서버와 클라이언트 간 지속적으로 주고받을 때
