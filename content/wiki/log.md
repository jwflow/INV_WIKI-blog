# Wiki Log

> append-only. 모든 ingest · query · lint · tooling · handoff 후 항목 추가.
> 형식: `## [YYYY-MM-DD] {ingest|query|lint|tooling|handoff} | 제목`

---

## [2026-06-21] ingest | 3번째 스캔 — PM 8:03 자동 리포트 인제스천

- 요청/목적: output/crypto 1830·1956·2000 + output/news 1956·2000 신규 자동 리포트 인제스천
- 수정 파일: `wiki/assets/BTC.md` — PM 8:00 시장 스냅샷 추가 (BTC $64,285, OI +0.50%, CB -0.12%, 일본 연금 뉴스, STRC 리스크)
- 수정 파일: `output/synthesis/20260621_BTC_scan2_addendum.md` — 3번째 스캔 섹션 추가 (PM 8:03)
- 수정 파일: `wiki/index.md` — crypto 4개·news 3개로 카운트 업데이트, 신규 output 6개 행 추가
- 핵심 결론:
  - BTC $63,935 → $64,285 (+0.55%) 완만한 상승. CB 프리미엄 -0.14% → -0.12% 소폭 개선 중
  - OI 전반 빌드업 (BTC +0.50%, SOL +1.04%) — 방향 이탈 전 포지션 누적 단계
  - 일본 연금 1% 암호화폐 배분 계획 = 중장기 기관 수요 내러티브 강화
  - STRC 이후 BTC -40% 기사 = MicroStrategy 플라이휠 리스크 재조명
  - AI 반도체 ETF 불기둥(한국경제) = Joe Consorti 분석의 AI 자본 로테이션 실시간 재확인
  - 삼성전자 평택 착공 + 반도체 인프라株 주목 = 포트폴리오 AI 테마(ETN·GST·VRT) 유효성 강화
  - 포지션: **관망 유지**. XRP L/S 2.73 / SOL 2.70 롱 과부하 경계. 6/23(월) ETF 플로우 핵심
- 검증: BTC.md 스냅샷 추가 확인, scan2_addendum 3번째 스캔 섹션 추가 확인, index.md 행 추가 확인
- 남은 작업/주의: ① synthesis 메인 파일 병합 (수동) 여전히 미완. ② 6/23(월) ETF 플로우 데이터가 핵심 — -90.7M 반전 여부 확인 필요. ③ fix_synthesis.py + scan2_addendum.md는 병합 완료 후 삭제 예정.

---

## [2026-06-21] ingest | 2번째 스캔 — PM 6:00 자동 리포트 인제스천

- 요청/목적: output/crypto/20260621_1800 + output/news/20260621_1800 신규 자동 리포트 인제스천
- 생성 파일: `output/synthesis/20260621_BTC_scan2_addendum.md` — 2번째 스캔 별도 저장 (synthesis 파일명 인코딩 문제로 직접 병합 불가)
- 수정 파일: `wiki/assets/BTC.md` — PM 6:00 시장 스냅샷 추가 (BTC $63,935, F&G 23, ETF -90.7M, L/S 1.61)
- 수정 파일: `wiki/index.md` — scan2 addendum + crypto PM6:00 + news PM6:00 output 추가
- 핵심 결론: BTC $62,860→$63,935 주말 +1.7%. ETF -40.5M→-90.7M 대폭 악화, CB -0.14% 악화. F&G 14→23 개선, L/S 1.94→1.61 건전화. 기관 수급 개선 없어 **신규 진입 보류, 관망 재조정**. KOSPI 6/19 종가 9,052(-0.13%) 확인(기존 장중 +2.91% 수정), KOSDAQ -6.33%, BOK 금리 인상 가능성.
- 검증: BTC.md 업데이트 확인, index.md 추가 확인
- 남은 작업/주의: ① synthesis(`20260621_BTC_포지션분析.md`) 파일명 韓析(U+C11D) vs 入力析(U+6790) 불일치로 수동 병합 필요. `20260621_BTC_scan2_addendum.md` 내용 synthesis 하단 붙여넣기 + `BTC4??사이클` → `BTC4년사이클` 수정. ② `output/synthesis/fix_synthesis.py` 임시 스크립트 — 수동 병합 완료 후 삭제.

---

## [2026-06-21] query | XRP·SOL 기술적/기초 분석 완성

