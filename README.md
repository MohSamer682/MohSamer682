<div align="center">

# Mohamed Samer Abdalla

### Software Engineer · Java · Spring Boot · Quality Engineering

*I build backend systems that are clean, tested, and ready for production, with a QA engineer's instinct for what can go wrong.*

<p>
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
</p>

<p>
  <a href="mailto:muhamedsamer286@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://www.linkedin.com/in/mohamed-samer"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <img src="https://img.shields.io/badge/Based_in-Egypt-informational?style=flat-square" alt="Location" />
  <img src="https://img.shields.io/badge/Open_to-Java_Backend_Roles-success?style=flat-square" alt="Open to work" />
</p>

</div>

---

## About

I'm a software engineer with 2+ years in enterprise systems, working across testing, requirements analysis, and delivery. That background shapes how I write code: I think about failure modes, API contracts, and testability from the first commit.

I'm focused on **Java backend engineering**, specifically REST API design, data modeling with JPA, layered architecture, and automated testing. I also use AI tools (Claude Code, Codex) in my workflow for analysis, test generation, and debugging, and I always review the output myself.

**Currently**
- Building Spring Boot backend projects (below)
- Completing the *IBM Java Developer Professional Certificate*
- Targeting **Java Backend Developer**, **Spring Boot Developer**, and **Java QA Automation Engineer** roles

---

## Tech Stack

