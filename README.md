# AI Trend Reports

매일 오전 9시(KST) 자동으로 생성되는 AI 트렌드 보고서 아카이브.

**Live site:** https://hong9595.github.io/ai-trend-reports/

## 구조

- `index.html` — 가장 최근 보고서 (Pages 진입점)
- `archive/YYYY-MM-DD.html` — 일자별 아카이브
- `latest-summary.txt` — 텔레그램 알림용 요약
- `.github/workflows/notify.yml` — 푸시 시 텔레그램 전송

## 자동화

Anthropic Cowork의 예약 작업이 매일 아침 리서치 후 이 리포에 푸시합니다.
푸시가 감지되면 GitHub Actions가 텔레그램으로 알림을 발송합니다.

## 설정

Actions secrets에 다음 두 개가 등록되어 있어야 합니다:

- `TELEGRAM_BOT_TOKEN`
- `TELEGRAM_CHAT_ID`
