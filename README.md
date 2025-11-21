# ITC (Investment Training Crypto)
> **실시간 암호화폐 데이터 기반 모의투자 · 시뮬레이션 · 뉴스 분석 · 리포트 · RAG 챗봇**  
> Microsoft Data School 프로젝트

---

## Overview
ITC는 암호화폐 시장에 대한 높은 진입 장벽(난해한 개념, 빠른 시세 변동, 복잡한 지표)을 낮추기 위해 기획된 **종합 투자 트레이닝 플랫폼**이다.  
실시간 데이터와 과거 데이터를 모두 활용하여 **안전하게 학습하고 전략을 검증할 수 있는 환경**을 제공한다.

**구성 요소**
- 실시간 모의투자  
- 과거 데이터 시뮬레이션  
- 실시간 뉴스 수집 & 감정 분석  
- 투자 리포트 & RAG 챗봇  
- 암호화폐 백과사전  
- 고객 분석 대시보드(Fabric)  
- 온보딩 시스템 & Q&A  

---

## Objectives
- 실시간/과거 기반 모의투자로 **투자 전략 검증**
- AI 기반 지표·뉴스 분석으로 **판단 근거 제공**
- 개인 투자 패턴을 활용한 **맞춤형 리포트 생성**
- 투자 초보자도 쉽게 접근할 수 있도록 **교육 중심 구조 제공**
- 전체 프로세스를 클라우드 기반으로 구성한 **엔드투엔드 플랫폼 구축**

---

# 1. Main Services

## 1) 실시간 모의투자 (Real-Time Trading)
- Upbit API 기반 실시간 가격·거래량 반영  
- BTC / ETH / XRP 선택  
- 이동평균선 및 기본 보조지표 제공  
- 지정가/시장가 매매  
- 대기주문 & 체결내역 확인  
- 실시간 호가창  
- 튜토리얼·RAG 챗봇 연동

**동시성 제어**
- FOR UPDATE 기반 잠금  
- 트랜잭션 원자성 보장  
- 커넥션 풀 + 데드락 방지 구조

---

## 2) 과거 데이터 시뮬레이션
- 상승 / 하락 / 횡보 3개 시나리오 제공  
- 실제 과거 데이터를 일 단위로 재현  
- 뉴스 팝업 기반 의사결정  
- 보유 금액·총자산·수익률 실시간 계산  
- Node.js + MariaDB + Chart.js Financial 기반

---

## 3) 실시간 뉴스 수집 · 감정 분석
- Naver 검색 API 기반 자동 수집 (1시간 주기)  
- Azure OpenAI(GPT-5) 감정 분석(긍정/부정/중립)  
- Azure MySQL 저장  
- 비트코인/이더리움/리플/암호화폐 키워드 자동 처리

---

## 4) 투자 리포트 (Report)
- 실시간 자산 데이터 반영  
- 평가금액 · 손익 · 총자산 정리  
- **개인 데이터 기반 RAG 챗봇**  
- PDF 저장 기능 지원

---

## 5) 암호화폐 백과사전
- 검색 기반 용어 탐색  
- 차트 지표 설명  
- 초보자 중심 기초 개념 정리

---

## 6) 마이페이지
- 보유 코인/평가금액/손익 요약  
- 계정 설정(로그아웃, 탈퇴)  
- 리포트 및 Q&A 접근

---

# 2. Sub Services

## Q&A
- 질문 등록(공개/비공개 + 비밀번호 기능)  
- 댓글 작성 및 조회  
- MariaDB 저장 구조

---

## 온보딩 가이드
- 코인 마스코트 기반 하이라이트 안내  
- 페이지별 첫 방문자 튜토리얼  
- Azure Speech 기반 TTS 음성 안내

---

## RAG 기반 챗봇
- 실시간 모의투자/리포트 데이터 참조  
- OpenWebUI API Gateway 기반 LLM 자동 선택  
- 개인 상황 기반 맞춤형 응답

---

## 고객 데이터 대시보드 (Microsoft Fabric)
- Azure SQL → Fabric Dataflow → Lakehouse 적재  
- Fact Table 생성 및 분석  
- 지역별/연령별/선호코인/거래패턴 시각화  

---

# 3. Infra & Migration

## Keycloak 기반 인증
- Microsoft/Google 간편 로그인  
- MariaDB 회원 DB 저장  
- 이메일 인증 후 14일 뒤 계정 영구 삭제

---

## Azure Kubernetes Service (AKS)
- 지능형 부하분산  
- 자동 복구 및 무중단 운영  
- 확장성 + DevOps 배포 자동화

---

## Azure DevOps Pipeline
**배포 플로우**  
Git push  
→ 빌드  
→ ACR 이미지 Push  
→ Key Vault 시크릿 로딩  
→ AKS 자동 배포

- 무중단 업데이트  
- 강화된 보안 관리  

---

## Airbyte + CDC (데이터 동기화)
- 온프레미스 ↔ 클라우드 실시간 동기화  
- 서비스 중단 없이 점진적 이전 가능

---

# 4. 역할 (Backend / Infra / AI Engineering)

- 실시간 데이터 처리 구조 설계  
- 동시성 제어(트랜잭션/락) 설계  
- 과거 데이터 조회 API 개발  
- Azure Functions + OpenAI 감정 분석 파이프라인 구축  
- RAG 챗봇 설계 및 연동  
- AKS · ACR · Key Vault · DevOps 파이프라인 통합  
- MariaDB / SQL Schema 설계 및 최적화  
- Fabric 기반 분석 구조 일부 수행  

---

# 5. Tech Stack

### Backend
- Node.js (Express)  
- WebSocket  
- MariaDB / Azure MySQL  
- Azure OpenAI, Azure Functions  
- Keycloak  
- Airbyte CDC

### Frontend
- React  
- Chart.js Financial  
- WebSocket Client  
- Onboarding UI Engine

### Infra
- Azure Kubernetes Service  
- Azure DevOps  
- Azure Container Registry  
- Azure Key Vault  
- Cloudflare Load Balancer  
- Microsoft Fabric

---

# 6. 실행 방법

```bash
# Clone
git clone https://github.com/USER/ITC.git
cd ITC

# Install
npm install

# Backend Start
npm run start

# Frontend Start
npm run dev
