# **Java Racingcar Precourse**

### 초간단 자동차 경주 게임을 구현한다.

### 입출력 요구사항

**입력**

- 경주할 자동차 이름(이름은 쉼표(,) 기준으로 구분)

```java
pobi,woni,jun
```

- 시도할 횟수

```java
5
```

**출력**

- 차수별 실행 결과

```java
pobi : --
woni : ----
jun : ---
```

- 단독 우승자 안내 문구

```java
최종 우승자 : pobi
```

- 공동 우승자 안내 문구
```java
최종 우승자 : pobi, jun
```

### 실행결과 예시

```java
경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)
pobi,woni,jun
시도할 횟수는 몇 회인가요?
5

실행 결과
pobi : -
woni : 
jun : -

pobi : --
woni : -
jun : --

pobi : ---
woni : --
jun : ---

pobi : ----
woni : ---
jun : ----

pobi : -----
woni : ----
jun : -----

최종 우승자 : pobi, jun
```


### 기능 요구 사항

- [x] 주어진 자동차들, 경주(전진) 횟수를 객체로 담아 서비스 레이어에게 전달한다.(Console 을 사용한다.)
- [x] 자동차 이름은 쉼표(,)를 기준으로 구분한다.
- [x] 이름은 5자 이하만 가능하다.
- [ ] 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4 이상일 경우이다.
- [ ] 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.
- [ ] 우승자가 여러 명일 경우 쉼표(,)를 이용하여 구분한다.
- [ ] 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시킨 후 애플리케이션은 종료되어야 한다.

### 과제 진행 요구사항

- [x] 미션은 자동차 경주 저장소를 포크하고 클론하는 것으로 시작한다.
- [x] 기능을 구현하기 전 README.md에 구현할 기능 목록을 정리해 추가한다.
- [x] Git의 커밋 단위는 앞 단계에서 README.md에 정리한 기능 목록 단위로 추가한다.
- [x] AngularJS Git Commit Message Conventions을 참고해 커밋 메시지를 작성한다.
- [x] 자세한 과제 진행 방법은 프리코스 진행 가이드 문서를 참고한다.

### 프로그래밍 요구 사항 1

- [x] JDK 21 버전에서 실행 가능해야 한다.
- [x] 프로그램 실행의 시작점은 `Application`의 `main()`이다.
- [x] `build.gradle` 파일은 변경할 수 없으며, **제공된 라이브러리 이외의 외부 라이브러리는 사용하지 않는다.**
- [x] 프로그램 종료 시 `System.exit()`를 호출하지 않는다.
- [x] 프로그래밍 요구 사항에서 달리 명시하지 않는 한 파일, 패키지 등의 이름을 바꾸거나 이동하지 않는다.
- [x] 자바 코드 컨벤션을 지키면서 프로그래밍한다.

### 프로그래밍 요구 사항 2

- [x] indent(인덴트, 들여쓰기) depth를 3이 넘지 않도록 구현한다. 2까지만 허용한다.
  - 예를 들어 while문 안에 if문이 있으면 들여쓰기는 2이다.
  - 힌트: indent(인덴트, 들여쓰기) depth를 줄이는 좋은 방법은 함수(또는 메서드)를 분리하면 된다.
- [x] 3항 연산자를 쓰지 않는다.
- [x] 함수(또는 메서드)가 한 가지 일만 하도록 최대한 작게 만들어라.
- [x] JUnit 5와 AssertJ를 이용하여 정리한 기능 목록이 정상적으로 작동하는지 테스트 코드로 확인한다.
  - 테스트 도구 사용법이 익숙하지 않다면 아래 문서를 참고하여 학습한 후 테스트를 구현한다.
  - JUnit 5 User Guide
  - AssertJ User Guide
  - AssertJ Exception Assertions
  - Guide to JUnit 5 Parameterized Tests

### 라이브러리

 - camp.nextstep.edu.missionutils에서 제공하는 Randoms 및 Console API를 사용하여 구현해야 한다.
   - Random 값 추출은 camp.nextstep.edu.missionutils.Randoms의 pickNumberInRange()를 활용한다.
   - 사용자가 입력하는 값은 camp.nextstep.edu.missionutils.Console의 readLine()을 활용한다.

**사용 예시**
- 0에서 9까지의 정수 중 한 개의 정수 반환
```java
Randoms.pickNumberInRange(0, 9);
```