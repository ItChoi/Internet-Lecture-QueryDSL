## 기본 Q-Type 활용
- Q 클래스 인스턴스를 사용하는 두 가지 방법
  - QMember qMember = new QMember("m") -> 별칭 직접 지정
  - QMember qMember = QMember.member -> 기본 인스턴스 사용
- QueryDSL은 결국 JPQL
  - use_sql_comments: true 하면 JPQL 쿼리 좀 더 자세하게 보기 가능!
- 같은 테이블을 선언해서 써야 하는 경우가 생길 때만 선언해서 사용하면 된다.