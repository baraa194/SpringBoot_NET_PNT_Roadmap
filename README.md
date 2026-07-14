# 🏥 Clinic Management System: Spring Boot Intensive 12-Session Roadmap



## 🗺️ Curriculum Overview

### 📍 Session 1: Spring Fundamentals & Core Architecture
* **Core Concepts:**
  * Understanding the Java Ecosystem: JDK, JRE, and JVM.
  * Dependency Management & Build Automation with Maven (`pom.xml`, Dependencies, Repositories, Lifecycle).
  * Spring Framework vs. Spring Boot: What happens under the hood?
  * Inversion of Control (IoC) Container & Bean Lifecycle.
  * Dependency Injection (DI) Types (Constructor vs. Field Injection).
  * Core Spring Annotations: `@Component`, `@Service`, `@Repository`, `@Autowired`.
  * Embedded Tomcat Server & introductory overview of Layered Architecture.
* **Hands-on / Practical Application:**
  * Developing local environment setup and bootstrapping a clean Spring Boot project.

### 📍 Session 2: REST API Fundamentals & Endpoints
* **Core Concepts:**
  * The HTTP Protocol: Methods (GET, POST, PUT, DELETE, PATCH), Headers, and Request/Response lifecycle.
  * Working with JSON data and proper HTTP Status Codes.
  * Developing Controllers using `@RestController` and `@RequestMapping`.
  * Managing request payloads and parameters using `@PathVariable` and `@RequestBody`.
* **Hands-on / Practical Application:**
  * Implementing the first REST endpoints: `POST /patients` and `GET /patients` using mock data.

### 📍 Session 3: Persistence Layer, ORM & PostgreSQL Integration
* **Core Concepts:**
  * Relational Database Management Systems: PostgreSQL setup.
  * Database configuration via `application.properties` (Datasource config, ddl-auto).
  * Object-Relational Mapping (ORM) and Hibernate basics.
  * JPA Entity Mapping: `@Entity`, `@Table`, `@Column`, `@Id`, `@GeneratedValue`.
  * The Repository Pattern: Utilizing Spring Data JPA's `JpaRepository`.
  * Reducing boilerplate code using Lombok basics (`@Data`, `@Getter`, `@Setter`, `@NoArgsConstructor`, `@AllArgsConstructor`).
* **Hands-on / Practical Application:**
  * Connecting the application to a local PostgreSQL instance and mapping/persisting Patient records directly to the database.

### 📍 Session 4: Patient Management & Data Operations
* **Core Concepts:**
  * Implementing HTTP verbs for safe and idempotent operations: `@GetMapping`, `@PostMapping`, `@PutMapping`, `@DeleteMapping`.
  * Best practices for designing Clean & Scalable Endpoints.
  * Data Integrity & Transaction control basics.
* **Hands-on / Practical Application:**
  * Creating the full suite of Patient Management endpoints and integrating them with the PostgreSQL database.

### 📍 Session 5: DTO Pattern & Service Layer Decoupling
* **Core Concepts:**
  * The Data Transfer Object (DTO) Pattern: Why exposing Database Entities directly to the API layer is a major security and design anti-pattern.
  * Separating concerns with a dedicated Service Layer (Business Logic encapsulation).
  * Manual Entity-to-DTO & DTO-to-Entity mapping techniques.
* **Hands-on / Practical Application:**
  * Complete architectural refactoring of the Patient Module to introduce DTOs and clean decoupling between layers.

### 📍 Session 6: Doctor Module & Relationship Mapping
* **Core Concepts:**
  * Database Relationships: Designing One-to-Many (`@OneToMany`) and Many-to-One (`@ManyToOne`) associations.
  * Defining ownership in relationships using `mappedBy` and customizing foreign keys via `@JoinColumn`.
  * Understanding Cascade Types (`PERSIST`, `MERGE`, `REMOVE`, `ALL`) and Fetch Strategies (`LAZY` vs. `EAGER`).
