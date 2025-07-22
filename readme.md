# Library App

## Description
Library App is a console-based library management system built with .NET 8 and C#. It demonstrates clean architecture principles, dependency injection, and JSON-based data persistence. The application allows users to search for patrons, manage book loans, and renew memberships through an interactive console interface.

## Project Structure
- GuidedProjectApp.sln
- AccelerateDevGitHubCopilot/
  - src/
    - Library.ApplicationCore/
      - Entities/
        - Author.cs
        - Book.cs
        - BookItem.cs
        - Loan.cs
        - Patron.cs
      - Enums/
        - EnumHelper.cs
        - LoanExtensionStatus.cs
        - LoanReturnStatus.cs
        - MembershipRenewalStatus.cs
      - Interfaces/
        - ILoanRepository.cs
        - ILoanService.cs
        - IPatronRepository.cs
        - IPatronService.cs
      - Services/
        - LoanService.cs
        - PatronService.cs
      - Library.ApplicationCore.csproj
    - Library.Infrastructure/
      - Data/
        - JsonData.cs
        - JsonLoanRepository.cs
        - JsonPatronRepository.cs
      - Library.Infrastructure.csproj
    - Library.Console/
      - Program.cs
      - ConsoleApp.cs
      - ConsoleState.cs
      - CommonActions.cs
      - Json/
        - Authors.json
        - Books.json
        - BookItems.json
        - Loans.json
        - Patrons.json
      - appSettings.json
      - Library.Console.csproj
    - tests/
      - UnitTests/
        - ApplicationCore/
          - LoanService/
            - ExtendLoan.cs
            - ReturnLoan.cs
          - PatronService/
            - ...
        - LoanFactory.cs
        - PatronFactory.cs
        - UnitTests.csproj

## Key Classes and Interfaces
- **Entities**: Represent core domain objects (`Author`, `Book`, `BookItem`, `Loan`, `Patron`).
- **Enums**: Define status and helper enums for business logic.
- **Interfaces**: Abstractions for repositories and services (`ILoanRepository`, `IPatronRepository`, `ILoanService`, `IPatronService`).
- **Services**: Business logic for loans and patrons (`LoanService`, `PatronService`).
- **Data Layer**: JSON-based repositories and data loader (`JsonData`, `JsonLoanRepository`, `JsonPatronRepository`).
- **ConsoleApp**: Main application controller handling user interaction and state transitions.

## Usage
1. **Build the Solution:**
   ```sh
   dotnet build
   ```
2. **Run the Console Application:**
   ```sh
   dotnet run --project AccelerateDevGitHubCopilot/src/Library.Console/Library.Console.csproj
   ```
3. **Follow the on-screen prompts** to search for patrons, manage loans, and renew memberships.

## License
This project is licensed under the MIT License.
