# 통합 분석 환경 플랫폼 상세 설계
## 실증구성도
![image](./architecture.jpg)
## 프라이버시 보장 헬스케어 서비스
* 서비스에 필요한 데이터를 암호화된 형태로 제공하며, 필요 시 소유자가 데이터를 복호화하여 확인 할 수 있는 서비스
## 동형암호 및 블록체인 키 관리 엔진
* 브라우저 익스텐션 형태의 어플리케이션을 활용하여 동형암호와 블록체인에 사용되는 키들을 관리하는 부분
* 동형암호 관련 기능과 블록체인 관련 기능이 들어있는 [ain-js](https://github.com/ainblockchain/ain-js) 라이브러리를 통해 구현
* 프라이버시 보장 헬스케어 서비스에서 해당 엔진을 통해 데이터를 암호화/복호화 하고, 블록체인에 암호화된 값을 쓰게 된다.
### APIs
#### Blockchain
* `sendTransaction(ref: string, value: any, nonce?: integer, parentTxHash?)`
  * Blockchain의 `ref` 경로에 `value` 값을 쓰기 위한 transaction을 생성하고 전송하는 함수
* `getPublicKey()`
  * Blockchain에 대한 public key를 받아오는 함수
#### Homomorphic Encryption
* `encryptData(data: Float64Array)`
  * Float64Array 형태로 표현된 데이터를 HE 기반의 base64 string 형태로 암호화하는 API
* `decryptData(data: string)`
  * Base64 string 형태로 표현된 암호화된 데이터를 복호화하는 API
* `getHEPublicKey()`
  * Homomorphic Encryption에 사용되는 public key를 받아오는 함수
## 이벤트 기반 실시간 블록체인 노드
* 암호화된 데이터 관리 및 접근 제어를 수행하며, 필요에 따라 이벤트 기반으로 동형암호 연산 작업을 워커에게 할당하는 역할
## 프라이버시 보장 데이터 분석 워커
* 암호화된 데이터를 기반으로 할당받은 작업을 수행하여 필요한 암호화된 결과를 다시 블록체인에 제공하는 역할
### HE Job Listener
* 워커의 AI Network Blockchain address 기반으로 job queue 경로가 정해지며, 해당 경로에 값이 적히는 event를 통해 자신에게 job이 할당되었음을 인지할 수 있다.
  * Job queue 경로 : `/apps/....`
