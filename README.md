# Task Board
This project is a Java application designed to simulate a task board system, allowing users to manage tasks (cards) within different columns. It demonstrates a layered architecture, applying Object-Oriented Programming (OOP) principles and common software design patterns for a robust and maintainable codebase.
## 🚀 Project Overview
The Task Board project provides a backend structure for managing tasks, organized into columns on a board. It includes functionalities for creating, querying, and potentially manipulating board columns and individual task cards.
## ✨ Key Features 
- Task Management: Ability to create, view, and manage tasks (cards).
- Column Organization: Tasks are organized into customizable board columns.
- Data Persistence: Integration with a database to store board, column, and card data.
- Business Logic: Dedicated service layer for handling core business rules related to task and board operations.
- Custom Exception Handling: Specific exceptions for business constraints (e.g., card blocked, card finished, entity not found).
- Data Transfer Objects (DTOs): Separation of data models for persistence and presentation/API layers.
- Basic User Interface (Console): A simple menu-driven interface for interacting with the task board system.
- Security (Basic): Basic security configuration using Spring Security, including password encoding and request authorization.
## 📚 Technologies & Concepts
- Java: The core programming language.
- Spring Boot: The framework used for rapid application development, dependency injection, and auto-configuration.
- Object-Oriented Programming (OOP): Applied throughout the project, demonstrating:
  - Encapsulation: Data protection through private fields and public accessors.
  - Abstraction: Use of interfaces or abstract classes for defining contracts.
  - Inheritance.
  - Polymorphism: (If different types of cards or columns behave differently).
- Layered Architecture: Clear separation of concerns into DTO, Exception, Persistence, Service, and UI layers.
- Data Persistence (JPA/Hibernate): Implied by persistence package with dao, entity, migration packages.
- Database Migration: Use of tools like Flyway or Liquibase for managing schema changes.
- Spring Security: For authentication and authorization.
- DTO Pattern: For efficient data transfer between layers.
- Service Layer Pattern: Encapsulating business logic.
- DAO/Repository Pattern: Abstracting database access.
- Custom Exceptions: For handling specific application errors gracefully.
## 📁 Project Structure
The project follows a standard Maven/Gradle structure, with core application logic residing in src/main/java/br/com/dio:

```bash
src/
└── main/
  └── java/
    └── br/
      └── com/
        └── dio/
        ├── config/             # Spring configuration classes (e.g., SecurityConfig)
        ├── dto/                # Data Transfer Objects (DTOs)
        │   ├── BoardColumnDTO.java
        │   ├── BoardColumnInfoDTO.java
        │   ├── BoardDetailsDTO.java
        │   └── CardDetailsDTO.java
        ├── exception/          # Custom application-specific exceptions
        │   ├── CardBlockedException.java
        │   ├── CardFinishedException.java
        │   └── EntityNotFoundException.java
        ├── persistence/        # Database interaction layer
        │   ├── config/         # Persistence configuration
        │   ├── converter/      # Data converters (e.g., Entity to DTO)
        │   ├── dao/            # Data Access Objects (Repositories)
        │   ├── entity/         # JPA Entities (database mappings)
        │   └── migration/      # Database migration scripts/logic
        ├── service/            # Business logic layer
        │   ├── BoardColumnQueryService.java
        │   ├── BoardQueryService.java
        │   ├── BoardService.java
        │   ├── CardQueryService.java
        │   └── CardService.java
        └── ui/                 # User Interface layer (console-based)
        ├── BoardMenu.java
        └── MainMenu.java
```

