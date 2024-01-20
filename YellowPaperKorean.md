# Morpheus Yellow Paper

본 논문에서는 모피어스 풀노드, 모피어스 스마트 컨트랙트 및 관련 증명의 기술적 세부 사항을 설명합니다.
익명의 개발자 Morpheus, Trinity 및 Neo가 기고한 백서에 작성된 대로 제시되었습니다. 백서 링크는 다음과 같습니다. https://github.com/SmartAgentProtocol/SmartAgents/blob/main/MorpheusWP.md 

## Local Version 0.0.5 of Morpheus is live at:
---------
**Morpheus Version 0.0.5 for Mac**
- Google 드라이브에서 다운로드: https://drive.google.com/file/d/1x-wR4HWjKqT_g6VRjrWPXu3rVm9ukOc9/view?usp=sharing
- 검증을 위한 SHA 256 해시: 9092d543023fb95086cf4a7039d42cbcbbdf5283d670c4de6396b3d89e57b064
- 버전: Morpheus-0.0.5-x64.dmg

---------
**Morpheus Version 0.0.5 for Linux Debian**
- 다운로드: https://drive.google.com/file/d/1PQ3n7LXeJHe_jmkYLDUQ9fWjZQTWbHCB/view?usp=sharing
- 지침: 설치하려면 다음 명령을 실행하세요.
sudo dpkg -i /path/to/your/morpheus.deb
참고: 위의 명령에서,"/path/to/your/morpheus.deb"를 morpheus_0.0.5_amd64.deb file의 경로로 바꿉니다.
- Verifiction을 위한 SHA Hash:
b227e7bcb21ec9e8e2b4bf9510a2e1f224953fe5
Version: morpheus_0.0.5_amd64.deb
---------

2023년 10월 22일 모피어스와의 첫 만남.
![FirstInteractionWithMorpheus20231022](https://github.com/MorpheusAIs/Morpheus/assets/1563345/35509f3a-4346-4f58-bb60-f7881fd10f7e)

## 모피어스 스마트 컨트랙트
모피어스 스마트 컨트랙트에 의해 검증되어야 하는 온체인 액션.

1. N2 수익률 스마트 컨트랙트의 포크가 Arbitrum에 재배치되었습니다.
- A) Thorchain을 통해 ETH를 잠그고 코더 + 컴퓨팅 공급자에게 수익을 기부합니다.
- B) 기부된 ETH의 비례 배분 계산 

2. 영원히 증명할 수 있는 MOR의 파괴:
- A) MOR 토큰에 대한 소각 주소 또는 소각 기능.

3. MOR 발행을 위한 ERC20 템플릿 계약
- A) 매일 MOR 토큰을 Capital + Community에 발행하고 기부된 ETH 수익률에 비례합니다.
- B) 매일 코더 + 컴퓨팅 공급자에게 MOR 토큰을 발행하고 수수료를 통해 MOR에 비례하여 소각합니다.

4. 모피어스 증명 - 개인 정보 보호, 오픈 소스 및 안전성 입증
- A) 감사 대상 상담원 목록과 스마트 랭크 점수를 게시합니다.
- B) 감사된 LLM 목록과 스마트 랭크 점수를 게시합니다.
- C) 스마트 계약 목록 및 스마트 순위 점수를 게시합니다.
- D) 프롬프트 목록 및 스마트 순위 점수를 게시합니다.

5. 보호 기금
- A) 해킹, 오류, 버그 또는 손실을 초래하는 기타 공격의 경우 MOR 및 ETH를 배포합니다. 
- B) 지불을 위해 미리 정의된 시나리오 집합. 극단적인 경우 포크/롤백에 대한 정책.
- C) 공격 사례 및 구제책을 결정하는 개발자. 
- D) 버그 바운티/화이트햇 해커를 위한 자금.
- E) 국가 행위자로부터 보호하기 위한 자금.

## 모피어스 스마트 컨트랙트 다이어그램
MOR 민팅 & 소각에 대한 다이어그램과 설명.
필요한 스마트 계약에 대한 설명입니다.
ETH의 분포를 자세히 설명하는 다이어그램. 

