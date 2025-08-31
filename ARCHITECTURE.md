# Spring Boot CRUD Application - Software Architecture & Documentation

## Overview

This project is a simple CRUD (Create, Read, Update, Delete) application built with Spring Boot. It demonstrates the use of Spring Data JPA for database operations and follows a layered architecture for maintainability and scalability.

## Folder Structure

```
crudapp/
│   mvnw
│   mvnw.cmd
│   pom.xml
│
└───src/
    ├───main/
    │   ├───java/
    │   │   └───com/
    │   │       └───kittipak/
    │   │           └───crudapp/
    │   │               │   CrudappApplication.java
    │   │               ├───entity/
    │   │               │       Person.java
    │   │               └───repository/
    │   │                       PersonDAO.java
    │   │                       PersonRepository.java
    │   └───resources/
    │           application.properties
    └───test/
        └───java/
            └───com/
                └───kittipak/
                    └───crudapp/
                            CrudappApplicationTests.java
```

## File & Folder Details

### Root Level

- **README.md**: Project overview, setup instructions, and usage.
- **crudapp/mvnw, mvnw.cmd**: Maven wrapper scripts for building the project without requiring Maven to be installed globally.
- **crudapp/pom.xml**: Maven configuration file specifying dependencies and build settings.

### `src/main/java/com/kittipak/crudapp/`

- **CrudappApplication.java**: Main entry point for the Spring Boot application. Contains the `main` method to launch the app.

#### `entity/`

- **Person.java**: JPA entity class representing the `Person` table in the database. Contains fields, getters/setters, and annotations for ORM mapping.

#### `repository/`

- **PersonDAO.java**: (If present) Custom Data Access Object interface or implementation for advanced queries or business logic not covered by Spring Data JPA.
- **PersonRepository.java**: Spring Data JPA repository interface for `Person` entity. Provides CRUD operations and query method definitions.

### `src/main/resources/`

- **application.properties**: Configuration file for Spring Boot application settings (e.g., database connection, server port).

### `src/test/java/com/kittipak/crudapp/`

- **CrudappApplicationTests.java**: Unit and integration tests for the application, ensuring correct behavior of components.

## Architectural Layers

1. **Entity Layer**: Contains JPA entities (e.g., `Person.java`) that map to database tables.
2. **Repository Layer**: Contains interfaces (e.g., `PersonRepository.java`) for data access using Spring Data JPA.
3. **Service Layer** (not present in current structure, but recommended): Would contain business logic and service classes.
4. **Controller Layer** (not present in current structure, but recommended): Would handle HTTP requests and responses.

## Recommendations

- Add a `service` package for business logic.
- Add a `controller` package for REST endpoints.
- Expand test coverage in the `test` directory.

---

This documentation provides a high-level overview and detailed explanation of each file and folder in the project. Update as the project evolves.
