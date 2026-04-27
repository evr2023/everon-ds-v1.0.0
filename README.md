# everon-ds-v1.0.0
에버온 브랜드의 일관된 사용자 경험과 시공 품질을 유지하기 위한  
**Design System · Figma Specbook · QA SOP 통합 가이드 저장소**입니다.

---

## 📦 구성 (3 Core Assets)

### 1. DS Guide (Design System Guide)
브랜드 및 UI/공간 디자인의 기준 정의

**포함 내용**
- Brand Identity (컬러, 타이포그래피, 톤앤매너)
- Component System (UI / 공간 그래픽 요소)
- Layout & Grid System
- Iconography
- EV 충전 존 공간 브랜딩 가이드
- Do & Don't

👉 목적:  
디자인 결과물이 아닌 **“일관된 기준” 제공**

---

### 2. Figma Specbook
실제 구현을 위한 디자인 상세 명세

**포함 내용**
- 컴포넌트 상세 스펙 (Auto Layout 포함)
- 사이즈 / 간격 / 패딩 정의
- 컬러 코드 (HEX / RGB / CMYK)
- 텍스트 스타일 (Font Size / Weight / Line-height)
- 상태값 (Hover / Active / Disabled)
- 반응형 규칙
- 시공용 도면 (벽면 그래픽 / 라인 / 존 구성)

👉 목적:  
디자인 → 개발/시공으로 넘어가는 **정확한 기준 제공**

---

### 3. QA SOP (Quality Assurance Standard Operating Procedure)
디자인 및 시공 결과 검수 기준

**포함 내용**
- 사전 검수 체크리스트
- 시공 중 품질 체크 기준
- 완료 후 검수 항목
- 오차 허용 범위 (mm 단위)
- 컬러 매칭 기준
- 설치 위치 및 정렬 기준
- 사진 검수 가이드

👉 목적:  
결과물의 품질을 **정량적으로 관리**

---

## 🔄 Workflow

```mermaid
graph LR
A[DS Guide] --> B[Figma Specbook]
B --> C[Implementation]
C --> D[QA SOP]
D --> E[Final Delivery]
