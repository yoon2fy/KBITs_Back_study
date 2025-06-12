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
# 스프링 MySQL Database 연동

