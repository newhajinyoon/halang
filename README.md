# 하랭 (하진어)
###### 오픈소스 엄랭 기반 언어 


하진어란 무엇인가요?
=
- 하진어란 엄랭(오픈소스 언어) 기반 쓰다보면 정신병 오는 언어입니다.
- 하진어 제작자는 정신병 걸리면 손해배상을 지불하지 않습니다
- 하진어로 게임을 만들면 칭찬해드립니다

## 하랭 관련 사이트

| 이름 | 링크 | 내용 |
| ------ | ------ | ------ |
| 웹 하랭 | http://newhajinyoon.kro.kr/halang/ | 온라인 하랭 처리기
| 깃헙 | https://github.com/newhajinyoon/halang | 이 페이지
| 하랭 계산기 (친구랑이같이 만든) | http://naver.me/GE51chBp | 엔트리

문법
=
하진어는 "충격", "비키라", "하진신께서", "진짜만약에" 네개의 키워드와 "히", "ㅋ", " ", "~", "저런" 다섯개의 기호로 코드가 이루어집니다.
모든 프로그램은 "짜잔 내가 돌아왔다"로 시작하며, 항상 "이딴게 코드냐"로 끝나야 합니다.

## 자료형

정수: ㅋ, ㄷ의 갯수로 나타냅니다. ㅋ의 갯수만큼 1을 더하며, ㄷ의 갯수만큼 1을 뻅니다.

```
ㅋㅋㅋ => 3
ㅋㅋ => 2
ㄷㄷ => -2
ㄷㄷㄷ => -3
ㅋㄷㅋㄷ => 0
```

## 연산자

- 1 증가: `ㅋ`
- 1 감소: `ㄷ`
- 곱하기: " "(공백)

```
ㅋㅋ -> 2
ㄷㄷ -> -2
ㅋㄷ -> 0
ㅋㅋ ㅋㅋ -> 4
ㅋㅋ ㄷㄷ -> -4
ㅋㅋㅋ ㅋㅋㅋ ㅋㅋㅋ -> 27
```

## 변수

변수는 인덱싱(정수)을 통해 접근하고 대입할 수 있습니다. 지정하지 않았을경우 모든 변수의 기본값은 0입니다.

### 대입(충격)

연음의 갯수번째 변수에 뒤에 오는 수를 대입합니다

```
저런저런충격 => 3번째 변수에 0 지정
저런충격 => 2번째 변수에 0 지정
충격ㅋㅋ => 1번째 변수에 2 지정
저런충격ㅋ => 2번째 변수에 1 지정
충격ㄷㄷㄷ => 1번째 변수에 -3 지정
```

### 사용(저런)

연음의 갯수번째 변수를 불러옵니다

```
저런 => 1번째 변수
저런 => 2번째 변수
저런 => 3번째 변수
```

## 콘솔

### 하진신께서물으시되

콘솔에서 정수를 입력받습니다.

```
충격하진신께서물으시되 => 콘솔을 입력받아서 1번째 변수에 대입한다.
저런충격하진신께서물으시되 => 콘솔을 입력받아서 2번째 변수에 대입한다.
```

### 하진신께서히

콘솔에 정수를 출력합니다.

```tsx
하진신께서ㅋㅋ히 => 콘솔에 2 출력
하진신께서저런히 => 콘솔에 첫번째 변수 출력
```

### 하진신께서샍

콘솔에 문자를 출력합니다. `하진신께서`와 `샍`사이에 오는 정수를 유니코드 문자로 변환하여 콘솔에 출력합니다. `하진신께서`와 `샍`사이에 정수가 주어지지 않으면 개행합니다(`하진신께서샍` => `\n`)

```tsx
하진신께서ㄷㄷㄷㄷㄷㄷㄷㄷㄷㄷㄷ ㄷㄷㄷㄷㄷㄷㄷㄷㅋ => 콘솔에 X 출력
```

## 지시문

### 진짜만약에물으시되

`진짜만약에{정수}물으시되{실행할 명령}`으로 작성합니다. 정수가 0이라면 `실행할 명령`이 실행되며, 그렇지 않다면 다음줄로 넘어갑니다.

### 비키라

`비키라` 뒤에 오는 정수번째 줄로 이동합니다. `비키라ㅋㅋ => 2번째 줄(글자)로 이동`. 원라인코드의 경우에는 `~`로 분리된 코드단위로 카운트하여 이동합니다.

### 나가

`나가` 뒤에 오는 정수를 반환하며 프로그램을 종료합니다.

예제 모음
=
## hello world 출력
```
짜잔 내가 돌아왔다
충격
저런충격
저런저런충격
저런저런저런충격
저런저런저런저런충격
저런저런저런저런저런충격
저런저런저런저런저런저런충격

충격ㅋㅋㅋㅋㅋㅋㅋㅋ ㅋㅋㅋㅋㅋㅋㅋㅋㅋ
저런충격ㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋ ㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋ
저런충격저런저런ㅋ
저런저런충격저런저런ㅋㅋㅋㅋㅋㅋㅋ
저런저런저런충격저런저런저런ㅋㅋㅋ
저런저런저런저런충격ㅋㅋㅋㅋ ㅋㅋㅋㅋ ㅋㅋ
저런저런저런저런저런충격저런저런저런저런ㅋㅋㅋㅋㅋㅋㅋㅋ
저런저런저런저런저런저런충격저런저런저런ㅋㅋㅋㅋㅋㅋ
저런저런저런저런저런저런충격저런저런ㄷ

진짜만약에물으시되{

하진신께서저런샍
하진신께서저런저런샍
하진신께서저런저런저런샍
하진신께서저런저런저런샍
하진신께서저런저런저런저런샍
하진신께서저런저런저런저런저런샍
하진신께서저런저런저런저런저런저런샍
하진신께서저런저런저런저런샍
하진신께서저런저런저런ㅋㅋㅋㅋㅋㅋ샍
하진신께서저런저런저런샍
하진신께서저런저런저런저런저런저런저런샍
하진신께서샍
}

나가

이딴게 코드냐
```
## 구구단
```
짜잔 내가 돌아왔다 

충격ㅋㅋ
저런충격ㅋ
ㅋㅋㅋㅋㅋㅋㅋㅋ
저런저런저런충격ㅋㅋㅋㅋㅋㅋㅋㅋㅋ

하진신께서저런히
하진신께서ㅋㅋㅋㅋㅋㅋㅋㅋ ㅋㅋㅋㅋ샍
하진신께서ㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋ ㅋㅋㅋㅋㅋㅋㅋㅋ샍
하진신께서ㅋㅋㅋㅋㅋㅋㅋㅋ ㅋㅋㅋㅋ샍
하진신께서저런저런히
하진신께서ㅋㅋㅋㅋㅋㅋㅋㅋ ㅋㅋㅋㅋ샍
하진신께서ㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋ샍
하진신께서ㅋㅋㅋㅋㅋㅋㅋㅋ ㅋㅋㅋㅋ샍
하진신께서저런 저런저런히
하진신께서샍
저런저런저런충격저런저런저런저런ㄷ
저런충격저런저런ㅋ
진짜만약에저런저런저런저런물으시되비키라ㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋ
비키라ㅋㅋㅋㅋㅋㅋㅋㅋ

충격저런ㅋ
저런저런충격저런저런저런ㄷ
저런저런저런충격ㅋㅋㅋㅋㅋㅋㅋㅋㅋ
저런충격ㅋ
진짜만약에저런저런저런물으시되나가ㅋ
하진신께서샍
비키라ㅋㅋㅋㅋㅋㅋㅋㅋ
이딴게 코드냐
```
