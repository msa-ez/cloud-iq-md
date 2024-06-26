## 애플리케이션 아키텍처 수준: Level 1.모노리식(Monolithic)

### 전환 원칙
- **모노리식 아키텍처**: 모든 기능이 하나의 애플리케이션 내에 통합되어 있습니다.
- **기능적 통합**: 시스템 내 다양한 기능들이 긴밀하게 연결되어 있으며, 하나의 기능 변경이 전체 시스템에 영향을 미칩니다.
- **개발 및 배포의 단순성**: 전체 애플리케이션을 하나의 단위로 개발하고 배포하는 것이 특징입니다.

### 전환 절차
#### **전환 평가(Assess)**
- 현재 모노리식 애플리케이션의 구조, 기능, 성능 지표를 분석합니다.
- 클라우드 네이티브 전환을 위한 주요 후보 기능 및 서비스를 식별합니다.
- 전환의 타당성, 비용, 기대 효과를 포함한 종합적인 평가 보고서를 작성합니다.

> **요약 :** 전환 평가 단계는 전환 프로젝트의 기초를 마련합니다. 현재 시스템을 깊이 있게 분석하고, 클라우드 네이티브로 전환하기에 적합한 부분을 식별하여, 전환의 전반적인 방향성과 범위를 결정합니다.

#### **마이그레이션 준비**
- 클라우드 환경에 맞는 인프라 및 기술 스택을 선택합니다.
- 전환 작업을 위한 팀 구성과 역할 분담을 확립합니다.
- 필요한 교육 및 도구 선택을 포함하여 전환 준비를 위한 전략을 세웁니다.

> **요약 :** 마이그레이션 준비 단계에서는 클라우드 전환을 위한 기술적, 조직적 기반을 마련합니다. 이 단계는 성공적인 클라우드 네이티브 전환을 위해 필수적인 과정으로, 적절한 인프라 및 기술 스택의 선택, 전문가 팀 구성, 그리고 필요한 교육 및 도구의 선택을 포함합니다.

#### **전환 계획(Plan) 수립**
- 전환할 애플리케이션의 구성요소와 서비스를 세분화하여 전환 계획을 수립합니다.
- 리스크 관리 계획 및 비상 대응 전략을 마련합니다.
- 프로젝트 일정, 마일스톤, KPIs를 정의합니다.

> **요약 :** 전환 계획 단계에서는 구체적인 실행 계획을 수립합니다. 이 단계는 프로젝트의 성공적인 수행을 위한 로드맵을 제공하며, 각 팀의 역할과 책임, 일정 관리, 리스크 관리 전략 등을 포함합니다.

#### **전환 설계(Design)**
- 마이크로서비스 아키텍처를 도입하여 시스템을 재설계합니다. 이 과정에서 각 서비스의 경계를 정의하고, 서비스 간의 의존성을 최소화합니다.
- 데이터 마이그레이션 전략을 수립하고, 필요한 경우 데이터의 분할 및 분산 방식을 결정합니다.
- 보안, 로드 밸런싱, 서비스 디스커버리 등 클라우드 네이티브 환경에서 필요한 인프라 요소를 설계합니다.

> **요약 :** 전환 설계 단계에서는 클라우드 네이티브 아키텍처로의 전환을 위한 세부 설계 작업을 수행합니다. 이 단계는 시스템의 재설계, 데이터 마이그레이션 계획, 그리고 클라우드 인프라의 구성 요소 설계를 포함합니다. 목표는 확장성, 유지보수성, 보안성을 갖춘 시스템 구조를 구축하는 것입니다.

#### **마이그레이션(Migration)**
- 실제로 애플리케이션과 데이터를 클라우드로 이전합니다. 이 과정에서 앞서 수립한 데이터 마이그레이션 전략을 따릅니다.
- 마이그레이션 이후 시스템 통합 테스트를 실시하여, 모든 서비스가 정상적으로 작동하는지 확인합니다.
- 사용자와의 피드백을 바탕으로 필요한 조정 작업을 수행합니다.

> **요약 :** 마이그레이션 단계에서는 설계된 아키텍처와 계획에 따라 실제 클라우드로의 전환 작업을 실행합니다. 이 단계는 애플리케이션 및 데이터의 이전, 시스템 통합 테스트, 그리고 초기 운영에 필요한 조정을 포함합니다. 목표는 전환된 시스템의 안정성과 성능을 검증하는 것입니다.

#### **전환 후 운영 최적화(Operate Optimize)**
- 클라우드 환경에서의 모니터링 및 로깅 시스템을 구축합니다. 이를 통해 시스템의 성능을 지속적으로 모니터링하고, 잠재적 문제를 조기에 발견할 수 있습니다.
- 자동화 도구를 활용하여 배포, 스케일링, 장애 복구 과정을 최적화합니다.
- 클라우드 리소스 사용량을 정기적으로 분석하고, 비용 효율성을 개선하기 위한 조치를 취합니다.

> **요약 :** 전환 후 운영 최적화 단계에서는 클라우드 네이티브 환경에서의 지속적인 운영과 관리를 위한 최적화 작업을 수행합니다. 이 단계는 시스템 모니터링, 자동화, 그리고 비용 관리를 포함합니다. 목표는 시스템의 안정적인 운영과 비용 효율성의 지속적인 개선입니다.

### References:
- 이벤트스토밍, 서비스 디컴포지션 (Service Decomposition) : <a href="https://www.msaschool.io/operation/design/design-three/" target="_blank"> https://www.msaschool.io/operation/design/design-three/</a>
- 이벤트스토밍 HowTo : <a href="https://intro-kor.msaez.io/business/" target="_blank">https://intro-kor.msaez.io/business/</a>
- 애플리케이션 아키텍처 설계 : <a href="https://www.msaschool.io/operation/design/design-five/" target="_blank">https://www.msaschool.io/operation/design/design-five/</a>
- 프론트-엔드 설계 : <a href="https://www.msaschool.io/operation/design/design-eight/" target="_blank">https://www.msaschool.io/operation/design/design-eight/</a>
- 게이트웨이(Gateway)를 통한 애플리케이션 창구 단일화 : <a href="https://www.msaschool.io/operation/implementation/implementation-six/" target="_blank">https://www.msaschool.io/operation/implementation/implementation-six/</a>
- 이벤트기반 메시지 채널, 카프카(Kafka) 활용 : <a href="https://www.msaschool.io/operation/implementation/implementation-seven/" target="_blank">https://www.msaschool.io/operation/implementation/implementation-seven/</a>
- MSA 성숙도 모델에 따른 구현 관점별 적용 레벨 : <a href="https://www.msaschool.io/operation/planning/planning/" target="_blank">https://www.msaschool.io/operation/planning/planning/</a>