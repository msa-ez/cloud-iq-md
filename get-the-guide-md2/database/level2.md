## DB 아키텍처 수준: Level 2.개별 스키마 정의(Scheme per Service)

### 전환 원칙
- **개별 스키마 정의**: 각 마이크로서비스는 자체적인 스키마를 가지며, 각 서비스의 데이터 구조와 필드 정의가 명확합니다.
- **다중 엔터프라이즈 데이터 조정**: 서비스 간의 다중 엔터프라이즈 데이터 저장소와의 트랜잭션 조정 방식을 정의하고 이를 구현합니다.
- **데이터 일관성 유지**: 데이터 조정 및 동기화 과정에서 데이터 일관성을 유지하기 위한 메커니즘을 도입합니다.

### 전환 절차
#### 전환 평가(Assess)
- 기존의 데이터베이스 아키텍처와 데이터 관리 방식을 분석하여, 각 서비스에 개별 스키마를 적용할 때의 장점과 단점을 평가합니다.
- 서비스 간 데이터 조정 및 일관성 유지에 대한 요구 사항을 식별합니다.

> **요약 :** 전환 평가 단계에서는 현재 시스템을 분석하고 개별 스키마 정의로의 전환 가능성을 평가합니다.

#### 마이그레이션 준비
- 전환을 위해 필요한 데이터베이스 관리 시스템(DBMS) 및 도구를 선택합니다.
- 데이터 모델링과 마이그레이션 계획을 수립합니다.

> **요약 :** 마이그레이션 준비 단계에서는 전환에 필요한 기술적 준비와 계획을 세웁니다.

#### 전환 계획(Plan) 수립
- 전환의 범위, 목표, 일정을 명확히 정의합니다.
- 리소스 배정과 리스크 관리 계획을 포함한 전체 프로젝트 계획을 작성합니다.

> **요약 :** 전환 계획 단계에서는 개별 스키마 적용을 위한 구체적인 실행 계획을 수립합니다.

#### 전환 설계(Design)
- 각 마이크로서비스에 대한 개별 스키마를 설계합니다. 이 과정에서 서비스별 데이터 구조, 관계, 인덱스 등을 정의합니다.
- 데이터 조정 및 일관성 유지 메커니즘을 설계합니다.

> **요약 :** 전환 설계 단계에서는 각 마이크로서비스의 개별 스키마 및 데이터 일관성 유지 방안을 설계합니다.

#### 마이그레이션(Migration)
- 설계된 아키텍처에 따라, 각 마이크로서비스의 데이터베이스 스키마를 구축합니다. 이는 서비스별로 독립적인 데이터 관리와 확장성을 가능하게 합니다.
- 기존 데이터베이스에서 새로운 스키마로의 데이터 마이그레이션 작업을 진행합니다. 데이터 마이그레이션 과정에서 데이터의 무결성과 일관성을 보장하기 위한 철저한 계획과 테스트가 수반되어야 합니다. 필요에 따라, ETL(Extract, Transform, Load) 도구를 사용하여 데이터를 추출, 변환 및 적재합니다.
- 각 마이크로서비스에서 사용할 데이터의 동기화 및 조정 메커니즘을 구현합니다. 이는 서비스 간의 데이터 일관성을 유지하는 데 중요한 역할을 합니다. 다중 엔터프라이즈 데이터 조정을 위한 전략, 예를 들어, 이벤트 소싱 또는 CQRS(명령 쿼리 책임 분리)를 적용할 수 있습니다.
- 마이그레이션 과정에서 발생할 수 있는 성능 문제나 데이터 일관성 문제를 해결하기 위해 광범위한 테스트를 실시합니다. 테스트 과정에는 단위 테스트, 통합 테스트, 부하 테스트가 포함되어야 합니다.

> **요약 :** 마이그레이션 단계에서는 각 마이크로서비스별로 독립된 데이터베이스 스키마 구축, 기존 데이터의 안전한 마이그레이션, 그리고 데이터 동기화 및 조정 메커니즘 구현을 통해 전환을 실현합니다. 철저한 계획, 구현 및 테스트를 통해 데이터의 무결성과 서비스 간의 데이터 일관성을 보장합니다.

#### 전환 후 운영 최적화(Operate Optimize)
- 새로운 아키텍처에서의 운영 최적화를 위해, 데이터베이스와 애플리케이션의 성능 모니터링을 강화합니다. 모니터링 도구를 사용하여 시스템의 성능 지표를 실시간으로 추적하고, 잠재적인 문제를 조기에 식별합니다.
- 데이터 관리 및 유지 보수를 위한 자동화 도구를 도입하여 운영 효율성을 향상시킵니다. 자동 백업, 데이터 정리, 인덱싱 최적화 등의 작업을 자동화하여 데이터베이스의 안정성과 성능을 지속적으로 관리합니다.
- 서비스별 데이터 스키마의 변경 사항을 관리하기 위한 버전 관리 시스템을 구축합니다. 데이터 스키마 변경 시, 변경 사항을 체계적으로 추적하고, 필요한 마이그레이션 스크립트를 적용하여 데이터 구조를 최신 상태로 유지합니다.

> **요약 :** 전환 후 운영 최적화 단계에서는 시스템의 성능 모니터링, 데이터 관리 자동화, 그리고 데이터 스키마의 변경 관리를 통해 시스템의 안정적인 운영과 데이터의 일관성을 지속적으로 관리 및 개선합니다. 이 단계는 새로운 DB 아키텍처가 도입된 후에도 시스템의 성능과 데이터 무결성을 유지하기 위한 중요한 활동을 포함합니다. 체계적인 모니터링과 자동화 도구의 적용을 통해, 운영 효율성을 높이고, 장기적인 시스템 관리에 필요한 자원을 최소화합니다.

### References:
- 분산 환경에서의 최종 일관성(Eventual Transaction) 유지 : <a href="https://www.msaschool.io/operation/integration/integration-four/" target="_blank">https://www.msaschool.io/operation/integration/integration-four/</a>
- MSA 환경에서의 데이터 프로젝션(Data Projection) 기법 : <a href="https://www.msaschool.io/operation/integration/integration-five/" target="_blank">https://www.msaschool.io/operation/integration/integration-five/</a>
- Front-end에서의 데이터 통합 : <a href="https://www.msaschool.io/operation/integration/integration-one/" target="_blank">https://www.msaschool.io/operation/integration/integration-one/</a>
- 동기 호출(Request/Response Communication)에 의한 데이터 통합 : <a href="https://www.msaschool.io/operation/integration/integration-two/" target="_blank">https://www.msaschool.io/operation/integration/integration-two/</a>
- 이벤트 소싱(Event Sourcing) 기반 데이터 통합 : <a href="https://www.msaschool.io/operation/integration/integration-three/" target="_blank">https://www.msaschool.io/operation/integration/integration-three/</a>
- 커맨드 모델과 쿼리 모델의 분리(CQRS) : <a href="https://www.msaschool.io/operation/integration/integration-six/" target="_blank">https://www.msaschool.io/operation/integration/integration-six/</a>
- CQRS 데이터 프로젝션 : <a href="https://intro-kor.msaez.io/development/dp-cqrs/" target="_blank">https://intro-kor.msaez.io/development/dp-cqrs/</a>
