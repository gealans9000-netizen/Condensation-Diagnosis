# 게알란코리아 창호 결로 진단 프로그램

실내외 온도·습도와 창호 성능으로 창의 결로·곰팡이·결빙 가능성을 진단하는 웹 계산기입니다.
testo 605i(testo Smart 앱) 측정 데이터(CSV)를 불러와 분석할 수 있습니다.

빌드 과정이 없는 정적 사이트입니다. Vercel에서 Framework Preset은 **Other**, Build Command는 비워 두면 됩니다.

## 파일
- `index.html` — 프로그램 전체 (HTML·CSS·JS 한 파일)
- `favicon.png`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `manifest.webmanifest` — 게알란코리아 로고 아이콘, 휴대폰 홈 화면 추가용
- `lib/html2canvas.min.js`, `lib/jspdf.umd.min.js` — 진단결과서를 PDF·그림 파일로 만드는 도구 (MIT 라이선스)
- `vercel.json` — Vercel 설정

## 계산 근거
DIN 4108-3 / EN ISO 13788 포화수증기압·노점식, fRsi = 1 − Rsi·U, 곰팡이 판정 표면습도 80%,
Hukka·Viitanen(1999) VTT 곰팡이 모델, 「공동주택 결로 방지를 위한 설계기준」 TDR 참고값.
