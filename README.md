# PUNGRYU Studio / 국악 Play

한국 전통악기를 직접 연주하고, **PUNGRYU Music Code**를 붙여 넣어 AI가 만든 연주를 실행하고 WAV로 내보낼 수 있는 웹앱입니다.

## 현재 기능

- 가야금 / 해금 / 대금 / 장구 / 북 / 단소 직접 연주
- PC 키보드 A–K 연주
- 연주 이벤트 녹음
- 녹음 결과 WAV 렌더링
- PUNGRYU Music Code 파서
- 여러 악기 트랙 동시 재생
- Music Code → WAV 오프라인 렌더링
- AI 가이드 문서 다운로드
- 실제 국악기 WAV 샘플을 넣기 위한 `samples/` 구조

현재는 실제 WAV가 없는 경우 Web Audio 기반 합성 폴백을 사용합니다.

## 로컬 실행

```bash
npm install
npm run dev
```

또는 정적 서버로 실행할 수도 있습니다.

```bash
python -m http.server 8080
```

## Cloudflare Workers 배포

이 저장소는 Workers Static Assets 형식의 `wrangler.jsonc`를 포함합니다.

```bash
npm install
npm run deploy
```

Cloudflare Dashboard에서 GitHub 저장소를 연결하는 경우:

- Repository: `Tdotcoperation/gukak-play`
- Build command: `npm install`
- Deploy command: `npx wrangler deploy`

## AI 가이드

전체 문법은 [docs/AI_GUIDE.md](./docs/AI_GUIDE.md)를 참고하세요.

## 실제 국악기 샘플

사용 권한을 확인한 WAV만 `samples/` 아래에 추가합니다. K-SOUND LIBRARY 음원을 사용할 경우 각 개별 음원의 라이선스와 표시 조건을 확인하고 저작자·출처 정보를 함께 기록해야 합니다.
