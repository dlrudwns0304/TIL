# TIL
## Vs code 주요 단축키
 `ctrl+k` -> `ctrl+\` 화면 분할
 `ctrl+j` 터미널 실행
 `q` or `ctrl+c` 터미널 입력안되는 에러 해결 단축키
## 작업폴더 설명
 `html_basic/` : html 기초 연습파일 모음
 `task/` : 과제제출 폴더, 파일 모음
 `README.md` : 배운 내용 기록, 어려운 점 및 막힌 점 자유롭게 기록
### 2025-04-04 - HTML 3일차 문서와 레이아웃
 `h1~h6` , `p`, `br`, `strong`, `em` , `del` , `s` ,`sup` , `sub`
 ### 2025-04-07 - HTML 4일차 레이아웃
  `div`, `span`
  웹/앱 레이아웃 뱡향과 의미에 따라 2개 이상의 요소를 묶어주는 레이아웃 요소|
  `div`는 생성 시 반드시 그룹을 구분할 수 있는 이름을 설정해야 한다 `span`은 선택
 이름 작성 시 주의사항 :  반드시 용도에 맞는 의미있는 영단어 사용
 ### HTML 구조 공부 순서
 1. 클론 코딩 & 디자인할 사이트 정하기
 2. 피그마에서 와이어프레임 만들기(레이어,폴더 이름주의)
 3. 피그젬에서 일부 화면 넘겨서 태그 계획하기
 4. 계획한 태그를 가족관계에 맞게 트리구조 만들기
 5. VS code.에서 실제 HTML 작성하기(트리구조 순서에 맞게 바깥쪽->안쪽순서로)
 ### 다른 환경에서 git 이어서 작업하기
 1. 새폴더 연결하기
 2. `git clone 저장소 주소 붙여넣기`
 3. `cd 복제할 파일 해주기`
 4. `자유롭게 수정하기`
 5. `git commit -m '' 해주기`
 6. `git push origin main`
 ### 위 이어서 다른 환경에서 git 이어 작업하기(학원)
  `git pull origin main` 집에서 올린 파일 내려받기
  ------
  ### 바로가기 메뉴 만들기
 0. (조건) 화면이 수직으로 충분히 이동할 수 있을만큼 스크롤 준비
 1. 바로가기 메뉴 a 태그 준비하기
 2. 바로가기 위치 div id명 준비하기
 3. 위 1번 `a` 속성 `href` 값으로 `#` 먼저 작성 후 위 2번 이름 작성하기
 4. 위 3번 결과 예시) id가 abcd일 경우 `<a href="#abcd"></a>`
 ------
 ### 링크복습
 `<a herf="#"></a>` 임시 링크
 `<a href="#header"></a>` header로 바로가기 링크
 `<a href="./basic/index.html"></a>` index.html 이동(상대경로링크)
 `<a href="./basci/index.html#main"></a>` index.html 로 이동하는데 절대경로와 상대경로를 같이 쓰는거
 ----
 ## CSS Style sheet
  외부스타일시트 파일 저장  **styles**폴더에 `파일명.css` 저장한다.
  위 파일 생성 후 css연결을 원하는 html파일 head위치에 `<link>`태그로 연결한다.
  html 작성 후 html의 모든 디자인형태를 초기화하는 `reset.css`반드시 연결한다
  웹 글꼴(noto sans kr, pretandrad 등) 연결 시 html파일에 `<link>` 태그 연결한다
### head태그 내에 들어가는 link태그 작성 순서
 1. 웹글꼴 포함 기타 플러그인 연결 주소
 2. reset.css
 3. 해당 html별 디자인.css
### 디자인 css 작성 시 작성 순서 및 주의사항
 **부모->자식**순서로 가장 바깥쪼고 부모부터 먼저 선택자를 만들고 디자인한다.
 레이아웃 관련 요소에 `width, height` 속성 작성 시 영영 확인을 위한 `background-color`를 꼭 함께 작성해서 정확히 구분한다. 이 때 색상은 쉬운 영역 구분을 위한 `aqua, lime, yellow, pink` 등의 밝은 색상 위주로 사용한다. 영역 확인과 디자인 작업을 모두 마친 후 위 색상은 제거로 마무리한다
  실제 디자인에 들어가는 색상은 rgba 또는 헥사코드로 입력하고 테스트용으로 입력하는 임시 색상은 영문명으로 입력해야 한다
### 자주 이용하는 css 속성 값과 기본값과 사용예시
 `letter-spacing` 자간 | 0 | `letter-spacing:-0.02rem`
 `line-height` 행간 | 100% | `line-height:1.4;`
 `font-size` 글자크기 | 16 | `font-size:1rem;`
 `color` 글자색 | `color:000;`
 `background-color` 배경색 | `background-color: 85E1FA;`
 `wdith` 가로크기 | `width:243px`
 `height` 세로크기 | `width:234px`
 `margin` 여백 | `margin-top:359px`
 `border-radius` 모서리 둥글기 | `boder-radius:50px`
 `font-weight` 글자굵기 | 400 | `font-weight:400;`
 `font-family` 글꼴 | `font-family:"pretendard", san-serif;`
