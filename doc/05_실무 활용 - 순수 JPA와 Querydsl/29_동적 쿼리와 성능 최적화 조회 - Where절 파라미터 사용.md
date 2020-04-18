## 동적 쿼리와 성능 최적화 조회 - Where절 파라미터 사용
- where 조건 하나를 조건으로 뺄 때, 예를 들어 usernameEq(username)
  - Predicate 타입 보다, BooleanExpression 타입으로 지정하는 게 좋다.
    - 나중에 조립해서 효율적으로 사용 가능
    - select Projection이 달라져도 조건들을 재사용 가능하다! 완전 좋다.
    - null만 조심하면 조립 가능!
  - 가끔 사용하다보면 BooleanBuilder로 사용해야할 때도 있다!