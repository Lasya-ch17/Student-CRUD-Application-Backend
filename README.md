# Student Management REST API

A simple **CRUD (Create, Read, Update, Delete)** REST API built using **Spring Boot**, **Spring Data JPA**, and **MySQL**. This project demonstrates how to build RESTful web services following a layered architecture with Controller, Service, and Repository layers.

## Features

* Create a new student
* Retrieve all students
* Retrieve a student by ID
* Update student details
* Delete a student
* RESTful API design
* MySQL database integration
* Spring Data JPA for database operations

## Tech Stack

* Java 17+
* Spring Boot
* Spring Web
* Spring Data JPA
* MySQL
* Maven
* Postman (for API testing)

## Project Structure

```text
src
└── main
    ├── java
    │   └── com.example.studentmanagement
    │       ├── controller
    │       │   └── StudentController.java
    │       ├── service
    │       │   └── StudentService.java
    │       ├── repository
    │       │   └── StudentRepository.java
    │       ├── model
    │       │   └── Student.java
    │       └── StudentManagementApplication.java
    └── resources
        └── application.properties
```

## REST API Endpoints

| Method | Endpoint         | Description                |
| ------ | ---------------- | -------------------------- |
| POST   | `/students`      | Create a new student       |
| GET    | `/students`      | Retrieve all students      |
| GET    | `/students/{id}` | Retrieve a student by ID   |
| PUT    | `/students/{id}` | Update an existing student |
| DELETE | `/students/{id}` | Delete a student           |

## Sample JSON

```json
{
    "name": "John Doe",
    "email": "john@example.com",
    "department": "Computer Science"
}
```

## Database Configuration

Update the `application.properties` file with your MySQL credentials.

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/studentdb
spring.datasource.username=your_username
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

## Running the Project

1. Clone the repository.

```bash
git clone https://github.com/your-username/student-management-api.git
```

2. Navigate to the project directory.

```bash
cd student-management-api
```

3. Configure MySQL in `application.properties`.

4. Run the application.

```bash
mvn spring-boot:run
```

or run the `StudentManagementApplication` class directly from your IDE.

The application will start on:

```text
http://localhost:8080
```

## Testing the API

You can test the endpoints using:

* Postman
* Insomnia
* cURL

Example:

```http
POST http://localhost:8080/students
```

```http
GET http://localhost:8080/students
```

```http
GET http://localhost:8080/students/1
```

```http
PUT http://localhost:8080/students/1
```

```http
DELETE http://localhost:8080/students/1
```

## Learning Outcomes

Through this project, I learned:

* Building REST APIs using Spring Boot
* Layered architecture (Controller, Service, Repository)
* Dependency Injection
* Spring Data JPA and Hibernate
* CRUD operations with MySQL
* Request mapping annotations (`@GetMapping`, `@PostMapping`, `@PutMapping`, `@DeleteMapping`)
* Handling JSON requests and responses with `@RequestBody`
* Testing APIs using Postman

## Future Improvements

* Input validation using Bean Validation
* Global exception handling
* Pagination and sorting
* Search functionality
* Swagger/OpenAPI documentation
* Unit and integration testing
* Authentication and authorization using Spring Security

GitHub: https://github.com/lasya-ch17
