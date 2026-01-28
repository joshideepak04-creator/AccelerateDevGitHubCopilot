# Library App

## Description
Library App is a console-based library management system built with .NET 8.0 and C#. It allows users to manage library operations such as managing patrons, books, loans, and memberships. The application uses a JSON-based data storage system and follows a clean architecture with a clear separation of concerns.

## Project Structure
- **AccelerateDevGitHubCopilot.sln**: Solution file for the project.
- **src**: Contains the source code for the application.
  - **Library.ApplicationCore**: Core domain layer containing business logic, entities, and interfaces.
    - **Entities**: Defines the core domain models such as `Book`, `Author`, `Patron`, and `Loan`.
    - **Enums**: Contains enumerations used across the application.
    - **Interfaces**: Defines interfaces for services and repositories.
    - **Services**: Contains the implementation of business logic services like `PatronService` and `LoanService`.
    - **Library.ApplicationCore.csproj**: Project file for the core library.
  - **Library.Console**: Console-based user interface for interacting with the library system.
    - **CommonActions.cs**: Defines common actions for user input.
    - **ConsoleApp.cs**: Main application logic for handling user interactions.
    - **ConsoleState.cs**: Enum representing the state of the console application.
    - **Json**: Contains JSON files for storing data such as books, authors, patrons, and loans.
    - **appSettings.json**: Configuration file for JSON file paths.
    - **Library.Console.csproj**: Project file for the console application.
    - **Program.cs**: Entry point of the application.
  - **Library.Infrastructure**: Data access layer for managing JSON-based data storage.
    - **Data**: Contains classes for handling JSON data, such as `JsonData`, `JsonPatronRepository`, and `JsonLoanRepository`.
    - **Library.Infrastructure.csproj**: Project file for the infrastructure library.
- **tests**: Contains unit tests for the application.
  - **UnitTests**: Test project for validating the functionality of core services.
    - **ApplicationCore**: Tests for services like `PatronService` and `LoanService`.
    - **UnitTests.csproj**: Project file for the test project.

## Key Classes and Interfaces
- **Core Entities**:
  - [`Library.ApplicationCore.Entities.Book`](src/Library.ApplicationCore/Entities/Book.cs): Represents a book in the library.
  - [`Library.ApplicationCore.Entities.Author`](src/Library.ApplicationCore/Entities/Author.cs): Represents an author of books.
  - [`Library.ApplicationCore.Entities.Patron`](src/Library.ApplicationCore/Entities/Patron.cs): Represents a library patron.
  - [`Library.ApplicationCore.Entities.Loan`](src/Library.ApplicationCore/Entities/Loan.cs): Represents a book loan.
- **Core Interfaces**:
  - [`Library.ApplicationCore.Interfaces.IPatronService`](src/Library.ApplicationCore/Interfaces/IPatronService.cs): Interface for patron-related operations.
  - [`Library.ApplicationCore.Interfaces.ILoanRepository`](src/Library.ApplicationCore/Interfaces/ILoanRepository.cs): Interface for loan data access.
- **Infrastructure**:
  - [`Library.Infrastructure.Data.JsonData`](src/Library.Infrastructure/Data/JsonData.cs): Handles loading and saving JSON data.
  - [`Library.Infrastructure.Data.JsonPatronRepository`](src/Library.Infrastructure/Data/JsonPatronRepository.cs): Repository for managing patron data.
  - [`Library.Infrastructure.Data.JsonLoanRepository`](src/Library.Infrastructure/Data/JsonLoanRepository.cs): Repository for managing loan data.
- **Console Application**:
  - [`Library.Console.ConsoleApp`](src/Library.Console/ConsoleApp.cs): Main application logic for user interaction.
  - [`Library.Console.CommonActions`](src/Library.Console/CommonActions.cs): Defines common user actions.

## Usage
1. Clone the repository:
   ```bash
   git clone <repository-url>