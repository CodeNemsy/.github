# COAI

> 개발자의 성장을 돕는 AI 페어 프로그래밍 파트너

COAI는 **AI 기반 코드 분석**, **알고리즘 문제 생성 및 풀이**, **실시간 코딩 배틀**, **커뮤니티**, **결제/포인트 시스템**을 통합한 개발자 학습 플랫폼입니다. 단순한 정답 채점이 아닌, 코드 품질과 성장에 집중합니다.

---

## 주요 기능

*  **AI 코드 품질 분석**
   가독성, 설계 원칙(SRP, DRY, KISS), 보안, 성능까지 종합 분석

* **AI 알고리즘 문제 생성**
  난이도 × 알고리즘 유형 × 스토리 테마 기반 실시간 문제 생성

* **알고리즘 문제 풀이**
  기본 모드 / 집중 모드 제공, 실시간 채점 및 AI 피드백

* **1vs1 실시간 코딩 배틀**
  Redis + WebSocket 기반 저지연 대결 시스템

* **집중 모드**
  시선 추적 기반 집중도 모니터링 및 위반 패널티 적용

* **커뮤니티**
  자유게시판 / 코드게시판 분리 운영, 확장 가능한 태그 시스템

* **결제 · 포인트 시스템**
  Toss Payments 기반 결제 / 환불 / 구독 관리

* **GitHub 연동**
  코드 불러오기 및 AI 피드백 자동 커밋

---

## 핵심 도메인

* 유저 및 권한 관리
* 알고리즘 문제 도메인
* AI 코드 분석 도메인
* 포인트 및 결제 도메인
* 커뮤니티 도메인

> 총 **5개 핵심 도메인**, **33개 테이블**로 구성

---

## 기술 스택

### Frontend

* React
* Vite
* Tailwind CSS
* Monaco Editor
* WebSocket

### Backend

* Spring Boot
* Spring Security
* MyBatis
* Redis
* MySQL / PostgreSQL
* Spring WebFlux (비동기 처리)

### AI / Data

* OpenAI API
* RAG (Retrieval-Augmented Generation)
* Qdrant (Vector Database)
* Langfuse (LLM Observability)

### DevOps / Infra

* Docker / Docker Hub
* Jenkins (CI/CD)
* AWS EC2, RDS, S3
* Nginx

---

## AI 코드 분석 기준

* 가독성(Readability) 및 인지 부하
* KISS / SRP / DRY 원칙
* 매직 넘버 및 네이밍 규칙
* 예외 처리 및 보안 취약점
* 성능 및 리소스 효율성
* 테스트 용이성 및 문서화

> **LLM-as-a-Judge + Few-shot Prompting + RAG** 기반 분석으로
> 정확성 · 일관성 · 개인화된 피드백 제공

---

## 알고리즘 문제 생성 파이프라인

1. 문제 구조 검증
2. 기존 문제와 유사도 검사
3. 최적화 코드 실행 검증
4. 효율성 비교 검증

* 실시간 요청 시 Pool 조회 → **2초 내 문제 반환**
* 백그라운드 스케줄러를 통한 사전 생성 및 검증

---

## 1vs1 코딩 배틀

* Redis 권위 상태 관리로 실시간 동기화
* WebSocket 기반 게임 상태 전파
* 연결 끊김 발생 시 유예 처리
* 결과 및 이력은 DB에 영구 저장

---

## 결제 시스템

* Toss Payments 연동
* 서버 내부 검증 + Toss 외부 검증 **이중 방어**
* 멱등성 보장 상태 전이

    * READY → PROCESSING → DONE
* 환불 및 구독 취소 지원

---

## 보안 설계

* JWT + Redis 기반 인증
* GitHub OAuth 소셜 로그인
* SQL Injection 방어 (PreparedStatement)
* XSS 방어 (화이트리스트 + React 자동 Escape)

---

## CI / CD

1. GitHub Push
2. Jenkins 자동 빌드
3. Docker 이미지 생성
4. EC2 컨테이너 배포

* 서비스별 독립 컨테이너 운영
* 배포 실패 시 로그 기반 즉시 원인 파악

---

## 팀 구성

* **김가연** : 알고리즘 문제 생성 / 채점 / 레벨 시스템
* **방성일** : AI 코드 분석 파이프라인
* **김소희** : 커뮤니티 플랫폼 설계 및 구현
* **배지수** : 결제 / 포인트 / 1vs1 배틀
* **정현목** : 관리자 페이지 / 백엔드 배포
* **최민석** : 로그인 / OAuth / 회원가입 / 프론트 배포

