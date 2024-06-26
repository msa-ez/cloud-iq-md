## DB 아키텍처 수준: Level 3.DBMS per Service, 폴리글랏 퍼시스턴스

### 전환 원칙
- **분산 데이터 관리**: 각 마이크로서비스는 완전히 분산된 데이터 관리를 수행하며, 필요에 따라 데이터의 파티셔닝, 샤딩, 복제 등을 구현합니다.
- **폴리글랏 퍼시스턴스**: 각 마이크로서비스는 자체적으로 다른 유형의 DBMS를 사용할 수 있는 폴리글랏 퍼시스턴스를 구현합니다.
- **데이터 접근 및 관리**: 각 마이크로서비스에서 필요한 데이터 액세스 방법을 선택하고, 이를 효율적으로 관리하며, 성능과 확장성을 고려합니다.

### 전환 절차
#### 전환 평가(Assess)
- 기존의 데이터베이스 아키텍처와 데이터 관리 방식을 분석하여, DBMS per Service, 폴리글랏 퍼시스턴스 전환의 장점과 단점을 평가합니다.
- 서비스별 데이터 요구 사항과 트랜잭션 패턴을 분석하여, 각 서비스에 가장 적합한 DBMS 유형을 식별합니다.

> **요약 :** 전환 평가 단계에서는 현재 시스템을 분석하고 DBMS per Service, 폴리글랏 퍼시스턴스 전환의 가능성을 평가합니다.

#### 마이그레이션 준비
- 전환을 위해 각 마이크로서비스에 적합한 DBMS를 선정하고, 필요한 데이터베이스 관리 도구 및 라이브러리를 조사합니다.
- 데이터 마이그레이션 계획을 수립하고, 데이터 모델링 및 마이그레이션 도구 선택을 진행합니다.

> **요약 :** 마이그레이션 준비 단계에서는 각 마이크로서비스에 적합한 DBMS 선택 및 필요한 기술적 준비를 합니다.

#### 전환 계획(Plan) 수립
- 전환의 범위, 목표, 일정을 명확히 정의하고, 리소스 배정 및 리스크 관리 계획을 포함한 전체 프로젝트 계획을 작성합니다.
- 관련 이해관계자와의 커뮤니케이션 계획을 마련합니다.

> **요약 :** 전환 계획 단계에서는 DBMS per Service, 폴리글랏 퍼시스턴스 전환을 위한 구체적인 실행 계획을 수립합니다.

#### 전환 설계(Design)
- **서비스별 DBMS 선정과 데이터 모델링**: 각 마이크로서비스의 특성과 요구 사항을 기반으로 최적의 DBMS를 선정합니다. 이 과정에서는 SQL, NoSQL, 그래프, 타임시리즈 등 다양한 DBMS 유형을 고려합니다. 선정된 DBMS에 맞춰 각 서비스의 데이터 모델 및 스키마를 설계합니다. 데이터 모델 설계 시, 서비스 간 데이터 중복 최소화, 접근 효율성, 확장성 및 유지 보수 용이성을 고려합니다.
- **분산 데이터 관리 전략 수립**: 서비스 간 데이터 일관성 및 트랜잭션 관리를 위한 전략을 수립합니다. 분산 데이터베이스 환경에서 데이터 일관성을 유지하기 위해 이벤트 소싱, CQRS(명령 쿼리 책임 분리), 사가 패턴 등의 전략을 적용할 수 있습니다.
- **데이터 마이그레이션 및 동기화 전략 개발**: 기존 데이터베이스 시스템에서 새로운 폴리글랏 퍼시스턴스 아키텍처로 데이터를 마이그레이션하기 위한 계획을 세웁니다. 또한, 지속적인 데이터 동기화를 위한 메커니즘을 구현하여 서비스 간 데이터 일관성을 보장합니다.

> **요약 :** 전환 설계 단계에서는 각 마이크로서비스에 적합한 DBMS를 선정하고, 서비스별 데이터 모델을 설계합니다. 분산 데이터 관리와 데이터 일관성 유지를 위한 전략을 수립하며, 기존 시스템에서 새로운 아키텍처로의 데이터 마이그레이션 및 동기화 방법을 개발합니다.

