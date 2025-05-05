# Library App

## Description
The Library App is a console-based library management system built with C# and .NET 8.0. It allows users to manage patrons, loans, and books through a clean architecture design. The application uses JSON files for data persistence and supports features like patron search, loan management, and membership renewal.

## Project Structure
- **GuidedProjectApp.sln**: The main solution file for the project.
- **AccelerateDevGitHubCopilot/**
  - **README.md**: Placeholder for project documentation.
  - **src/**
    - **Library.ApplicationCore/**: Contains the core business logic and domain entities.
      - **Entities/**: Defines domain models like `Patron`, `Loan`, and `Book`.
      - **Enums/**: Contains enumerations used across the application.
      - **Interfaces/**: Defines interfaces for repositories and services.
      - **Services/**: Implements business logic services like `LoanService` and `PatronService`.
    - **Library.Console/**: Implements the console-based user interface.
      - **appSettings.json**: Configuration file for JSON data paths.
      - **CommonActions.cs**: Defines common user actions in the console app.
      - **ConsoleApp.cs**: Main application class managing the console interface.
      - **ConsoleState.cs**: Enum for managing application states.
      - **Program.cs**: Entry point for the application.
      - **Json/**: Folder containing sample JSON data files.
    - **Library.Infrastructure/**: Implements data access logic.
      - **Data/**: Contains classes like `JsonData`, `JsonPatronRepository`, and `JsonLoanRepository`.
  - **tests/**
    - **UnitTests/**: Contains unit tests for the application.

## Key Classes and Interfaces
- **Core Classes**:
  - `Patron`, `Loan`, `Book`: Domain models representing library entities.
  - `LoanService`, `PatronService`: Business logic services for managing loans and patrons.
- **Repositories**:
  - `IPatronRepository`, `ILoanRepository`: Interfaces for data access.
  - `JsonPatronRepository`, `JsonLoanRepository`: JSON-based implementations of the repositories.
- **Infrastructure**:
  - `JsonData`: Handles loading, saving, and populating JSON data.
- **Console**:
  - `ConsoleApp`: Main class managing the console-based user interface.
  - `ConsoleState`: Enum for application state transitions.
  - `CommonActions`: Enum for user actions in the console app.

## Usage
1. **Build the Project**:
   - Open the solution file `GuidedProjectApp.sln` in Visual Studio.
   - Build the solution to restore dependencies and compile the code.

2. **Run the Application**:
   - Set `Library.Console` as the startup project.
   - Run the application to interact with the library system via the console.

3. **Configuration**:
   - Update `appSettings.json` in the `Library.Console` project to specify paths for JSON data files.

4. **Unit Testing**:
   - Run the tests in the `UnitTests` project to verify the application's functionality.

## License
This project is licensed under the MIT License. See the LICENSE file for details.