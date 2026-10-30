# [Frontend PRD] Architecture & Client-Side Specifications

## 1. 기술 스택 (Tech Stack)
- **Framework / Core**: HTML5, CSS3, Vanilla JavaScript (복잡한 프레임워크 배제, 빠른 렌더링 우선)
- **Styling**: Tailwind CSS (빠른 스타일링 및 반응형 구현)
- **Animation**: CSS Transitions/Animations, Vanilla JS 기반 Intersection Observer (스크롤 모션)
- **Design/Asset**: Figma (디자인 토큰, 에셋 추출), Phosphor Icons 또는 Lucide (경량 아이콘)
- **Hosting**: Vercel 또는 GitHub Pages (무료, 빠른 배포)

## 2. 화면 단위 구조 및 컴포넌트 계층도
```text
/ (Index.html - 원페이지 구성)
 ├── Header (Sticky Nav - Logo, [Services, Portfolio, Process, Contact])
 ├── HeroSection 
 │    ├── Headline & Subheadline
 │    └── CTA Buttons (Primary: 문의하기, Secondary: 포트폴리오 보기)
 ├── ServicesSection
 │    └── ServiceCards (반응형, 인터랙션, 초고속 배포) - 3 Column Grid
 ├── PortfolioSection (Showcase)
 │    └── ProjectCards
 │         ├── Thumbnail Image (Figma Mockup)
 │         ├── Project Title & Tags (e.g., #Landing #Responsive)
 │         └── Action Links (Live Demo, Details)
 ├── ProcessSection
 │    └── Step-by-step Timeline View
 └── Footer (Contact & CTA)
      ├── Final CTA Message
      ├── Open Kakao / Email Link
      └── Social Links (Optional)
```

## 3. UI 인터랙션 세부 규격
- **스크롤 애니메이션**: `IntersectionObserver`를 활용하여 각 섹션(Services, Portfolio 등)이 뷰포트에 진입할 때 `transform: translateY(20px)`에서 `translateY(0)` 및 `opacity: 0` -> `1`로 부드럽게 전환 (`transition: all 0.6s ease-out`).
- **3D Button Interaction (Duo Style)**:
  - `box-shadow`: 하단 솔리드 보더 효과 (`border-b-4`)
  - `:active`: `transform: translateY(2px)`, 물리적 눌림감 구현
- **반응형 분기점 (Tailwind 기준)**:
  - `sm`: 640px (모바일 가로/태블릿 세로)
  - `md`: 768px (태블릿 가로)
  - `lg`: 1024px (데스크톱)