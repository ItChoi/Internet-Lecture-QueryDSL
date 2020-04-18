## SQL function 호출
- JPQL에서 호출 가능하고, QUERYDSL에서도 SQL 방식 (방언) 호출
- dialect를 직접 만들어 사용하고 싶은 경우 
  - package org.hibernate.dialect; public class H2Dialect extends Dialect를 상속 받아 사용
- 간단한 함수, 소문자로 바꾸는 lower라던가 이런 간단한 함수들은 이미 안씨 표준에 등록이 되어 있다.
  - 간단한 함수는 querydsl에 이미 내장되어 있다. 
  - 따라서 querydsl 방식으로 사용할 수 있다.