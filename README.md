
### 오른쪽으로 보내고 싶은 형제 요소가 2개 이상이라면?
 2개를 묶어서 그룹으로 처리하고 `float:right` 한번만 작성한다
 `float:right`는 2번 이상 사용하면 역순이 되므로 **한번만 작성해야한다**
### float를 적용하는 형제의 부모의 높이가 max-content(기본값)이라면?
 부모의 높이를 제대로 인식못하므로 높이를 강제 (px)시키거나 `overflow:hidden` 높이를 안주고 영역 재인식을 시켜 float에 의한 오류를 없애준다
## form 태그 관련 속성 주요 뜻과 사용 용도
 입력 양식 `input type=` text, password, email, search, number 등..
 선택 양식 `input type=` checkbox, radio, select, option 등..
 입력 양식과 선택양식에 따라 같은 스펠링의 속성의 뜻이 달라지므로 주의해야 한다!
## 양식에 따라 다른 속성의 뜻
 `value` : 입력양식(사용자가 입력하는 입력값(속성작성x)) 선택양식(사용자가 선택해서 서버에 전송되는 값(속성작성o))
 `name` : 입력양식(사용자가 선택해서 서버에 전송되는 값(작성0)) 선택양식(2개 이상의 선택양식을 묶어주는 동일 그룹(작성0))
 입력양식에서 `value`의 초기값을 작성하는 경우: 쇼핑몰의 주문수량(기본값 1)
## form 속성에 사용자정의값 이름 작성할 경우 주의사항
 name, value, id, class 등 속성의 이름을 작성할 때는 **중복명칭_개별명칭**을 섞어서 작성한다.
 중복명칭에서 주로 사용하는 단어 : `admin, user`
 개별명칭은 요소의 특징에 따라 달라진다(`male, id, btn, pw `등)
 중복명칭 설정 시 작성 방향도 동일하게 해야한다. 
  ex`user_id == user_pw` 0
    `user_id == pw_user` x
## 목록양식 select, option (선택 목록이 2개 이상일 경우)
 기준목록비교해서 외우기 select(ul) ,  option(li)
 `select` 태그는 option을 묶어주는 그룹개념으로 그룹 속성(name)이 함께 적용된다.
 `option` 태그는 사용자가 실제 선택하는 값이므로 데이터 구분값 속성(value) 작성한다.
 `option` 태그 작성 시 모든 value속성은 필수가 아닌 사용자가 선택하는 데이터에만 사용한다.
 선택 option -> 1. 컬러(value x) 2. 블랙(black) 3. 화이트(white) 4. 코랄(colar)
 ## 선택양식 radio, checkbox 주의사항과 label 주의사항
  radio , checkbox는 name(동일 그룹), value(개별 데이터값) 속성을 구분해서 사용한다.
  `id` 속성을 적용할때는 javascript와 연결을 위해서 하거나 또는 label의 `for` 속성 연결을 위해서 사용한다. 이때 id값은 기존 개별데이터값을 가진 `value`와 동일한 값을 작성해도 된다
   `label`은 사용자가 선택하는 이미지 또는 글자를 묶어서 작성하고 기존 선택양식 input의 형제로 작성한다면 반드시 `for` 속성을 입력해서 input의 id와 동일하게 입력하고, 반대로 input의 부모로 작성한다면 for을 입력하지 않아도 된다. 대신 이경우엔 선택하는 이미지 또는 글자를 반드시 다른 인라인 태그로 묶어야 한다
 input radio, checkbox는 사용자커스텀 css 디자인이 불가능하기 때문에 사이트에 어울리는 모습으로 디자인하고 싶다면 `display:none` 숨기고 선택글자를 묶은 태그에 `background-image` 디자인 해야 한다.
### input 과 label이 형제인 경우
 `<input id="a"><label for="a">선택글자</label>`
### input 과 label이 부모-자식인 경우
 `<label><input id="a"><span>선택글자</span></label>`
## button 속성 종류와 사용처
 `<button type="속성종류" id="버튼구분명">보이는글자 or 이미지</button>`
 속성종류 1. button : 범용기능(주소찾기, 중복확인, 이전, 다음, 재생, 정지 등)
 속성종류 2. submit : `form action` 주소에 `method` 값 형태로 전달되는 최종 서버전송버튼
 속성종류 3. reset : 취소 or 삭제 버튼(가입취소, 주문취소 등)
 -----
 ## css calc() 함수
  css에서 길이, 비율, 수치 등을 계산할 때 사용하는 함수
  단위가 다른(px, % 등)값도 계산할 수 있어서 레이아웃 조정 시 유용함
  `+ , -, *, /` 산술 연산자 모두 사용 가능
  계산시 **연산자 앞 뒤 반드시 공백 포함**해서 작성하기
### css cllc() 함수 예시
 `height:calc(50vh - 100px);`
 `padding:calc(100% - (10px * 3));`  우선순휘 괄후 추가 사용 가능
 `width:calc(90% - (60px + 5px));`  우선순위도 연산자 앞뒤 공백 필수
 `width:calc(90% - 65px);`
## flex layout
 flex는 수평, 수직 1차원 레이아웃으로 메인축과 교차축을 고려하여 다양한 레이아웃을 만들 수 있는 css3의 새로운 레이아웃 속성입니다.
  container(부모속성), item(자식속성)에 주는 속성이 다르기 때문에 주의해서 작성해야 합니다 **기본 시작은 부모**
 `display:flex` 부모(container) 대상에 display 명령어로 해당 레이아웃이 flex 라는 선언부터 시작한다
  (위) flex 선언을 진행 시 메인축은 기본값 수평, 교차축은 기본값 수직으로 정렬된다