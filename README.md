# Project Overview

- Go-ZenaNet는 평화(고대 그리스 철학) 테마를 중심으로 설계된 PoS(Blockchain Proof-of-Stake) 기반 블록체인 네트워크입니다.
- 이 프로젝트는 Go 언어를 기반으로, go-ethereum을 포크하여 수정된 버전으로 개발됩니다.
- 추가적으로, ChatGPT API를 활용하여 스마트 계약 및 네트워크 내 다양한 애플리케이션의 생성을 자동화하는 기능을 제공합니다.

목표: 1. 사용자 친화적이고 효율적인 PoS 블록체인 구축. 2. 테스트넷 환경에서의 안정성 검증. 3. 스마트 계약 개발의 자동화를 통해 개발자의 접근성을 높임.

---

## Core Functionalities

### 1. 블록체인 코어

    -	go-ethereum 포크 및 커스터마이징:
    -	기존 Geth(go-ethereum) 소스 코드 포크.
    -	PoW(Proof-of-Work) 알고리즘 → PoS(Proof-of-Stake)로 전환.
    -	커스텀 합의 알고리즘 구현 (테마: 고대 그리스 평화와 조화).
    -	합의 알고리즘 명칭: “Eirene Consensus”.
    -	네트워크 명칭 및 구성:
    -	메인넷: Go-ZenaNet
    -	테스트넷: Eirene Testnet
    -	네트워크 ID, 체인 ID 설정 (포크 시 수정 필요).

### 2. 스마트 계약 자동 생성 시스템

    -	ChatGPT API 연동:
    -	사용자가 요구사항을 입력하면 자동으로 스마트 계약을 생성.
    -	ERC-20 토큰 계약 템플릿 생성.
    -	NFT 표준(ERC-721) 계약 생성.
    -	코드 생성 후 기본적인 보안 검토 및 배포 가이드 제공.
    -	예제 사용자 경험:
    -	사용자는 “ERC-20 토큰” 옵션 선택 후 토큰 이름, 심볼, 총 발행량 입력.
    -	AI가 자동으로 코드를 생성 및 테스트넷에 배포.

### 3. 지갑 및 노드 관리

    -	CLI 툴: 사용자 친화적 CLI를 통해:
    -	지갑 생성 및 관리.
    -	스테이킹 기능 활성화.
    -	트랜잭션 전송 및 조회.
    -	노드 운영: 경량 및 풀 노드 설정 지원.

---

## 3. Documentation

- 사용자 가이드 (Documentation Outline):
  1.  네트워크 설정 가이드:
  - go-ethereum 포크 코드 컴파일 및 설치 방법.
  - 네트워크 ID 및 구성 요소 세부 설정.
  2.  PoS 합의 알고리즘 설명:
  - “Eirene Consensus” 개요.
  - 스테이킹 및 블록 보상 메커니즘.
  3.  ChatGPT 기반 스마트 계약 생성 사용법:
  - API 키 설정.
  - 스마트 계약 자동 생성 워크플로우.
  4.  테스트넷 연결 가이드:
  - 테스트 지갑 생성 및 토큰 수령.
  - 샘플 스마트 계약 배포 연습.

---

## 4. File Structure

```bash
/go-zenanet
│
├── /cmd
│   └── geth/           # Geth 실행 파일 및 CLI 명령어
│
├── /consensus
│   └── eirene/         # PoS 합의 알고리즘 코드
│
├── /contracts
│   └── templates/      # 스마트 계약 템플릿 (ERC-20, ERC-721 등)
│
├── /docs
│   └── guides/         # 사용자 및 개발자 가이드 문서
│
├── /tests
│   └── network/        # 테스트넷 시뮬레이션 및 PoS 테스트
│
└── /api
    └── chatgpt/        # ChatGPT API 연동 코드
```

---

## 5. Additional Requirements

- 기술 스택

  - 언어: Go
  - 블록체인 포크: go-ethereum
  - AI 연동: OpenAI ChatGPT API
  - 컨테이너화: Docker로 노드 배포 및 테스트 지원.

- 디자인 및 명칭 가이드라인
  - 테마: 평화, 고대 그리스 문화.
  - 키워드 예시:
  - 스마트 계약 생성기: Sophia (지혜).
  - 스테이킹 노드 이름: Aegis Node.
  - 테스트넷 토큰 이름: Eirene Token (ERT).
