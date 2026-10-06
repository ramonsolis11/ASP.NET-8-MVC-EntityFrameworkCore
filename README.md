# ASP.NET 8 MVC + Entity Framework Core

CRUD application built with **ASP.NET Core MVC** and **Entity Framework Core**, using **SQL Server** as the persistence layer.

This repository demonstrates a conventional server-rendered .NET web application with a clear separation between presentation, controllers, data access, domain models and database migrations.

## Technical Scope

- ASP.NET Core MVC
- .NET 8
- Entity Framework Core
- SQL Server
- Razor Views
- Dependency Injection
- Code First migrations
- CRUD operations

## Architecture

```text
Browser
   |
   v
ASP.NET Core MVC
   |
   +--> Controllers
   |
   +--> Models
   |
   +--> Razor Views
   |
   +--> Data / DbContext
            |
            v
        SQL Server
```

The project follows the standard MVC request flow:

1. A request reaches an MVC controller.
2. The controller coordinates the use case.
3. Entity Framework Core interacts with SQL Server through the application data layer.
4. The controller returns the corresponding Razor View.

## Project Structure

```text
├── Controllers/
├── Datos/
├── Migrations/
├── Models/
├── Views/
├── Program.cs
├── CrudNet8MVC.csproj
└── ProyectoCrudNet8MVC.sln
```

## Core Capabilities

The application provides the fundamental operations expected from a CRUD workflow:

- Create records
- Read and list records
- Update existing records
- Delete records
- Persist changes through Entity Framework Core

## Requirements

- .NET 8 SDK
- Visual Studio 2022+ or another compatible IDE
- SQL Server / SQL Server LocalDB
- EF Core CLI tools if migrations will be managed from the command line

## Running Locally

Clone the repository:

```bash
git clone https://github.com/ramonsolis11/ASP.NET-8-MVC-EntityFrameworkCore.git
cd ASP.NET-8-MVC-EntityFrameworkCore
```

Restore dependencies:

```bash
dotnet restore
```

Review the database connection string in `appsettings.json` or the relevant environment-specific configuration file.

Apply migrations when required:

```bash
dotnet ef database update
```

Run the application:

```bash
dotnet run
```

## Engineering Focus

This project is useful as a compact reference for:

- MVC request/response lifecycle
- EF Core persistence
- relational database integration
- dependency injection in ASP.NET Core
- migration-based schema evolution
- organizing a small .NET application with maintainable boundaries

## Notes

The application targets **.NET 8**. The current project file includes Entity Framework Core SQL Server tooling and design-time dependencies used for persistence and migration management.

## Author

**Ramón Solís Núñez**  
Solution Architect · Technical Lead · .NET & Cloud Solutions
