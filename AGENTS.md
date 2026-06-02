
# Project: Customer API Service

## Overview
This is a Java Spring Boot REST API for customer data management.

## Stack
- Java 17
- Spring Boot 3
- Maven
- PostgreSQL
- JUnit 5 + Mockito

---

## Build & Run

- Build project:
  mvn clean package

- Run application:
  mvn spring-boot:run

---

## Testing

### Run all tests
- mvn test

### Run a single test class
- mvn -Dtest=CustomerServiceTest test

### Run a specific test method
- mvn -Dtest=CustomerServiceTest#shouldCreateCustomer test

### Run tests with coverage (JaCoCo)
- mvn clean verify

### Run integration tests only
- mvn failsafe:integration-test

---

## Code Style & Conventions

- Use constructor injection (no field injection)
- Follow REST naming conventions:
  - /customers
  - /customers/{id}
- Use DTOs for API responses
- Keep controllers thin, business logic in services

---

## Project Structure

- src/main/java → application code
- src/test/java → unit tests
- src/test/resources → test configs
- /db → database scripts

---

## Before Committing

Always run:
- mvn clean verify

Check:
- All tests pass
- No compile warnings
- Code formatted correctly

---

## Rules / Boundaries

Always:
- Write unit tests for new logic
- Update existing tests when modifying behavior

Ask first:
- Before modifying database schema
- Before refactoring public APIs

Never:
- Modify files under `/legacy/`
- Commit secrets (API keys, passwords)
- Skip tests when committing


