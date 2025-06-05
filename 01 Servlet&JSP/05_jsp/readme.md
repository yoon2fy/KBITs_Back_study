# 05_jsp (basic/advancd)
## FrontController

```java
🗂️ ex06
├── 📁 java/org/scoula/ex06/
│   ├── 📁 command/
│   │   └── 📄 Command.java
│   │ 
│   └── 📁 controller/
│        ├── 📄 DispatcherServlet.jsp
│        └── 📄 FrontControllerServlet.java
│
└── 📁 webapp/
    ├── 📄 index.jsp
    └── 📁 WEB-INF/views/
         ├── 📄 404.jsp
         └── 📁 todo/
              ├── 📄 create.jsp
              ├── 📄 list.jsp
              ├── 📄 update.jsp
              └── 📄 view.jsp
```

📄 FrontControllerServlet.java
- url 맵핑: "/"
- 메서드 `init()`, `doGet()`, `doPost()`

📄 Command.java
- interface

📄 FrontControllerServlet.java
- GET 요청 처리 맵
- POST 요청 처리 맵
- 메서드: `init()`, `getCommandName()`, `getCommand()`, `execute()`

📄 HomeController.java
- 메서드: `getIndex()`, 

📄 index.jsp
- html 파일 (최초 페이지 전용)

📄 404.jsp
- html 파일 (404 페이지 전용)

📄 TodoController.java
- 메서드: `getList()`, `getView()`, `getCreate()`, `postCreate()`, `getUpdate()`, `postUpdate()`, `postDelete()`

📄 list.jsp
- html 파일 (Todo List 1 페이지 전용)

📄 view.jsp
- action: delete
- method: POST

📄 create.jsp
- action: 현재 URL
- method: POST

📄 update.jsp
- action: 현재 URL
- method: POST

📄 DispatcherServlet.java
- FrontController.java 의 재사용을 위해 사용되는 부모 클래스
- 실제 url 매핑: createMap() 메서드에서함
- 실제 구현: 자식 클래스가 작성함.
