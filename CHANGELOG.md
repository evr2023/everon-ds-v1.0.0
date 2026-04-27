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

# 9. Git Tag 전략

## 🎯 Versioning Rule (Semantic Versioning 기반)

형식:

```
vMAJOR.MINOR.PATCH
```

### 기준

* **MAJOR (v1 → v2)**

  * 디자인 시스템 구조 변경
  * 기존 호환성 깨짐 (Breaking Change)

* **MINOR (v1.0 → v1.1)**

  * 새로운 컴포넌트 / 패턴 추가
  * 기존 시스템 확장

* **PATCH (v1.0.0 → v1.0.1)**

  * 버그 수정
  * 수치 보정 / 오타 수정

---

## 📌 Tag 네이밍 규칙

* `v1.0.0` → 초기 릴리즈
* `v1.1.0` → 기능 추가
* `v1.1.1` → QA 수정

---

## 🚀 Release 프로세스

1. feature 브랜치 작업
2. develop 브랜치 merge
3. QA 검증 완료
4. main 브랜치 merge
5. Tag 생성

```bash
git tag v1.1.0
git push origin v1.1.0
```

---

## 🧭 브랜치 전략

* main: 릴리즈 버전
* develop: 통합 개발
* feature/*: 기능 단위 작업
* hotfix/*: 긴급 수정

---

# 10. Pull Request 템플릿

## 📄 PR Title 규칙

```
[type] 간단한 설명
```

예:

* feat: EV Zone 패턴 추가
* fix: 로고 정렬 오류 수정
* chore: 토큰 구조 정리

---

## 🧾 PR Template

```markdown
## 🔍 변경 내용
- 무엇을 변경했는지 명확히 작성

## 🎯 변경 이유
- 왜 이 변경이 필요한지 설명

## 🧩 작업 범위
- [ ] DS Guide
- [ ] Figma Specbook
- [ ] QA SOP

## ⚠️ 영향도
- [ ] 기존 디자인 영향 없음
- [ ] 일부 컴포넌트 영향
- [ ] 전체 시스템 영향

## 🖼 Before / After
- (이미지 또는 링크 첨부)

## ✅ 체크리스트
- [ ] 디자인 원칙 준수
- [ ] 토큰 일관성 유지
- [ ] QA 기준 영향 검토
- [ ] 문서 업데이트 완료

## 🧪 QA 확인
- 테스트 완료 여부 작성

## 🔗 관련 이슈
- Closes #issue_number
```

---

## 💡 운영 팁

* PR은 작게 나누는 것이 좋음 (1 기능 = 1 PR)
* 최소 1명 이상 리뷰 필수
* 디자인 변경은 반드시 시각 자료 포함

---

---

# 11. GitHub Issue 템플릿

## 🐞 Bug Report (버그)

```markdown
## 🐞 문제 설명
- 발생한 문제를 구체적으로 작성

## 📍 발생 위치
- 페이지 / 컴포넌트 / 공간 위치

## 🔁 재현 방법
1. 
2. 
3. 

## 🎯 기대 결과
- 정상 동작 또는 기대 상태 설명

## 📸 스크린샷
- (가능하면 첨부)

## 🧪 환경
- OS:
- Browser:
- 디바이스:

## ⚠️ 영향도
- [ ] 낮음
- [ ] 중간
- [ ] 높음 (서비스 영향)
```

---

## 🎨 Design Request (디자인 요청)

```markdown
## 🎨 요청 내용
- 필요한 디자인 작업 설명

## 🎯 목적
- 왜 필요한지 (비즈니스/UX 관점)

## 📍 적용 범위
- [ ] DS Guide
- [ ] Figma Specbook
- [ ] 공간 디자인

## 🧩 참고 자료
- 레퍼런스 링크 / 이미지

## ⏱ 우선순위
- [ ] Low
- [ ] Medium
- [ ] High

## 📅 희망 일정
- 
```

---

## 🏗 Construction Issue (시공 이슈)

```markdown
## 🏗 이슈 내용
- 현장에서 발생한 문제 설명

## 📍 위치
- 주차장 / 층 / 구역

## 📏 실제 시공 상태
- (치수, 오차 등 구체적으로 작성)

## 🎯 기준 대비 문제
- 어떤 기준과 다른지 명시 (DS / 도면 / QA)

## 📸 현장 사진
- 필수 첨부

## ⚠️ 영향도
- [ ] 경미
- [ ] 기능 영향
- [ ] 안전 문제

## 🛠 요청 조치
- 수정 / 재시공 / 검토 등

## 👷 담당자
- 
```

---

## 💡 운영 팁

* Issue는 반드시 **유형(label)** 구분

  * bug
  * design
  * construction

* 시공 이슈는 항상 **사진 + 치수 포함**

* 디자인 요청은 반드시 **목적 포함**
  
