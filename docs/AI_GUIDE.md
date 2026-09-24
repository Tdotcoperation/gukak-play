# PUNGRYU Music Code — AI Guide v0.1

PUNGRYU Music Code는 한국 전통악기 기반 웹 연주 엔진을 위한 텍스트 형식입니다.

## 기본 형식

```text
@title "곡 이름"
@tempo 108
@time 4/4

track gayageum {
  C4 1/4 velocity=90
  E4 1/4
  G4 1/2
}
```

## 지원 악기

- `gayageum` 가야금
- `haegeum` 해금
- `daegeum` 대금
- `janggu` 장구
- `buk` 북
- `danso` 단소

## 음표

멜로디 악기는 `C4`, `D4`, `E4`, `F#4` 형태의 음높이를 사용합니다.

지원 길이: `1/1`, `1/2`, `1/4`, `1/8`, `1/16`

쉼표:

```text
rest 1/4
```

강약:

```text
C4 1/4 velocity=80
```

`velocity`는 1~127입니다.

## 타악기

장구 기본 토큰: `deong`, `deok`, `kung`, `dda`

북 기본 토큰: `soft`, `mid`, `hard`, `rim`

## AI 작성 규칙

1. 반드시 track 블록 안에서 음표를 작성합니다.
2. 지원하지 않는 악기 이름을 만들지 않습니다.
3. 한 줄에 하나의 이벤트를 작성합니다.
4. 마디 길이를 가능하면 박자에 맞춥니다.
5. 지나치게 빠른 연속음을 피합니다.
6. 30~240 BPM만 사용합니다.

## 예제 프롬프트

PUNGRYU Music Code 형식으로 가야금, 대금, 장구를 사용하는 약 20초 길이의 밝은 음악을 작성해줘. BPM 108, 4/4박자이고 마지막은 자연스럽게 끝나게 해줘. 코드만 출력해줘.