#### 마이그레이션(Migration)
- **데이터베이스 구축 및 초기 설정**: 설계된 각 마이크로서비스의 DBMS 구성에 따라, 필요한 데이터베이스 인스턴스를 생성합니다. 이 과정에는 선택된 DBMS의 설치, 구성, 최적화 작업이 포함됩니다. 폴리글랏 퍼시스턴스 접근 방식에 따라 다양한 유형의 데이터베이스(예: 관계형, NoSQL, 그래프 등)가 구축될 수 있습니다.
- **데이터 마이그레이션 실행**: 기존 시스템에서 새롭게 구축된 데이터베이스로 데이터를 이전하는 과정을 수행합니다. 이는 데이터의 추출(Extract), 변환(Transform), 적재(Load) 과정을 포함하는 ETL 작업을 통해 진행됩니다. 데이터 마이그레이션 과정에서 데이터 일관성, 무결성 검증을 위한 철저한 테스트가 필요합니다.
- **서비스 간 데이터 동기화 및 통합 테스트**: 데이터 이전 후, 각 마이크로서비스 간의 데이터 동기화를 확인하고, 전체 시스템이 정상적으로 작동하는지 검증하기 위한 통합 테스트를 실시합니다. 이 단계는 새로운 데이터베이스 구조 내에서의 데이터 접근 패턴, 트랜잭션 처리, 분산 데이터 관리 메커니즘의 효율성을 검증합니다.
- **성능 최적화 및 보안 설정 확인**: 새롭게 마이그레이션된 데이터베이스의 성능 최적화 작업을 수행하고, 데이터베이스와 데이터 접근에 대한 보안 설정을 재검토합니다. 이 과정에서 데이터베이스 쿼리 최적화, 인덱스 조정, 보안 규칙 및 액세스 제어 리스트(ACL) 설정 검토가 이루어집니다.

> **요약 :** 마이그레이션 단계에서는 각 마이크로서비스에 맞춰 데이터베이스를 구축하고, 기존 데이터를 새 시스템으로 이전합니다. 이 과정에는 데이터베이스 구축, 데이터 이전, 서비스 간 데이터 동기화 검증, 성능 최적화 및 보안 설정 검토가 포함됩니다. 전체 시스템의 통합 테스트를 통해 새로운 DB 아키텍처의 효율성과 안정성을 확보하는 것이 핵심입니다.

### References:
- 분산 환경에서의 최종 일관성(Eventual Transaction) 유지 : <a href="https://www.msaschool.io/operation/integration/integration-four/" target="_blank">https://www.msaschool.io/operation/integration/integration-four/</a>
- MSA 환경에서의 데이터 프로젝션(Data Projection) 기법 : <a href="https://www.msaschool.io/operation/integration/integration-five/" target="_blank">https://www.msaschool.io/operation/integration/integration-five/</a>
- Front-end에서의 데이터 통합 : <a href="https://www.msaschool.io/operation/integration/integration-one/" target="_blank">https://www.msaschool.io/operation/integration/integration-one/</a>
- 동기 호출(Request/Response Communication)에 의한 데이터 통합 : <a href="https://www.msaschool.io/operation/integration/integration-two/" target="_blank">https://www.msaschool.io/operation/integration/integration-two/</a>
- 이벤트 소싱(Event Sourcing) 기반 데이터 통합 : <a href="https://www.msaschool.io/operation/integration/integration-three/" target="_blank">https://www.msaschool.io/operation/integration/integration-three/</a>
- 커맨드 모델과 쿼리 모델의 분리(CQRS) : <a href="https://www.msaschool.io/operation/integration/integration-six/" target="_blank">https://www.msaschool.io/operation/integration/integration-six/</a>
- CQRS 데이터 프로젝션 : <a href="https://intro-kor.msaez.io/development/dp-cqrs/" target="_blank">https://intro-kor.msaez.io/development/dp-cqrs/</a>
