# everon Design System · `everon-ds`

> **스마트한 충전, 에버온** — 브랜드·제품·커뮤니케이션의 시각·언어 규칙과 재사용 가능 자산의 집합

[![Release](https://img.shields.io/badge/release-v1.0.0-12AAE2?style=flat-square)](https://github.com/everon/everon-ds/releases/tag/v1.0.0)
[![License](https://img.shields.io/badge/license-Everon%20Proprietary-1A2C5B?style=flat-square)](#license)
[![DS Guide](https://img.shields.io/badge/docs-DS%20Guide%20v1.0-0A6E95?style=flat-square)](./01_docs/EVR-DS-Guide-v1.0.pdf)
[![Figma](https://img.shields.io/badge/Figma-everon--ds%20Library-12AAE2?style=flat-square&logo=figma&logoColor=white)](https://figma.com/@everon-develop/에버온 앱_차기ver)
[![Slack](https://img.shields.io/badge/Slack-%23ds--release-6B7280?style=flat-square&logo=slack)](https://everon.slack.com/channels/ds-release)

---

## 목차

1. [개요](#1-개요)
2. [패키지 구성](#2-패키지-구성)
3. [3종 문서 가이드](#3-3종-문서-가이드)
   - [DS Guide v1.0](#31-ds-guide-v10)
   - [Figma Specbook v1.0](#32-figma-specbook-v10)
   - [QA SOP v1.0](#33-qa-sop-v10)
4. [빠른 시작](#4-빠른-시작)
5. [디렉터리 구조](#5-디렉터리-구조)
6. [디자인 토큰](#6-디자인-토큰)
7. [버전 정책](#7-버전-정책)
8. [기여 가이드](#8-기여-가이드)
9. [연락처](#9-연락처)
10. [라이선스](#10-라이선스)

---

## 1. 개요

**Everon Design System(everon-ds)** 은 에버온이 제공하는 모든 제품·서비스·커뮤니케이션에서
일관된 브랜드 경험과 사용성을 확보하기 위한 공용 규칙과 자산의 집합입니다.

```
DS는 '제한'이 아니라 '가속'을 위한 도구입니다.
동일한 메시지를 더 빠르고, 더 신뢰성 있게 전달하기 위한 공용 자산으로 운영합니다.
```

### 적용 범위

| 영역 | 예시 |
|------|------|
| **대외 제안서 · IR 자료** | 투자자 덱, 파트너사 제안서 |
| **운영 대시보드** | CSMS / EMS 관제 화면 |
| **충전기 UI · 사이니지** | 충전기 스크린, 현장 안내판 |
| **모바일 · 웹 고객 앱** | 에버온 앱, 웹사이트 |
| **마케팅 · 인쇄물** | 배너, 리플렛, 전시 부스 |

### 핵심 원칙 — 3C

```
Clarity      데이터·메시지를 군더더기 없이 전달한다.
Consistency  어디서 보아도 같은 에버온임을 알 수 있다.
Credibility  검증된 데이터와 절제된 표현으로 신뢰를 준다.
```

---

## 2. 패키지 구성

`everon-ds v1.0.0` 릴리즈는 아래 9개 구성 요소를 **단일 ZIP**으로 묶어 배포합니다.

| # | 구성 요소 | 형식 | 필수 |
|---|-----------|------|------|
| 1 | **DS Guide v1.0** | DOCX + PDF | ✅ |
| 2 | **Figma Library Specbook v1.0** | DOCX + PDF | ✅ |
| 3 | **Component QA SOP v1.0** | DOCX + PDF | ✅ |
| 4 | Design Tokens | JSON · CSS · SCSS | ✅ |
| 5 | Icon Set | SVG · WOFF2 | ✅ |
| 6 | PPT / Word 템플릿 | PPTX · DOCX | ✅ |
| 7 | Changelog / Release Notes | MD | ✅ |
| 8 | License / README | MD | ✅ |
| 9 | Sample / Cheatsheet | PDF · PNG | 선택 |

> **3종 문서는 분리 배포되지 않습니다.**  
> DS Guide만 수정하고 Figma Specbook · QA SOP를 그대로 두는 것은 금지입니다.  
> 원칙 변경은 반드시 구현 표준 · 검수 기준에 동시 반영되어 패키지로 묶여 배포됩니다.

---

## 3. 3종 문서 가이드

3종 문서는 서로를 참조하는 단일 진실 공급원(Single Source of Truth)으로 운영됩니다.

```
┌──────────────┐  규칙 정의    ┌───────────────────┐  구현 표준    ┌───────────────┐
│   DS Guide   │ ──────────▶ │  Figma Specbook   │ ──────────▶ │    QA SOP     │
│ (원칙·토큰)  │               │  (속성·Variant)    │             │   (검수 기준)    │
└──────┬───────┘             └─────────┬─────────┘             └───────┬───────┘
       │                               │                                │
       └──────── 공통 참조: design-tokens.json · everon-icons ───────────┘
                                       │
              모든 제작물(IR·대시보드·UI·사이니지·인쇄물)이 3문서를 동시 참조
```

---

### 3.1 DS Guide v1.0

> **문서 번호** `EVR-DS-GUIDE-v1.0` · **발행일** 2026-06-01 · **분류** 대외 배포용

브랜드·제품·커뮤니케이션 전반에 적용되는 **시각 규칙과 컴포넌트 체계**를 정의합니다.

#### 컬러 시스템

| 토큰 | HEX | 용도 |
|------|-----|------|
| `color-primary` | `#12AAE2` | 브랜드 강조, CTA 버튼, KPI 숫자 |
| `color-primary-deep` | `#0A6E95` | 헤더·타이틀 보조 |
| `color-neutral-dark` | `#1A2C5B` | 본문 강조, 표 헤더 |
| `color-accent-red` | `#E8231A` | 경고·오류 상태 |
| `color-accent-green` | `#00B15A` | 정상·성공 상태 |
| `color-neutral-mid` | `#6B7280` | 보조 텍스트 |
| `color-bg-subtle` | `#F5F6FA` | 배경·카드 바탕 |

**60 · 30 · 10 원칙** — 한 화면에서 Primary는 반드시 10% 강조 포인트로만 사용합니다.

#### 타이포그래피

```
기본 서체: Pretendard (1순위) / NanumGothic (Fallback)
숫자 강조: Pretendard ExtraBold

Role     Size        Weight
Display  40–56pt     ExtraBold (800)
H1       28–32pt     Bold (700)
H2       20–24pt     Bold (700)
Body     14–16pt     Regular (400)
Caption  10–12pt     Regular (400)
Number   32–72pt     ExtraBold (800)  ← KPI 숫자 전용
```

#### 컴포넌트 구조 — Atomic Design

```
Atoms      Button · Badge · Tag · Input
Molecules  Card · List · Form
Organisms  GlobalHeader · DashboardKPIGroup · Table
Signage    충전기 번호판 · 상태 LED · 현장 안내판
```

#### 금지 사례 — 주요 12항

| ID | 금지 내용 |
|----|-----------|
| D-01 | Primary 컬러를 한 화면에 여러 번 반복 사용 |
| D-03 | Pretendard / NanumGothic 외 장식체 사용 |
| D-05 | 의미를 색상만으로 전달 (아이콘·레이블 병기 필수) |
| D-06 | DS 외부 아이콘 혼용 (everon-icons 단일 사용) |
| D-07 | 출처·기간·단위 없는 차트 |
| D-10 | 승인되지 않은 로고 변형 |

> 전체 12항은 [`01_docs/EVR-DS-Guide-v1.0.pdf`](./01_docs/EVR-DS-Guide-v1.0.pdf) §6 참조

---

### 3.2 Figma Specbook v1.0

> **문서 번호** `EVR-DS-Figma-Specbook-v1.0` · **발행일** 2026-06-01 · **분류** 제한 공개

DS Guide의 원칙을 **Figma Library 속성·Variant·상태값**으로 구현한 명세서입니다.

#### Figma 파일 구조

```
[EVR] {도메인}·{자산}
├── 01_Cover
├── 02_Foundation      ← 컬러·타이포·그리드 토큰
├── 03_Components      ← Atoms / Molecules / Organisms
├── 04_Templates       ← IR·대시보드·충전기 UI·사이니지
└── 05_Changelog
```

#### 컴포넌트 명명 규칙

```
패턴: {Type}{Name}{Variant?}{State?}   (PascalCase)

예시:
  ButtonPrimary
  ButtonPrimary-disabled
  CardKPI
  CardKPI-success
  TableCompare
  HeaderSignage
```

#### Figma Library 접근

```
🔗 figma.com/@everon/everon-ds   (초대 전용 — ds@everon.co.kr 문의)
```

> 컴포넌트 속성 상세는 [`01_docs/EVR-DS-Figma-Specbook-v1.0.pdf`](./01_docs/EVR-DS-Figma-Specbook-v1.0.pdf) 참조

---

### 3.3 QA SOP v1.0

> **문서 번호** `EVR-DS-QA-SOP-v1.0` · **발행일** 2026-06-01 · **분류** 내부 전용

모든 배포 산출물이 DS 기준을 충족하는지 검증하는 **Gate 기반 품질 검수 절차**입니다.

#### 검수 Gate 구조

```
G1  디자인 토큰 매핑 검증   컬러·폰트·간격이 design-tokens.json 값과 일치하는가
G2  컴포넌트 48항목 체크     Atoms → Organisms 전 계층 Variant·State 검수
G3  접근성 · WCAG AA        대비비 4.5:1 이상, 색상+아이콘+레이블 3중 표현
G4  릴리즈 최종 서명        DSLead · QALead · PMO 3인 Sign-off
```

#### 30초 DS 적용 체크리스트

```
☐  Primary (#12AAE2)를 한 화면에 1회만 강조로 사용했는가?
☐  상태 컬러가 아이콘+레이블과 함께 표기되었는가?
☐  본문은 Pretendard / NanumGothic을 사용했는가?
☐  한 화면에 Weight가 3단계 이내로 제한되는가?
☐  차트에 제목·단위·기간·출처가 모두 있는가?
☐  버튼·카드·표가 DS 컴포넌트를 그대로 사용했는가?
☐  파일명·슬라이드 제목이 명명 규칙을 따르는가?
☐  색맹·저시력 사용자를 위한 대체 표현이 있는가?
☐  6장 금지 사례 12개 항목에 해당하는 요소가 없는가?
☐  대외 배포 자료의 경우 PMO 검수를 마쳤는가?
```

> 전체 Gate 및 48항목 체크리스트는 [`01_docs/EVR-DS-QA-SOP-v1.0.pdf`](./01_docs/EVR-DS-QA-SOP-v1.0.pdf) 참조

---

## 4. 빠른 시작

### 디자이너

```
1. Figma → '에버온 앱_차기ver' 라이브러리 활성화 (초대 링크: everon79517@gmail.com)
2. 04_templates/ 에서 PPT · Word 템플릿 다운로드
3. DS Guide §5 사용 예시 참고하여 제작 시작
4. 배포 전 30초 체크리스트 (§3.3) 자가 점검
```

### 프런트엔드 개발자

```bash
# 디자인 토큰 가져오기
cp 02_tokens/design-tokens.css  src/styles/tokens.css
cp 02_tokens/design-tokens.json src/tokens.json

# 아이콘 폰트 적용
cp 03_icons/everon-icons.woff2  public/fonts/

# CSS 토큰 사용 예시
.btn-primary {
  background-color: var(--color-primary);   /* #12AAE2 */
  color: var(--color-bg-white);
  border-radius: var(--radius-md);           /* 8px */
}
```

### 파트너사 · 외주사

```
1. 패키지 다운로드: intranet.everon.co.kr/ds/releases
2. SHA256 체크섬 검증: sha256sum -c everon-ds-v1.0.0.zip.sha256
3. MANIFEST.json에서 컴포넌트 버전 확인
4. DS Guide §2·§6 필독 후 제작 착수
```

---

## 5. 디렉터리 구조

```
everon-ds-v1.0.0/
├── 00_README.md                          ← 패키지 진입점 (이 파일)
├── 00_CHANGELOG.md                       ← 버전별 변경 이력
├── 00_LICENSE.md                         ← 사용 권한·제한
├── 00_MANIFEST.json                      ← 패키지 메타데이터 (자동 생성)
│
├── 01_docs/                              ← 배포용 문서 3종
│   ├── EVR-DS-Guide-v1.0.docx
│   ├── EVR-DS-Guide-v1.0.pdf
│   ├── EVR-DS-Figma-Specbook-v1.0.docx
│   ├── EVR-DS-Figma-Specbook-v1.0.pdf
│   ├── EVR-DS-QA-SOP-v1.0.docx
│   └── EVR-DS-QA-SOP-v1.0.pdf
│
├── 02_tokens/                            ← 디자인 토큰 (개발 소비용)
│   ├── design-tokens.json               ← 단일 원본 (Source of Truth)
│   ├── design-tokens.css
│   ├── design-tokens.scss
│   └── design-tokens.figma.json
│
├── 03_icons/                             ← 아이콘 자산
│   ├── svg/                             ← 80종 SVG
│   ├── everon-icons.woff2
│   ├── icons-index.json
│   └── icons-preview.pdf
│
├── 04_templates/                         ← 제작 템플릿
│   ├── ppt/
│   │   ├── EVR-IR-Template-v1.0.pptx
│   │   ├── EVR-Sales-Deck-Template-v1.0.pptx
│   │   └── EVR-Internal-Report-Template-v1.0.pptx
│   └── word/
│       ├── EVR-Proposal-Template-v1.0.docx
│       └── EVR-Report-Template-v1.0.docx
│
├── 05_samples/                           ← 참고 샘플·치트시트
│   ├── cheatsheet-1page.pdf
│   ├── do-dont-examples.pdf
│   └── kpi-card-variations.png
│
└── 99_release-notes/                     ← 릴리즈 노트 상세
    ├── v1.0.0-release-note.md
    └── migration-guide-from-v0.9.md
```

---

## 6. 디자인 토큰

모든 토큰은 `{category}-{role}-{modifier?}` 패턴을 따릅니다.

```json
{
  "color-primary":        "#12AAE2",
  "color-primary-deep":   "#0A6E95",
  "color-neutral-dark":   "#1A2C5B",
  "color-text-default":   "#111111",
  "color-text-muted":     "#6B7280",
  "color-bg-surface":     "#FFFFFF",
  "color-bg-subtle":      "#F5F6FA",
  "color-state-success":  "#00B15A",
  "color-state-danger":   "#E8231A",
  "font-family-base":     "Pretendard, NanumGothic, sans-serif",
  "font-size-h1":         "32",
  "radius-md":            "8",
  "spacing-4":            "16",
  "shadow-card":          "0 2px 8px rgba(17,17,17,0.06)"
}
```

CSS Custom Properties로도 동일하게 사용 가능합니다:

```css
/* 02_tokens/design-tokens.css */
:root {
  --color-primary:       #12AAE2;
  --color-primary-deep:  #0A6E95;
  --font-family-base:    Pretendard, NanumGothic, sans-serif;
  --radius-md:           8px;
  --shadow-card:         0 2px 8px rgba(17,17,17,0.06);
}
```

---

## 7. 버전 정책

`everon-ds`는 **Semantic Versioning (MAJOR.MINOR.PATCH)** 을 따릅니다.

| 변경 유형 | SemVer | 사전 공지 |
|-----------|--------|-----------|
| 브랜드 컬러·폴더 구조·Component Property 이름 변경 | **MAJOR** | 90일 전 |
| 신규 컴포넌트·Variant·템플릿 추가 | **MINOR** | 릴리즈 공지 |
| 오탈자·아이콘 픽셀·링크 수정 | **PATCH** | 불필요 |
| Deprecated 컴포넌트 제거 | **MAJOR** | 90일 전 + 1 MINOR 유예 |

### 브랜치 전략

```
main              최신 안정 버전
develop           다음 MINOR 통합
release/v1.1      릴리즈 후보 안정화
hotfix/v1.0.1     긴급 PATCH 수정
feature/*         신규 컴포넌트 작업
```

---

## 8. 기여 가이드

### 신규 컴포넌트 요청

1. [이슈 트래커](https://intranet.everon.co.kr/ds/issues) → `feat:` 프리픽스로 등록
2. DSWG이 **2주 이내** 수용 여부 회신
3. 승인 후 `feature/` 브랜치에서 개발 → PR → `develop` 병합

### PR 체크리스트

```
☐  design-tokens.json 값이 변경된 경우 CSS · SCSS도 동시 업데이트
☐  신규 컴포넌트의 경우 Figma Specbook 동시 업데이트
☐  QA SOP G2 48항목 자가 점검 완료
☐  금지 사례 D-01~D-12 위반 없음 확인
☐  CHANGELOG.md 업데이트 (Added / Changed / Deprecated / Fixed)
☐  파일명이 EVR-{도메인}-{이름}-v{버전} 규칙 준수
```

### 긴급 수정 (P0 Hotfix)

```
T+0   P0 탐지 → 릴리즈 Hold 공지         QALead
T+2h  원인 분석 + Rollback/Hotfix 결정    DSLead + QALead
T+6h  PATCH 버전 빌드 (예: v1.0.1)        ReleaseTeam
T+12h QA G3 재실행 + Sign-off            QALead + PMO
T+24h 긴급 배포 + 전사 공지               ReleaseTeam
T+7d  사후 회고 + CAPA 문서화             DSWG
```

---

## 9. 연락처

| 채널 | 용도 | 주소 |
|------|------|------|
| **DS Working Group** | 일반 문의·기여 제안 | ds@everon.co.kr |
| **QA 문의** | 검수 기준·Gate 질문 | ds-qa@everon.co.kr |
| **릴리즈 공지 구독** | 버전 업데이트 수신 | ds-release@everon.co.kr |
| **긴급 P0** | 크리티컬 이슈 | Slack `#ds-p0` |
| **라이선스 문의** | 재배포·파생물 | legal@everon.co.kr |
| **사내 포털** | 패키지 다운로드 | intranet.everon.co.kr/ds |
| **이슈 트래커** | 버그·기능 요청 | intranet.everon.co.kr/ds/issues |

---

## 10. 라이선스

```
Copyright © 2026 에버온(주). All rights reserved.

사용 범위  에버온과 정식 계약을 체결한 임직원·파트너·외주사에 한함.
재배포     금지. 필요 시 에버온 법무실 서면 승인 필수.
파생물     본 패키지를 이용해 제작된 결과물의 저작권은 별도 계약을 따름.
위반 시    즉시 사용 중지 + 법적 조치 가능.
```

자세한 내용은 [`00_LICENSE.md`](./00_LICENSE.md) 참조.

---

<p align="center">
  <strong>everon Design System v1.0.0</strong><br>
  <sub>2026-06-01 · EVR-DS-PKG-v1.0 · DS Working Group</sub>
</p>
