# 🧠 맬리 3.1 - 4.0 (Mali)
> **일상 건강은 맬리에서 매일 이롭게 (Every day with Mali)**<br>
> CloudFront Signed Cookie 보안 도입 · 대한체육회 프로토타입 · Android 100% 단독 개발

---

## 🗂 목차
1. [개요](#-개요)
2. [핵심 성과](#-핵심-성과)
3. [기술 스택](#-기술-스택)
4. [주요 기여](#-주요-기여)
5. [스크린샷](#-스크린샷)
6. [역활](#-역할)

---

## 📝 개요
운동 프로세스 전면 개편과 CloudFront Signed Cookie 기반 미디어 보안 시스템을 Android 100% 단독으로 구축, 대한체육회 프로토타입으로 사업 영역 확장

![서비스 커버](https://github.com/chani01/portfolio_info/blob/main/images/meli/meli_cover(31).png)

---

## 📈 핵심 성과
| 지표 | 결과 |
|------|------|
| 미디어 보안 | 서버 발급 **CloudFront Signed Cookie**를 Android에 연동하여 미디어 접근 제어 구현 |
| 프로토타입 | **대한체육회** 대상 프로토타입의 기능 정의 및 Android 개발 수행 |
| 공공 협업 | **인천 남동구 보건소 치매안심센터** 협력 서비스의 Android 기능 개발 및 운영 지원 |

---

## 🛠 기술 스택
**Android**  
`Kotlin` `Jetpack Compose` `Room`

**Architecture**  
`MVVM` `Clean Architecture`

**Network & Cloud**  
`GraphQL` `AWS CloudFront`

**Distribution**  
`Firebase App Distribution`

**AI Tools**  
`Claude Code` `Firebender`

---

## 🚀 주요 기여

### 1. 운동 프로세스 전면 개편
- 시니어 사용자가 운동 수치와 진행 상태를 직관적으로 확인할 수 있도록 **운동 프로세스 및 UI 전면 개편**
- Jetpack Compose 기반 동적 UI를 구현하여 **다양한 운동 시나리오와 상태 변화에 유연하게 대응**
- 운동 진행 상태에 따른 화면 및 데이터 흐름을 구조화하여 유지보수성과 기능 확장성 개선

### 2. CloudFront 기반 미디어 접근 제어
- 서버에서 발급한 CloudFront Signed Cookie를 Android에서 전달받아 미디어 요청에 적용
- 인증된 사용자만 미디어 콘텐츠에 접근할 수 있도록 Signed Cookie 기반 인증 처리 구현
- 인증 정보를 유지·관리하며 안정적인 미디어 스트리밍 처리

### 3. 로컬 데이터 및 서버 통신 고도화
- Room DB를 활용해 재활·운동 기록을 로컬에서 관리하고 데이터 저장 및 조회 구조 개선
- GraphQL 기반 API 연동을 통해 서비스에 필요한 데이터 조회·갱신 로직 구현
- 로컬 데이터와 서버 데이터의 상태를 고려한 데이터 동기화 및 예외 처리

---

## 🖼 스크린샷
<img src="https://github.com/chani01/portfolio_info/blob/main/images/meli/meli31.png" width="100%">

---

## 📊 역할
- Android 개발자 | Android 개발 기여도 100%
- 운동 프로세스 전면 개편 및 CloudFront Signed Cookie 기반 미디어 인증 연동
- Claude Code · Firebender AI를 활용한 코드 작성·분석 및 개발 생산성 향상
