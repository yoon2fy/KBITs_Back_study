# 웹 어플리케이션 프로젝트 (심화1)
## Q1. 앞에서 만든 프로젝트를 war 파일로 만드세요.

### A1.
`ex02` 프로젝트를 예로 들어보자.
war 파일로 만들기 위해서는 `ex02-1.0-SNAPSHOT.war` 파일을 가져와야 한다. 이를 하기 위해서는 파일의 경로를 알아야 한다. war 파일은 `ex02/build/libs/`에 존재한다.

</br>

# 웹 어플리케이션 프로젝트 (심화2)
## Q2. 앞에서 만든 war 파일을 tomcat의 root 어플리케이션으로 배포하세요.

### A2.
첫번째, war 파일을 배치해야한다. 이는, `C:apache-tomcat-9.0.98/webapps/`에 배치하면 된다.
두번째, ROOT 애플리케이션을 설정해야한다. 경로는, `C:apache-tomcat-9.0.98/conf/server.xml`이고, 아래의 코드를 `<Host>태그` 사이에 넣으면 된다.

```js
<Context path = "/" docBase = "ex02-1.0-SNAPSHOT" reloadable = "false" ></Context>
```

세번째, 실제 Tomcat 서버를 실행하면 된다. 실행을 하는 방법은, `C:\apache-tomcat-9.0.98\bin\startup/bat` 을 실행하면 된다.

마지막으로 윈도우의 경우, 콘솔 한글 로그 문자셋을 설정하면 된다. 이는, `C:\apache-tomcat-9.0.98\conf\logging.properties` 을 실행하여 다음과 같이 수정을 진행하면 된다.

```java
java.util.logging.ConsoleHandler.encoding = EUC-KR
```

