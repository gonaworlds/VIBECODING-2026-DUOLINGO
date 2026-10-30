# [Execution Brief] Vibe Coding Sprint Guide

## 1. 구현 범위 (MVP Phase 1)
- **스코프**: 원페이지 포트폴리오 사이트 (Index.html) 완벽 구현
  - Hero, Services, Portfolio, Process, Contact 5개 핵심 섹션
  - Tailwind CSS를 활용한 모바일 최적화 반응형 디자인 적용
  - Vanilla JS를 활용한 스크롤 애니메이션 (Intersection Observer) 적용
  - 하드코딩된 포트폴리오 더미 데이터(향후 작업물로 교체) 배치

## 2. 데이터 구조 (더미 데이터용 JSON 구조 예시)
```json
[
  {
    "id": 1,
    "title": "피트니스 무료 체험 신청 랜딩페이지",
    "category": "Landing Page",
    "image": "assets/img/mockup-fitness.webp",
    "liveLink": "https://demo-fitness.vercel.app",
    "tags": ["Mobile-First", "Form Validation"]
  },
  {
    "id": 2,
    "title": "프리랜서 실수령액 계산기",
    "category": "Interactive Web Tool",
    "image": "assets/img/mockup-calc.webp",
    "liveLink": "https://demo-calc.vercel.app",
    "tags": ["Vanilla JS", "DOM Manipulation"]
  }
]
```

## 3. 개발 체크리스트
- [ ] Figma 와이어프레임 기반으로 기초 HTML 뼈대 작성 (시맨틱 태그 준수)
- [ ] Tailwind CSS CDN 또는 빌드 환경 설정
- [ ] 2D 플랫 벡터 스타일(두꺼운 아웃라인, 고대비) 기준 테마(Color, Typography) 설정
- [ ] 3D 눌림 버튼 UI 컴포넌트(CSS 클래스) 제작
- [ ] 모바일(기본) -> 태블릿(md) -> 데스크톱(lg) 순으로 반응형 레이아웃 적용
- [ ] Vanilla JS `IntersectionObserver` 스크립트 작성 및 적용
- [ ] Vercel/GitHub Pages 배포 테스트