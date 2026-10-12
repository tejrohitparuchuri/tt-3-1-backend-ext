# TeamPulse - Backend Service

Backend service repository for **TeamPulse**, containing the Spring Boot application and project documentation under the `backend/` directory.

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy?repo=https://github.com/tejrohitparuchuri/tt-3-1-backend-ext)

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
- **Language:** Java 24
- **Database:** MySQL 8.0+ (`jdbc:mysql://127.0.0.1:3306/teampulse`)
- **Port:** `3333`
- **Security:** Spring Security 6 & BCrypt Password Encoding
- **Real-Time:** Spring WebSocket & STOMP messaging

---

## 🚀 Quick Start

1. **Navigate to the Spring Boot project folder:**
   ```bash
   cd backend/tp
   ```

2. **Verify MySQL is running:**
   Ensure MySQL is running on `127.0.0.1:3306` with database `teampulse`.
   Credentials can be updated in `backend/tp/src/main/resources/application.properties`.

3. **Run the Application:**
   - **Windows:**
     ```powershell
     .\mvnw.cmd clean spring-boot:run
     ```
   - **Linux / macOS:**
     ```bash
     ./mvnw clean spring-boot:run
     ```

The backend server will run on `http://localhost:3333`.

