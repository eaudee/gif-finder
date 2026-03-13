# GIF Finder 🎭

다양한 상황에 맞는 GIF를 쉽고 빠르게 찾을 수 있는 웹 앱입니다.

🔗 **라이브**: [eaudee.github.io/gif-finder](https://eaudee.github.io/gif-finder/)

---

## 주요 기능

### 검색
- 키워드로 GIF 검색
- 13개 카테고리 탭 (트렌딩, 웃김, 놀람, 슬픔, 기쁨, 화남, 피곤, 생각중, 파이팅, 칭찬, 짜증, 사랑, 댄스)
- 무한 스크롤 (더 보기)

### 랜덤 뽑기
- 룰렛 스핀 애니메이션으로 감정 카테고리 선택
- 결과 확정 시 2D 컨페티 폭죽 효과
- 뽑힌 카테고리의 랜덤 GIF 자동 표시

### GIF 팝업
- 클릭 시 상세 팝업
- URL 복사 / 다운로드 / 즐겨찾기 버튼
- **비슷한 GIF 4개** 자동 추천 (팝업 하단)

### 즐겨찾기
- localStorage에 저장 (새로고침 후에도 유지)
- 우측 슬라이드 패널에서 관리

---

## 기술 스택

| 항목 | 내용 |
|------|------|
| 구성 | 단일 HTML 파일 (빌드 도구 없음) |
| API | [Tenor API v1](https://tenor.com/gifapi) |
| 스타일 | CSS 변수 기반 다크 모드 |
| 애니메이션 | Canvas 2D (룰렛, 컨페티) |
| 배포 | GitHub Pages |

---

## 로컬 실행

```bash
python3 -m http.server 3000
```

브라우저에서 `http://localhost:3000` 접속
