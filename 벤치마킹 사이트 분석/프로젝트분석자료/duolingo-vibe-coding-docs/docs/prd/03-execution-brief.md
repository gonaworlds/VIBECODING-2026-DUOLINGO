# [Execution Brief] Vibe Coding Sprint Guide

## 1. 구현 범위 (MVP Phase 1)
- **스코프**: 
  1. `/learn` 메인 로드맵 뷰 (상단 상태바 + 3~5개 더미 노드)
  2. `/lesson` 퀴즈 세션 (Word Bank 1종 + Multi-Choice 1종 구현)
  3. 사운드 피드백 및 하트 차감 로직
  4. 로컬 스토리지 기반 상태 저장 (Hearts, Streak, Completed Nodes)

## 2. 데이터 스키마 (TypeScript Types)
```typescript
export type QuestionType = 'WORD_BANK' | 'MULTIPLE_CHOICE' | 'MATCHING';

export interface Question {
  id: string;
  type: QuestionType;
  prompt: string;
  characterExpression?: 'neutral' | 'happy' | 'thinking' | 'crying';
  options: { id: string; text: string; audioSrc?: string }[];
  correctAnswer: string[] | string;
}

export interface LessonSessionState {
  currentQuestionIndex: number;
  totalQuestions: number;
  hearts: number;
  streak: number;
  isCompleted: boolean;
  userAnswers: Record<string, any>;
}
```

## 3. 개발 체크리스트
- [ ] Tailwind 테마에 Duo 컬러 팔레트 구성 (Feather Green, Macaw Blue, Fox Red 등)
- [ ] 3D 누름 버튼 컴포넌트(`Button3D`) 베이스 제작
- [ ] Zustand 기반 `useLessonStore` 인터페이스 및 액션 구현
- [ ] 단어 조립(Word Bank) 양방향 탭 인터랙션 작성
- [ ] 성공/실패 인터랙티브 바텀 피드백 시트 완성