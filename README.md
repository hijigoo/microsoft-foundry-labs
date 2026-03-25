# Microsoft Foundry Hands-on Workshop

Microsoft Foundry의 핵심 기능을 실습을 통해 학습하는 워크샵입니다. 이 워크샵에서는 모델 배포, 에이전트 생성, 지식 기반 구축, 워크플로우 설계 등 Foundry의 주요 기능들을 단계별로 경험할 수 있습니다.

> 🌏 **Language / 언어**: [한국어 가이드](./README.md) | [English Guide](./portal-guide/en/README.md)

## 📓 실습 방식 선택

이 워크샵은 두 가지 실습 방식을 제공합니다:

### 1️⃣ 포털 기반 실습 ([portal-guide/](./portal-guide/))
- Microsoft Foundry Portal을 사용한 UI 기반 실습
- 코드 작성 없이 포털에서 직접 설정
- **시작하기**: [portal-guide/01-setup.md](./portal-guide/01-setup.md)

### 2️⃣ 코드 기반 실습 ([code-guide/](./code-guide/))
- Python 코드로 리소스 생성 및 관리
- 자동화 및 스크립트 작성에 유용
- **시작하기**: [code-guide/01-setup.ipynb](./code-guide/01-setup.ipynb)

> 💡 **권장**: 포털 실습으로 개념을 익힌 후, 코드 실습으로 자동화를 학습하세요!

## 📚 워크샵 개요

이 워크샵은 Microsoft Foundry의 새로운 포털을 사용하여 다음 내용을 다룹니다:

- **모델 관리**: 다양한 AI 모델의 배포 및 Model Router 구성
- **에이전트 개발**: File Search, Web Search, Code Interpreter 기반 에이전트 구축
- **Foundry IQ**: AI Search 및 Blob Storage 기반 지식 베이스 구축
- **워크플로우**: Sequential, Group Chat, Human-in-loop 워크플로우 설계
- **평가**: 에이전트 성능 평가 및 분석
- **관리**: Control Plane을 통한 운영 모니터링

## 🎯 사전 요구사항

### 필수 요구사항

- **Microsoft Entra ID 계정** (이전 Azure Active Directory)
- **Azure 구독** (활성화된 계정)
  - 구독에 대한 **소유자(Owner) 역할** 필요
  - 리소스 생성 및 역할 할당 권한 필요
- **GitHub 계정**
- Azure Portal 접근 권한
- 텍스트 에디터 또는 IDE (VS Code 권장)
- Python 3.8 이상 (코드 실행 실습용)

### 권장 사항

- **GitHub Codespaces 사용 권장** (브라우저에서 바로 실습 가능)
  - 별도의 개발 환경 설정 불필요
  - Python, Azure CLI 등이 사전 설치됨
  - 무료 사용 시간 제공 (월 120 코어 시간)
- Azure CLI 설치 (로컬 환경 사용 시)
- Git 설치 (로컬 환경 사용 시)
- 기본적인 Python 프로그래밍 지식
- REST API 및 JSON 기본 지식

## 📖 워크샵 구성

각 모듈은 독립적으로 실습 가능하도록 구성되어 있습니다:

### 01. 환경 설정
**[Portal Guide](./portal-guide/01-setup.md)** | **[Code Guide](./code-guide/01-setup.ipynb)**
- Resource Group 생성
- Foundry 리소스 생성
- New Foundry 포털 활성화

### 02. 모델 및 배포
**[Portal Guide](./portal-guide/02-models.md)** | **[Code Guide](./code-guide/02-models.ipynb)**
- 모델 리더보드 탐색
- 모델 비교 및 배포
- Model Router 구성

### 03. 에이전트 개발
**[Portal Guide](./portal-guide/03-agents.md)** | **[Code Guide](./code-guide/03-agents.ipynb)**
- ModelRouterAgent 생성
- FileSearchAgent 구축
- WebSearchAgent 구축
- CodeInterpreterAgent 구축
- 에이전트 배포 및 호출

### 04. Foundry IQ
**[Portal Guide](./portal-guide/04-foundry-iq.md)** | **[Code Guide](./code-guide/04-foundry-iq.ipynb)**
- Foundry IQ 개요
- AI Search 연결
- Knowledge Base 생성 (AI Search Index)
- Knowledge Base 생성 (Blob Storage)
- KnowledgeAgent 통합

### 05. 워크플로우
**[Portal Guide](./portal-guide/05-workflows.md)** | **[Code Guide](./code-guide/05-workflows.ipynb)**
- Sequential Workflow 구축
- Group Chat Workflow 구축
- Human-in-loop Workflow 구축

### 06. 평가
**[Portal Guide](./portal-guide/06-evaluations.md)** | **[Code Guide](./code-guide/06-evaluations.ipynb)**
- 에이전트 평가 설정
- 평가 기준 정의
- 평가 결과 분석

### 07. Control Plane
**[Portal Guide](./portal-guide/07-control-plane.md)** | **[Code Guide](./code-guide/07-control-plane.ipynb)**
- Fleet Overview 모니터링
- Assets 관리
- Compliance 및 보안
- Quota 관리
- Admin 기능

## 🚀 시작하기

### 포털 기반 실습
1. **환경 설정부터 시작하세요**: [portal-guide/01-setup.md](./portal-guide/01-setup.md)를 따라 Azure Portal에서 리소스를 생성합니다.
2. **순차적 학습 권장**: 각 모듈이 이전 모듈의 리소스를 활용하므로 순서대로 진행하세요.

### 코드 기반 실습 (Jupyter Notebook)
1. **환경 변수 설정**: 각 노트북 시작 부분의 `FOUNDRY_NAME`을 고유한 이름으로 변경하세요.
2. **Azure 인증**: Azure CLI를 사용하여 로그인 (`az login`)
3. **순차 실행**: [code-guide/01-setup.ipynb](./code-guide/01-setup.ipynb)부터 셀을 순서대로 실행하며 진행하세요.

> ⚠️ **중요**: 노트북 실습 시 반드시 `FOUNDRY_NAME`을 변경해야 합니다 (예: `foundry-myname`)

### 공통 사항
- **필요한 부분만 선택**: 특정 기능에 관심이 있다면 해당 섹션만 선택하여 실습할 수 있습니다.
- **리소스 정리**: 실습 후 불필요한 리소스는 삭제하여 비용을 절감하세요.

## 📚 참고 문서

- [Microsoft Foundry Documentation](https://ai.azure.com/docs)
- [What is Microsoft Foundry](https://ai.azure.com/docs/what-is-azure-ai-foundry)
- [Get Started with Code](https://ai.azure.com/docs/quickstarts/get-started-code)
- [Foundry Agent Service at Ignite 2025](https://techcommunity.microsoft.com/blog/azure-ai-foundry-blog/foundry-agent-service-at-ignite-2025-simple-to-build-powerful-to-deploy-trusted-/4469788)
- [Agents Overview](https://ai.azure.com/docs/agents/overview)

## 💡 팁

- 각 실습 후 리소스를 정리하여 비용을 절감하세요
- 에러 발생 시 Azure Portal의 Activity Log를 확인하세요
- 실습 중 생성된 코드는 저장하여 재사용하세요
- Control Plane에서 리소스 사용량을 주기적으로 확인하세요

## 🤝 기여

이 워크샵에 대한 피드백이나 개선 사항이 있다면 Issue를 생성해 주세요.

## 📝 라이선스

이 워크샵 자료는 교육 목적으로 제공됩니다.

---

**다음 단계**: [포털 가이드 시작하기](./portal-guide/01-setup.md) | [코드 가이드 시작하기](./code-guide/01-setup.ipynb)
