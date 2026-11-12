# 나를 말하는 한 점 찾기 · ARTOTEM

아르템(ARTOTEM)의 무료 취향 진단 콘텐츠. 8개의 질문에 답하면 6가지 예술 취향 유형 중 하나와 "곁에 두면 좋을 첫 한 점"을 추천한다. 수익 구조 제안의 **제안 1 · 나의 한 점 진단형 리드마그넷**이다.

## 유형 6가지

| 키 | 유형 | 한 줄 |
| --- | --- | --- |
| quiet | 고요한 여백가 | 비워 둔 자리에서 숨을 고르는 사람 |
| light | 빛을 모으는 사람 | 따뜻한 불빛 하나로 공간을 바꾸는 사람 |
| story | 이야기 수집가 | 작품보다 그 뒤의 이야기에 먼저 반하는 사람 |
| color | 컬러 플레이어 | 한 점의 색으로 기분을 바꾸는 사람 |
| nature | 자연 산책자 | 집 안에 계절 하나를 들여놓는 사람 |
| wit | 위트 큐레이터 | 벽에도 유머 한 줄이 필요한 사람 |

## 기능

- 질문 8개, 답마다 유형 점수 가중치를 매기고 동점이면 story → light → color → nature → quiet → wit 순서로 정함
- 결과 화면: 유형 설명, 추천 첫 한 점 3가지, 어울리는 공간, 궁합 유형, 취향 분포 막대
- **결과 이미지 저장**: 1080×1350(인스타 4:5) PNG
- **공유**: 모바일은 공유 시트, PC는 링크 복사. `index.html#color`처럼 유형 키를 붙인 링크는 결과 화면이 바로 열림
- **쇼핑 링크**: `utm_source=hanjeom_test&utm_medium=leadmagnet&utm_campaign=my_one_piece&utm_content={유형}`로 어느 유형에서 유입됐는지 확인 가능

## 수정하는 곳

모든 내용은 `index.html` 하나에 있다.

- `SHOP`: 이동할 주소. 유형별 기획전이 생기면 `renderResult()`의 `$('go').href`를 유형별 주소로 바꾼다
- `TYPES`: 유형 이름·설명·추천 작품·공간
- `Q`: 질문과 보기, 점수 가중치

## 배포 (GitHub Pages)

Settings → Pages → Source: **Deploy from a branch**, Branch: `main` / `(root)` → Save.
1~2분 뒤 `https://ellekim1004.github.io/artotem/`에서 열린다.

---
제작: 파키라랩
