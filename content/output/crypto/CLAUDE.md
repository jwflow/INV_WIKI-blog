# output/crypto/ 운영 규칙

이 폴더는 **암호화폐 30분 포지셔닝 워처**(`watch-crypto-positioning.ps1`)가 자동 생성하는 리포트 저장소다.

## 파일 명명

`YYYYMMDD_HHmm_암호화폐포지셔닝.md`

예: `20260608_1000_암호화폐포지셔닝.md`

## 파일 구조

각 리포트는 다음 섹션을 포함한다:
- **포지셔닝 신호** — 점수, 편향(위험선호/중립/방어), AI 인사이트
- **시장 스냅샷** — BTC/ETH/XRP/SOL/LINK/ONDO 가격 + 1h/24h 변동
- **기관/달러 플로우** — BTC/ETH ETF 일간·5일 순유입 (Farside)
- **파생 포지셔닝** — 펀딩비, 미결제약정, 롱/숏 비율 (Binance)
- **주요 뉴스** — CoinDesk, Cointelegraph, Decrypt, Bitcoin Magazine

## AI 용도

- 리포트를 직접 읽어 최신 포지셔닝 판단에 활용한다.
- `output/synthesis/` 업데이트 시 이 리포트의 핵심 신호를 교차 참조한다.
- wiki 업데이트는 하지 않는다 — 이 폴더는 일시적 스냅샷이다.

## 자동화

- `scripts/watch-crypto-positioning.ps1` — 30분마다 실행, 리포트 저장 + Telegram 전송
- `INV_WIKI_CryptoPositioning` — Windows Task Scheduler, 로그인 시 자동 시작
- 로그: `scripts/watch-crypto-positioning.log`
