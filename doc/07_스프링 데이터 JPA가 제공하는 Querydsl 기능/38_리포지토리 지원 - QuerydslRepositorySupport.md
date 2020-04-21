## 리포지토리 지원 - QuerydslRepositorySupport
- 장점
  - 스프링 데이터가 제공하는 페이징을 querydsl로 편리하게 변환 가능 (sort는 안된다. 에러 발생)
  - from()으로 시작하는 기능
  - EntityManager 제공
- 단점
  - querydsl 3.0 버전 대상... 4.0이 나온 jpaQueryFactory로 시작할 수 없다.

- 페이징 이슈만 아니면 써도 가능
- 메소드 체인이 끊기는 단점... 가독성!