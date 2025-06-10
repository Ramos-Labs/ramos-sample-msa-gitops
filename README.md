# Ramos Sample MSA GitOps
- 라모스의 MSA Demo Application에 대한 GitOps root directory
- 각 서비스별 GitOps, Tekton Pipeline이 구성됨.
  - Service Discovery
  - Gateway
  - Book Service
  - Author Service
  - Review Service
  - Book Client (Frontend)
- CONE-Chain(NHN Native Deck)을 활용한 CI/CD 예제 코드를 직접 개발 및 구성함.
  - Common Cluster의 초기 작업용 구성은 이 Repository에서 제외함.
  - 주 목적은 OpenTelemetry 수집을 위한 샘플용 MSA 예제 코드를 개발하고 GitOps 기반으로 CI/CD 배포.
- Ingress Controller로 외부 요청 수신 → Gateway Server로 전달.
- 각 서비스는 PVC/PV로 구성된 스토리지를 사용하고 OpenTelemetry 수집을 위해 Kustomization에서 각 마이크로서비스의 Deployment에 JVM Option으로 에이전트를 추가하도록 patch하여 배포함.
- Frontend의 경우, Build 결과로 나타나는 정적 파일 경로를 nginx 컨테이너의 정적 리소스 경로로 구성하여 배포. 
- author: HakHyeon Song
- 2025.04 ~ 2025.05

![Image](https://github.com/user-attachments/assets/9e3c062f-501d-4411-97da-6d02e2688b92)

![Image](https://github.com/user-attachments/assets/23bdc0cd-4187-4117-8ac4-54bad8b73fee)

![Image](https://github.com/user-attachments/assets/3bd6404b-bc93-4f48-b069-755bdd122d85)
