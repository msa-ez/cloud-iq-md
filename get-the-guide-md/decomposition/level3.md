### 기능분해: 도메인 컨텍스트 기반 분리

- Ubiquitous language 가 다른 bounded context간의 커뮤니케이션 시, Anti-corruption layer를 통해 수행
- Ubiquitous language 정의: 각 bounded context에서 사용될 공통 언어와 용어를 정의하고 이를 문서화함
- Boundary 정의: 각 bounded context의 경계를 명확하게 정의하고 외부에서의 커뮤니케이션 방식을 결정
- Anti-corruption layer 구현: bounded context 간의 통신을 관리하기 위해 Anti-corruption layer를 구현하고 외부 인터페이스 변환 및 데이터 변환을 수행
