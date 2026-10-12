## '''Try my project here : [TeamPulse](teampulsebyptr.web.app)'''
# TeamPulse - Backend Service

Backend service repository for **TeamPulse**, containing the Spring Boot application and project documentation under the `backend/` directory.

---

## 🔗 Related Repositories

- **Main Full-Stack Repository:** [tejrohitparuchuri/TeamPulse](https://github.com/tejrohitparuchuri/TeamPulse)
- **Frontend Client Repository:** [tejrohitparuchuri/tt-3-1-frontend-ext](https://github.com/tejrohitparuchuri/tt-3-1-frontend-ext)

---

## 📂 Repository Structure
```
.
└── backend/
    ├── TeamPulse_Project_Abstract.docx
    └── tp/                               # Spring Boot application root
        ├── pom.xml                       # Maven build file
        ├── mvnw / mvnw.cmd               # Maven wrappers
        ├── src/
        │   ├── main/
        │   │   ├── java/app/             # Application code (controllers, entities, repositories, services)
        │   │   └── resources/
        │   │       └── application.properties # Server port (3333), MySQL configuration
        │   └── test/
        └── .gitignore
```

---

## 🛠️ Tech Stack
- **Framework:** Spring Boot 4.1.1
- **Language:** Java 17+
- **Database:** MySQL 8.0+ (`jdbc:mysql://127.0.0.1:3306/teampulse`)
- **Port:** `3333`
- **Security:** Spring Security 6 & BCrypt Password Encoding
- **Architecture:** REST API + Spring Data JPA

---

## 🚀 Quick Start

1. **Navigate to the Spring Boot project folder:**
   ```bash
   cd backend/tp
   ```

2. **Verify MySQL is running:**
   Ensure MySQL is running on `127.0.0.1:3306` with database `teampulse`.
   Credentials can be configured in `backend/tp/src/main/resources/application.properties`:
   ```properties
   spring.application.name=teampulse
   server.port=3333
   spring.datasource.url=jdbc:mysql://127.0.0.1:3306/teampulse
   spring.datasource.username=root
   spring.datasource.password=ptr3
   ```

3. **Run the Application:**
   - **Windows:**
     ```powershell
     .\mvnw.cmd clean spring-boot:run
     ```
   - **Linux / macOS:**
     ```bash
     ./mvnw clean spring-boot:run
     ```

The backend server will run on **`http://localhost:3333`**.