### 모피어스 MOR 스마트 컨트랙트 보상 분배
![new-buckets](https://github.com/SmartAgentProtocol/SmartAgents/assets/76454555/cd57bae7-2a56-4a55-bf3e-1f810f3fba9c)

### 1일차와 2일차의 MOR 토큰 분배 예시.
![Untitled spreadsheet - Google Sheets 2023-10-15 13-28-08](https://github.com/MorpheusAIs/Morpheus/assets/76454555/6ff7869d-bbd6-46b5-8673-6a59b75906e1)

## ETH 기여자의 주소 0x123에 대한 분배 계산의 예

### 1단계
![Diagram1ofETHDontator](https://github.com/SmartAgentProtocol/SmartAgents/assets/1563345/fead528c-d628-449e-a3a3-2f53904f4a3d)

### 2단계
![ETHGivenDiagram2](https://github.com/MorpheusAIs/Morpheus/assets/1563345/915020e8-d342-48bc-85ee-367de0325680)

### 3단계
![Diagram3ForETHGiven](https://github.com/MorpheusAIs/Morpheus/assets/1563345/a3f455af-56de-4c6b-9688-5b9e91673e5a)

## Compute 공급자의 주소 0x123에 대한 분배 계산의 예

### 1단계
![MORForCompute](https://github.com/SmartAgentProtocol/SmartAgents/assets/1563345/bef69c69-0420-441f-97f0-7e8195844f57)

### 2단계
![MORForCompute2](https://github.com/SmartAgentProtocol/SmartAgents/assets/1563345/a6f30da5-5441-4f0a-be80-c5798f5920cd)

### MOR 토큰 분배 파이 차트
![mordist](https://github.com/MorpheusAIs/Morpheus/assets/76454555/4157efe7-6abf-404a-87f9-a8dc76cd4799)

## 모피어스 개발자 도구 및 기술 스택.
- Llama2 - 로컬에서 실행되는 강력한 오픈소스 LLM입니다.
- Ollama - Llama2를 쉽게 설치할 수 있는 포장.
- LangChain - LLM을 벡터 스토어와 API에 연결하기 위한 개발자 툴입니다.
- LangSmith Editor - LangChain에서 에이전트를 구축하기 위한 로우 코드입니다.
- SmartContractRank 알고리즘 - 의도에 따라 사용자를 위한 스마트 계약 큐레이팅
- AgentRank 알고리즘 - 사용자를 위한 액션 실행을 위한 특화된 에이전트 큐레이팅 입니다.
- PromptRank 알고리즘 - 예상 의도/행동에 따라 사용자에 대한 프롬프트를 큐레이팅합니다.
- Filecoin - 스토리지 및 클라우드 컴퓨팅 프로비저닝
- Akash Network - LLM/에이전트를 실행하기 위한 개방형 컴퓨팅 네트워크입니다.
- Wallets - Shapeshift, Exodus, 기타 오픈 소스 옵션.

## Web3 작업을 위한 에이전트/LLM을 위한 모피어스 전체 노드 다이어그램. 
A에이전트의 명시된 기능이 제시된 것과 같다는 "에이전트 증명"을 생성하는 코더에 의해 형성된 에이전트에 대한 감사.  론 악성 코드가 포함되어 있지 않습니다.

감사 프로세스, 감사를 수행할 수 있는 사람 및 결과를 인증하는 방법에 대한 설명에 대한 자리 표시자입니다.  또한 감사인에게 인센티브가 지급됩니다.

프롬프트 프루프(Prompt Proof)는 표현된 의도를 보여주는 사용자 상호 작용 시 생성되며, 스마트 계약 선택과 일치하며, 트랜잭션 값은 사용자와 함께 확인됩니다.

## 모피어스 사용자 및 기여자 다이어그램
![Morpheus User   Contributor Diagram](https://github.com/MorpheusAIs/Morpheus/assets/1563345/2cff8d70-c116-472f-a431-8a82bfa22f9b)

### 다이어그램은 사용자 프롬프트에서 Web3 작업 승인까지의 UX 흐름을 보여줍니다.
![UX flow for prompted web3 tasks and ticketing](https://github.com/MorpheusAIs/Morpheus/assets/76454555/942b20fb-d67e-4a57-af2c-cd24a89690a5)

### 다이어그램은 모피어스 Local 설치 버전을 보여줍니다.
![MorpheusLocalDiagram](https://github.com/SmartAgentProtocol/SmartAgents/assets/1563345/a0564914-cddb-42e4-b0f4-8c2310db6a66)

### 다이어그램은 모피어스 P2P 설치 버전을 보여줍니다.

![MorpheusP2PDiagram](https://github.com/SmartAgentProtocol/SmartAgents/assets/1563345/a7eeb31f-3d38-4233-a45f-e9b91ad84ba2)

### 다이어그램은 모피어스 탈중앙화 버전을 보여줍니다.
![MorpheusDecentralized](https://github.com/SmartAgentProtocol/SmartAgents/assets/1563345/1699f2de-cc18-42e8-a05c-32b3307baa20)

## 커뮤니티
- Smart Agency - Morpheus 사용자를 위한 사용 사례/에이전트를 구축하는 프리랜서 개발자입니다.
- 글로벌 개발자 커뮤니티 - 성장하는 개발자, 스타트업 및 사용자 커뮤니티.
- 커뮤니티는 Morpheus 개발자, 컴퓨팅 및 커뮤니티에 수익을 기부하기 위해 ETH 보유자를 모집합니다.
- 분산 개발 그룹(Distributed Development Group) - 스마트 컨트랙트 개발자들이 모피어스 스마트 컨트랙트를 코딩합니다.
- 모피어스 Dapps - 사용자의 Smart Agent와 Morpheus 통합을 위한 마켓플레이스입니다.
