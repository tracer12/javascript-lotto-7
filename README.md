# ** 로또 발매기 구현 **

## 구현할 기능 목록
### 1. 로또 구입 금액 입력받기
- [X] 정수 형태의 로또 구입 금액 입력
- [X] 로또 구입 금액 유효성 검사 함수 작성

### 2. 랜덤한 6개의 숫자 출력 기능
- [X] 구입 금액을 1000으로 나누고 나눈 만큼 1부터 45까지 중복되지 않는 랜덤한 6개의 번호 뽑기
- [X] 각각의 로또 번호들을 오름차순 정렬
- [X] 구입한 로또 개수와 각각의 로또 번호들을 출력한다

### 3. 당첨 번호 입력 기능
- [X] 쉼표를 포함한 문자열 형태의 당첨 번호 입력
- [X] 쉼표를 기준으로 당첨 번호 분리
- [X] 당첨 번호 오름차순 정리
- [X] 당첨 번호 유효성 검사 함수 작성

### 4. 보너스 번호 입력 기능
- [ ] 보너스 번호를 입력받는다
- [ ] 보너스 번호 유효성 검사 함수 작성

### 5. 결과 출력 기능
- [ ] 1~5등 까지의 당첨 내역을 출력한다
- [ ] 소수점 둘째 자리에서 반올림 한 수익률을 출력한다

### 6. 예외 처리
#### 로또 구매 금액 입력 에러 -> 에러메세지 출력 후 해당 지점부터 다시 입력 받기
- [X] 구입 금액이 1000의 배수가 아닌 경우
- [X] 구입 금액이 1000원 미만인 경우
- [X] 구입 금액이 공백일 경우(""), 공백은 앞뒤만 허용
- [X] 구입 금액이 숫자가 아닐 경우
#### 당첨 번호 입력 에러 -> 에러메세지 출력 후 해당 지점부터 다시 입력받기
- [X] 당첨 번호가 중복되는 경우
- [X] 당첨 번호에 숫자가 아닌 문자가 포함된 경우
- [X] 당첨 번호에 공백이 있는 경우(""), 공백은 앞뒤만 허용
- [X] 당첨 번호가 1~45가 아닌 경우
- [ ] 당첨 번호가 6개가 아닌 경우
#### 보너스 번호 입력 에러 -> 에러메세지 출력 후 해당 지점부터 다시 입력받기
- [ ] 보너스 번호가 당첨 번호와 중복인 경우
- [ ] 보너스 번호에 숫자가 아닌 문자가 포함된 경우
- [ ] 보너스 번호가 1~45가 아닌 경우

### 7. 테스트코드 추가
#### 로또 구입 금액 테스트코드
- [X] 구입 금액이 1000의 배수가 아닌 경우 테스트코드 추가
- [X] 구입 금액이 1000원 미만인 경우 테스트코드 추가
- [X] 구입 금액이 공백일 경우 테스트코드 추가
- [X] 구입 금액이 숫자가 아닐 경우 테스트코드 추가
#### 당첨 번호 테스트코드
- [X] 당첨 번호가 중복되는 경우 테스트코드 추가
- [X] 당첨 번호에 숫자가 아닌 문자가 포함된 경우 테스트코드 추가
- [X] 당첨 번호가 1~45가 아닌 경우 테스트코드 추가
- [X] 당첨 번호가 6개가 아닌 경우
#### 보너스 번호 테스트코드
- [ ] 보너스 번호가 당첨 번호와 중복인 경우 테스트코드 추가
- [ ] 보너스 번호에 숫자가 아닌 문자가 포함된 경우 테스트코드 추가
- [ ] 보너스 번호가 1~45가 아닌 경우 테스트코드 추가
- [ ] 보너스 번호가 공백인 경우 테스트코드 추가
#### 정상 입력
- [ ] 구입 금액이 정상인 경우 테스트코드 추가
- [ ] 당첨 번호가 정상인 경우 테스트코드 추가
- [ ] 보너스 번호가 정상인 경우 테스트코드 추가
- [ ] 통합 테스트코드 추가

# 기능 요구 사항

**간단한 로또 발매기를 구현한다.**

- 로또 번호의 숫자 범위는 1~45까지이다.
- 1개의 로또를 발행할 때 중복되지 않는 6개의 숫자를 뽑는다.
- 당첨 번호 추첨 시 중복되지 않는 숫자 6개와 보너스 번호 1개를 뽑는다.
- 당첨은 1등부터 5등까지 있다. 당첨 기준과 금액은 아래와 같다.
    - 1등: 6개 번호 일치 / 2,000,000,000원
    - 2등: 5개 번호 + 보너스 번호 일치 / 30,000,000원
    - 3등: 5개 번호 일치 / 1,500,000원
    - 4등: 4개 번호 일치 / 50,000원
    - 5등: 3개 번호 일치 / 5,000원
- 로또 구입 금액을 입력하면 구입 금액에 해당하는 만큼 로또를 발행해야 한다.
- 로또 1장의 가격은 1,000원이다.
- 당첨 번호와 보너스 번호를 입력받는다.
- 사용자가 구매한 로또 번호와 당첨 번호를 비교하여 당첨 내역 및 수익률을 출력하고 로또 게임을 종료한다.
- 사용자가 잘못된 값을 입력할 경우 "[ERROR]"로 시작하는 메시지와 함께 Error를 발생시키고 해당 메시지를 출력한 다음 해당 지점부터 다시 입력을 받는다.


# 추가된 프로그래밍 요구 사항
- 함수(또는 메서드)의 길이가 15라인을 넘어가지 않도록 구현한다.
    - 함수(또는 메서드)가 한 가지 일만 잘 하도록 구현한다.
- else를 지양한다
    - 때로는 if/else, when문을 사용하는 것이 더 깔끔해 보일 수 있다. 어느 경우에 쓰는 것이 적절할지 스스로 고민해 본다.
    - 힌트: if 조건절에서 값을 return하는 방식으로 구현하면 else를 사용하지 않아도 된다.
- 구현한 기능에 대한 단위 테스트를 작성한다. 단, UI(System.out, System.in, Scanner) 로직은 제외한다.
    - 단위 테스트 작성이 익숙하지 않다면 LottoTest를 참고하여 학습한 후 테스트를 작성한다.

# Lotto 클래스
- 제공된 Lotto 클래스를 사용하여 구현해야 한다.
- Lotto에 numbers 이외의 필드(인스턴스 변수)를 추가할 수 없다.
- numbers의 접근 제어자인 #은 변경할 수 없다.
- Lotto의 패키지를 변경할 수 있다.

```
class Lotto {
  #numbers;

  constructor(numbers) {
    this.#validate(numbers);
    this.#numbers = numbers;
  }

  #validate(numbers) {
    if (numbers.length !== 6) {
      throw new Error("[ERROR] 로또 번호는 6개여야 합니다.");
    }
  }

  // TODO: 추가 기능 구현
}
```