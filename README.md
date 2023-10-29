# kotlin-racingcar

## 프로그래밍 요구 사항
- [x] 모든 로직에 단위 테스트를 구현한다. 단, UI(System.out, System.in) 로직은 제외
  - 핵심 로직을 구현하는 코드와 UI를 담당하는 로직을 구분한다.
  - UI 로직을 InputView, ResultView와 같은 클래스를 추가해 분리한다.
- [x] indent(인덴트, 들여쓰기) depth를 2를 넘지 않도록 구현한다. 1까지만 허용한다.
  - 예를 들어 while문 안에 if문이 있으면 들여쓰기는 2이다.
  - 힌트: indent(인덴트, 들여쓰기) depth를 줄이는 좋은 방법은 함수(또는 메소드)를 분리하면 된다.
- [x] 함수(또는 메소드)의 길이가 15라인을 넘어가지 않도록 구현한다.
  - 함수(또는 메소드)가 한 가지 일만 잘 하도록 구현한다.
- [x] 기능을 구현하기 전에 README.md 파일에 구현할 기능 목록을 정리해 추가한다.
- [x] git의 commit 단위는 앞 단계에서 README.md 파일에 정리한 기능 목록 단위로 추가한다.

## 기능사항
### Car
- 자동차의 현재 Step 상태와, 앞으로 갈 수 있는지에 대한 클래스입니다.
- 자동차는 moveForward() 함수를 통해 +1씩 이동합니다.
- 자동차는 Random 함수를 통해 0~9의 숫자중 4 이상인 경우 이동합니다.
- 자동차는 5자를 넘을 수 없으며, 공백의 경우 입력실패로 간주합니다.
### CarRacing
- 자동차의 경주를 구현합니다. 정해진 횟수동안 반복 진행합니다.
- 자동차 경주 이후, 결과를 보여줍니다.
### InputView
- 사용자의 입력을 받는 클래스입니다.
- 입력을 받아 공백을 제거해줍니다.
- 입력한 값을 Validate하는 곳과 연결해줍니다. (RoundNumberValidator, CarNamesDuplicateValidator)
### OutputView
- 사용자에게 보여줄 String을 가진 클래스입니다.
- 자동차 경주의 결과를 보여주는 기능을 가지고 있습니다.
### RoundNumberValidator
- 사용자의 입력된 문자가 올바른지 판별합니다. ex) 숫자가 0인지, 음수 값인지, Double형 실수를 입력했는지 등
### CarNamesDuplicateValidator
- 사용자의 입력된 문자가 올바른지 판별합니다. ex) 중복된 값을 입력했는지

## Patch note - Step 4: 우승자 기능 추가
- 익명의 자동차 대수가 아닌 이름으로 자동차를 분별합니다.
- 종료 후 최종 우승자를 발표합니다.

## 기능 추가 목록
- 기존 Validator 요구사항에 맞게 수정하기
- 자동차 이름 Validator 추가하기
- 자동차 이름 입력 받기 (5자 초과 금지)
- 입력받은 이름을 OutputView에 출력하기
- 추가된 기능 테스트 코드 추가하기
- 자동차 이름 중복요소 제거
## 특이사항
