# javascript-calculator-precourse

## 미션간단설명

주어진 문자열에서 숫자만 뽑아 더하는 계산기를 만드는 문제입니다. `:`, `,` 구분자로 분리하며, 추가적인 커스텀 구분자를 지정할 수 있습니다. 또한 잘못된 입력 시 ERROR 가 발생됩니다.

## 요구사항, 제약조건 정리

### 입력 조건

- 구분자와 양수로 구성된 문자열이 입력된다.
- `@woowacourse/mission-utils` 의 `Console.readLineAsync()` 를 활용한다.
- 잘못된 값을 입력할 경우 `Error` 를 발생시킨다.
  - [숫자] 음수인 경우
  - [숫자] 문자열 진행 중 등록되지 않은 구분자가 나오는 경우
  - [커스텀 구분자] `//` 를 제외한 구분자가 나오는 경우
  - [커스텀 구분자] 커스텀 구분자에 숫자가 포함된 경우
  - [숫자, 커스텀 구분자] 중간에 공백이 있는 경우

### 출력 조건

- 덧셈 결과를 출력한다
- `@woowacourse/mission-utils` 의 `Console.print()` 을 활용한다.
- 잘못된 값을 입력할 경우 "[ERROR]" 로 시작하는 메시지와 함께 `ERROR` 를 발생시킨 후 종료

#### 실행 결과 예시

```
덧셈할 문자열을 입력해 주세요.
1,2:3
결과 : 6
```

### 그 외 제약사항

- Node.js 20.17.0 버전 사용
- 프로그램 실행의 시작점은 `App.js` 의 `run()`
- 제공된 라이브러리, 스타일 라이브러리 이외의 외부 라이브러리 사용금지
- `process.exit()` 사용금지
- [JavaScript Style Guide](https://github.com/woowacourse/woowacourse-docs/tree/main/styleguide/javascript) 코드 컨벤션 지키기
- \_\_test\_\_/ApplicationTest 에 있는 모든 테스트 케이스가 성공해야 한다

### 기능별 요구사항

- 문자열 시작점 `//`, `\n` 사이에 커스텀 구분자 입력받기
  - //;\n1;2;3 인 경우 `;` 가 커스텀 구분자이며, 6이 반환
- 문자열에서 기본 구분자(`:`, `,`)로 숫자 분리
- 커스텀 구분자가 주어진다면, 해당 구분자도 사용하여 숫자 분리
- 모든 숫자를 분리하고 합 계산
  - 예: "" => 0, "1,2" => 3, "1,2,3" => 6, "1,2:3" => 6
- 잘못된 입력 시 "\[ERROR]" 메시지와 함께 `Error` 발생 후 종료

## 구현할 기능 목록

- 문자열 입력받기
  - `@woowacourse/mission-utils` 의 `Console.readLineAsync()` 를 활용
- 커스텀 구분자가 있는지 검사하는 메서드 구현
- 커스텀 구분자 지정하는 메서드 구현
  - 잘못된 입력 예외처리
    - [커스텀 구분자] 입력 도중 공백이 나오는 경우
    - [커스텀 구분자] 커스텀 구분자에 숫자가 포함된 경우
- 구분자를 모두 ',' 로 대체하는 메서드 구현
- 입력된 문자열을 더하는 메서드 구현
  - 잘못된 입력 예외처리
    - [숫자] 음수인 경우
    - [숫자] 지정되지 않은 구분자가 나오는 경우
    - [숫자] 중간에 공백이 나오는 경우
- 계산결과 출력
  - `@woowacourse/mission-utils` 의 `Console.print()` 을 활용

## 구현 체크리스트

- [x] 문자열 입력받기
  - [x] `@woowacourse/mission-utils` 의 `Console.readLineAsync()` 를 활용
- [x] 커스텀 구분자가 있는지 검사하는 메서드 구현
- [x] 커스텀 구분자 지정하는 메서드 구현
  - [x] 잘못된 입력 예외처리
    - [x] [커스텀 구분자] 입력 도중 공백이 나오는 경우
    - [x] [커스텀 구분자] 커스텀 구분자에 숫자가 포함된 경우
- [ ] 구분자를 모두 ',' 로 대체하는 메서드 구현
- [ ] 입력된 문자열을 더하는 메서드 구현
  - [ ] 잘못된 입력 예외처리
    - [ ] [숫자] 음수인 경우
    - [ ] [숫자] 지정되지 않은 구분자가 나오는 경우
    - [ ] [숫자] 중간에 공백이 나오는 경우
- [ ] 계산결과 출력
  - [ ] `@woowacourse/mission-utils` 의 `Console.print()` 을 활용
