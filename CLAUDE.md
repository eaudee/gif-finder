# GIF Finder - Claude Instructions

## 프로젝트 구조
- 단일 파일: `index.html` (HTML + CSS + JS 전부 포함)
- 빌드 도구 없음, 프레임워크 없음
- 미리보기는 `/tmp/gif-finder/index.html`에 복사 후 Ruby WEBrick 서버 사용

## 미리보기 서버
```bash
# index.html 수정 후 반드시 복사
cp index.html /tmp/gif-finder/index.html
```
- launch.json 서버명: `gif-finder` (포트 3000)
- 한글 경로 문제로 `/tmp/gif-finder/`를 serving directory로 사용

## API
- **Tenor API v1** (`https://api.tenor.com/v1`)
- 공개 dev key: `LIVDSRZULELA`
- 페이지네이션: cursor 기반 (`next` 필드 → `nextCursor` 변수)
- 엔드포인트: `/trending`, `/search`, `/random`

## 배포
- GitHub Pages: https://eaudee.github.io/gif-finder/
- 저장소: https://github.com/eaudee/gif-finder
- 브랜치: `main`
- 코드 수정 → commit → push하면 자동 배포

## 주요 JS 함수
| 함수 | 역할 |
|------|------|
| `load()` | 트렌딩/검색 결과 로드 |
| `doSearch()` | 검색창 검색 실행 |
| `selectTab()` | 카테고리 탭 전환 |
| `openModal(gif)` | GIF 상세 팝업 열기 |
| `findSimilar()` | 비슷한 GIF 4개 자동 로드 |
| `getRandomGif()` | 룰렛 오버레이 열기 |
| `spinRoulette()` | 룰렛 스핀 시작 |
| `launchConfetti()` | 컨페티 폭죽 효과 |
| `toggleFav()` | 즐겨찾기 추가/제거 |

## 코드 수정 시 주의사항
- `gifObjFromData(d)` — Tenor 응답에서 GIF 객체 생성, 포맷 변경 시 여기부터 확인
- 즐겨찾기는 `localStorage('gif_favs')`에 저장
- 룰렛 세그먼트는 `SEGMENTS` 배열로 관리
