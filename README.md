# TeamPulse - Backend Service

Backend service for **TeamPulse**, built with **Spring Boot 4 / Java 24** and **MySQL**. Provides RESTful APIs and WebSocket support for user authentication, workspaces, channel communication, team engagement ranking, and sentiment analytics.

---

## 🛠️ Tech Stack
- **Framework:** Spring Boot 4.1.1
- **Language:** Java 24
- **Database:** MySQL 8.0+
- **Security:** Spring Security 6+ & BCrypt Password Encoding
- **ORM / Persistence:** Spring Data JPA / Hibernate ORM
- **Build Tool:** Maven (Maven Wrapper included)
- **Real-Time:** Spring WebSocket & STOMP messaging

---

## 📂 Repository Structure
```
.
├── src/
│   ├── main/
│   │   ├── java/app/
│   │   │   ├── config/          # Security, Web & WebSocket configurations
│   │   │   ├── controller/      # REST API Controllers (Auth, Workspace, Channels, etc.)
│   │   │   ├── model/           # JPA Entities (User, Workspace, Channel, Message, etc.)
│   │   │   ├── repository/     # Spring Data JPA Repositories
│   │   │   └── service/         # Business Logic & Services
│   │   └── resources/
│   │       └── application.properties # Server port, MySQL connection, JPA settings
│   └── test/                    # Unit & Integration tests
├── pom.xml                      # Maven dependencies and plugins
├── mvnw / mvnw.cmd              # Maven wrapper scripts
└── TeamPulse_Project_Abstract.docx
```

---

## ⚙️ Prerequisites & Setup

1. **Java JDK 17+ or 24+** installed.
2. **MySQL Database**:
   Create a database named `teampulse`:
   ```sql
   CREATE DATABASE teampulse;
   ```
3. **Configure Database Connection**:
   Update `src/main/resources/application.properties` with your MySQL credentials:
   ```properties
   spring.datasource.url=jdbc:mysql://127.0.0.1:3306/teampulse
   spring.datasource.username=root
   spring.datasource.password=YOUR_PASSWORD
   server.port=3333
   ```

---

## 🚀 Running the Application

### Using Maven Wrapper (Windows PowerShell / CMD):
```powershell
.\mvnw.cmd clean spring-boot:run
```

### Using Maven Wrapper (Linux / macOS):
```bash
./mvnw clean spring-boot:run
```

The server will start on port `3333` (e.g., `http://localhost:3333`).

---

## 🔑 Key API Endpoints

### Authentication (`/api/auth`)
- `POST /api/auth/register` - Register a new user (`username`, `name`, `email`, `password`, `age`, `gender`, `position`, `company`, `role`)
- `POST /api/auth/login` - Login with credentials (`usernameOrEmail`, `password`)
- `GET /api/auth/check-username?username={val}` - Check if a username is available
- `GET /api/auth/check-email?email={val}` - Check if an email is registered

### Workspaces & Channels (`/api/workspaces`, `/api/channels`)
- `GET /api/workspaces` - Retrieve user workspaces
- `POST /api/workspaces` - Create workspace
- `GET /api/channels/{channelId}/messages` - Channel message history
- `POST /api/channels/{channelId}/messages` - Send message to channel

---

## 🌐 CORS Configuration
CORS is configured in `WebConfig.java` to allow cross-origin requests from frontend clients (e.g., `http://localhost:5500`).