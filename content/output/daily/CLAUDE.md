# output/daily/ 운영 규칙

`scripts/watch-daily.ps1`이 평일 오후 5시에 자동 생성하는 일일 투자 점검 보고서 폴더다.

## 파일 명명

`YYYYMMDD_일일점검.md`

예: `20260605_일일점검.md`

## 생성 조건

- 평일(월~금) 오후 5시 자동 생성 (`INV_WIKI_DailyGenerate` 작업)
- 평일 오후 6시 텔레그램 전송 (`INV_WIKI_DailySend` 작업)
- 수동 즉시 실행: `watch-daily.ps1 -Once -DryRun`

## 보고서 형식

```yaml
---
type: daily-review
date: YYYY-MM-DD
generated_at: YYYY-MM-DD PM H시MM분
assets_count: N
alerts_count: N
---
```

## 자산 설정

`scripts/daily-assets.json` — Yahoo Finance 심볼, 그룹, 진입가 설정

진입가(`entry_price`) 설정 방법: `daily-assets.json`에서 해당 자산의 `entry_price` 값을 실제 매입가로 수정.
진입가 미설정(null) 시 진입가 대비 손실 계산 생략.

## 경고 기준

| 경고 | 조건 |
|---|---|
| DROP | 일간 하락 ≥ -3% (기본값, `alert_daily_drop_pct` 설정 가능) |
| SURGE | 일간 상승 ≥ +5% (`alert_daily_gain_pct`) |
| LOSS | 진입가 대비 손실 ≥ -10% (`alert_loss_from_entry_pct`) |
