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

### Backend
- 언어: TypeScript
- 프레임워크: Nest.js
- 데이터베이스: Mongo DB
- 주요 기능: 
            1) 채팅 로그 관리: 사용자가 LLM과 소통시 주고 받은 대화의 로그 기록
            2) sse 중계: RAG 서버와 Front 서버를 Server Sent Event로 중계하여 임베딩 진척사항 및 실시간 채팅 구현
            3) AOP 기반 에러 코드 및 로그 관리: 관점지향을 통해 로그관리와 Client단 요청-응답 관리
            4) API key 생성 및 sha256암호화 진행: 사용자의 API 요청 header에 API 암호화된 key를 확인하고 암호화된 key를 통해 사용자 정보를 파악
            5) 블랙 리스트 관리: 동 접속자가 반복적으로 같은 요청을 할시 블랙리스트에 올려 1일간 사용금지 조치
            -> 회원가입 통한 회원 정보 없이 사용자의 IP와 user agent 정보 통한 중복 처리 알고리즘 개발   
            6) RAG API : Embeding, Retriever, Vector Store delete 등 RAG 관련 요청 관리
            7) LLM streaming Handler: 하나의 API로 여러 LLM에 요청을 보내고 스트리밍으로 응답 (LLM 통합관리)  

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
