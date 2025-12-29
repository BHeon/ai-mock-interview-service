# AI 기반 모의면접 웹 서비스 (Final Project)

취업 준비 과정에서 반복되는 면접 연습의 비효율성을 개선하기 위해  
**AI를 활용한 모의면접 · 면접 분석 · PDF 리포트 제공 웹 서비스**를 개발했습니다.

사용자는 실제 면접과 유사한 흐름으로 질문과 답변을 주고받으며 면접을 진행할 수 있고,  
면접 종료 후에는 AI 분석 결과를 확인하고 이를 PDF 리포트로 저장할 수 있습니다.

---

## 🔹 프로젝트 개요

- 형태: 팀 프로젝트
- 기간: 2025.11.18 ~ 2025.12.23 (6주)
- 주제: AI 기반 모의면접 및 면접 분석 웹 서비스

---

## 🔹 주요 기능

- AI 모의면접 진행 (질문 / 답변 반복)
- 면접 종료 후 AI 분석 결과 제공
  - 점수
  - 강점 / 약점
  - 종합 피드백
- 면접 분석 결과 PDF 리포트 생성 및 다운로드
- JWT 기반 로그인 / 인증
- 사용자 다크모드 지원
- 마이페이지 (면접 기록 / 문의 / 방명록)

---

## 🔹 시스템 흐름 요약

1. 사용자가 면접을 시작하면 면접 세션 생성
2. 질문과 답변을 반복하며 면접 진행
3. 면접 종료 시 질문/답변 데이터 DB 저장
4. GPT API를 호출하여 면접 분석 수행
5. 분석 결과 DB 저장
6. 분석 결과 화면 출력
7. 분석 데이터를 기반으로 PDF 리포트 생성
8. PDF 파일 다운로드

---

## 🔹 기술 스택

### Backend
- Java 17
- Spring Boot
- Spring Security
- JWT
- MyBatis
- MySQL

### Frontend
- React (JSX)
- React Router
- Axios
- Zustand
- MUI
- Tailwind CSS
- lucide-react

### Infra / DevOps
- AWS EC2 (Ubuntu)
- Docker
- Nginx
- GitHub Actions

### AI / API
- OpenAI GPT API
- Spring AI API
- PDFBox / jsPDF

---

## 🔹 담당 역할

- 면접 분석 기능 전체 구현
- GPT 분석 결과 파싱 및 검증 로직 설계
- 면접 분석 결과 조회 기능 구현
- PDF 리포트 생성 및 다운로드 기능 구현
- 공용 컴포넌트(Header / Footer / 다크모드) 구현

---

## 🔹 프로젝트 구조
.
├── backend
│ └── Spring Boot 기반 서버
├── frontend
│ └── React 기반 클라이언트
└── docs
├── flowchart
├── erd
└── ppt


---

## 🔹 실행 방법

### Backend
```bash
./gradlew bootRun

### Frontend
npm install
npm star

---

## 🔹 회고

본 프로젝트를 통해
단순히 기능을 구현하는 것을 넘어,
AI 기능을 실제 서비스 로직에 자연스럽게 녹여내는 구조를 설계하는 경험을 할 수 있었습니다.

특히 GPT API를 단순 호출이 아닌
분석 도메인에 맞게 파싱하고 검증하여 재사용 가능한 분석 데이터로 저장하는 과정에서
서비스 관점의 설계 중요성을 체감했습니다.
