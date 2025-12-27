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

## 🚀 다음 단계

- [ ] 실제 AI API 연동 (OpenAI GPT-4 Vision)
- [ ] 백엔드 서버 구축 (Firebase/Supabase)
- [ ] Phase 2-4 워크시트 제작
- [ ] 모바일 앱 개발

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
