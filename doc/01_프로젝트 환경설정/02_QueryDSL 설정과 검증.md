## QueryDSL 설정과 검증
- QueryDSL에 그래들에 설정하고, 그래들 설정 과정에서 Q Type을 뽑아야 하는데, 그게 좀 어렵다~
  1. id "com.ewerk.gradle.plugins.querydsl" version "1.0.10"
  2. Lib 추가
     - implementation 'com.querydsl:querydsl-jpa'  
  3. 제일 끝에 추가
     - 빌드와 관련!
       
  ```groovy
  // (3) query 추가 시작
  // build -> genertated -> querydsl이 source 폴더로 잡혔다. 엔티티가 있는 패키지를 그대로 Q 엔티티가 생긴다.
  def querydslDir = "$buildDir/generated/querydsl"
  
  querydsl {
      jpa = true
      querydslSourcesDir = querydslDir
  }
  
  sourceSets {
      main.java.srcDir querydslDir
  }
  
  configurations {
      querydsl.extendsFrom compileClasspath
  }
  
  compileQuerydsl {
      options.annotationProcessorPath = configurations.querydsl
  }
  // (3) query 추가 끝
  ```

- QueryDSL은 Q Type을 뽑고 이를 통해 쿼리를 한다.
- Q Type은 git 관리대상에서 빼야 한다!  
