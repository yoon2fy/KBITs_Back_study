*03_spring(basic)*
# 스프링 MySQL Database 연동

📝 다음과 같이 데이터베이스와 사용자를 준비하세요.

```sql
CREATE DATABASE scoula_db;
CREATE USER 'scoula'@'%' identified by '1234';
GRANT ALL PRIVILEGES ON scoula_db.* TO 'scoula'@'%';
```

</br>

📝 프로젝트를 생성하세요.
- 프로젝트 템플릿: SpringLegacy
- 의존성 설정에 MySQL JDBC 드라이버 추가
- Enable Annotation Processor 활성화

</br>

📝 JDBC 드라이버를 통해 DB 연결 테스트 코드를 작성하세요. (`📄 JDBCTest.java`)

📝 HikariCP DataSource를 위한 의존성을 추가하세요.

📝 `📄 resources/application.properties`에 데이터소스 연결에 필요한 설정을 추가하세요.

📝 `📄 RootConfig.java`에 `📄 application.properties` 정보를 이용하여 DataSource 빈을 등록하는 코드를 추가하세요.

📝 `📄 DataSourceTest.java`를 테스트에 추가하고, `📄 RootConfig.java`의 DataSource 빈 생성을 테스트 하세요.

</br>

---

*03_spring(advance)*
# 스프링 MySQL Database 연동 (심화1)
📝 MyBatis와 관련된 의존 라이브러리를 추가하세요.

📝 mybatis 설정 파일을 만들고 기본 설정 구조를 추가하세요. (`📄 main/resources/mybatis-config.xml`)

📝 `📄 config/RootConfig.java`에 MyBatis를 위한 기본 설정을 하세요.
- SqlSessionFactory 빈 등록 --> 정상 등록 되었는지 확인하기 (TDD 방식).
- DataSourceTransactionManager 빈 등록 --> 정상 등록 되었는지 확인하기 (TDD 방식).

📝 다음처럼 `📄 TimeMapper.java` 인터페이스를 추가하세요.
- 경로: /org/scoula/mapper
- `String getTime()` 메서드에 현재 시간을 리턴하는 쿼리를 연결하세요. ( *@Select* )

📝 `📄 RootConfig.java`에 Mapper를 스캔하는 설정을 추가하세요. ( *@MapperScan()* )

📝 다음처럼 **단위 테스트** `📄 TimeMapperTest.java`를 생성하고, 앞에서 작성한 `getTime()` 메서드를 테스트하세요.

📝 `log4jdbc-log4j2` 의존성을 프로젝트에 추가하세요.

📝 `📄 resources/log4jdbc.log4j2.properties`에 `log4jdbc-log4j2` 설정을 추가하세요.

📝 `📄 application.properties`에서 DataSource 연결을 위한 드라이버 클래스명과 접속 url을 수정하세요.

📝 `📄 log4j2.xml`을 다음과 같이 수정하세요.
- 기본 로그 레벨: info
- 단위 테스트용
- main 운영용

</br>

# 스프링 MySQL Database 연동 (심화2)
해당 프로젝트를 템플릿으로 등록하세요.
- File > New Project Setup > Save Project As Template ...

