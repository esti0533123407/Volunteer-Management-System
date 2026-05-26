# Volunteer Management System

A robust and scalable .NET 9.0 Core Web API designed for managing volunteers and their skills. This project follows clean architecture principles and implements the Repository Pattern to ensure high code maintainability, clear separation of concerns, and optimized data access.

---

## Technologies & Tools

* **Backend Framework:** .NET 9.0 (ASP.NET Core Web API)
* **Database & ORM:** SQL Server via Entity Framework Core (Code First approach)
* **Architecture:** Clean Architecture (Multi-layered setup)
* **Design Patterns:** Repository Pattern
* **API Documentation:** Swagger UI (OpenAPI)
* **Data Mapping:** AutoMapper
* **Security:** JWT Authentication

---

## Project Architecture

The solution is divided into distinct decoupled layers to enforce a clean separation of concerns:

* **Volunteer.Api:** The entry point of the application. Contains the Controllers, middleware, authentication setup, and handles incoming HTTP requests.
* **Volunteer.Service (Business Logic):** Manages the core business logic and orchestrates data flow between the API and data access layers.
* **Repository:** The Data Access Layer (DAL). Houses the DataContext, handles database transactions, and encapsulates raw query logic.
* **Volunteer.Entities:** Contains the domain models and core database entities (e.g., MyVolunteer, Skill).
* **DTOs (Data Transfer Objects):** Defines specialized data contract models optimized for safe mapping and data exposure across boundaries.

---

## Key Features

* **Full CRUD Operations:** Seamless management for creating, reading, updating, and deleting records.
* **Synchronous Data Layer:** Structured data retrieval optimized for straightforward integration and clear workflow tracing.
* **Automatic Migrations:** Data layer managed using EF Core migrations for transparent schema tracking.
* **Robust Error Handling:** API endpoints return standardized HTTP status responses (such as 200 OK, 404 Not Found, etc.) for easier client integration.

---

## Getting Started & Installation

### Prerequisites
* .NET 9 SDK
* SQL Server Express or LocalDB
* Visual Studio 2022 (with ASP.NET and web development workload)

### Running the Project Locally

1. **Clone the Repository:**
```bash
   git clone [https://github.com/tamaramitay2-pixel/Volunteer-Management-System.git](https://github.com/tamaramitay2-pixel/Volunteer-Management-System.git)
   cd Volunteer-Management-System
Configure the Database Connection:
Open the appsettings.json file inside the Volunteer.Api project and update your connection string:

JSON
   "ConnectionStrings": {
     "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=VolunteerDb;Trusted_Connection=True;"
   }
Apply Database Migrations:
Open the Package Manager Console in Visual Studio and run:

PowerShell
   Update-Database
Launch the Application:
Press F5 in Visual Studio or execute the following command in your terminal inside the API project directory:

Bash
   dotnet run
The interactive Swagger UI page will open automatically in your browser so you can test the live endpoints.

Developed as part of a final software engineering course evaluation project
