# 잘살아보세 MVP 개발 업데이트

**작성일:** 2024년 12월 27일  
**GitHub:** https://github.com/jacopast/jalsal-mvp  
**라이브 사이트:** https://jacopast.github.io/jalsal-mvp/

---

## 📋 완료된 작업

### 1. ✅ Phase 1 워크시트 (4장)
영어 5학년 수준의 읽기 워크시트를 HTML로 제작 (인쇄 가능)

| 워크시트 | 학습 스킬 | 읽기 지문 |
|----------|-----------|-----------|
| B-M-E | 이야기 구조 (시작-중간-끝) | The Lost Library Book |
| SWBST | 요약 (누가-원했다-하지만-그래서-그 다음) | The Science Fair Surprise |
| Main Idea | 중심 생각 찾기 | The Amazing Honeybee |
| Character | 인물 분석 | The New Kid |

**파일 위치:** `worksheets/phase1/`

---

### 2. ✅ 랜딩페이지 + GitHub Pages 배포
- 한글 랜딩페이지 제작 (모던 다크 테마)
- 기능 소개, 사용법, 12주 커리큘럼, 이메일 구독 CTA
- **라이브 URL:** https://jacopast.github.io/jalsal-mvp/

---

### 3. ✅ 앱 UI 목업 (인터랙티브)
클릭 가능한 4화면 목업 제작:
- 홈: 아이 진도, 최근 활동
- 스캔: 카메라 UI
- AI 피드백: 점수 + 잘한 점/개선할 점
- 프로필: 스킬별 진도바, 통계

**파일:** `mockup/app-mockup.html`

---

### 4. ✅ 작동하는 웹앱 프로토타입
실제로 동작하는 웹앱 구현:

| 기능 | 설명 |
|------|------|
| 📷 사진 업로드 | 드래그&드롭, 카메라 촬영 지원 |
| 🤖 AI 자동 인식 | 워크시트 유형 자동 감지 (선택 불필요) |
| 📊 피드백 생성 | 점수 + 잘한 점 + 개선할 점 |
| 💾 프로필 저장 | localStorage 기반 (브라우저 저장) |
| 📈 스킬 진도 | 스킬별 점수 자동 계산 + 시각화 |

**파일:** `app/index.html`

---

## 🔄 UX 개선 사항

### 워크시트 자동 인식으로 변경
**Before (기존):**
```
워크시트 유형 선택 → 사진 업로드 → AI 분석
```

**After (개선):**
```
사진 업로드 → AI가 자동으로 워크시트 유형 감지 + 분석
```

- 사용자 단계 감소
- 더 직관적인 UX

---

## 📁 최종 파일 구조

```
jalsal-mvp/
├── index.html              ← 랜딩페이지 (GitHub Pages)
├── app/
│   └── index.html          ← 작동하는 웹앱 프로토타입
├── mockup/
│   └── app-mockup.html     ← 인터랙티브 목업
├── worksheets/
│   └── phase1/
│       ├── 01_bme_structure.html
│       ├── 02_swbst_summary.html
│       ├── 03_main_idea.html
│       └── 04_character_analysis.html
└── guides/
    └── parent_guide.md     ← 부모용 AI 프롬프트 가이드
```

---

## 🚀 다음 단계 (우선순위)

1. **실제 AI API 연동**
   - OpenAI GPT-4 Vision API 연결
   - 실제 손글씨 분석 + 피드백 생성

2. **백엔드 서버 구축**
   - Firebase 또는 Supabase
   - 학습 프로필 영구 저장
   - 사용자 인증

3. **Phase 2-4 워크시트 제작**
   - Theme & Text Evidence
   - Literary Analysis
   - Non-Fiction & Argument

---

## 🔗 바로가기

- **GitHub Repo:** https://github.com/jacopast/jalsal-mvp
- **라이브 랜딩페이지:** https://jacopast.github.io/jalsal-mvp/
- **웹앱 프로토타입:** (로컬에서 `app/index.html` 실행)
- **이전 PRD 문서:** https://docs.google.com/document/d/1Pq_gTnlPbiFCc6ndOkx2qY8hWidUsqQOI8JgxQSsLt0/edit

---

## 💬 피드백 요청

1. 워크시트 디자인/내용 괜찮은지?
2. 앱 UX 플로우 개선할 점?
3. AI 피드백 내용 (잘한 점/개선할 점) 톤이 적절한지?
4. 우선순위 조정 필요한 부분?
