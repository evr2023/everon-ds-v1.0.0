# Changelog · `everon-ds`

모든 주요 변경 사항을 이 파일에 기록합니다.  
형식은 [Keep a Changelog](https://keepachangelog.com/ko/1.0.0/)를 따르며,  
버전은 [Semantic Versioning](https://semver.org/lang/ko/)을 준수합니다.

> **범례**
> - `[BREAKING]` — 하위 호환 불가, MAJOR 변경
> - `[NEW]` — 신규 추가, MINOR 변경
> - `[IMPROVED]` — 개선·수정, MINOR 또는 PATCH
> - `[DEPRECATED]` — 다음 버전에서 제거 예정
> - `[FIXED]` — 버그·오탈자 수정, PATCH
> - `[SECURITY]` — 보안 관련 변경

---

## [1.0.0] — 2026-06-01 · Initial Release

> **패키지** `everon-ds-v1.0.0.zip`  
> **SHA256** `{자동 생성 — 배포 시 MANIFEST.json 참조}`  
> **릴리즈 주관** DS Working Group / PMO  
> **Sign-off**  인프라구축팀 · 플랫폼사업담당 · 전략기획실 (3인 서명 완료)

### 🎉 최초 정식 릴리즈 — 전사 배포

에버온 디자인 시스템의 첫 번째 공식 릴리즈입니다.  
DS Guide · Figma Specbook · Component QA SOP 3종이 단일 패키지로 통합 배포됩니다.

---

#### Added — DS Guide v1.0 (`EVR-DS-GUIDE-v1.0`)

- **[NEW] 디자인 원칙 3C 정의** — Clarity / Consistency / Credibility 원칙 및 실무 체크포인트 명문화
- **[NEW] 컬러 시스템 확립** — Primary `#12AAE2` 기반 8종 팔레트, 60-30-10 사용 비율 가이드, 상태 컬러 매핑(Success / Info / Warning / Danger / Disabled)
- **[NEW] WCAG AA 접근성 기준 적용** — 본문 4.5:1 이상, 대형 텍스트 3:1 이상 대비비 규칙 수립
- **[NEW] 타이포그래피 체계** — Pretendard / NanumGothic 서체 지정, Display ~ Code까지 7단계 Role 정의
- **[NEW] 그리드 & 레이아웃** — 슬라이드(12col) · 문서(6col) · Web Desktop(12col) · Mobile(4col) 매체별 기준 수립
- **[NEW] 아이콘 · 이미지 · 모션 가이드** — everon-icons 전용 셋 지정, 이미지 보정 기준, 이징 200-300ms 규칙
- **[NEW] Atomic Design 컴포넌트 체계** — Atoms / Molecules / Organisms 3계층 정의
  - Button (Primary / Secondary / Ghost / Danger / Disabled) 5종 Variant
  - Badge / Tag 상태 컬러 매핑
  - Input 포커스·오류 상태
  - Card(KPI · 콘텐츠 · 정보) / List / Form
  - GlobalHeader / DashboardKPIGroup / Table
  - 차트 유형별 컬러 매핑 (Bar / Line·Area / Donut / Combo)
  - 사이니지 / 현장 전용 컴포넌트 (충전기 번호판, 상태 LED, 야간 가독성 기준)
- **[NEW] 명명 규칙 체계** — 디자인 토큰 / 컴포넌트 / 파일명 / Figma 레이어 4종 규칙
- **[NEW] 사용 예시** — IR·제안서 / 운영 대시보드(CSMS/EMS) / 충전기 UI / 현장 표시물 4개 시나리오
- **[NEW] 금지 사례 12항 (D-01 ~ D-12)** — 브랜드 일관성·가독성을 해치는 패턴 명문화
- **[NEW] DS 적용 체크리스트 (10항목)** — 30초 자가 점검 양식
- **[NEW] 용어집 (Glossary)** — DS / 디자인 토큰 / Atomic Design / CSMS / EMS / PnC / WCAG AA / KPI 정의
- **[NEW] 리소스 배포 링크** — Figma Library / GitHub Tokens / 아이콘 / 템플릿 / 사내 포털 / 이슈 트래커

---

#### Added — Figma Specbook v1.0 (`EVR-DS-Figma-Specbook-v1.0`)

- **[NEW] Figma 파일 구조 표준화** — `[EVR] {도메인}·{자산}` 네이밍, 01_Cover ~ 05_Changelog 5개 페이지 체계
- **[NEW] 컴포넌트 속성 · Variant · State 명세** — DS Guide 원칙을 Figma 구현값으로 번역
- **[NEW] 프레임 명명 기준** — `{ScreenName}/{Size}/{Mode}` 패턴 (예: `Dashboard-KPI/Desktop-1440/Light`)
- **[NEW] 레이어 명명 기준** — 컴포넌트명 + 역할 (예: `ButtonPrimary/Label`, `CardKPI/Trend`)
- **[NEW] DS Guide 크로스 레퍼런스 규칙** — `Specbook → Guide` 참조 방향·표기 방식 정의
- **[NEW] Figma Library 배포 채널** — Community 초대 전용 링크 운영 (`figma.com/@everon_develop`)

---

#### Added — Component QA SOP v1.0 (`EVR-DS-QA-SOP-v1.0`)

- **[NEW] Gate 기반 검수 프로세스 수립** — G1(토큰 매핑) → G2(컴포넌트 48항) → G3(접근성) → G4(Sign-off) 4단계
- **[NEW] 릴리즈 체크리스트 20항목** — 스코프 / QA / 문서 / 자산 / 빌드 / 승인 / 배포 전 과정 점검
- **[NEW] 파트너 수신 확인 체크리스트 5항목** — SHA256 검증 / GPG 서명 / MANIFEST 확인 절차
- **[NEW] QASOP ↔ DS Guide 크로스 레퍼런스** — `QA B3 → Guide 2.2.3 + D-05` 형태 상호 참조 체계

---

#### Added — 토큰 · 자산 · 패키지 인프라

- **[NEW] design-tokens.json** — Single Source of Truth, CSS / SCSS / Figma Tokens Studio 연동 4종 포맷
- **[NEW] everon-icons v0.8.0** — SVG 80종 + WOFF2 아이콘 폰트, icons-index.json 매핑
- **[NEW] PPT 템플릿 3종** — EVR-IR / EVR-Sales-Deck / EVR-Internal-Report
- **[NEW] Word 템플릿 2종** — EVR-Proposal / EVR-Report
- **[NEW] MANIFEST.json 스키마** — 패키지 버전·구성 요소·SHA256·호환성 자동 생성
- **[NEW] 무결성 검증 파이프라인** — Build → Hash → Manifest → Lint → Diff → GPG Sign 6단계
- **[NEW] 배포 채널 5종** — 사내 포털 / GitHub Releases(Private) / Figma Community / 파트너 포털 / 이메일 공지
- **[NEW] Hotfix(P0) 절차** — T+0 탐지 ~ T+24h 배포 ~ T+7d 회고 6단계 SLA
- **[NEW] Deprecation 3단계 정책** — Announce → Soft Freeze → Remove, 90일 전 통지 규칙

---

### Changed

_초최 릴리즈로 해당 없음_

### Deprecated

_초최 릴리즈로 해당 없음_

### Fixed

_초최 릴리즈로 해당 없음_

---

## [0.95] — 2026-05-18 · Internal Review Draft

> **배포 범위** DSWG / PMO 내부 검토용 (비공개)

### Changed

- **[IMPROVED] 컴포넌트 명명 규칙 구체화** — PascalCase + Variant-State 하이픈 결합 방식으로 정리
- **[IMPROVED] 금지 사례 보강** — D-08(사이니지 3D 효과), D-09(비교 차트 기준 혼용), D-11(개인정보 마스킹) 추가
- **[IMPROVED] 사이니지 컴포넌트 상세화** — 야간 가독성 7:1 대비비, 5m·3초 가독성 기준 명문화
- **[IMPROVED] Figma Specbook 컴포넌트 Variant 구체화** — Button State 5단계, Card Shadow 토큰 정의
- **[IMPROVED] QA SOP Gate 체계 재구성** — G1~G4 단계별 산출물·담당자·기준 명확화
- **[IMPROVED] PMO 내부 리뷰 피드백 반영** — 차트 컬러 매핑 표 추가, 조판 규칙 보완

### Fixed

- **[FIXED]** 타이포그래피 Line-height 값 오기 수정 (H3: 1.35 → 1.3)
- **[FIXED]** 상태 컬러 Warning HEX 오기 수정 (`#F59E0B` 통일)
- **[FIXED]** 파일명 규칙 예시 오탈자 수정

---

## [0.9] — 2026-04-27 · Initial Draft

> **배포 범위** DSWG / 디자인팀 내부 초안 (비공개)

### Added

- **[NEW]** 컬러 시스템 초안 — Primary `#12AAE2` 및 보조 색상 시안
- **[NEW]** 타이포그래피 초안 — Pretendard 서체 1순위 지정
- **[NEW]** Figma 파일 구조 초안 — 페이지 체계 1차 설계
- **[NEW]** Button / Card 컴포넌트 초안
- **[NEW]** DS Guide 문서 골격 작성 (목차·섹션 구조)

---

## 예정 릴리즈 로드맵

> 아래 일정은 내부 계획이며 변경될 수 있습니다.

### [1.1.0] — 예정: 2026-Q3

- **[NEW]** Stepper 컴포넌트 추가
- **[NEW]** 모바일 사이니지 컴포넌트 (QR/NFC 안내 패널)
- **[NEW]** EVR-Finance-Report 템플릿 추가
- **[IMPROVED]** Button에 'link' Variant 추가
- **[IMPROVED]** DashboardKPIGroup 반응형 레이아웃 가이드

### [1.0.1] — 예정: 2026-Q3 (필요 시)

- **[FIXED]** 발견된 오탈자 · 링크 오류 · 아이콘 픽셀 보정

### [2.0.0] — 미정

- **[BREAKING]** 브랜드 리프레시 시 컬러 팔레트 전면 교토
- **[BREAKING]** Component Property 이름 체계 재정비

---

## 변경 이력 관리 원칙

```
1. 모든 변경 사항은 PR merge 시점에 이 파일에 기록합니다.
2. 섹션 순서: Added → Changed → Deprecated → Fixed → Security
3. 각 항목은 '[태그] 변경 내용' 형식으로 작성합니다.
4. Breaking Change는 반드시 [BREAKING] 태그를 명시합니다.
5. 비공개 내부 버전(0.x)은 배포 후 소급 기재합니다.
```

---

<p align="center">
  <sub>everon Design System · CHANGELOG · 2026</sub>
</p>
