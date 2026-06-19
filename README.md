# 💷 지출 트래커 (Spending Tracker)

Monzo(및 기타 은행)의 CSV 거래내역을 드래그&드롭하면 자동으로 분석해주는 1파일 웹앱입니다.
서버가 필요 없고, **모든 데이터는 본인 브라우저(localStorage)에만 저장**됩니다.

## 기능
- 📥 Monzo CSV 드래그&드롭 (여러 달 파일 누적, 중복 자동 제거)
- 📊 이번 달 vs 지난 달 총지출 비교
- 🎯 월 전체 / 카테고리별 예산 목표 대비 진행률
- 🥧 카테고리별 지출 분석 (도넛 차트)
- 📈 월별 지출 추세 (최근 12개월)
- 🔎 거래 검색 · 통화 선택(£/₩/$/€)
- 💾 백업(JSON) 내보내기 / 복원

## Monzo에서 CSV 빼는 법
1. Monzo 앱에서 거래 피드 옆 **Manage** 탭
2. **Bank statements** 선택
3. 날짜 범위 선택 → 포맷을 **CSV**로 선택해 내보내기
> Monzo Plus 이용자는 매월 1일 Google Drive/OneDrive로 자동 내보내기도 가능합니다.

다른 은행 CSV도 `Date`, `Amount`(또는 `Money Out`/`Money In`), `Category`, `Name`/`Description` 컬럼이 있으면 인식됩니다.

## 실행
`index.html`을 브라우저로 열기만 하면 됩니다. (인터넷은 차트 라이브러리 로딩에만 필요)

## GitHub Pages로 배포하기
아래 명령어를 폴더에서 실행하세요 (`<USERNAME>`을 본인 깃헙 아이디로 교체):

```bash
git init
git add index.html README.md
git commit -m "지출 트래커 웹앱"
git branch -M main
git remote add origin https://github.com/<USERNAME>/spending-tracker.git
git push -u origin main
```

그런 다음 GitHub 저장소 → **Settings → Pages → Source: main / root** 로 설정하면
`https://<USERNAME>.github.io/spending-tracker/` 에서 접속됩니다.

## 개인정보
거래 데이터는 외부로 전송되지 않습니다. 전부 브라우저 안에서만 처리·저장됩니다.