* **Hands-on / Practical Application:**
  * Building the Doctor and Department modules, establishing relationships, and implementing APIs to dynamically assign Doctors to Departments.

### 📍 Session 7: Appointment Scheduling & Business Rules
* **Core Concepts:**
  * Designing complex relationships (Many-to-Many mapping considerations).
  * Enforcing Domain Business Rules (e.g., preventing double-booking, validating operating hours).
  * Handling Date and Time data types in Java: `LocalDate` and `LocalTime`.
* **Hands-on / Practical Application:**
  * Implementing the Appointment Scheduler API with strict validation and business logic rules.

### 📍 Session 8: Robust Data Validation
* **Core Concepts:**
  * Implementing Input Validation at the API controller boundary (Jakarta Validation API).
  * Utilizing standard validation annotations: `@Valid`, `@NotNull`, `@NotBlank`, `@Email`, `@Size`, `@Min`, `@Max`.
  * Validating nested request payloads.
* **Hands-on / Practical Application:**
  * Securing all REST request payloads across the entire system and rejecting invalid data payloads with descriptive errors.

### 📍 Session 9: Global Exception Handling & Logging
* **Core Concepts:**
  * Professional error propagation: Handling business rule violations and runtime errors.
  * Decoupling exception logic from Controllers using `@ControllerAdvice` and `@ExceptionHandler`.
  * Intercepting and customized handling of `MethodArgumentNotValidException` to return clean validation error models to the client.
  * Implementing enterprise logging with Slf4j instead of standard console printing.
* **Hands-on / Practical Application:**
  * Developing a unified Global Exception Handler returning consistent, clean JSON error responses across the entire API suite.

### 📍 Session 10: Enterprise Security & Authentication
* **Core Concepts:**
  * Fundamentals of Web Security, Authentication (Who are you?), and Authorization (What can you do?).
  * Introduction to Spring Security architecture.
  * Securing user credentials using a cryptographic hashing algorithm (`BCryptPasswordEncoder`).
  * Modeling user roles, authorities, and access levels.
* **Hands-on / Practical Application:**
  * Building safe User Registration and Login endpoints with password encryption.

### 📍 Session 11: JWT (JSON Web Tokens) & Role-Based Authorization
* **Core Concepts:**
  * State vs. Stateless APIs: The architecture of Token-Based Authentication.
  * Anatomy of a JSON Web Token (Header, Payload, Signature).
  * Implementing a Custom JWT Filter within the Spring Security chain to intercept incoming requests.
  * Role-Based Access Control (RBAC): Restricting system actions by roles (`ADMIN`, `DOCTOR`, `PATIENT`).
* **Hands-on / Practical Application:**
  * Securing all API endpoints with JWT, requiring authentication, and enforcing role-based permissions on specific actions.

### 📍 Session 12: Medical Records, Query Optimization, & Production Readiness
* **Core Concepts:**
  * Advanced Entity relations: Designing Medical Records and Prescriptions workflows.
  * Handling large datasets: Pagination & Sorting using `Pageable` and `Sort` parameters.
  * Custom database operations: Derived Queries vs. explicit `@Query` annotations (JPQL).
  * API Self-Documentation: Integrating Swagger UI for interactive OpenAPI documentation.
  * Compiling, packaging (`.jar` build), and preparing the backend for production execution.
* **Hands-on / Practical Application:**
  * Implementing the Medical Records and Prescription modules, building optimized search APIs with filtering/pagination, documenting the full system with Swagger, and generating a runnable production JAR.

---

## 🛠️ Tech Stack & Key Tools
* **Language:** Java 17+
* **Framework:** Spring Boot (Spring Data JPA, Spring Security)
* **Database:** PostgreSQL
* **ORM:** Hibernate
* **Authentication:** JWT (JSON Web Tokens)
* **Documentation:** Swagger / OpenAPI UI
* **Build Tool:** Maven
