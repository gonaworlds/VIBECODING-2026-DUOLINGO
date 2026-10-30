# Vibe Coding Portfolio Starter

이 패키지는 "AI 마이크로 툴 & 템플릿 빌더" 컨셉의 프리랜서 포트폴리오 사이트를 빠르게 구축(바이브코딩)하기 위한 표준 가이드 마크다운(MD) 문서 및 커서 규칙 파일 모음입니다.

## 프로젝트 개요
- **목적**: 사업자 없이 단기 외주 및 자동화 수익을 창출하기 위한 "나만의 무기(포트폴리오)" 구축
- **기술 스택**: Figma, Cursor AI, Vanilla JS, HTML/CSS (Tailwind)

## 디렉터리 구조
```text
├── README.md
├── .cursorrules                 # AI 에디터(Cursor) 전용 글로벌 규칙 파일
├── docs/
│   └── prd/
│       ├── 01-full-prd.md           # 1. 전체 기획서 (핵심 여정 및 컨셉)
│       ├── 02-frontend-prd.md       # 2. 프론트엔드 전용 상세 PRD
│       └── 03-execution-brief.md    # 3. 개발 실행용 요약 브리프
└── agents/
    ├── designer-agent.md            # 4. 디자이너 AI 에이전트 지침 (2D 플랫 벡터 고정)
    ├── developer-agent.md           # 5. 개발자 AI 에이전트 지침 (Vanilla JS + Tailwind 기본)
    └── developer-workflow.md        # 6. 개발자 에이전트 작업 프로세스 및 프롬프트
```