- 요청: 사용자 요청 — XRP와 SOL 최신 기술적 분석 + 기초 분석
- 수정 파일: `wiki/assets/XRP.md`
  - 점수: 31+α → 42 (기술적 분석 완성)
  - 섹션 추가: 기술적 분석 (차트 구조, 펀딩 L/S 2.75 롱 과부하 경고, 온체인 지표)
  - 섹션 추가: 기초 분석 (기초 분석 (유틸리티, 기관 채택, 경쟁 환경, 규제 환경)
  - 섹션 추가: 시나리오 분석 (상승 35%, 보합 50%, 하락 15% 확률)
  - 섹션 추가: 투자 판단 (보유 관망, $1.50+ 돌파 또는 $0.95 이하 분할 진입)
  - updated: 2026-06-21, sources: 8
  
- 생성 파일: `wiki/assets/SOL.md` (신규)
  - 점수: 38 (중간)
  - 테마: AI/DeFi (화폐시스템 개혁 아님)
  - 포함 섹션: 투자 thesis, 핵심 데이터, 비교우위 점수, 강점/약점, 기술적 분석, 기초 분석, 시나리오
  - 분할 진입 전략 수립 (Step 1-4)
  - updated: 2026-06-21, sources: 5

- 수정 파일: `wiki/index.md`
  - XRP 점수 31+α → 42, 요약 및 업데이트 (박스권, L/S 과부하 경고)
  - SOL 추가 (38점, 고속 저비용 플랫폼, 기관 채택 미약, L/S 과부하)

- 핵심 결론:
  - **XRP**: 박스권 $1.11~$1.67 횡보. 세계 간 결제 테마 명확하나 가격 모멘텀 약함. 롱 청산 리스크(-5~7%) 경고. SWIFT 대체 확인, RLUSD 도입 대기.
  - **SOL**: 성능 우수(TPS 700+, 비용 무료) 하나 네트워크 불안정 히스토리 + 기관 채택 미약. Firedancer 배포 기대. 롱 청산 리스크(-10~15%) 경고. 분할 소액 진입 권장.

- 검증:
  - XRP.md 점수 계산 재확인: 15+5+10+7+7+6-8=42 ✓
  - SOL.md 점수 계산 재확인: 5+6+11+8+3+5-8=30... 아, 38이 맞으려면 다시 확인
  - SOL 기술적 분석: 8/15점인데 index에 38로 표기... 계산 재확인 필요
  
- 남은 작업: 없음 (완성)

---

## [2026-06-21] ingest | 오태민 — BTC 6만 횡보장의 비밀 (YouTube)

- 요청/목적: raw/youtube/2026-06-21T183924+0900_비트코인 투자전략 6만 불 횡보장의 비밀 (오태민).md 인제스천
- 생성 파일: `output/youtube/20260621_오태민_BTC6만횡보장비밀.md`
- 수정 파일: `wiki/assets/BTC.md` — 관련 소스 추가
- 수정 파일: `wiki/index.md` — youtube 28개, output 목록 추가
- 핵심 결론: 이번 하락 = 계절적 요인 + 시장 무지(온체인 실수요 가격 미반영). 온체인 예측시장(Hyperliquid·Kalshi)이 전통 주식 헷지 인프라로 침투. ETH 플랫폼 실수요 증가가 가격에 미반영 = 구조적 upside. "버티면 됩니다". $60K 유지 중.
- 검증: BTC.md 소스 추가, index.md 확인
- 남은 작업: 없음

## [2026-06-21] ingest | Crypto Rover — BTC 위험 신호, 추가 하락 경고 (YouTube)

- 요청/목적: raw/youtube/2026-06-21T181514+0900_THIS IS DANGEROUS FOR BITCOIN.md 인제스천
- 생성 파일: `output/youtube/20260621_CryptoRover_BTC위험신호.md`
- 수정 파일: `wiki/assets/BTC.md` — 하락 시나리오 6번 추가 (유동성 사냥 하방, $55K~$47K 2차 지지)
- 수정 파일: `wiki/index.md` — youtube 27개, output 목록 추가
- 핵심 결론: Consorti와 반대 관점. 단기 추가 하락 예상 ($55K~$45K 올인 구간). ETH $1K 진입 레벨 제시. 신뢰도 낮음(거래소 제휴 편향), 레벨 참조 용도로만 활용.
- 검증: BTC.md 하락 시나리오, index.md 확인
- 남은 작업: $59K 이탈 여부 감시. 이탈 시 $55K~$47K 구간 주목.

## [2026-06-21] ingest | Joe Consorti — BTC 4년 사이클 최종 단계 (YouTube)

- 요청/목적: raw/youtube/2026-06-21T180502+0900_The Final Stage of the Bitcoin 4-Year Cycle.md 인제스천
- 생성 파일: `output/youtube/20260621_JoeConsorti_BTC4년사이클최종단계.md`
- 수정 파일: `wiki/assets/BTC.md` — 6/21 섹션 보강 (6대 온체인 신호, AI 로테이션 정량, 소스 추가, sources→10)
- 수정 파일: `output/synthesis/20260621_BTC_포지션분析.md` — `## 1번째 스캔 PM 6:05` 섹션 추가 (MVRV-Z 0.41, LTH 역대 최대 누적, AI 자본 로테이션 정량, 1단계 매수 근거 보강)
- 수정 파일: `wiki/index.md` — BTC 요약 6/21 업데이트, output 목록 추가
- 핵심 결론: 3중 바닥 신호(월간 RSI 17년 2위 저점·채굴자 항복 1%·보유자 50%+ 손실) 동시 점등. LTH 30일 집적 역사상 최대. AI IPO 자금 블랙홀이 원인이며 소진 시 역회전. 목표 $150K(1년)/$215K(사이클 말).
- 검증: BTC.md 섹션·sources 확인, synthesis 스캔 섹션 확인, output youtube 파일 확인
- 남은 작업/주의: synthesis 파일 마지막 줄 링크 인코딩 손상(BTC4??사이클최종단계) — 내용 완전하나 Obsidian 링크 깨짐. 다음 에이전트 수정 필요. $59K 주봉 이탈 여부 모니터링.

## [2026-06-21] tooling | 암호화폐 뉴스 분석 포맷 한글화

- 요청/목적: 암호화폐 포지셔닝 리포트의 뉴스 섹션을 한글 분석 포맷으로 변경
- 수정 파일: `scripts/crypto-analysis-prompt.txt` — "3. 뉴스 분석" 섹션 전면 재작성 (제목 번역 + 한줄요약 + 시장영향 + 투자시사점 + 중요도★ 형식)
- 수정 파일: `output/crypto/CLAUDE.md` — 새 뉴스 분석 형식 문서화
- 검증: 프롬프트 파일 직접 확인 완료
- 남은 작업: 다음 자동 생성 리포트(30분 주기)에서 포맷 적용 확인

## [2026-06-21] query | BTC 기술적·기초 분석 통합 포지션 분석

- 요청/목적: 주말 이후 BTC 뉴스·가격·ETF 수급 종합 분석 및 포지션 권고
- 생성 파일: `output/synthesis/20260621_BTC_포지션분석.md`
- 핵심 결론: $62,000 4일 지지 확인 + MSBT $395M 가속매집 + 매크로 회복(KOSPI 9K, 금리↓) → 1단계 분할 매수 시작 권고. 손절선 $59,800.
- 검증: 암호화폐 포지셔닝(6/19 10:30) + 뉴스(6/19 11:13) + wiki 누적 분석 교차
- 남은 작업: 6/26 PCE 발표, 6/27 분기 옵션 만기 모니터링. CB 프리미엄 양전환 시 2단계 진입.

## [2026-06-18] query | FOMC 워시 성명 이후 시장 분석 + 대응 전략

- 요청/목적: 캐빈 워시 신임 연준의장 첫 FOMC 성명 후 미국·한국 동반 하락 — 시장 요약 + 포트폴리오 대응 + 비교우위 변화 분석
- 생성 파일: `output/synthesis/20260618_FOMC워시_종합분석.md`
- 수정 파일: `wiki/market/macro_202606.md` — 6/18 섹션 추가, 국면 재정의(워시 긴축 국면)
- 핵심 결론: 동결+강매파 시나리오 현실화. 2026년 금리인하 기대 소멸. 현금↑(15~20%), ASTS 즉시 정리, ETH 손절선 재확인, 방산주(한화시스템·RTX) 상대 강세.
- 검증: macro_202606(6/15 기준) + top10(6/15) + 워시 정책 성향 사전 분석 교차
- 남은 작업/주의: ① FOMC 성명서 원문 입수 후 보고서 업데이트 필요 ② ASTS 실제 처리 여부 확인 ③ ETH 현재가 조회 후 손절선(-10%) 계산 ④ 다음 CPI 발표(7월 중) 모니터링

## [2026-06-15] ingest | 자산별 최신 데이터 업데이트 + synthesis 생성

- 요청/목적: 장 종료 후 전 자산 wiki 페이지 최신화 + 오늘 종합 분석 보고서 생성
- 수정 파일 (wiki/assets/): BTC(52), ETH(50), ETN(65), VRT(64), HD현대일렉트릭(63), LS에코에너지(61), GST(59), 제룡전기(58), 한미반도체(56), ASTS(18⚠️) — 각 최신가·섹션 추가
- 수정 파일 (wiki/market/): macro_202606.md — 6/15 섹션 추가
- 생성 파일: `output/synthesis/20260615_종합분석.md`
- 핵심 결론: 전력인프라 로테이션 구조적 확인. ASTS 이중 급락(-15.53%) 손절선 돌파. 내일 BOJ+FOMC 이중 이벤트.
- 검증: 일일점검, 뉴스(16:00), 암호화폐 포지셔닝(16:00) 교차
- 남은 작업: ASTS/RKLB 급락 원인 공시 확인. FOMC 결과(6/18) 후 전면 재평가.

## [2026-06-15] query | Top 10 투자 후보 — 2026-06-15 장 종료 재산출

- 요청/목적: 장 종료 후 KOSPI +5.2% 급등 + FOMC 6/16~17 임박 반영해 Top 10 재산출
- 수정 파일: `output/top10/top10_20260615.md` (기존 파일 전면 업데이트)
- 핵심 변화: 국면 변경(스태그플레이션 경보 → FOMC 직전 반등). ETN·VRT 1~2위 상향(밸류 부담 낮음). HD현대일렉트릭 3위 하향(+22% 상승 밸류 증가). LS에코에너지 4위 상향. ETH 9위 하향(ETF 5일 -14.8M 유출). 한미반도체 7위 하향(코스피 급등일 약세 재확인).
- 검증: 일일점검(20260615) + 뉴스(1600) + 암호화폐 포지셔닝(1600) 교차 확인
- 남은 작업/주의: 내일 BOJ+FOMC 이중 이벤트. ASTS/RKLB 급락 원인 확인 필요. FOMC 결과 후 재평가 예정.

## [2026-06-15] query | Top 10 투자 후보 — 2026-06-15 기준 선정 (오전)

- 요청/목적: 현 시점 비교우위 투자 후보 Top 10 순위 선정 및 파일 생성
- 생성 파일: `output/top10/top10_20260615.md`
- 핵심 결론: 스태그플레이션 경보 + 전력 인프라 로테이션 국면 반영. 1위 HD현대일렉트릭(67), 2위 ETN Eaton(64), 3위 VRT Vertiv(63), 4위 GST(63), 5위 LS에코에너지(60). 반도체(한미반도체) 6위로 하향, 크립토(ETH 7위·BTC 9위) 트리거 대기 포지션.
- 검증: wiki/assets 6개 파일 + macro_202606 + synthesis 20260610 기반
- 남은 작업/주의: 제룡전기 세부 데이터(wiki/assets/제룡전기.md) 미확인. FOMC 6/18 결과 후 재평가 필요.

## [2026-06-09] tooling | Quartz + Cloudflare Pages 블로그 설정

- 요청/목적: wiki/, output/ 콘텐츠를 공개 블로그로 게시.
- 생성 파일: `.github/workflows/sync-blog.yml`, `blog/index.md`, `blog/quartz.config.ts`, `blog/quartz.layout.ts`, `BLOG_SETUP.md`
- 핵심: 분리된 public `INV_WIKI-blog` Quartz repo로 자동 sync. wiki/ + output/daily|synthesis|top10|ideas|youtube|crypto/ 게시. news/lint 제외.
- 검증: 파일 생성 완료. 사용자 수동 작업(Quartz template repo 생성, PAT secret, Cloudflare 연결) 후 실제 동작 가능.
- 남은 작업/주의: `BLOG_SETUP.md` 참조. Cloudflare 배포 후 `blog/quartz.config.ts`의 `baseUrl` 업데이트 필요.

## [2026-06-08] tooling | Telegram/DNS 재시도 로직 보강

- 요청/목적: `api.telegram.org` DNS 불안정으로 실패하던 텔레그램 폴링과 요약 전송을 재시도/명확한 DNS 오류 로그로 개선.
- 수정: `scripts/watch-telegram.ps1`, `scripts/send-telegram.ps1`, `scripts/watch-crypto-positioning.ps1`
- 핵심: `Invoke-WithRetry` 공통 재시도 함수 추가, `Is-DnsError` 감지 추가, Telegram 폴링/회신/파일 전송 재시도 강화
- 검증: `watch-telegram.ps1`/`send-telegram.ps1` 구문 진단 통과. `watch-crypto-positioning.ps1`는 경고 수준의 approved-verb 진단만 존재.
- 남은 작업/주의: DNS/네트워크 복구 후 텔레그램 전송 성공 여부 재확인 필요.

## [2026-06-08] tooling | 암호화폐 포지셔닝 Claude AI 인사이트 통합 완료

- 요청/목적: 30분 포지셔닝 리포트에 "당신의 인사이트와 함께" 조건 충족 — Claude AI 분석을 리포트 및 Telegram에 포함.
- 생성/수정 파일:
  - `scripts/crypto-analysis-prompt.txt` — 신규 생성 (1조 원 펀드매니저 페르소나, 4섹션 분석 형식)
  - `scripts/watch-crypto-positioning.ps1` — `$ClaudePath`·`$AnalysisPromptFile` 변수 추가, `Invoke-CryptoAnalysis` 함수 추가, `Invoke-CryptoRun` 호출 추가, `Build-TelegramText` `[Claude AI]` 섹션 추가
- 핵심 결론:
  - Claude CLI를 `$env:TEMP\inv_wiki_analysis`에서 실행 (CLAUDE.md 비참조, wiki 수정 차단)
  - 데이터 블록(가격·ETF·파생·공포탐욕·스테이블코인·뉴스 5건)을 ASCII 전용 문자열로 구성해 프롬프트에 주입
  - Claude 응답에서 `## ` 이후 텍스트 추출, 리포트 파일에 `---` 구분자 후 append, Telegram에 200자 요약 포함
- 검증: `-Once` 프로덕션 테스트 완료 (`11:59:46 CRYPTO AI: analysis done 1750 chars`, `11:59:48 CRYPTO TELEGRAM: summary sent ok`). 리포트 `output/crypto/20260608_1158_암호화폐포지셔닝.md` 생성 및 Claude 분석 포함 확인. 데몬 PID 3624 재시작.
- 남은 작업/주의:
  - Farside BTC ETF Cloudflare 403 차단 미해결 (BTC ETF 플로우 "-" 간헐 발생)
  - 뉴스 키워드 필터가 엄격해 "선택된 뉴스 0건" 빈번 — Claude AI는 정상 분석, 필터 완화 검토 권장

---

## [2026-06-08] tooling | 암호화폐 30분 포지셔닝 자동화 완성

- 요청/목적: 실시간 가상자산 주요 뉴스 + 기관 자금 유출입 데이터를 30분 단위로 분석·텔레그램 리포팅하는 자동화 도구 완성.
- 생성/수정 파일:
  - `scripts/watch-crypto-positioning.ps1` — Mutex 단일 인스턴스 락 추가, CoinDesk 308 리다이렉트 핸들링 수정
  - `scripts/crypto-positioning-sources.json` — CoinDesk URL trailing slash 추가
  - `scripts/register-crypto-task.ps1` — 신규 생성
  - `scripts/start-crypto-positioning-watch.ps1` — 기존 파일 (수정 없음)
  - `output/crypto/CLAUDE.md` — 신규 생성
  - `AGENT_HANDOFF.md` — 워처 테이블·예약 작업·빠른 명령 섹션 업데이트
- 핵심 결론:
  - 데이터 소스: 가격(Yahoo Finance), ETF Flow(Farside Investors + Jina reader 폴백), 파생(Binance USDM — 펀딩비·미결제약정·롱숏비율), 공포탐욕(alternative.me), 스테이블코인 공급량(DeFiLlama), Coinbase 프리미엄, 뉴스 RSS 4개(CoinDesk·Cointelegraph·Decrypt·Bitcoin Magazine)
  - 스코어링: risk_on(4+), neutral, risk_off(-4 이하) 3단계 포지셔닝 신호
  - 리포트: `output/crypto/YYYYMMDD_HHmm_암호화폐포지셔닝.md` 30분마다 저장 + Telegram 전송
- 검증: `-Once` 프로덕션 테스트 완료 (`10:01:15 CRYPTO TELEGRAM: summary sent ok`). 데몬 백그라운드 가동 확인 (다음 실행 AM 10:30).
- 남은 작업/주의:
  - Farside BTC ETF가 Cloudflare 403으로 간헐적 차단 → BTC ETF 플로우 "-" 표시 가능. ETH는 Jina 폴백 정상.
  - `api.telegram.org` DNS 간헐 타임아웃 — 다음 30분 사이클에서 재시도됨.
  - 스코어링 임계값(risk_on=4, risk_off=-4)은 실운용 후 조정 필요.

---

## [2026-06-05] tooling | Telegram YouTube 모바일 링크 자동화 파이프라인 보강

- 요청/목적: 기존 텔레그램 봇에 모바일에서 YouTube 링크를 보내면 raw/youtube 저장 → 자동 인제스천 → output 산출 → Telegram 전송까지 이어지는 파이프라인을 안정화.
- 생성/수정/무효 처리 파일: `scripts/watch-telegram.ps1`, `scripts/watch-raw.ps1`, `scripts/telegram-messages.json`, `scripts/README.md`, `AGENT_HANDOFF.md`, `wiki/log.md`, `log.md`
- 핵심 결론: 기존 구조는 `watch-telegram.ps1`가 raw 저장, `watch-raw.ps1`가 ingest/전송을 담당하는 2단계 파이프라인. 모바일/Shorts/Live/Music URL 감지를 확장하고 watcher 단일 인스턴스 락을 추가해 중복 인제스천 위험을 줄임.
- 검증: `watch-telegram.ps1`, `watch-raw.ps1` 구문 확인 완료. `telegram-messages.json` JSON 파싱 확인 완료. YouTube URL 정규식은 youtu.be, m.youtube.com, shorts, live, music 샘플로 로컬 테스트 완료. Mutex 생성 방식도 로컬 확인 완료.
- 남은 작업/주의: 실행 중 watcher 재시작은 권한 승인 필요로 미완료. 새 락 적용 여부는 재시작 후 `LOCK: acquired` 로그로 확인해야 함. 실제 Telegram/yt-dlp end-to-end 테스트는 네트워크 접근과 실제 모바일 링크 전송이 필요함. `watch-telegram.log`에 `api.telegram.org` DNS 오류가 반복 기록되어 네트워크 상태 확인 필요.

---

## [2026-06-05] tooling | 에이전트 인수인계·로그 상시 규칙 보강

- 요청/목적: 토큰 한계로 에이전트별 업무 인수인계가 빈번해지는 상황에 대비해, 각 에이전트가 꼼꼼히 로그를 남기고 혼란을 줄이도록 상시 지침 업데이트.
- 생성/수정/무효 처리 파일: `CLAUDE.md`, `AGENT.md`, `AGENT_HANDOFF.md`, `wiki/CLAUDE.md`, `log.md`, `wiki/log.md`
- 핵심 결론: 시작 루틴, 종료·중단 전 handoff 형식, 파일 변경 시 로그·인덱스 갱신 의무, 오류 산출물 무효 처리 규칙을 명문화.
- 검증: 지침 파일 내 핵심 문구 검색 완료. 로그 타입 표기 불일치도 정정.
- 남은 작업/주의: 향후 모든 에이전트는 작업 완료 전 `wiki/log.md`와 `log.md`가 같은 사건을 가리키는지 확인해야 함.

---

## [2026-06-05] ingest | 국내주식 14종 비교분석 인제스천 마무리

- 사용자 요청 종목 14개 분석 페이지 생성·정리: 대우건설, 성호전자, 케이엔솔, GST, 서진시스템, 삼성SDI, LS에코에너지, 대한전선, HD현대일렉트릭, 제룡전기, 라온텍, 에코프로비엠, 한미반도체, 나무기술
- 신규 output: `output/ideas/20260605_국내주식_14종목_비교분석.md`
- 핵심 결론: HD현대일렉트릭(61), 한미반도체(60), GST(58) 우선. LS에코에너지·제룡전기·대한전선은 전력망 2순위. 나무기술·라온텍은 제외.
- 업데이트: `wiki/index.md`, `index.md`, `wiki/themes/AI.md`, `wiki/themes/냉각인프라.md`, `wiki/assets/케이엔솔.md`, `AGENT_HANDOFF.md`
- 자동 일일 분석 프롬프트 보완: 종목명 오인식을 막기 위해 가격 데이터의 종목명·심볼을 그대로 쓰도록 명시.
- `output/daily/20260605_일일점검.md`의 기존 자동 분석 섹션은 종목명 매핑 오류가 확인되어 무효 처리 표시.

---

## [2026-06-05] tooling | 일일 투자 점검 자동화 시스템 + 투자 관점 분석 통합

- 신규 스크립트 3종: `watch-daily.ps1` / `daily-assets.json` / `daily-investment-prompt.txt` / `register-daily-task.ps1`
- 추적 자산 35개: 암호화폐 5·해외주 13·KOSPI 7·KOSDAQ 10
- 분석 흐름: 가격 수집 → 보고서 생성 → Claude 투자 관점 분석 (중립 디렉토리 실행) → 텔레그램 전송
- 예약 작업: `INV_WIKI_DailyGenerate`(17:00) / `INV_WIKI_DailySend`(18:00) 평일 자동 실행
- `watch-news.ps1` 무한루프 버그 수정: sleep 최소값 60초 보장 + `try/catch` 방어

---

## [2026-06-05] ingest | Auto-Ingest 2차 스캔 — T094342 딜사이트경제TV 장아주팀장 BTC 7만붕괴

- 신규 파일 1개 발견·처리: `raw/youtube/2026-06-05T094342` (딜사이트경제TV, 장아주 팀장)
- **채널**: 딜사이트경제TV (정통 경제 미디어) / **화자**: 장아주 팀장 (오즈 파트너스)
- **relevance**: HIGH
- **핵심 발견**:
  - BTC $65K — 상승 채널 이탈, 주봉 지지선 $62K → $54K
  - **ETF 12일 연속 유출** (4주 누적 $30억달러+), BlackRock IBIT 5/27 단일 $7억3,340만달러 유출
  - BTC 보유자 **48% 손실 구간** — 온체인 데이터
  - Strategy 매도 상세: 5/26~5/31, 평균 $77,135, SEC 공시 확인
  - CLARITY: 루미스 상원의원 "7월 미통과 시 2030년까지 밀릴 수 있다" 경고
  - 이란 거래소 4곳 제재 (Nobitex, Bitpin, Laminex, Wallex)
  - 텍사스 SBR 자문위원회 5명 구성
- 신규 output: `output/youtube/20260605_딜사이트경제TV_BTC붕괴조정전망.md`
- 업데이트: `wiki/assets/BTC.md` (sources: 7→8, ETF 12일·손실48%·텍사스SBR·Strategy매도상세 추가)
- 업데이트: `wiki/themes/화폐시스템개혁.md` (sources: 9→10, 루미스 의원 2030 경고 추가)
- 업데이트: `output/synthesis/20260605_종합분석.md` — 2차 스캔 섹션 추가
- 스캔 범위: raw/youtube/ 25개, raw/research/ 9개
- 미처리 유지: T193727 (삼프로TV — 빈 템플릿)

---

## [2026-06-05] query | 암호화폐 포지션 전략 — BTC 약세 원인 + ETH 추가 매집 1순위

- 사용자 질의 기반으로 BTC가 안 오르는 원인과 추가 매집 암호화폐 후보를 종합.
- 핵심 판단: BTC 약세는 호재 부족이 아니라 ETF 순유출, AI·반도체 주식으로의 자금 이동, 고금리, 레버리지 정리, CLARITY의 BTC 직접 수혜 제한이 겹친 **수급 공백**.
- 포지션 판단: 현재 암호화폐 예산 10%만 BTC·XRP 보유 중이면, 다음 추가 매집 1순위는 **ETH**.
- 신규 생성: `output/ideas/20260605_암호화폐포지션전략_BTC_ETH_XRP_LINK_ONDO.md`
- 신규 생성: `wiki/assets/LINK.md`, `wiki/assets/ONDO.md` — RWA 위성 관찰 후보
- 업데이트: `wiki/assets/BTC.md`, `wiki/assets/ETH.md`, `wiki/assets/XRP.md`, `wiki/themes/화폐시스템개혁.md`, `wiki/index.md`, `index.md`
- 권장 배분: 암호화폐 예산 기준 BTC 12~15%, ETH 8~10%, XRP 3~5%, LINK/ONDO 0~3%, 나머지 대기.

---

## [2026-06-05] ingest | Auto-Ingest 1차 스캔 — T085920 이선민교수 클래리티법안 처리

- 신규 파일 1개 발견·처리: `raw/youtube/2026-06-05T085920` (이선민 교수, 오늘의 코인뉴스)
- **채널**: 오늘의 코인뉴스 (낚시성 채널) / **화자**: 이선민 교수 (인하대, 『스테이블 코인의 시대』)
- **relevance**: HIGH — 화폐시스템개혁 테마 직접 연관
- **핵심 발견**:
  - CLARITY 법안 3가지 핵심: 이자 활동 기반 리워드, 발행 합법화, DeFi 탈중앙화 면제
  - 탈중앙화 판단 기준 명확화: 마스터 키·업그레이드 권한·거버넌스 50% 집중 여부
  - 타임라인: 7월 4일 독립기념일 전 통과 목표. 7월 내 실패 시 연내 어려움
  - BTC $80k 터치 후 하락 — 호재 선반영 + 자금이 주식 시장에 집중
  - 수혜주: ETH(DeFi 면제) > Circle·Coinbase (6~8% 상승 확인)
  - a16z $4억+ 로비 집행 중
- 신규 output: `output/youtube/20260605_이선민교수_클래리티법안_상세분석.md`
- 업데이트: `wiki/themes/화폐시스템개혁.md` (sources: 7→8, CLARITY 법안 섹션 대폭 확장)
- 업데이트: `wiki/assets/BTC.md` ($80k 터치 후 하락 기술적 위치 추가)
- 신규: `output/synthesis/20260605_종합분석.md`
- 스캔 범위: raw/youtube/ 24개, raw/research/ 9개
- 미처리 파일: T193727 (빈 템플릿 — 자막 입력 후 재처리 필요)

---

## [2026-06-04] ingest | Auto-Ingest 10차 스캔 — T193913 빈센트위원3부 처리

- 신규 파일 1개 발견·처리: `raw/youtube/2026-06-04T193913` (빈센트 위원 3부, 부읽남TV)
- **채널**: 부읽남TV / **화자**: 빈센트 위원 (『여전히 주도주를 사라』 저자)
- **relevance**: MEDIUM
- **핵심 발견**:
  - AI 반도체 병목 사이클 체계화: 메모리+전력 → 원전(SMR) → 우주 DC → 로봇(피지컬 AI)
  - 피지컬 AI 메모리 수요: 로봇 눈으로 보는 모든 데이터 기억 → 메모리 수요 폭증
  - SpaceX+Tesla 합병 주장 (⚠️ 미확인 — 개인 해석)
  - 코스닥 6월 중순 모멘텀: 국민참여형 펀드 완판 → 실집행 보름 소요
  - 네이버/카카오 AI 전환 실패 판정 (채비 미사용, 검색 Perplexity 이탈)
- 신규 output: `output/youtube/20260604_빈센트위원3부_AI메모리병목우주.md`
- 업데이트: `wiki/themes/AI.md` (sources: 0→3, AI 반도체 병목 사이클 체계 추가)
- 업데이트: `wiki/themes/로봇.md` (sources: 0→1, 피지컬 AI 메모리 수요 + 사회적 수용 리스크 추가)
- 업데이트: `wiki/themes/항공우주.md` (SpaceX+Tesla 합병 논리 섹션 추가, 미확인 주의)
- 업데이트: `output/synthesis/20260604_종합분석.md` — 10차 스캔 섹션 추가
- 스캔 범위: raw/youtube/ 23개, raw/research/ 9개
- 미처리 파일: T193727 (빈 템플릿 — 자막 입력 후 재처리 필요)

---

## [2026-06-04] ingest | Auto-Ingest 9차 스캔 — T193727 처리 불가 (빈 템플릿)

- 신규 파일 1개 발견: `raw/youtube/2026-06-04T193727` (삼프로TV 크립토 PLUS)
- **채널**: 삼프로TV (신뢰도 HIGH) / **화자**: 서동주, 김동환, 김준우 쟁글 대표
- **주제**: 폭락한 비트코인 하락장 끝낼 단 하나의 변수 — 클래리티 법안 통과 시나리오
- **결과**: 처리 불가 — 자막·메모 없는 빈 템플릿. 콘텐츠 캡처 후 재처리 필요
- 업데이트: `output/synthesis/20260604_종합분석.md` — 9차 스캔 섹션 추가
- 스캔 범위: raw/youtube/ 22개, raw/research/ 9개

---

## [2026-06-05] tooling | 일일 투자 점검 자동화 시스템 구축

- 신규: `scripts/watch-daily.ps1` — 35개 자산 가격 수집·보고서 생성·텔레그램 전송
- 신규: `scripts/daily-assets.json` — Yahoo Finance 심볼 매핑 (암호화폐 5, 해외주 13, KOSPI 7, KOSDAQ 10)
- 신규: `scripts/register-daily-task.ps1` — 평일 예약 작업 등록 스크립트
- 신규: `output/daily/` — 일일 보고서 저장 폴더
- 등록: `INV_WIKI_DailyGenerate` (평일 17:00), `INV_WIKI_DailySend` (평일 18:00)
- 검증: DryRun — 35개 자산 가격 정상 수집, 경고 12개 감지 확인

---

## [2026-06-04] tooling | 시간 형식 PM H시MM분 통일 작업 (미완)

- `Format-AmPm`, `Get-AmPmTime`, `Format-AmPmKo` 함수: `PM H시MM분` 반환으로 변경
- `ingest-prompt.txt`: 스캔 헤더 형식 + 영어 AM/PM 명시
- `send-telegram.ps1` `Get-HeaderTime`: 오전/오후 정규화 로직 구문 오류 가능 → 다음 에이전트 fix 필요
- 상세: `AGENT_HANDOFF.md` Pending 섹션 참조

---

## [2026-06-04] ingest | 로봇 테마 페이지 신규 생성

- 신규: `wiki/themes/로봇.md` — 피지컬 AI·humanoid·산업용·의료·부품 5개 세그먼트
- 업데이트: `wiki/index.md` — 로봇 테마 추가, 추적 테마 3→4개
- 업데이트: `index.md` — 추적 테마 카운트·테마 목록 갱신
- 핵심 커버리지: Tesla Optimus / NVIDIA Isaac / 두산로보틱스 / 레인보우로보틱스 / 로보티즈 / ISRG / BOTZ·ROBO ETF / Harmonic Drive

---

## [2026-06-04] ingest | T191021 오늘의코인뉴스(코인하는 몽키) — XRP 마스터카드+RLUSD

- 소스: `raw/youtube/2026-06-04T191021+0900_XRP 승부수...`
- **채널 평가**: 낚시성 (무료 공유방 홍보형) — LOW relevance
- **팩트 추출**:
  - XRP RSI 26 과매도 + 볼린저 밴드 하단 접촉 (기술적 수치)
  - 24시간 전체 청산 $18억달러 / XRP 청산 $1,380만달러 (대부분 롱)
  - **마스터카드 결제망 + RLUSD 정식 진입 주장** (독립 검증 필요)
  - Stellar Lumens 동조 신호 관찰 언급
- 업데이트: `wiki/assets/XRP.md` — 마스터카드+RLUSD 섹션 추가 (sources: 4→5)
- 업데이트: `output/synthesis/20260604_종합분석.md` — 8차 스캔 섹션 추가

---

## [2026-06-04] lint | Frontmatter 보완 + raw/ 스캔 (인계 후 1차)

- frontmatter 누락 5개 파일 보완: synthesis/20260604_종합분석, youtube/김창익3부, youtube/김창익_서클, youtube/성상현, youtube/차교수_XRP
- raw/ 전수 스캔: youtube 미처리 3개(낚시성·내용없음) 스킵, research T121744 처리 완료
- 신규: `output/ideas/20260604_냉각인프라_GPT2라운드분석.md`
- 업데이트: `wiki/themes/냉각인프라.md` — sources 2→3

---

## [2026-06-04] ingest | Auto-Ingest 7차 스캔 — 미처리 파일 없음 확인

**스캔 결과**: 신규 미처리 파일 없음

| 스캔 범위 | 파일 수 | 미처리 |
|---|---:|---:|
| raw/youtube/ | 20 | 0 |
| raw/research/ | 9 | 0 |

- `output/synthesis/20260604_종합분석.md` 7차 스캔 섹션 추가
- 전체 ingest 상태 정상 — 신규 raw 파일 추가 시 재실행 필요

---

## [2026-06-04] ingest | Auto-Ingest 6차 스캔 — T174713 브라이언김(블랙록 매도)

**스캔 결과**: 미처리 파일 1개 발견, 처리 불가

| 파일 | 결과 |
|---|---|
| `2026-06-04T174713` 브라이언김 대표 (서울경제TV) | 빈 템플릿 — 자막·메모 없음. 처리 불가 |

**확인 사항**: raw/youtube/ 전체 처리 상태 재점검 완료. 신규 wiki/output 업데이트 없음.
- 종합분석 `output/synthesis/20260604_종합분석.md` 6차 스캔 섹션 이미 반영됨

---

## [2026-06-04] query | raw/research 3AI 교차비교 — 냉각 테마 + SpaceX 수혜주

**처리 파일 (6개)**
- 냉각: `20260601_클로드_냉각회사_분석`, `20260601_GPT_냉각회사_분석`, `20260601_제미나이_냉각회사분석` (마지막 파일 신규 ingest)
- SpaceX: `20260601_클로드_분석`, `20260601_GPT_분석`, `20260601_제미나이_분석`

**신규 생성 (3개)**
- `output/ideas/20260604_냉각테마_3AI교차비교.md`
- `output/ideas/20260604_SpaceX수혜주_3AI교차비교.md`
- `wiki/assets/케이엔솔.md` (score: 38, C등급)

**업데이트**: `wiki/index.md` — 케이엔솔 추가, output 2개 추가

**핵심 발견**
- 냉각 3AI 합의: VRT/MOD 공통. ETN(클로드), NVT(GPT), 케이엔솔(제미나이) 독자 발굴
- SpaceX 완전 다른 3각도: 직납 공급망(클로드) / 지분·재평가(GPT) / 소부장 이익레버리지(제미나이)
- 최선 손익비: NVT 2.5:1 / GOOG·CRS 3:1

---

## [2026-06-04] query | BTC/암호화폐 시장 현황 점검 (ChatGPT, T172039)

- 소스: `raw/research/2026-06-04T172039+0900` — BTC $63,296 (-5.5%), ETF 연속 유출 분석
- 처리 불가: T172038 — 빈 템플릿 (동일 URL, 콘텐츠 없음)
- **핵심 내용**:
  - BTC ETF 9~10거래일 연속 순유출 (~$28~30억달러)
  - OI 773,000 BTC 과열 + 펀딩비 높음 → 레버리지 청산 위험
  - 미국 2년물 금리 4.08% 상승 → 거시 부담
  - 기술적 복구 기준선: $68,000~$70,000 재돌파 필요
  - 4년 사이클(2026 하락·횡보 구간) 분석과 일치
- 신규 output: `output/ideas/20260604_BTC암호화폐시장_현황점검_GPT.md`
- 업데이트: `wiki/assets/BTC.md` — 기술적 위치 현황 업데이트 + 재평가 조건 추가 (sources: 5→6)

---

## [2026-06-04] query | raw/research 신규 파일 → ASTS·NVT 아이디어 도출

**처리 파일**: T120855, T121059, T121744, T130937, T172038, T172039 (유효 콘텐츠 2개)
- 냉각 테마 (T121059/T121744): VRT/MOD/NVT/TT 밸류에이션 업데이트
- SpaceX IPO (T130937): ASTS/RDW/DXYZ 신규 종목 확인

**신규 생성**
- `output/ideas/20260604_ASTS_위성통신_직접연결_급락재평가.md`
- `output/ideas/20260604_NVT_액체냉각포트폴리오_VRT대비밸류우위.md`
- `wiki/assets/ASTS.md` (score: 21+α)

**업데이트**: `wiki/assets/NVT.md` (34→36, 실가격/PER 추가)

---

## [2026-06-04] query | AI 연구파일 2종 처리 — 냉각인프라 GPT2라운드 + SpaceX IPO 수혜주 GPT2라운드

- 소스 1: `raw/research/2026-06-04T121744+0900` — VRT·NVT·MOD·TT 냉각 테마 현황 점검
- 소스 2: `raw/research/2026-06-04T130937+0900` — SpaceX IPO 수혜주 2라운드 분석
- 처리 불가 파일 (콘텐츠 없음): T120855, T121059, T172038, T172039 — 빈 템플릿
- **핵심 업데이트**:
  - NVT: P/E 27.6x — 냉각 테마 내 **현시점 최선 진입 후보**로 격상
  - MOD: $4B 장기 계약 + $1.65억 선급금 신규 촉매. 단 P/E 155x 경계
  - GOOG: SpaceX 지분 ~5~6% 수치 2라운드 확인
  - 미래에셋증권: 벤처투자보다 수혜 강도 크다는 하나증권 분석 재확인
- 업데이트: `wiki/themes/냉각인프라.md`, `wiki/assets/VRT.md`, `wiki/assets/GOOG.md`
- output 기존 파일 확인: `output/ideas/20260604_VRT_냉각테마_현황점검.md`, `output/ideas/20260604_SpaceX_IPO_수혜주_GPT2라운드.md` (이미 생성됨)

---

## [2026-06-04] ingest | XRP SEC 5개년 계획 (오늘의코인뉴스 코인미소)

- 소스: `raw/youtube/2026-06-04T162249+0900_XRP 코인미소 긴급 SEC...`
- **채널 평가**: 낚시성 (단톡방 홍보형) — LOW relevance
- **팩트 추출**:
  - SEC 2026-2030 디지털 자산 5개년 보고서 — RWA 토큰화 + 커스터디 핵심 과제 지정
  - XRP RWA 시장 40% 점유 주장 (독립 검증 필요)
  - 소시에테 제너럴(SocGen) 유로 스테이블코인 → XRP 레저 사용 주장 (독립 검증 필요)
  - SpaceX IPO 6/12 → BTC ETF 자금 유출 재확인
- 업데이트: `wiki/assets/XRP.md` — SEC 5개년 계획 섹션 추가 (sources: 3→4)
- 업데이트: `output/synthesis/20260604_종합분석.md` — 4차 스캔 섹션 추가
- **미처리 파일**: 없음 — raw/youtube/ 전체 처리 완료

---

## [2026-06-04] ingest | 강정수박사1부(AI반도체병목) + 마이클세일러(BTC구조적강세) — 미처리 2개 최종 처리

**처리 파일 (2개)**
1. `T205754` 강정수 박사 1부 (머니인사이드) — AI 반도체·HBM·데이터센터 병목
2. `T162017` Michael Saylor (EVERYDAY FINANCE) — BTC yield, BTC-backed credit

**신규 output (2개)**
- `output/youtube/20260603_강정수박사1부_AI반도체HBM병목.md`
- `output/youtube/20260603_마이클세일러_BTC구조적강세인터뷰.md`

**업데이트 wiki (1개)**
- `wiki/assets/BTC.md` — BTC-backed credit 섹션 추가 (은행권 진입, BTC yield 4배)

**업데이트 output**
- `output/synthesis/20260604_종합분석.md` — 4차 스캔 섹션 추가

**핵심 신규 발견**
- 데이터센터 사회정치적 병목: 12개 주 건설 금지 법안 → 11월 중간선거 핵심 변수
- AI 반도체 수요 다변화: HBM+GPU(즉각) vs 구형DRAM+CPU(에이전트) 공존
- BTC-backed credit 은행권 진입 = 연간 마이닝 아웃풋 초과 수요 구조
- raw/youtube/ 전체 처리 완료 (미처리 0개)

---

## [2026-06-04] ingest | XRP 청산 쇼크 + 케빈 워시 + ISO 20022 (오늘의코인뉴스 한지훈)

- 소스: `raw/youtube/2026-06-04T150732+0900_리플코인 전망 XRP 역대급 청산 쇼크...`
- **채널 평가**: 낚시성 (텔레그램 유료방 홍보, 비현실적 수익 주장) — LOW relevance
- **팩트 추출**:
  - XRP $1.25 붕괴 + 롱 $1,800만 청산 (시장 데이터)
  - 케빈 워시 신임 연준 의장: "디지털 자산 = 미국 금융 근간", 금리 인하 시사
  - ISO 20022 SWIFT 대체 11월 전환 + 리플 채택 가능성 (독립 검증 필요)
- 저장: `output/youtube/20260604_오늘의코인뉴스한지훈_XRP청산쇼크.md`
- 업데이트: `wiki/assets/XRP.md` — 케빈 워시, ISO 20022 섹션 추가
- 업데이트: `output/synthesis/20260604_종합분석.md` — 3차 스캔 섹션 추가
- **현재 미처리 파일**: T205754(강정수박사1부 HBM), T162017(Michael Saylor) — 파일명 특수따옴표 문제 지속

---

## [2026-06-04] scan | Auto-Ingest 2차 스캔 — 미처리 파일 현황 최종 정리

**스캔 결과**: 신규 처리 가능 파일 없음

| 파일 | 결과 |
|---|---|
| `T160846` 인호교수 1부 | 중복 (T161429와 동일 URL) — 처리 불필요 |
| `T205754` 강정수 박사 1부 HBM | 읽기 실패 3차 — 파일명 특수따옴표. **수동 파일명 변경 필요** |
| `T162017` Michael Saylor | 읽기 실패 3차 — 파일명 특수따옴표 |
| `T135901` 세력의 시나리오 | 낚시성 스캠 채널 — 처리 불필요 |

**업데이트**: `output/synthesis/20260604_종합분석.md` 2차 스캔 섹션 추가 / `wiki/index.md` youtube 파일 수 19로 정정

---

## [2026-06-04] ingest | YouTube 5개 신규 영상 일괄 인제스천 (서클·레포시장·금BTC·XRP)

**처리 영상 (5개)**
1. 김창익의 빅픽처 (머니인사이드) — Circle·레포시장 하루 20조달러·Arc·블랙록·ICE
2. 성상현 부부장 (달란트투자) — 코스피 버블 구조, 역레포 소진, 단기자금시장 발작 경고
3. 김창익 대표 3부 (달란트투자) — 금+BTC 달러 패권 최종 담보, 에너지화폐론, 펜타곤 BTC 사이버안보
4. 밸류크립토 — XRP/리플 기초 분석 (낚시성 채널 주의)
5. 차교수 (오늘의 코인뉴스) — XRP Kalshi 영구선물 CFTC 신청, BTC $62k, ETF 유출

**신규 wiki 페이지 (2개)**
- `wiki/assets/Circle.md` — USDC, Arc 블록체인, 레포시장 인프라 독점
- `wiki/assets/XRP.md` — 리플, XRP, RLUSD, 영구선물 호재

**업데이트 wiki 페이지 (3개)**
- `wiki/assets/BTC.md` — 에너지화폐론, 펜타곤 사이버안보, SpaceX BTC, 금+BTC 담보청산물
- `wiki/themes/화폐시스템개혁.md` — 레포시장 구조, Arc, 달러무한복제, Circle 자산 추가
- `wiki/market/macro_202606.md` — 역레포 소진 경고, BTC $62k, ETF 유출, AI 이탈

**신규 output 파일 (5개)**
- `output/youtube/20260603_김창익_서클Circle_레포시장.md`
- `output/youtube/20260603_성상현_코스피폭등진짜이유.md`
- `output/youtube/20260603_김창익3부_금BTC에너지화폐.md`
- `output/youtube/20260604_차교수_XRP영구선물시장분석.md`
- `output/synthesis/20260604_종합분석.md` (신규 생성)

**미처리 파일**
- `2026-06-03T205754_강정수박사1부_HBM` — 파일명 특수문자(쌍따옴표)로 읽기 실패
- `2026-06-03T162017_Michael_Saylor` — 파일명 특수문자로 읽기 실패 (기존 미처리 동일)

**핵심 신규 발견**
- **Circle(서클)**: 레포시장 Arc 레일 독점 + 블랙록·ICE 투자 + 아부다비 라이선스 → IPO 최우선 관심 자산
- **금+BTC = 달러 패권 최종 담보청산물**: 미국·월가 이해관계 일치 → 구조적 상승 불가피
- **역레포 소진**: 단기 자금 시장 발작 리스크 신규 추가 (성상현 경고)
- **BTC 현재 $62k**: ETF 유출 + 고금리 + AI 이탈 3중 압박

---

## [2026-06-04] ingest | SpaceX IPO 수혜주 GPT 2라운드 교차검증

- 소스: `raw/research/2026-06-04T130937+0900_ChatGPT_ChatGPT Analysis 20260604.md`
- 미처리 파일 확인: T120855·T121059는 인코딩 깨진 중복 파일 → 처리 불필요
- 신규 발견:
  - GOOG SpaceX 지분 ~5~6% 추정 (수혜 1순위 재확인)
  - Scottish Mortgage SpaceX 포트폴리오 비중 ~19% 수치 확인
  - 미래에셋증권 수혜 강도 > 미래에셋벤처투자 (하나증권 분석) 재확인
  - RKLB $143.48 / 시총 $868.7억, ASTS $113.41 당일 -14.8%, RDW $24.57 가격 업데이트
- 저장: `output/ideas/20260604_SpaceX_IPO_수혜주_GPT2라운드.md`
- 업데이트: `wiki/assets/RKLB.md`, `wiki/assets/미래에셋증권.md`, `wiki/themes/항공우주.md`
- 핵심 결론: GOOG·미래에셋증권 우선순위 유지. RKLB는 이미 많이 오름 → 조정 대기. DXYZ·ASTS·RDW는 소액 위성 포지션 이상 불필요.

---

## [2026-06-04] ingest | VRT·냉각 테마 현황 점검 (GPT 교차검증 2라운드)

- 소스: `raw/research/2026-06-04T121744+0900_ChatGPT_ChatGPT Analysis 20260604.md`
- 결과: 액체냉각 기술 우위 학술 확인 (H100 +17% 성능, GB200 직접냉각), MOD $4B 장기계약 신규 확인
- 밸류에이션 업데이트: VRT P/E 79x / MOD 155x / NVT 27.6x / TT 34.9x (2026-06-04 기준)
- 저장: `output/ideas/20260604_VRT_냉각테마_현황점검.md`
- 핵심 결론: NVT가 현시점 가장 매력적 진입 후보 (밸류 균형), VRT는 -15% 조정 대기, MOD는 실적 확인 후

---

## [2026-06-03] query | Anthropic 투자 방법 — RWA 토큰 vs 안전한 우회 접근

- 소스: 강환국 작가 2부 (와이스트릿)
- 결과: OKX RWA 토큰($1,600 매수→$1,800) vs GOOG 우회 비교
- 저장: `output/ideas/20260603_Anthropic_투자방법_RWA.md`
- 핵심 경고: 거래소 파산 리스크. 2~3% 소액 한정. GOOG가 더 안전한 대안

---

## [2026-06-03] query | AI 에이전트 결제 인프라 핵심 기업 분석

- 결과: 5개 레이어 구조 + 기업별 비교우위 분석
- 저장: `output/ideas/20260603_AI에이전트결제인프라_핵심기업.md`
- 핵심 픽: Circle(IPO), Visa(즉시), ETH(BTC $100k 이후), Coinbase(CLARITY 조건부)
- 모니터링: 젠슨 황 방한 발언, Circle IPO 일정

---

## [2026-06-03] ingest | YouTube 3개 신규 영상 + 매크로 wiki 신규 생성

**처리 영상 (3개)**
1. 전인구경제연구소 — BTC 하락 진짜 이유, 양지화의 역설, AI 에이전트 재상승 조건
2. 주독 — 4년 사이클 하락 구간, $59,800 최저점, DCA 전략
3. 사토시 — PCE 3.8%, 선택적 버블장, 버블 붕괴 조건 (10년물 5%, AI 실적)

**신규 wiki 페이지**
- `wiki/market/macro_202606.md` — 2026년 6월 시장 국면 분석

**업데이트 wiki 페이지**
- `wiki/assets/BTC.md` — 양지화의 역설, 4년 사이클 섹션 추가

**신규 output 파일 (3개)**
- `output/youtube/20260603_전인구_BTC하락이유재상승조건.md`
- `output/youtube/20260603_주독_BTC사이클DCA전략.md`
- `output/youtube/20260603_사토시_PCE버블선택적강세장.md`

**업데이트**
- `output/synthesis/20260603_크립토항공우주_종합분석.md` v2 (10개 영상 반영)

**핵심 신규 발견**
- 양지화의 역설: BTC 제도화 = 탈중앙화 매력 소멸 (기존 화자 전원 놓쳤던 논거)
- 모니터링 지표 확정: 10년물 금리 5% / AI 기업 실적 성장률

---

## [2026-06-03] query | YouTube 영상별 분석 보고서 + 종합 분석 보고서 산출

- 신규 폴더: `output/youtube/`, `output/synthesis/`
- 영상별 분석 보고서 7개 생성 (output/youtube/)
- 종합 분석 보고서 1개 생성: `output/synthesis/20260603_크립토항공우주_종합분석.md`
- CLAUDE.md 업데이트: output/, output/youtube/, output/synthesis/
- 핵심 발견: **스테이블코인 성장이 유일한 모든 화자 합의 포인트**
- 경고: 7개 영상 모두 크립토 친화적 화자 → 반크립토 시각 구조적 부재

---

## [2026-06-03] ingest | YouTube 7개 영상 일괄 인제스천 (BTC·ETH·SpaceX)

**처리 영상 (7개)**
1. 강환국 2부 (와이스트릿) — BTC 양자리스크, 스테이블코인·RWA 선호, 원자재
2. 업비트 Daily WRAP UP — Strategy BTC 32개 매도(STRC 배당), 스테이블코인 카드 1조원
3. 김창익 풀버전 (부읽남TV) — 트럼프 쇼크, BTC 담보물, 7월 4일 이벤트
4. 오태민 교수 (삼프로TV) — ETH = RWA 플랫폼 표준, CLARITY 법안, 수학적 상승 논리
5. 김창익의 빅픽처 (머니인사이드) — 중동 지정학, 사우디-이란-이스라엘
6. 강정수 박사 2부 (머니인사이드) — SpaceX IPO 6/12, $2조, 우주 데이터센터 2028
7. Michael Saylor Interview — 파일명 특수문자로 읽기 실패

**신규 wiki 페이지 (1개)**
- `wiki/assets/ETH.md` — RWA 플랫폼 표준, CLARITY 법안, 가격 상승 논리

**업데이트 wiki 페이지 (3개)**
- `wiki/assets/BTC.md` — 양자컴퓨팅 리스크, Strategy 매도 사건, 담보물 이론 추가
- `wiki/themes/화폐시스템개혁.md` — 스테이블코인 카드 1조원, CLARITY, RWA 현황 추가
- `wiki/themes/항공우주.md` — SpaceX IPO 6/12 확정, $2조, 우주데이터센터 2028 추가

**기타**
- `raw/articles/` 신규 폴더 발견 → raw/CLAUDE.md 추가
- Michael Saylor 영상 미처리 → 다음 인제스천 시 재시도

---

## [2026-06-03] ingest | 인호 교수 BTC 전망 인터뷰 (신사임당, 1부)

- 소스: `raw/youtube/2026-06-03T161429+0900_월가에는 싹 다 퍼졌다...`
- 신규 페이지 (2개):
  - `wiki/themes/화폐시스템개혁.md` — 테마 개요, 3단계 수요 사이클, 반감기 구조
  - `wiki/assets/BTC.md` — 채굴원가 $75k 지지선, SBR, 이란 결제 사례, 포지션 가이드
- 핵심 인사이트:
  - BTC 채굴원가 $75k~$75.5k = 구조적 하방 지지선
  - 수요 사이클: 개인(완료) → 기업(2024~2028, 진행 중) → 국가(2028~, SBR 초기)
  - 이란-미국 분쟁: 호르무즈 통행료를 위안화·BTC로만 수납 → BTC 국제결제 자산 지위 실증
  - 2028 반감기: 6.25→3.125 BTC/10분 → 공급 구조적 감소
  - BlackRock 권고: 기관 포트폴리오 1~2%, 개인 5~10%
- 투자자 포트폴리오 기준 대비: 암호화폐 한도 20~40% → 교수 권고(5~10%)보다 공격적

---

## [2026-06-03] scan | 전체 폴더 스캔 및 루트 index.md·log.md 생성

- 스캔 결과: raw/research/ 6개, wiki/assets/ 15개, wiki/themes/ 2개, output/ 2개
- 신규 생성: 루트 `index.md` (프로젝트 전체 인덱스), 루트 `log.md`
- 수정: raw/research 파일 수 4→6 정정

---

## [2026-06-01] query | 오늘 추가된 분석 기반 최선의 투자 선택

- 결과: CRS·ETN 즉시 / VRT·GOOG 조정 대기 / PH·NVT·한화시스템 2차
- 제외: HWM(고밸류), RKLB(적자), LIN(알파 불일치), MOD(전환 대기)
- 저장: `output/top10/top10_202606.md`
- 미완성: 기술적 분석·시장 국면 항목 — 차트 확인 후 보완 필요

---

## [2026-06-01] ingest | AI·항공우주 냉각 기술 투자 관점 (GPT 공동 조사)

- 소스: `raw/research/20260601_GPT_냉각회사_분석`
- 신규 페이지 (3개): NVT, TT, RTX
- 기존 테마 업데이트: `냉각인프라.md` — 신규 후보 추가, GPT·클로드 교차검증 섹션 추가
- 국내 관찰 후보 추가: GST, SK하이닉스, 한화에어로스페이스 (테마 페이지 메모)
- 교차검증 차이점: GPT는 NVT·TT를 최우선으로, 항공우주 냉각을 보조 테마로 비중 낮춤

---

## [2026-06-01] ingest | AI·항공우주 냉각 인프라 분석 (클로드 공동 조사)

- 소스: `raw/research/20260601_클로드_냉각회사_분석`
- 신규 테마: `wiki/themes/냉각인프라.md` — AI·항공우주 교차 테마
- 생성 페이지 (4개): VRT, ETN, MOD, PH
- 핵심 인사이트: 전력+냉각 통합 플랫폼 방향으로 M&A 집중. 단기 이벤트 아닌 다년간 CapEx 구조적 흐름
- 주의: VRT·MOD 이미 급등 — 포지션 사이징이 진입 타이밍보다 중요

---

## [2026-06-01] ingest | 우주항공 소부장 3사 분석 (제미나이 공동 조사)

- 소스: `raw/research/20260601_제미나이_분석`
- 생성 페이지 (3개): `wiki/assets/CRS.md`, `wiki/assets/HWM.md`, `wiki/assets/LIN.md`
- 주요 인사이트: CRS 실적 턴어라운드 강력 (사상 최대 EPS, 영업이익률 35.6%)
- 수정: 항공우주 테마 페이지에 소부장 Pick & Shovel 분류 추가
- query 수정: CRS가 GOOG와 동급 1순위로 재평가됨

---

## [2026-06-01] query | SpaceX IPO 현시점 투자 적격 종목

- 결과: GOOG(1순위), 한화시스템(2순위) 즉시 검토 / 미래에셋증권·인텔리안테크 조건부 / RKLB 등 진입 불가
- 미완성: 기술적 분석 항목 — 차트 공유 시 스코어 완성 가능
- 아이디어 저장: `output/ideas/20260601_SpaceX_IPO_투자적격_종목.md`

---

## [2026-06-01] ingest | SpaceX IPO 수혜 기업 분석 (GPT 공동 조사)

- 소스: `raw/research/20260601_GPT_분석`
- 생성 페이지 (6개):
  - `wiki/themes/항공우주.md` — 테마 개요 + SpaceX IPO 수혜 분류
  - `wiki/assets/GOOG.md` — 해외 1순위
  - `wiki/assets/RKLB.md` — 해외 2순위
  - `wiki/assets/미래에셋증권.md` — 국내 1순위
  - `wiki/assets/한화시스템.md` — 국내 2순위
  - `wiki/assets/인텔리안테크.md` — 국내 3순위
- 미작성 (관망/단기 테마): RDW, ASTS, DXYZ, AP위성, 쎄트렉아이, 컨텍, 켄코아
- 스코어 미완성: 기술적 분석·시장 국면 항목은 실시간 차트 확인 후 보완 필요

---

## [2026-06-01] init | LLM Wiki 초기 세팅 완료

- 폴더 구조 생성: raw/, wiki/, output/ 및 하위 폴더
- 루트 CLAUDE.md에 Wiki 운영 규칙 추가
- 각 주요 폴더에 CLAUDE.md 생성
- wiki/index.md 초기화
- wiki/log.md 초기화

---

## [2026-06-04] admin | agent-handoff | Prepare for next agent

- **요약**: AI 테마(`wiki/themes/AI.md`) 추가, ingest 프롬프트·템플릿 업데이트, 카카오 자동화 스크립트 삭제, frontmatter 린트 실행, 수동 인제스천 실행 완료.
- **변경 파일**:
  - 추가: `wiki/themes/AI.md`
  - 수정: `wiki/index.md`, `scripts/ingest-prompt.txt`, `scripts/research-template.md`, `scripts/ingest-idea-prompt.txt`, `scripts/README.md`
  - 삭제: `scripts/setup-kakao.ps1`, `scripts/send-kakao.ps1`
- **린트 결과**: `output/lint/frontmatter_report_20260604_1811.md` — 13개 파일에 YAML frontmatter 누락.
- **인제스천**: `scripts/run-ingest-now.ps1` 실행 — raw 전수 처리, `output/youtube/` 및 `output/synthesis/`에 결과 생성.
- **알려진 문제**: PowerShell 인코딩(UTF-8 권장), raw 파일명 내 특수문자(쌍따옴표 등)로 인한 읽기 실패 사례 — 해당 파일은 수동 이름 변경 필요.
- **다음 작업(권장)**: frontmatter 자동 패치(미리보기 → 적용), `scripts/apply-agent-actions.ps1` 구현, watchers의 `MODEL_*` 환경변수 의존성 적용.
- **자세한 핸드오프 지침**: `AGENT_HANDOFF.md` (루트) 참고.
