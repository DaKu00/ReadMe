# RAG 서비스 Ddabong

## 프로젝트 소개
[프로젝트에 대한 간단한 소개와 주요 기능을 작성해주세요]

이 프로젝트는 RAG(Retrieval-Augmented Generation) 기술을 활용한 Chat Bot 서비스입니다.
다양한 기술? 을 통해 압도적인 정확도와 실행시간을 가지고있음

[목업 이미지 넣을공간]

### 주요 기능
- 문서 검색 및 관련 정보 추출
- 컨텍스트 기반 응답 생성
- 로드밸런싱
- vLLM 호스팅
- 이것저것

## 기술 스택

## Backend

### 기술 스택
- **언어**: TypeScript  
- **프레임워크**: Nest.js  
- **데이터베이스**: MongoDB  

---

### 주요 기능

#### 1. 채팅 로그 관리  
사용자와 LLM 간의 대화 내용을 기록하여 추후 분석 및 개선에 활용할 수 있도록 관리합니다.  

#### 2. SSE 중계  
- **역할**: RAG 서버와 Front 서버 간 **Server-Sent Events(SSE)**를 활용한 실시간 데이터 중계.  
- **기능**: 임베딩 진행 상태 및 실시간 채팅 기능 지원.  

#### 3. AOP 기반 에러 및 로그 관리  
- **관점 지향 프로그래밍(AOP)**을 통해 로그 관리와 클라이언트 요청-응답 처리 로직을 효율화.  
- 주요 로그 및 에러 발생 시 중앙 집중적으로 관리하여 유지보수 용이성 향상.  

#### 4. API 키 관리 및 보안  
- **API 키 생성 및 암호화**:  
  - 사용자 API 요청 시, 헤더에 포함된 API 키를 **SHA-256**으로 암호화.  
  - 암호화된 키를 통해 사용자 식별 및 권한 관리.  
- **보안 강화**: API 키를 통한 불법적 접근 방지.  

#### 5. 블랙리스트 관리  
- **중복 요청 방지**:  
  - 동일 IP와 User Agent 정보를 기반으로 중복 요청 탐지.  
  - 반복적인 동일 요청 시, 사용자를 블랙리스트에 등록.  
- **제한 조치**: 블랙리스트에 등록된 사용자는 **1일간 서비스 이용 제한**.  
- **특징**: 회원가입 없이 사용자 정보를 최소한으로 활용하여 효율적 관리.  

#### 6. RAG API  
- **주요 역할**:  
  - RAG 관련 요청 관리(예: Embedding, Retriever, Vector Store 삭제 등).  
- **기능 통합**: 다양한 RAG 기능을 단일 API로 제공.  

#### 7. LLM 스트리밍 핸들러  
- **기능**:  
  - 단일 API를 통해 여러 LLM 모델에 요청 전송.  
  - 스트리밍 방식으로 응답 처리, 다중 모델 통합 관리 가능.  
- **효율성**: 다양한 LLM 서비스와의 유연한 연결 및 확장성 지원.  

---

### 추가 설명  
이 백엔드 모듈은 높은 확장성과 안정성을 고려하여 설계되었습니다.  
AOP, SSE, API 키 암호화 등 다양한 기술적 접근을 통해 보안성과 실시간성을 강화하였으며,  
RAG 서비스와의 원활한 통합을 목표로 최적화된 구조를 제공합니다.


### Frontend
- 프레임워크: React

### AI/ML
- LLM: [사용한 언어 모델]
- 벡터 데이터베이스: [벡터 DB]
- 임베딩 모델: [임베딩 모델명]

## 시스템 아키텍처
[시스템 아키텍처 다이어그램 또는 설명 추가]

### 요구사항
- [필요한 소프트웨어 및 버전]
- [시스템 요구사항]

## 성능 및 평가

### 성능 지표
- 응답 시간: [성능 지표]
- 정확도: [정확도 지표]
- 리소스 사용량: [리소스 사용 지표]


## 주요 기능 구현
[주요 기능들의 스크린샷 또는 설명]

## 기술적 의사 결정
[주요 기술 선택의 이유와 대안 분석]

## 성능 최적화
[성능 개선을 위해 적용한 기술과 결과]

## 배포
- on-premise GPU 서버 구축
- docker 통한 컨테이너 관리
- Front·Back·RAG 서버 https 배포
- middle ware : nginx 활용한 로드밸런싱
- multi GPU 분산처리

## 프로젝트 진행 중 해결한 문제
- 멀티스레드 문제 -> 로드밸런싱
- PDF 파싱
- 이미지 처리
- [기억나는대로 제가 적어봤는데 제대로 추가해주세요]

## 향후 개선 사항
- [개선이 필요한 부분]
- [추가하고 싶은 기능]
- [현재 한계점]
### Backend
- Monorepo 구조로 변경 후 분산처리
- 관리자용 통계 기능 


## 팀 구성 및 역할
[팀원 정보 및 역할]


## 문의
- Email: [이메일 주소]
- Issue: [이슈 트래커 링크]
