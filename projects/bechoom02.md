# 🌙 비춤 0.2 (Bechoom 0.2)
> **인증 체계 강화 및 백엔드 인프라 전환을 통한 서비스 고도화**<br>
> Firebase → Supabase 마이그레이션 · SNS 로그인 · 생체 인식 인증 · Android · Backend 단독 개발

---

## 🗂 목차
1. [개요](#-개요)
2. [핵심 성과](#-핵심-성과)
3. [기술 스택](#-기술-스택)
4. [주요 기여](#-주요-기여)
5. [스크린샷](#-스크린샷)
6. [역할](#-역할)

---

## 📝 개요
비춤 0.1의 Firebase 기반 데이터 구조를
**Supabase(PostgreSQL) 기반 백엔드로 전환**한 프로젝트입니다.

Android 앱 개발뿐만 아니라 Supabase 프로젝트 구성,
DB 스키마 설계, Auth 및 Storage 설정 등
**백엔드 환경 설계와 구축을 직접 담당**했습니다.

또한 Google·Kakao·Naver SNS 로그인과
Android Biometric API 기반 생체 인증을 구현하여
서비스의 인증 기능을 확장했습니다.

![서비스 커버](https://github.com/chani01/portfolio_info/blob/main/images/bechoom/bechoom001_cover.png)

---
## 📈 핵심 성과

| 구분 | 성과 |
|------|------|
| Backend | Firebase에서 **Supabase(PostgreSQL) 기반 백엔드로 전환** |
| DB 설계 | 서비스 데이터 구조에 맞는 **PostgreSQL DB 스키마 직접 설계** |
| 인증 | **Google · Kakao · Naver SNS 로그인** 및 세션 관리 구현 |
| 보안 | Android **Biometric API 기반 생체 인증 기능 구현** |
| 개발 범위 | **Android · Backend 단독 개발** |

---

## 🛠 기술 스택

**Android**  
`Kotlin` `Jetpack Compose` `Room` `Biometric API`

**Architecture**  
`MVVM` `Clean Architecture`

**Backend & Database**  
`Supabase` `PostgreSQL` `Supabase Auth` `Supabase Storage`

**Authentication**  
`Google Login` `Kakao Login` `Naver Login`

**AI Tools**  
`Claude Code` `Firebender`

**Design**  
`Figma`

---

## 🚀 주요 기여

### 1. Firebase → Supabase 백엔드 마이그레이션

- 기존 Cloud Firestore 기반 데이터 구조를 **Supabase(PostgreSQL) 기반으로 전환**
- 서비스 요구사항을 기반으로 **PostgreSQL DB 스키마 직접 설계**
- Supabase 프로젝트 생성부터 **Database · Auth · Storage 환경 구성**
- Android 앱의 기존 Firebase 데이터 처리 로직을 **Supabase 기반으로 전환**
- Supabase와 Android 앱 간 **데이터 저장·조회·수정 로직 구현**

### 2. SNS 로그인 및 인증 시스템 개발

- **Google · Kakao · Naver SNS 로그인 기능 연동**
- Supabase Auth를 기반으로 SNS 인증 결과를 **서비스 사용자 인증 체계와 연동**
- 로그인 상태 유지를 위한 **인증 토큰 및 세션 관리 로직 구현**
- 인증 상태에 따른 **Android 화면 및 사용자 흐름 처리**

### 3. 생체 인식 인증 기능 개발

- Android **Biometric API를 활용한 지문·얼굴 인식 기능 구현**
- 로그인된 사용자가 생체 인식을 통해 앱에 접근할 수 있는 **간편 인증 기능 개발**
- 생체 인증 성공·실패 및 사용 가능 여부에 따른 **인증 상태 처리**
- 꿈 기록 등 사용자 데이터 접근 전 **추가 인증 절차 구현**

---

## 🖼 스크린샷

<p align="center">
  <img src="https://github.com/chani01/portfolio_info/blob/main/images/bechoom/bechoom_login.png" width="100%">
</p>

---

## 📊 역할
- **Android · Backend 단독 개발**
- MVVM · Clean Architecture 기반 **Android 앱 개발**
- Firebase → Supabase **백엔드 마이그레이션**
- PostgreSQL **DB 스키마 설계 및 Supabase 백엔드 환경 구축**
- Supabase Auth 기반 **SNS 인증 및 세션 관리 구현**
- Android Biometric API 기반 **생체 인증 기능 개발**
- 인증 및 백엔드 전환 관련 **기능 정의·설계 참여**
