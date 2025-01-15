# CRUDProject

This Spring Boot application provides basic **CRUD** functionality to manage **User** and **Family** entities, with support for validation, pagination, filtering, and sorting. It also includes **Spring Boot Actuator** for health checks and application metrics.

## Features

- **User Management**: Create, retrieve, update, and delete users.
- **Family Management**: Add, retrieve, and remove family members associated with users.
- **Validation**: Input validation for all fields using **Hibernate Validator** annotations.
- **Pagination & Filtering**: Pagination for the `/users` endpoint and filtering by user status (**ACTIVE/INACTIVE**).
- **Error Handling**: Global exception handling for API errors and invalid inputs.
- **Health Checks & Metrics**: Integrated **Spring Boot Actuator** for application health checks and monitoring.

## API Endpoints

### User API

- **POST /users**: Create a new user.
- **GET /users**: Retrieve all users with pagination and status filtering.
- **GET /users/{id}**: Retrieve a user by ID.
- **PUT /users/{id}**: Update all details of a user.
- **PATCH /users/{id}**: Update specific user details.
- **DELETE /users/{id}**: Delete a user.

### Family API

- **POST /users/{userId}/family**: Add a family member for a user.
- **GET /users/{userId}/family**: Retrieve all family members of a user.
- **DELETE /users/{userId}/family/{familyId}**: Remove a family member from a user.
- **PUT /users/{userId}/family/{id}**: Update family member details.
- **PATCH /users/{userId}/family/{id}**: Partially update family member details.

## Technologies Used

- **Spring Boot**: Backend framework for creating the application.
- **Spring Data JPA**: For database interactions and entity management.
- **Hibernate Validator**: To validate inputs with annotations like `@NotNull`, `@Size`, `@Email`, etc.
- **Spring Boot Actuator**: For health checks and metrics collection.

