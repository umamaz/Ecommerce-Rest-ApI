# E-Commerce REST API

A RESTful backend application built with **Java and Spring Boot** for managing product categories through CRUD operations.

## Tech Stack

* Java
* Spring Boot
* Spring Data JPA
* Hibernate
* H2 Database
* Maven
* Postman

## Features

* Create product categories
* Retrieve all product categories
* Retrieve a category by ID
* Update product categories
* Delete product categories
* RESTful API endpoints
* HTTP status code handling
* Error handling with `ResponseStatusException`
* JPA/Hibernate database persistence
* H2 database console for development and testing

## Project Architecture

The application follows a layered architecture:

```text
Controller
    ↓
Service
    ↓
Repository
    ↓
Database
```

### Layers

**Controller**
Handles HTTP requests and exposes REST API endpoints.

**Service**
Contains the application/business logic for category operations.

**Repository**
Uses Spring Data JPA to interact with the database.

**Model**
Contains the JPA entity representing product categories.

## API Endpoints

| Method | Endpoint               | Description          |
| ------ | ---------------------- | -------------------- |
| GET    | `/api/categories`      | Get all categories   |
| GET    | `/api/categories/{id}` | Get a category by ID |
| POST   | `/api/categories`      | Create a category    |
| PUT    | `/api/categories/{id}` | Update a category    |
| DELETE | `/api/categories/{id}` | Delete a category    |

## Example Request

### Create Category

```http
POST /api/categories
Content-Type: application/json
```

```json
{
  "name": "Electronics"
}
```

## Error Handling

The application handles invalid requests and missing resources using appropriate HTTP status codes and `ResponseStatusException`.

For example, attempting to retrieve a category that does not exist returns an appropriate error response instead of silently failing.

## Database

The application uses **H2** as the database during development.

JPA and Hibernate are used for object-relational mapping and persistence.

The H2 console can be used to inspect database records during development.

## Testing

The REST API endpoints were tested using **Postman** to verify:

* CRUD operations
* Request/response behavior
* HTTP status codes
* Error handling
* Database persistence

## Running the Application

### Prerequisites

* Java 21 or compatible JDK
* Maven

### Clone the Repository

```bash
git clone https://github.com/umamaz/Ecommerce-Rest-ApI.git
cd Ecommerce-Rest-ApI
```

### Run with Maven

```bash
./mvnw spring-boot:run
```

On Windows:

```powershell
.\mvnw.cmd spring-boot:run
```

The application will start on the configured local server port.

## Project Structure

```text
src/
├── main/
│   ├── java/
│   │   └── com/ecommerce/project/
│   │       ├── controller/
│   │       ├── model/
│   │       ├── repositories/
│   │       └── service/
│   └── resources/
│       └── application.properties/
└── test/
    └── java/
```

## Author

**Umama Azhar**

Java | Spring Boot | REST APIs
