## 애플리케이션 아키텍처 수준 : Level 2.하이브리드(Monolith & Microservice)

### 전환 원칙
- **하이브리드 아키텍처**: 시스템은 모노리스와 마이크로서비스 기능이 혼합된 구조입니다.
- **서비스 분리의 시작**: 중요한 기능을 별도의 마이크로서비스로 분리합니다.
- **시스템 간 통신**: 모노리스와 마이크로서비스 간의 통신 구조를 관리합니다.

### 전환 절차
#### 전환 평가(Assess)
- 현재 시스템의 구조와 기능을 분석하여 클라우드 네이티브 전환을 위한 후보 영역을 식별합니다.
- 기술적, 비즈니스적 타당성 평가를 수행합니다.

> **요약 :** 전환 평가 단계는 시스템의 현재 상태를 분석하고, 클라우드 네이티브 전환의 잠재적 이점과 리스크를 평가합니다.

#### 마이그레이션 준비
- 전환에 필요한 인프라, 도구, 기술 스택을 선택합니다.
- 팀 구성원에 대한 교육 계획을 수립하고, 역할과 책임을 할당합니다.

> **요약 :** 마이그레이션 준비 단계에서는 클라우드 전환을 위한 기술적, 조직적 준비를 진행합니다.

#### 전환 계획(Plan) 수립
- 상세한 전환 로드맵, 일정, 예산을 수립합니다.
- 리스크 관리 계획과 비상 대응 전략을 마련합니다.

> **요약 :** 전환 계획 단계에서는 전환 프로젝트의 구체적인 실행 계획을 수립합니다.

#### 전환 설계(Design)
- 하이브리드 아키텍처를 위한 세부 설계를 수행합니다.
- 모노리스와 마이크로서비스 간 통신 방식을 결정합니다.

> **요약 :** 전환 설계 단계에서는 하이브리드 클라우드 아키텍처에 맞는 시스템 설계를 완성합니다.

#### 마이그레이션(Migration)
- 설계된 아키텍처에 따라 애플리케이션 및 데이터를 클라우드로 이전합니다.
- 마이그레이션 후 테스트와 검증을 수행합니다.

> **요약 :** 마이그레이션 단계에서는 실제로 애플리케이션과 데이터를 클라우드 환경으로 이전합니다.

#### 전환 후 운영 최적화(Operate Optimize)
- 클라우드 환경에서의 모니터링, 로깅, 자동화 도구를 활용하여 운영 효율성과 가시성을 향상시킵니다.
- 시스템 성능을 지속적으로 모니터링하고, 필요한 경우 스케일링 전략을 조정하여 리소스 사용을 최적화합니다.
- 비용 관리 전략을 수립하고, 클라우드 비용을 효율적으로 관리하기 위한 방안을 실행합니다.
- 보안 정책을 주기적으로 검토하고, 클라우드 환경에 맞는 보안 강화 조치를 적용합니다.

> **요약 :** 전환 후 운영 최적화 단계에서는 클라우드 환경에서의 운영 효율성을 높이고, 성능 및 비용 최적화를 위한 지속적인 관리와 개선 활동을 수행합니다. 이를 통해 시스템의 안정성, 보안, 비용 효율성을 보장합니다.

### References:
- 이벤트스토밍, 서비스 디컴포지션 (Service Decomposition) : <a href="https://www.msaschool.io/operation/design/design-three/" target="_blank"> https://www.msaschool.io/operation/design/design-three/</a>
- 이벤트스토밍 HowTo : <a href="https://intro-kor.msaez.io/business/" target="_blank">https://intro-kor.msaez.io/business/</a>
- 애플리케이션 아키텍처 설계 : <a href="https://www.msaschool.io/operation/design/design-five/" target="_blank">https://www.msaschool.io/operation/design/design-five/</a>
- 프론트-엔드 설계 : <a href="https://www.msaschool.io/operation/design/design-eight/" target="_blank">https://www.msaschool.io/operation/design/design-eight/</a>
- 게이트웨이(Gateway)를 통한 애플리케이션 창구 단일화 : <a href="https://www.msaschool.io/operation/implementation/implementation-six/" target="_blank">https://www.msaschool.io/operation/implementation/implementation-six/</a>
- 이벤트기반 메시지 채널, 카프카(Kafka) 활용 : <a href="https://www.msaschool.io/operation/implementation/implementation-seven/" target="_blank">https://www.msaschool.io/operation/implementation/implementation-seven/</a>
- MSA 성숙도 모델에 따른 구현 관점별 적용 레벨 : <a href="https://www.msaschool.io/operation/planning/planning/" target="_blank">https://www.msaschool.io/operation/planning/planning/</a>
