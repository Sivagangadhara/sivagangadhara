<div align="center">

  <img src="https://capsule-render.vercel.app/api?type=venom&color=0:0f2027,50:203a43,100:2c5364&height=220&section=header&text=MediBook&fontSize=72&fontColor=ffffff&fontAlignY=55&desc=Doctor%20Appointment%20Management%20System&descAlignY=75&descColor=7ecfff&animation=fadeIn" width="100%"/>

  <br/>

  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=15&duration=2800&pause=900&color=7ECFFF&center=true&vCenter=true&width=680&lines=Secure+%7C+Scalable+%7C+Production-Ready+Healthcare+Backend;OTP+Authentication+%2B+Full+RBAC+%28Admin+%2F+Doctor+%2F+Patient%29;Built+with+Java+%7C+Spring+Boot+%7C+Spring+Security;RESTful+API+Architecture+%2B+Transactional+Integrity" alt="Typing animation"/>

  <br/><br/>

  ![Java](https://img.shields.io/badge/Java_17-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
  ![Spring Boot](https://img.shields.io/badge/Spring_Boot_3-6DB33F?style=flat-square&logo=springboot&logoColor=white)
  ![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
  ![MySQL](https://img.shields.io/badge/MySQL_8-00758F?style=flat-square&logo=mysql&logoColor=white)
  ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
  <br/>
  ![Status](https://img.shields.io/badge/Status-Active_Development-brightgreen?style=flat-square)
  ![License](https://img.shields.io/badge/License-MIT-7ecfff?style=flat-square)
  ![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-ff6b35?style=flat-square)
  ![Made with Love](https://img.shields.io/badge/Made_with-Love_in_India-FF4C60?style=flat-square)

  <br/><br/>

  [**📖 Docs**](#-installation) · [**🚀 Live Demo**](#-screenshots--demo) · [**🐛 Report Bug**](https://github.com/mutyalasiva/medibook/issues) · [**✨ Request Feature**](https://github.com/mutyalasiva/medibook/issues)

</div>

---

## 📋 Table of Contents

- [About the Project](#-about-the-project)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Architecture Overview](#-architecture-overview)
- [Screenshots & Demo](#-screenshots--demo)
- [Installation](#-installation)
- [Usage](#-usage)
- [API Reference](#-api-reference)
- [Project Structure](#-project-structure)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Author](#-author)

---

## 🏥 About the Project

**MediBook** is a production-grade **Doctor Appointment Management System** built on a mobile-first backend architecture. It provides a secure, role-driven platform where patients can book appointments, doctors can manage their schedules, and admins can oversee the entire ecosystem — all through clean, documented RESTful APIs.

### Why MediBook?

Healthcare scheduling systems are plagued by security gaps, poor access control, and inconsistent data handling. MediBook addresses this with:

- ✅ **OTP-based mobile authentication** — no passwords, no vulnerabilities
- ✅ **Strict RBAC** — every endpoint locked down by role (Admin / Doctor / Patient)
- ✅ **Transactional integrity** — `@Transactional` on every critical operation, no partial writes
- ✅ **Normalized, indexed MySQL schemas** — built for query performance at scale
- ✅ **Clean layered architecture** — Controller → Service → Repository, full separation of concerns

> Built to production standards — not just a portfolio project, but a system you'd actually deploy.

---

## ✨ Key Features

### 🔐 Security & Authentication
- **OTP-Based Login** — Mobile number + one-time password via SMS integration
- **JWT Token Management** — Stateless session handling with configurable expiry
- **Spring Security Integration** — Filter chains, custom `UserDetailsService`, method-level security
- **Role-Based Access Control** — Three distinct roles with fully scoped permissions

### 👥 Role Management

| Role | Capabilities |
|---|---|
| 🛡️ **Admin** | Manage doctors, view all appointments, configure system settings, generate reports |
| 🩺 **Doctor** | View own schedule, update availability, manage appointment status, access patient notes |
| 🧑‍💼 **Patient** | Register, book/cancel appointments, view history, receive OTP notifications |

### 📅 Appointment Engine
- Book, reschedule, and cancel appointments with real-time slot availability
- Doctor availability management with configurable time slots
- Appointment status lifecycle: `PENDING → CONFIRMED → COMPLETED / CANCELLED`
- Conflict detection — prevents double-booking at the database level

### 🗄️ Data Layer
- Fully normalized MySQL schemas (3NF) with foreign key constraints
- Strategic indexing on high-query columns (`doctor_id`, `patient_id`, `appointment_date`)
- `@Transactional` coverage across all multi-step business operations
- JPA/Hibernate with optimized lazy loading and fetch strategies

### 🔧 Engineering Quality
- Centralized exception handling with `@ControllerAdvice`
- Structured error responses with HTTP-appropriate status codes
- Input validation via Bean Validation (JSR-380)
- Comprehensive logging with SLF4J + Logback

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Technology | Purpose |
|---|---|---|
| **Language** | ![Java](https://img.shields.io/badge/Java_17-ED8B00?style=flat-square&logo=openjdk&logoColor=white) | Core application logic |
| **Framework** | ![Spring Boot](https://img.shields.io/badge/Spring_Boot_3-6DB33F?style=flat-square&logo=springboot&logoColor=white) | Application framework & auto-configuration |
| **Security** | ![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white) | Authentication, authorization, filter chain |
| **ORM** | ![Hibernate](https://img.shields.io/badge/Hibernate_6-59666C?style=flat-square&logo=hibernate&logoColor=white) | Object-relational mapping, JPA provider |
| **Database** | ![MySQL](https://img.shields.io/badge/MySQL_8-00758F?style=flat-square&logo=mysql&logoColor=white) | Primary relational data store |
| **Containerization** | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) | Environment consistency & deployment |
| **API Testing** | ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white) | API validation & documentation |
| **Build Tool** | ![Maven](https://img.shields.io/badge/Maven-C71A36?style=flat-square&logo=apachemaven&logoColor=white) | Dependency management & build lifecycle |
| **Version Control** | ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) | Source control |

</div>

---

## 🏗️ Architecture Overview

```
┌─────────────────────────────────────────────────────────────┐
│                        CLIENT LAYER                          │
│              (Mobile App / Web / Postman)                    │
└─────────────────────────┬───────────────────────────────────┘
                          │  HTTPS / REST
┌─────────────────────────▼───────────────────────────────────┐
│                   SPRING SECURITY LAYER                      │
│        JWT Filter → Authentication → Authorization           │
│              Role Check: ADMIN | DOCTOR | PATIENT            │
└─────────────────────────┬───────────────────────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────────┐
│                    CONTROLLER LAYER                          │
│    AuthController · AppointmentController · UserController   │
│    DoctorController · AdminController · ReportController     │
└─────────────────────────┬───────────────────────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────────┐
│                     SERVICE LAYER                            │
│   Business Logic · OTP Handling · Scheduling Engine          │
│   @Transactional boundaries · Validation · Mapping           │
└─────────────────────────┬───────────────────────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────────┐
│                   REPOSITORY LAYER                           │
│           Spring Data JPA / Hibernate / JDBC                 │
└─────────────────────────┬───────────────────────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────────┐
│                   MySQL DATABASE                             │
│   users · doctors · patients · appointments · otp_tokens     │
│   availability_slots · audit_logs · notifications            │
└─────────────────────────────────────────────────────────────┘
```

---

## 📸 Screenshots & Demo

> 🚧 **Demo deployment coming soon.** API documentation and Postman collection available below.

<div align="center">

| Endpoint | Method | Role | Description |
|---|---|---|---|
| `/api/auth/send-otp` | `POST` | Public | Send OTP to mobile number |
| `/api/auth/verify-otp` | `POST` | Public | Verify OTP, receive JWT |
| `/api/appointments/slots` | `GET` | Patient | View available slots |
| `/api/appointments/book` | `POST` | Patient | Book an appointment |
| `/api/appointments/{id}/status` | `PUT` | Doctor | Update appointment status |
| `/api/admin/dashboard` | `GET` | Admin | Full system overview |

</div>

📮 **[Download Postman Collection](https://github.com/mutyalasiva/medibook)** — Import and test all endpoints locally in minutes.

---

## ⚙️ Installation

### Prerequisites

Make sure the following are installed on your machine:

```bash
java --version     # Java 17 or higher
mvn --version      # Maven 3.8+
mysql --version    # MySQL 8.0+
docker --version   # Docker (optional — for containerized setup)
```

---

### Option 1 — Local Setup

```bash
# 1. Clone the repository
git clone https://github.com/mutyalasiva/medibook.git
cd medibook

# 2. Create the database
mysql -u root -p -e "CREATE DATABASE medibook_db;"

# 3. Set environment variables
export DB_URL=jdbc:mysql://localhost:3306/medibook_db
export DB_USERNAME=your_mysql_user
export DB_PASSWORD=your_mysql_password
export JWT_SECRET=your_256bit_secret_key
export OTP_API_KEY=your_sms_provider_key

# 4. Build and run
mvn clean install
mvn spring-boot:run
```

> Server starts at `http://localhost:8080`

---

### Option 2 — Docker Setup (Recommended)

```bash
# 1. Clone the repository
git clone https://github.com/mutyalasiva/medibook.git
cd medibook

# 2. Configure your environment
cp .env.example .env
# Edit .env with your credentials

# 3. Build and launch all containers
docker-compose up --build

# 4. Tear down
docker-compose down
```

> Docker Compose automatically provisions both the Spring Boot app and MySQL 8 instance.

---

## 🚀 Usage

### Step 1 — Authenticate via OTP

```bash
# Request OTP
curl -X POST http://localhost:8080/api/auth/send-otp \
  -H "Content-Type: application/json" \
  -d '{"mobile": "+919876543210"}'

# Verify OTP — receive JWT
curl -X POST http://localhost:8080/api/auth/verify-otp \
  -H "Content-Type: application/json" \
  -d '{"mobile": "+919876543210", "otp": "482931"}'

# Response
# { "token": "eyJhbGciOiJIUzI1NiIsInR5...", "role": "PATIENT" }
```

### Step 2 — Book an Appointment (Patient)

```bash
curl -X POST http://localhost:8080/api/appointments/book \
  -H "Authorization: Bearer <your_jwt_token>" \
  -H "Content-Type: application/json" \
  -d '{
    "doctorId": 5,
    "date": "2025-11-15",
    "timeSlot": "10:00",
    "reason": "General checkup"
  }'
```

### Step 3 — Admin Dashboard Access

```bash
curl -X GET http://localhost:8080/api/admin/dashboard \
  -H "Authorization: Bearer <admin_jwt_token>"
```

---

## 📁 Project Structure

```
medibook/
│
├── 📂 src/main/java/com/medibook/
│   ├── 📂 config/               # Security config, JWT config, CORS
│   │   ├── SecurityConfig.java
│   │   └── JwtConfig.java
│   │
│   ├── 📂 controller/           # REST controllers (request/response handling)
│   │   ├── AuthController.java
│   │   ├── AppointmentController.java
│   │   ├── DoctorController.java
│   │   ├── PatientController.java
│   │   └── AdminController.java
│   │
│   ├── 📂 service/              # Business logic & transactional operations
│   │   ├── OtpService.java
│   │   ├── AppointmentService.java
│   │   ├── DoctorService.java
│   │   └── UserService.java
│   │
│   ├── 📂 repository/           # Spring Data JPA repositories
│   ├── 📂 entity/               # JPA entity classes (mapped to DB tables)
│   ├── 📂 dto/                  # Request/Response DTOs
│   ├── 📂 exception/            # Custom exceptions & global @ControllerAdvice
│   ├── 📂 security/             # JWT filter, UserDetailsService impl
│   └── 📂 util/                 # Helpers, constants, validators
│
├── 📂 src/main/resources/
│   ├── application.properties
│   ├── application-dev.properties
│   └── application-prod.properties
│
├── 📂 src/test/                 # Unit & integration tests
├── 📄 Dockerfile
├── 📄 docker-compose.yml
├── 📄 pom.xml
└── 📄 README.md
```

---

## 🗺️ Roadmap

| Status | Feature |
|---|---|
| ✅ Done | OTP-based authentication |
| ✅ Done | RBAC — Admin, Doctor, Patient |
| ✅ Done | Appointment booking & cancellation |
| ✅ Done | Doctor availability management |
| ✅ Done | `@Transactional` data integrity |
| 🔄 In Progress | Email + SMS notification service |
| 🔄 In Progress | Full Postman collection |
| 📌 Planned | Swagger / OpenAPI 3.0 documentation |
| 📌 Planned | Redis caching for OTP tokens |
| 📌 Planned | Prescription & medical records module |
| 📌 Planned | Video consultation booking |
| 📌 Planned | GitHub Actions CI/CD pipeline |
| 📌 Planned | Kubernetes deployment manifests |

---

## 🤝 Contributing

Contributions make open source thrive. Any improvements are **greatly appreciated**.

```bash
# 1. Fork the repository

# 2. Create your feature branch
git checkout -b feature/your-feature-name

# 3. Commit using Conventional Commits
git commit -m "feat: add prescription management module"

# 4. Push your branch
git push origin feature/your-feature-name

# 5. Open a Pull Request against main
```

### Guidelines

- Follow the existing package structure and code conventions
- Use [Conventional Commits](https://www.conventionalcommits.org/) for all messages
- Write or update tests for new functionality
- Ensure `mvn test` passes before submitting your PR
- For major changes, open an issue first to align on approach

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for full details.

---

## 👨‍💻 Author

<div align="center">

### Siva Gangadhara Rao Mutyala

**Java Backend Developer** · 3 years of production engineering  
Specializing in **Spring Boot · REST APIs · Spring Security · Microservices**  
Delivered systems processing **10,000+ daily transactions** in healthcare & fintech

<br/>

[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mutyalasivagangadhara@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/mutyalasiva)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/918074680643)

</div>

---

## 📣 For Recruiters & Hiring Managers

<div align="center">

> If this project caught your eye, I'd love to connect.

I'm a backend engineer with **3 years of hands-on production experience** in Java, Spring Boot, and microservices.  
I build systems that handle real-world load — not demos, but live platforms with real users.

**I'm open to:**
🏢 Full-time Backend / Java Engineer roles &nbsp;|&nbsp; 🔗 Contract backend projects &nbsp;|&nbsp; 🤝 Open-source collaboration

**What I bring:**
Clean, maintainable production-grade code · Security-first mindset · High-throughput system experience · Team-oriented engineering

<br/>

[![Hire Me](https://img.shields.io/badge/💼_Open_to_Work-Let's_Talk-0072FF?style=for-the-badge)](mailto:mutyalasivagangadhara@gmail.com)
[![GitHub Profile](https://img.shields.io/badge/Explore_More_Projects-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/mutyalasiva)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,100:0f2027&height=100&section=footer&text=Thanks+for+visiting!&fontSize=18&fontColor=7ecfff&fontAlignY=70&animation=fadeIn" width="100%"/>

⭐ **If this project helped you or impressed you — drop a star. It means a lot.**

`Crafted with precision · Hyderabad, India · 2025`

</div>
