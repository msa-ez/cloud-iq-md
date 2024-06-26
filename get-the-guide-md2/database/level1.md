## DB 아키텍처 수준: Level 1.싱글 DBMS 사용

### 전환 원칙
- **트랜잭션 관리**: 각 마이크로서비스에서 ACID(Atomicity, Consistency, Isolation, Durability) 기반의 트랜잭션을 유지하기 위한 방법과 프레임워크를 도입합니다.
- **데이터 일관성 유지**: Canonical Data Model을 도입하여 데이터의 일관성을 유지하고, 데이터 중복을 최소화합니다.

### 전환 절차
#### 전환 평가(Assess)
- 현재 데이터베이스 아키텍처와 데이터 관리 방식을 분석하여, 싱글 DBMS 사용으로 전환할 때의 잠재적 이점과 리스크를 평가합니다.
- 데이터 일관성, 트랜잭션 관리, 성능 요구 사항 등을 고려하여 단일 DBMS 사용이 적합한지 검토합니다.

> **요약 :** 전환 평가 단계에서는 현재 시스템의 데이터베이스 아키텍처를 분석하고, 싱글 DBMS 사용으로의 전환 가능성을 타진합니다.

#### 마이그레이션 준비
- 전환을 위해 선택된 DBMS에 대한 기술적 요구 사항과 호환성을 평가합니다.
- 데이터 모델링, 백업 및 복구 전략, 데이터 마이그레이션 도구 선택 등 전환 준비를 위한 계획을 수립합니다.

> **요약 :** 마이그레이션 준비 단계에서는 전환에 필요한 기술적 준비와 계획을 세웁니다.

#### 전환 계획(Plan) 수립
- 전환 일정, 리소스 배정, 리스크 관리 계획을 포함한 전환 프로젝트 계획을 수립합니다.
- 관련 이해관계자와의 커뮤니케이션 계획을 마련합니다.

> **요약 :** 전환 계획 단계에서는 싱글 DBMS 사용으로의 전환을 위한 구체적인 실행 계획을 수립합니다.

#### 전환 설계(Design)
- 단일 DBMS를 사용하기 위한 데이터베이스 스키마를 설계하고, 트랜잭션 관리 및 데이터 일관성 유지를 위한 메커니즘을 정의합니다.
- 데이터 액세스 계층을 설계하여 애플리케이션과 데이터베이스 간의 상호작용을 최적화합니다.

> **요약 :** 전환 설계 단계에서는 싱글 DBMS 사용을 위한 데이터베이스 스키마 및 데이터 액세스 계층을 설계합니다.

#### 마이그레이션(Migration)
- **데이터베이스 구축**: 설계 단계에서 정의된 데이터베이스 스키마를 바탕으로 새로운 단일 DBMS 인스턴스를 구축합니다. 이 과정에서 데이터의 저장 구조, 인덱스, 관계 등을 세밀하게 설정합니다.
- **데이터 마이그레이션**: 기존 시스템에서 새로운 단일 DBMS로 데이터를 이전하는 작업을 진행합니다. 이때 데이터의 무결성과 일관성을 보장하기 위해 철저한 계획과 검증이 필요합니다. 데이터 변환 스크립트나 ETL(Extract, Transform, Load) 도구를 사용하여 데이터를 적절히 변환하고 이전합니다.
- **테스트 및 검증**: 데이터 마이그레이션 후, 새로운 DBMS에서 애플리케이션의 데이터 접근, 트랜잭션 처리, 데이터 일관성 등이 올바르게 동작하는지 체계적으로 테스트합니다. 성능 테스트를 포함하여, 새 시스템의 응답 시간과 처리량도 평가합니다.

> **요약 :** 마이그레이션 단계에서는 새로운 단일 DBMS 인스턴스의 구축, 기존 데이터의 마이그레이션, 그리고 테스트 및 검증을 통해 시스템의 데이터 저장 및 관리 체계를 전환합니다. 이 과정은 데이터의 무결성과 일관성 유지를 최우선으로 고려합니다.

#### 전환 후 운영 최적화(Operate Optimize)
- **성능 모니터링 및 최적화**: 새로운 DBMS 환경에서 시스템의 성능을 지속적으로 모니터링합니다. 쿼리 성능, 트랜잭션 처리 시간, 리소스 사용량 등을 분석하여 필요한 성능 최적화 조치를 취합니다.
- **백업 및 재해 복구 계획**: 데이터의 안전성을 보장하기 위해 정기적인 백업 계획을 수립하고, 재해 발생 시 데이터를 신속하게 복구할 수 있는 전략을 마련합니다.
- **보안 강화**: DBMS의 보안 설정을 점검하고, 데이터 액세스 관리, 암호화, 취약점 방어 등을 포함한 보안 강화 조치를 실행합니다.

> **요약 :** 전환 후 운영 최적화 단계에서는 새로운 DBMS 환경에서의 시스템 성능 모니터링 및 최적화, 데이터의 안전성을 위한 백업 및 재해 복구 계획 수립, 그리고 데이터 보안 강화 조치를 진행합니다. 이는 시스템의 안정적인 운영과 데이터의 안전을 보장하기 위한 중요한 활동입니다.

### References:
- 분산 환경에서의 최종 일관성(Eventual Transaction) 유지 : <a href="https://www.msaschool.io/operation/integration/integration-four/" target="_blank">https://www.msaschool.io/operation/integration/integration-four/</a>
- MSA 환경에서의 데이터 프로젝션(Data Projection) 기법 : <a href="https://www.msaschool.io/operation/integration/integration-five/" target="_blank">https://www.msaschool.io/operation/integration/integration-five/</a>
- Front-end에서의 데이터 통합 : <a href="https://www.msaschool.io/operation/integration/integration-one/" target="_blank">https://www.msaschool.io/operation/integration/integration-one/</a>
- 동기 호출(Request/Response Communication)에 의한 데이터 통합 : <a href="https://www.msaschool.io/operation/integration/integration-two/" target="_blank">https://www.msaschool.io/operation/integration/integration-two/</a>
- 이벤트 소싱(Event Sourcing) 기반 데이터 통합 : <a href="https://www.msaschool.io/operation/integration/integration-three/" target="_blank">https://www.msaschool.io/operation/integration/integration-three/</a>
- 커맨드 모델과 쿼리 모델의 분리(CQRS) : <a href="https://www.msaschool.io/operation/integration/integration-six/" target="_blank">https://www.msaschool.io/operation/integration/integration-six/</a>
- CQRS 데이터 프로젝션 : <a href="https://intro-kor.msaez.io/development/dp-cqrs/" target="_blank">https://intro-kor.msaez.io/development/dp-cqrs/</a>

