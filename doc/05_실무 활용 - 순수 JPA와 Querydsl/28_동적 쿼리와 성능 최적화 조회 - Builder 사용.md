## 동적 쿼리와 성능 최적화 조회 - Builder 사용
- 생성자에 @QueryProjection 사용
  - QDto 사용하기 위함 -> compileQuerydsl 하기
    - 단점: Dto가 순수하게 dto답게 사용하지 못한다.
    - Querydsl 라이브러리에 결국 의존하게 된다.
    
- 동적 쿼리를 짤 땐 기본 조건이 있는 게 좋다. 페이징이나 리밋이 있는 것이 좋다. 조건이 없을 경우 다 끌고 오면, 많은 데이터를 다 가져오게 된다.
