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
- **뉴스 분석** — CoinDesk, Cointelegraph, Decrypt, Bitcoin Magazine 원문 뉴스를 한글로 분석

## 뉴스 분석 섹션 형식 (2026-06-21 변경)

투자에 영향을 줄 수 있는 뉴스 항목마다 아래 형식으로 **한글** 분석을 제공한다:

```markdown
### 📰 [한글로 번역한 뉴스 제목]

- **한줄 요약**: 뉴스 내용을 한국어로 1문장으로 요약
- **시장 영향**: BTC·ETH·알트코인 가격 또는 투자자 심리에 미치는 직접적 영향 (2~3줄)
- **투자 시사점**: 포지션 관리 또는 진입/청산 판단에 활용할 구체적 시사점 (1~2줄)
- **중요도**: ★ (낮음) / ★★ (중간) / ★★★ (높음)
```

투자와 무관한 뉴스는 생략하며, 분석할 뉴스가 없으면 "주요 뉴스 없음"으로 표시한다.

## AI 용도

- 리포트를 직접 읽어 최신 포지셔닝 판단에 활용한다.
- `output/synthesis/` 업데이트 시 이 리포트의 핵심 신호를 교차 참조한다.
- wiki 업데이트는 하지 않는다 — 이 폴더는 일시적 스냅샷이다.

## 자동화

- `scripts/watch-crypto-positioning.ps1` — 30분마다 실행, 리포트 저장 + Telegram 전송
- `INV_WIKI_CryptoPositioning` — Windows Task Scheduler, 로그인 시 자동 시작
- 로그: `scripts/watch-crypto-positioning.log`
