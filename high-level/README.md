# P2P 클라우드 컴퓨팅 플랫폼 설계

## 전체 목표 시스템
![image](./target_system.jpg)

## P2P 클라우드 컴퓨팅 플랫폼 설계 (상위 기획서)
* 문서 주소: [https://ainetwork.ai/public/architecture.pdf](https://ainetwork.ai/public/architecture.pdf)
* 내용:
  * 딥 컴퓨팅 아키텍처 (Deep computing architecture)
  * 보안 런타임 환경 (Secure runtime environment)
  * 빅스토리지 (Big storage)
  * AIN 블록체인 프로토콜 (AIN blockchain protocol)
  * AIN 프로토콜 상에서의 기계학습 패턴 (Machine learning patterns on AIN protocol)
  * 보안 설계 (security) 

## 암호화 키 기반 클라우드 접속 플랫폼 상세 설계
* 문서 주소: [https://github.com/ainblockchain/ain-js/blob/master/src/he/README.md](https://github.com/ainblockchain/ain-js/blob/master/src/he/README.md)
* 내용:
  * 클라우드 접속에 사용되는 암호화 키를 기반으로한 라이브러리 설계 및 사용법 포함
  * 동형암호 사용법에는 동형암호 키 생성 방법, 초기화 방법, 암복호화 실행 방법, 동형암호 연산 실행 방법 등 포함
  * 클라우드 접속 및 암호화 키 기반 연산 방법 예시 포함

## 블록체인 프로토콜 상세 설계
* 문서 주소: [https://docs.ainetwork.ai](https://docs.ainetwork.ai)
* 내용:
  * 블록체인 APIs:
    * 블록체인에 트랜젝션을 보내고 트랜젝션의 상태를 확인하기 위한 API
    * 블록체인의 블록들의 내용을 확인하기 위한 API
    * 블록체인의 상태 DB의 내용을 확인하기 위한 API
    * 블록체인 상의 계정 정보를 확인하기 위한 API
    * 블록체인 네트워크의 상태를 확인하기 위한 API
    * 블록체인에 대한 디버깅을 수행하기 위한 API
  * 블록체인 SDK:
    * 블록체인에 트랜젝션을 보내고 트랜젝션의 상태를 확인하기 위한 SDK 상세 설계 
    * 블록체인의 블록들의 내용을 확인하기 위한 SDK 상세 설계
    * 블록체인의 검증노드들의 상태를 확인하기 위한 SDK 상세 설계
    * 블록체인의 상태 DB의 내용을 확인하기 위한 SDK 상세 설계
    * 블록체인 동형암호 암호화/복호화를 수행하기 위한 SDK 상세 설계
    * 블록체인 네트워크의 상태를 확인하기 위한 SDK 상세 설계
    * 블록체인에 전자지갑(crypto wallet)의 기능을 수행하기 위한 SDK 상세 설계

## 통합 분석 환경 플랫폼 상세 설계
* 문서 주소: [https://github.com/ainblockchain/he-healthcare-docs/blob/master/integration/README.md](https://github.com/ainblockchain/he-healthcare-docs/blob/master/integration/README.md)
* 내용:
  * 프라이버시 보장 헬스케어 서비스
  * 동형암호 및 블록체인 키 관리 엔진
  * 블록체인 APIs
  * 동형암호 APIs
  * 이벤트 기반 실시간 블록체인 노드
  * 프라이버시 보장 데이터 분석 워커
  * HE Job Listener