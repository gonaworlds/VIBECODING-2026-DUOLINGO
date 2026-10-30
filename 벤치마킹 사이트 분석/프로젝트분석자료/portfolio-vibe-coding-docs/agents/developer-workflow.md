# [Developer Agent Workflow & Instruction Manual]

## 1. 개요
본 문서는 개발자 AI 에이전트가 코드를 생성하고 리팩토링할 때 준수해야 하는 작업 프로토콜과 프롬프트 템플릿 표준입니다. Cursor 환경에서 활용 시 최적화되어 있습니다.

## 2. 작업 단계별 실행 지침
### Step 1: 뼈대 구성 (HTML & Tailwind Setup)
- 시맨틱 마크업을 기반으로 원페이지 HTML 뼈대 작성.
- Tailwind CSS 환경 설정 및 디자인 에이전트가 제시한 폰트(Pretendard), 커스텀 컬러 테마 등록.

### Step 2: 공통 UI 요소 구현
- `Button`: 입체적인 3D 눌림 효과가 적용된 버튼 CSS 유틸리티 또는 클래스 조합 완성.
- `Section Container`: 좌우 패딩이 일관되게 적용된 반응형 컨테이너 레이아웃 구성 (`max-w-7xl mx-auto px-4 sm:px-6 lg:px-8`).

### Step 3: 섹션별 마크업 및 스타일링
- Hero -> Services -> Portfolio -> Process -> Contact 순서로 Tailwind 클래스를 적용하며 레이아웃 완성.

### Step 4: 인터랙션 적용 (Vanilla JS)
- `script.js` 분리 작성 (또는 `<script>` 하단 추가).
- `IntersectionObserver`를 세팅하여 특정 클래스(예: `.animate-on-scroll`)를 가진 요소가 화면에 나타날 때 애니메이션 클래스를 추가(Add)하는 로직 구현.

## 3. Vibe Coding 프롬프트 템플릿
에이전트에게 기능을 요청할 때는 아래 구조로 컨텍스트를 주입합니다:
```text
[Goal]: 구현하려는 기능 또는 수정사항 (예: Services 섹션 3열 그리드 적용)
[Context]: 참조할 파일 경로 (index.html의 #services 영역)
[Constraints]: 모바일 퍼스트 준수, 2D 플랫 디자인 토큰 적용
[Deliverable]: 수정/추가될 해당 영역의 전체 HTML/CSS/JS 코드
```