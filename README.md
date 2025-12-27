# 잘살아보세 🌱

> **AI와 함께하는 5학년 영어 읽기·쓰기 튜터링**

[🌐 라이브 사이트](https://jacopast.github.io/jalsal-mvp/) · [📱 웹앱 데모](app/index.html) · [📄 PRD 문서](https://docs.google.com/document/d/1Pq_gTnlPbiFCc6ndOkx2qY8hWidUsqQOI8JgxQSsLt0/edit)

---

## 🎯 프로젝트 개요

NJ 북부 한인 학부모를 위한 **AI 기반 영어 읽기·쓰기 학습 시스템**

```
📸 사진 업로드 → 🤖 AI 자동 분석 → 💾 학습 프로필 저장 → 📝 맞춤 피드백
```

### 핵심 특징
- 📄 **출력형 워크시트** - 손글씨 학습 유지
- 🤖 **AI 자동 인식** - 워크시트 유형 자동 감지
- 📊 **학습 프로필** - 스킬별 진도 추적
- 🇰🇷 **한글 피드백** - 부모님께 한글로 전달

---

## ✅ 완료된 작업

### 1. Phase 1 워크시트 (4장)

| 워크시트 | 학습 스킬 | 읽기 지문 |
|:--------:|:---------:|:---------:|
| 📖 B-M-E | 이야기 구조 | The Lost Library Book |
| 📝 SWBST | 요약하기 | The Science Fair Surprise |
| 🔍 Main Idea | 중심 생각 | The Amazing Honeybee |
| 👤 Character | 인물 분석 | The New Kid |

### 2. 웹앱 프로토타입

| 기능 | 상태 |
|------|:----:|
| 사진 업로드 (드래그&드롭) | ✅ |
| AI 워크시트 자동 인식 | ✅ |
| 피드백 생성 (점수 + 코멘트) | ✅ |
| 학습 프로필 저장 | ✅ |
| 스킬별 진도 시각화 | ✅ |

### 3. 기타
- ✅ 랜딩페이지 + GitHub Pages 배포
- ✅ 인터랙티브 앱 UI 목업
- ✅ 부모용 AI 프롬프트 가이드

---

## 📁 파일 구조

```
jalsal-mvp/
├── index.html              ← 랜딩페이지 (GitHub Pages)
├── app/
│   └── index.html          ← 🚀 웹앱 프로토타입
├── mockup/
│   └── app-mockup.html     ← 📱 인터랙티브 목업
├── worksheets/phase1/      ← 📄 워크시트 4장
│   ├── 01_bme_structure.html
│   ├── 02_swbst_summary.html
│   ├── 03_main_idea.html
│   └── 04_character_analysis.html
└── guides/
    └── parent_guide.md     ← 📘 부모용 가이드
```

---

## 🚀 다음 단계 (상세)

### 1️⃣ 실제 AI API 연동 (우선순위 높음)

현재 AI 분석은 **시뮬레이션**입니다. 실제 동작하려면:

```javascript
// app/index.html의 analyzeWorksheet() 함수에서
// 현재: 랜덤 피드백 생성
// 변경: OpenAI API 호출

const response = await fetch('https://api.openai.com/v1/chat/completions', {
  method: 'POST',
  headers: {
    'Authorization': `Bearer ${OPENAI_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    model: 'gpt-4-vision-preview',
    messages: [{
      role: 'user',
      content: [
        { type: 'text', text: '이 워크시트를 분석해주세요...' },
        { type: 'image_url', image_url: { url: base64Image } }
      ]
    }]
  })
});
```

**할 일:**
- [ ] OpenAI API 키 발급
- [ ] `app/index.html`의 `analyzeWorksheet()` 함수 수정
- [ ] 프롬프트 작성 (워크시트 유형 감지 + 피드백 생성)
- [ ] API 키 보안 처리 (백엔드 필요)

---

### 2️⃣ 백엔드 서버 구축

현재 프로필은 **브라우저 localStorage**에 저장됩니다. 영구 저장 + 다기기 동기화를 위해:

**옵션 A: Firebase (추천 - 빠름)**
```bash
npm install firebase
```
- Firestore: 학습 프로필 저장
- Auth: 구글/이메일 로그인
- Functions: AI API 키 숨김

**옵션 B: Supabase (PostgreSQL 원하면)**
- 오픈소스 Firebase 대안
- SQL 쿼리 가능

**할 일:**
- [ ] Firebase/Supabase 프로젝트 생성
- [ ] 인증 설정 (구글 로그인)
- [ ] 학습 프로필 스키마 설계
- [ ] API 호출을 서버리스 함수로 이동

---

### 3️⃣ Phase 2-4 워크시트 제작

Phase 1 (4장)은 완료. 나머지 제작 필요:

| Phase | 워크시트 | 스킬 |
|:-----:|----------|------|
| 2 | Theme.html | 주제 찾기 |
| 2 | TextEvidence.html | P.E.E. (Point-Evidence-Explanation) |
| 3 | FigurativeLanguage.html | 비유적 표현 |
| 3 | Symbolism.html | 상징 분석 |
| 4 | FactVsOpinion.html | 사실 vs 의견 |
| 4 | OREOEssay.html | 에세이 구조 |

**참고:** `worksheets/phase1/` 폴더의 기존 워크시트 스타일 따라서 제작

---

### 4️⃣ (선택) 모바일 앱 또는 PWA

**옵션 A: PWA로 전환**
- `manifest.json` + Service Worker 추가
- 홈 화면에 앱처럼 설치 가능
- 가장 빠른 방법

**옵션 B: React Native**
- 진짜 네이티브 앱
- 카메라 연동 더 자연스러움
- 개발 시간 더 필요

---

## 📌 현재 상태 요약

| 항목 | 상태 | 비고 |
|------|:----:|------|
| 워크시트 Phase 1 | ✅ 완료 | 4장 |
| 웹앱 프로토타입 | ✅ 완료 | 시뮬레이션 |
| 랜딩페이지 | ✅ 완료 | GitHub Pages |
| AI API 연동 | ⏳ 대기 | OpenAI 필요 |
| 백엔드 | ⏳ 대기 | Firebase 권장 |
| 워크시트 Phase 2-4 | ⏳ 대기 | 8장 추가 필요 |

---

## 🛠️ 로컬에서 실행하기

```bash
# 레포 클론
git clone https://github.com/jacopast/jalsal-mvp.git
cd jalsal-mvp

# 웹앱 실행 (브라우저에서 열기)
open app/index.html

# 또는 로컬 서버로 실행
npx serve .
```

---

## 📚 12주 커리큘럼 로드맵

| Phase | 주차 | 리딩 스킬 | 라이팅 스킬 |
|:-----:|:----:|-----------|-------------|
| 1 | 1-3 | B-M-E, SWBST, Main Idea | 문장 다양성, 단락 구성 |
| 2 | 4-6 | Theme, P.E.E. | 서론/본론/결론 |
| 3 | 7-9 | Figurative Language | 설득문, 정보문 |
| 4 | 10-12 | Fact vs Opinion | OREO 에세이 |

---

## 💬 피드백 환영!

질문이나 제안이 있으면 이슈 남겨주세요!

---

<p align="center">
  Made with ❤️ for Korean parents in North Jersey
</p>
