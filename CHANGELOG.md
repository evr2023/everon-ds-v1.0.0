# Everon Design System – Implementation Pack

본 문서는 실제 실행 가능한 수준의 **Figma 구조 / Design Token(JSON) / QA 체크리스트**를 포함합니다.

---

# 1. Figma 파일 구조 (실무형)

## 📁 File: Everon_DS_v1.0.fig

### Pages 구조

1. **00_Foundation**

   * Color Styles
   * Typography
   * Grid System
   * Elevation

2. **01_Tokens**

   * Primitive Tokens
   * Semantic Tokens

3. **02_Components**

   * Buttons
   * Inputs
   * Cards
   * EV Charger UI

4. **03_Patterns**

   * Layout Templates
   * EV Zone Layout

5. **04_Spatial (중요)**

   * Wall Graphics
   * Parking Line System
   * Signage

6. **05_Specbook**

   * 컴포넌트 상세 스펙
   * 간격 / 수치 정의

---

## 🧱 Auto Layout 규칙

* Padding: 16 / 24 / 32 기준
* Gap: 8pt grid
* Radius: 8 / 16 / 999

---

# 2. Design Token (JSON)

```json
{
  "color": {
    "primary": {
      "main": "#1E88E5",
      "light": "#6AB7FF",
      "dark": "#005CB2"
    },
    "neutral": {
      "900": "#111111",
      "700": "#555555",
      "500": "#9E9E9E",
      "100": "#F5F5F5"
    }
  },
  "spacing": {
    "xs": 4,
    "sm": 8,
    "md": 16,
    "lg": 24,
    "xl": 32
  },
  "radius": {
    "sm": 8,
    "md": 16,
    "full": 999
  },
  "typography": {
    "h1": {
      "size": 32,
      "weight": 700
    },
    "body": {
      "size": 16,
      "weight": 400
    }
  }
}
```

---

# 3. EV 공간 디자인 규격

## 📐 벽면 그래픽

* 라운드 프레임 두께: 120mm
* 내부 채움 비율: 70%
* 로고 중심 정렬

## 🚗 주차 라인

* 라인 두께: 100mm
* 색상: Primary
* 텍스트 위치: 중앙 하단

---

# 4. QA 체크리스트 (실무용)

## 🧾 사전 검수

* [ ] 도면과 시공 위치 일치
* [ ] 컬러 코드 확인
* [ ] 재질 확인

## 🔧 시공 중

* [ ] 수평/수직 정렬
* [ ] 라인 두께 오차 ±5mm
* [ ] 간격 오차 ±10mm

## ✅ 완료 후

* [ ] 브랜드 로고 위치 정확성
* [ ] 조명 균일성
* [ ] 오염 및 마감 상태

---

# 5. 사진 검수 가이드

* 정면 1컷
* 좌/우 45도
* 디테일 컷

---

# 6. 운영 규칙

* 모든 변경은 PR 기반
* QA 기준 변경 시 전체 업데이트

---

# 7. 확장 방향

* 앱 UI 연동
* 스마트 충전 UX 연결
* IoT 데이터 시각화

---

---

# 8. CHANGELOG

## [v1.0.0] - Initial Release

### Added

* Design System Guide 초안 정의
* Figma Specbook 구조 설계
* Design Token(JSON) v1.0 정의
* EV 충전 존 공간 디자인 가이드
* QA SOP 체크리스트 구축

---

## [v1.1.0] - Brand Zone 고도화

### Added

* 라운드 프레임형 브랜드 존 패턴 추가
* 벽면 그래픽 확장 규칙 정의

### Changed

* Primary Color 대비 개선 (접근성 기준 반영)
* 주차 라인 두께 기준 80mm → 100mm 수정

---

## [v1.2.0] - Spec 정밀화

### Added

* Auto Layout 규칙 상세화
* 컴포넌트 간격 토큰 확장

### Fixed

* 텍스트 정렬 오차 기준 수정
* 로고 위치 가이드 보정

---

## [v1.3.0] - QA 체계 강화

### Added

* 시공 오차 허용 범위 정의 (mm 단위)
* 사진 검수 가이드 추가

### Changed

* QA 체크리스트 단계별 분리 (사전/중간/완료)

---

## [Unreleased]

### Planned

* Figma Tokens 자동 연동
* QA 모바일 체크 시스템
* 스마트 충전 UX 연계 가이드

---

End of Document

