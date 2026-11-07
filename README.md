# 북빌리지 스쿨 (BookVillage School)

고전·인문학 독서 활동을 게이미피케이션과 3D 메타버스 학교에 결합한 웹게임 프로토타입.
Three.js(CDN) 단일 파일(`index.html`) 구조 — 빌드 과정 없음.

## 실행
```bash
node serve.js   # http://localhost:8765
```
(ES module 사용으로 `file://` 직접 열기는 불가, 정적 서버 필요. 인터넷 필요: Three.js·폰트 CDN)

## 구조 (index.html 내부)
- 데이터: `BOOKS`(책·스토리 장면), `SHOP`, `TIERS`, `HASHTAGS`
- 3D 아바타: `buildAvatar` (six-sense `avatar.ts` 옵션 재사용)
- 씬: `SCENES.campus / library / classroom / art / music / creator`
- 활동: `coopGame`(15소년 표류기 협동), `playStory`, `writeReview`
- AI 표지: `drawCover` — 현재는 키워드 기반 캔버스 생성(대역). 실제 AI API로 교체 예정
- 저장: localStorage (`bookvillage-save-v1`)

## 알려진 한계 / TODO
- 친구 NPC·리그 순위·문집 타인 글은 데모용 가상 데이터 → 서버(Supabase 등) 연동 필요
- 협동 게임·피아노 실사용 테스트 필요
- 배포: 비즈코더(onpod) 예정
- 디자인 참고: 젤다 스카이워드 소드 스카이로프(Knight's Academy)
