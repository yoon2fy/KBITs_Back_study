# 04_jsp (basic/advancd)
## EL, JSTL (기본)

```java
🗂️ ex05
├── 📁 java/
│   ├── 📄 LoginServlet.java
│   ├── 📄 ScopeServlet.java
│   └── 📁 domain/
│        └── 📄 Member.java
│
└── 📁 webapp/
    ├── 📄 login_form.jsp
    ├── 📄 login.jsp
    └── 📄 scope.jsp
```

📄 login_form.jsp
- 데이터를 받는 html 파일

📄 LoginServlet.java
- url 맵핑: "/login"
- `request` 스코프에 저장함.
- login.jsp로 포워딩함.

📄 login.jsp
- 요청 url: "login"
- `request` 스코프에 저장된 데이터를 출력함.

📄 ScopeServlet.java
- url 맵핑: "/scope"
- `request` 스코프에 저장함.

📄 scope.jsp
- 요청 url: "scope"
- 스코프에 저장된 데이터를 출력함.

<br>

---

<br>

## 요청 포워딩, 리다이렉트 (심화1)

```java
🗂️ demo-ex04
├── 📁 java/
│   ├── 📄 RequestServlet.java
│   ├── 📄 RequestRedirectServlet.java
│   └── 📄 ResponseRedirectServlet.java
│
└── 📁 webapp/
    ├── 📄 response.jsp
    └── 📄 redirect_response.jsp
```

📄 RequestServlet.java
- url 맵핑: "/request"
- `request` 스코프에 저장함.
- response.jsp로 포워딩 함.

📄 response.jsp
- 요청 url: "request"
- `request` 스코프에 저장된 데이터를 출력함.
- /request 요청으로 결과를 확인함.

📄 RequestRedirectServlet.java
- url 맵핑: "/request_redirect"
- `request` 스코프에 속성을 **설정**함.
- request_redirect로 리다이렉트 함.

📄 ResponseRedirectServlet.java
- url 맵핑: "/response_redirect"
- `request` 스코프에 속성을 **추출**함.
- 추출한 속성을 다시 `request` 스코프에 **저장**함.
- redirect_response.jsp로 포워딩 함.

📄 redirect_response.jsp
- `request` 스코프에 저장된 데이터를 출력함.
- /request_redirect 요청으로 결과를 확인함.

<br>

---

<br>

## EL, JSTL (심화1)

```java
// 문제-풀이와 관련된 부분만 정리했습니다.
🗂️ ex05
├── 📁 java/
│   └── 📄 JstlServlet.java
│
└── 📁 webapp/
    └── 📄 jstl_ex.jsp
```

📄 JstlServlet.java
- url 맵핑: "/jstl_ex"
- `request` 스코프에 속성을 **추출**함.
- jstl_ex.jsp로 포워딩 함.

📄 jstl_ex.jsp
- role 속성값을 검사하는 기능.
- <List> members 목록을 이용하여 <table>로 **출력**함.