---

## 향후 개선 계획

* GraphRAG 기반 개인화 분석 고도화
* 태그 자동 추천
* 대용량 트래픽 대응 (Auto Scaling)
* 실시간 알림 기능
* 쿼리 최적화 및 성능 테스트(nGrinder)

---

# COAI

> An AI Pair Programming Partner for Developer Growth

**COAI** is a developer learning platform that integrates **AI-powered code analysis**, **algorithm problem generation and solving**, **real-time coding battles**, **community features**, and a **payment & point system**.  
Rather than focusing solely on correct answers, COAI emphasizes **code quality and continuous growth**.

---

## Key Features

* **AI Code Quality Analysis**  
  Comprehensive analysis covering readability, design principles (SRP, DRY, KISS), security, and performance

* **AI Algorithm Problem Generation**  
  Real-time problem generation based on difficulty × algorithm type × story theme

* **Algorithm Problem Solving**  
  Normal mode / Focus mode, real-time judging, and AI-driven feedback

* **1vs1 Real-Time Coding Battles**  
  Low-latency competitive system powered by Redis + WebSocket

* **Focus Mode**  
  Gaze-tracking-based concentration monitoring with penalty enforcement

* **Community**  
  Separate free board and code board, with an extensible tag system

* **Payment & Point System**  
  Payment, refund, and subscription management powered by Toss Payments

* **GitHub Integration**  
  Import code and automatically commit AI feedback to repositories

---

## Core Domains

* User & authorization management  
* Algorithm problem domain  
* AI code analysis domain  
* Points & payment domain  
* Community domain  

> Composed of **5 core domains** and **33 database tables**

---

## Tech Stack

### Frontend

* React  
* Vite  
* Tailwind CSS  
* Monaco Editor  
* WebSocket  

### Backend

* Spring Boot  
* Spring Security  
* MyBatis  
* Redis  
* MySQL / PostgreSQL  
* Spring WebFlux (asynchronous processing)  

### AI / Data

* OpenAI API  
* RAG (Retrieval-Augmented Generation)  
* Qdrant (Vector Database)  
* Langfuse (LLM Observability)  

### DevOps / Infrastructure

* Docker / Docker Hub  
* Jenkins (CI/CD)  
* AWS EC2, RDS, S3  
* Nginx  

---

## AI Code Analysis Criteria

* Readability and cognitive load  
* KISS / SRP / DRY principles  
* Magic numbers and naming conventions  
* Exception handling and security vulnerabilities  
* Performance and resource efficiency  
* Testability and documentation  

> Powered by **LLM-as-a-Judge + Few-shot Prompting + RAG**  
> to deliver accurate, consistent, and personalized feedback

---

## Algorithm Problem Generation Pipeline

1. Problem structure validation  
2. Similarity check against existing problems  
3. Optimized code execution verification  
4. Efficiency comparison validation  

* Real-time requests return problems **within 2 seconds**
* Pre-generation and validation via background schedulers

---

## 1vs1 Coding Battles

* Redis-based authoritative state management for real-time synchronization  
* WebSocket-based game state broadcasting  
* Grace period handling for disconnections  
* Match results and history persistently stored in the database  

---

## Payment System

* Integrated with Toss Payments  
* Dual verification: internal server validation + external Toss verification  
* Idempotent state transitions  

  * READY → PROCESSING → DONE  

* Supports refunds and subscription cancellation  

---

## Security Design

* JWT + Redis-based authentication  
* GitHub OAuth social login  
* SQL Injection prevention (PreparedStatement)  
* XSS protection (whitelist + React automatic escaping)  

---

## CI / CD Pipeline

1. GitHub push  
2. Jenkins automated build  
3. Docker image creation  
4. EC2 container deployment  

* Independent containers per service  
* Immediate root-cause identification through logs on deployment failure  

---

## Team

* **Gayeon Kim** – Algorithm problem generation, judging, level system  
* **Seongil Bang** – AI code analysis pipeline  
* **Sohee Kim** – Community platform design and implementation  
* **Jisu Bae** – Payments, points, 1vs1 battle system  
* **Hyunmok Jung** – Admin panel, backend deployment  
* **Minseok Choi** – Login, OAuth, user registration, frontend deployment  

---

## Future Improvements

* Advanced personalized analysis using GraphRAG  
* Automatic tag recommendation  
* Large-scale traffic handling (Auto Scaling)  
* Real-time notification system  
* Query optimization and performance testing (nGrinder)  