| Area | Technologies |
|------|--------------|
| **Languages** | ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) |
| **Frameworks** | ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![Spring Data JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=flat-square&logo=spring&logoColor=white) ![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white) ![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=flat-square&logo=hibernate&logoColor=white) |
| **Data** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) |
| **Testing** | ![JUnit5](https://img.shields.io/badge/JUnit_5-25A162?style=flat-square&logo=junit5&logoColor=white) ![Mockito](https://img.shields.io/badge/Mockito-78A641?style=flat-square&logoColor=white) ![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=flat-square&logo=selenium&logoColor=white) ![TestNG](https://img.shields.io/badge/TestNG-FF6F00?style=flat-square&logoColor=white) ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white) ![JMeter](https://img.shields.io/badge/JMeter-D22128?style=flat-square&logo=apachejmeter&logoColor=white) |
| **Tooling** | ![Maven](https://img.shields.io/badge/Maven-C71A36?style=flat-square&logo=apachemaven&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Jira](https://img.shields.io/badge/Jira-0052CC?style=flat-square&logo=jira&logoColor=white) ![Azure DevOps](https://img.shields.io/badge/Azure_DevOps-0078D7?style=flat-square&logo=azuredevops&logoColor=white) |
| **AI-assisted** | ![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=anthropic&logoColor=white) ![Codex](https://img.shields.io/badge/Codex-412991?style=flat-square&logo=openai&logoColor=white) |

---

## Featured Projects

### 1. Employee Information System

A layered **Spring Boot REST API** for employee-record management, built around clean separation of concerns, validated input, and consistent error handling.

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Data JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=flat-square&logo=spring&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![OpenAPI](https://img.shields.io/badge/OpenAPI-6BA539?style=flat-square&logo=openapiinitiative&logoColor=white)

**Highlights**
- Full **CRUD** over a REST contract with correct HTTP semantics and status codes
- **DTO layer** separating API models from JPA entities
- **Bean Validation** on request payloads, with centralized error responses via `@RestControllerAdvice` (RFC 7807 `ProblemDetail`)
- **Pagination and sorting** through Spring Data
- Interactive API documentation with **Swagger / OpenAPI**
- Unit tests (JUnit 5, Mockito) and controller tests (MockMvc)

**Architecture**

```mermaid
flowchart LR
    C[Client] --> CT[Controller]
    CT --> SV[Service]
    SV --> RP[Repository]
    RP --> DB[(MySQL)]
    CT -. validation .-> EH[Exception Handler]
    SV -. mapping .-> DTO[DTO Mapper]
```

**Endpoints**

| Method | Path | Description |
|--------|------|-------------|
| `POST` | `/api/employees` | Create an employee |
| `GET` | `/api/employees` | List employees (paged, sortable) |
| `GET` | `/api/employees/{id}` | Get one employee |
| `PUT` | `/api/employees/{id}` | Update an employee |
| `DELETE` | `/api/employees/{id}` | Delete an employee |

---

### 2. AI-Powered Resume Screener

A **Spring Boot + LLM** service that ranks candidates against a job description. Upload a JD and a batch of resumes; the system extracts text, scores each candidate with structured LLM output, and returns a ranked shortlist with a justification for every score.

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Batch](https://img.shields.io/badge/Spring_Batch-6DB33F?style=flat-square&logo=spring&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MinIO](https://img.shields.io/badge/MinIO-C72E49?style=flat-square&logo=minio&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

**Highlights**
- **PDF text extraction and cleanup** with Apache PDFBox
- **Prompt engineering** for skill extraction, returning structured JSON that is validated before use
- **Asynchronous batch scoring** for large resume sets (Spring Batch)
- **Configurable scoring weights** (skills, experience, education) per job description
- **Ranked shortlist** with per-candidate justification, exportable to Excel
- Resume files stored in **MinIO**, results in **PostgreSQL**, everything runnable with **Docker Compose**

**Pipeline**

```mermaid
flowchart LR
    U[Upload JD + Resumes] --> API[REST API]
    API --> S[(MinIO)]
    API --> B[Batch Job]
    B --> P[PDFBox Extraction]
    P --> L[LLM Scoring]
    L --> V[JSON Validation]
    V --> D[(PostgreSQL)]
    D --> R[Ranked Shortlist]
    R --> X[Excel Export]
```

---

### 3. Test Generator: Java & OOP

A Java application that builds tests from instructor-provided questions, with object-oriented design applied to question management, test generation, and output.

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)

---

### 4. Active Accident Prevention: Graduation Project (A+)

A vehicle-safety prototype combining **lane-departure warning** and **traffic-sign detection**. A HuskyLens AI camera and sensors recognize signs and alert the driver when the vehicle drifts out of its lane.

![Arduino](https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=arduino&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine_Learning-FF6F00?style=flat-square&logoColor=white)

---

## Experience

| Role | Company | Period |
|------|---------|--------|
| **Software Test Engineer** | Madkour Technology | Oct 2025 – Present |
| **System Engineer** | Paragon Developments | Mar 2024 – Sep 2025 |
| **Software Engineering Intern** | ACUD | Aug 2023 – Jan 2024 |

- Validate an enterprise platform end to end: functional, regression, role-based access, and **JMeter performance testing**
- Build **AI-assisted QA workflows** that produce test plans, cases, and reports, reviewed before use
- Translate stakeholder needs into requirements and user stories through gap analysis
- Tested Zoho CRM, Odoo HR, Procore, Autodesk Docs, and an ERP system

---

## Engineering Principles

- **Clean layering:** controllers stay thin, business rules live in services, persistence stays behind repositories
- **Contract first:** explicit DTOs, validation, and predictable error responses
- **Test what matters:** unit tests for logic, slice tests for the web layer, integration tests against real databases
- **Reproducible setups:** Docker for local environments, Maven for builds
- **Review everything:** AI-generated code and tests get the same scrutiny as any other change

---

## Education & Learning

- **B.Sc. Software Engineering**, Arab Academy for Science, Technology and Maritime Transport (2019 – 2023)
- **IBM Java Developer Professional Certificate**, Coursera *(in progress)*
- **Java Spring Boot 3 & Spring 6**, Udemy *(completed)*
- **Software Testing Bootcamp**, Nezam Academy
- **Performance Testing with JMeter**, SWQ Academy

---

## Let's Connect

I'm open to Java backend and Spring Boot opportunities, and happy to talk about API design, testing strategy, or AI-assisted engineering.

<div align="center">

[![Email](https://img.shields.io/badge/muhamedsamer286@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:muhamedsamer286@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mohamed-samer)

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0e75b6,100:6DB33F&height=90&section=footer" alt="footer" />

</div>
