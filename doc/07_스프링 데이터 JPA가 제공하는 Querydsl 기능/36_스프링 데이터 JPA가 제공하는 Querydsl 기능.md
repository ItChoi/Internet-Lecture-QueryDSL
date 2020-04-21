## 스프링 데이터 JPA가 제공하는 Querydsl 기능
- 제약이 커서 복잡한 실무 환경에서 사용하기에는 많이 부족하다.

### 인터페이스 지원 - QueryDslPredicateExecutor
- 파라미터를 querydsl 조건을 넣어줄 수 있다.
  - QMember findMember = QMember.member; Iterable<Member> result = memberRepository.findAll(findMember.age.between(20, 40).and(findMember.username.eq("member1")));
  - 한계가 명확하다. 
    - 조인이 안된다. 묵시적 조인 가능, left join 불가능
    - 클라이언트가 Querydsl에 의존해야 하낟.
    - 복잡한 실무환경에서 사용하기에는 한계가 명확
    - 테이블 하나 조회는 모르겠는데, 실무에서는 권장하지 않는다!