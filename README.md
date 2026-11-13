# Student Management System – C# with SQL Server

## Project Description

The Student Management System is a desktop application developed using C# and Microsoft SQL Server. It helps users manage student information efficiently by performing basic database operations.

The application uses ADO.NET to establish a connection between the C# application and SQL Server.

## Technologies Used

- C#
- .NET
- SQL Server
- ADO.NET
- Microsoft.Data.SqlClient
- Visual Studio

## Features

- Add new student records.
- View all student details.
- Update existing student information.
- Delete student records.
- Store student information in SQL Server.
- Retrieve data from the database.

## Database Details

**Database Name:** StudentDB

**Table Name:** Students

| Column Name | Data Type | Description |
|---|---|---|
| Id | INT | Student ID (Primary Key) |
| Name | VARCHAR(50) | Student Name |
| Age | INT | Student Age |
| Department | VARCHAR(50) | Department Name |

## Database Setup

### Step 1: Create Database

```sql
CREATE DATABASE StudentDB;
```

### Step 2: Create Table

```sql
USE StudentDB;

CREATE TABLE Students
(
    Id INT IDENTITY(1,1) PRIMARY KEY,
    Name VARCHAR(50),
    Age INT,
    Department VARCHAR(50)
);
```

## Database Connectivity

The application uses ADO.NET to connect C# with SQL Server.

### Connection String

```csharp
string connectionString =
    @"Server=YOUR_SERVER_NAME;
      Database=StudentDB;
      Trusted_Connection=True;
      TrustServerCertificate=True;";
```

Replace `YOUR_SERVER_NAME` with your SQL Server instance name.

## ADO.NET Components

| Component | Purpose |
|---|---|
| SqlConnection | Connects to SQL Server |
| SqlCommand | Executes SQL queries |
| SqlDataReader | Reads database records |
| SqlDataAdapter | Retrieves data |
| DataTable | Stores data in memory |

## CRUD Operations

CRUD represents four basic database operations.

1. **Create** – Insert new student records.
2. **Read** – Retrieve and display student records.
3. **Update** – Modify existing student details.
4. **Delete** – Remove student records.

## Project Structure

```text
StudentManagement/
│
├── Database/
│   └── StudentDB.sql
│
├── Models/
│   └── Student.cs
│
├── Data/
│   └── DatabaseConnection.cs
│
├── Views/
│   └── MainWindow.xaml
│
├── MainWindow.xaml.cs
│
└── README.md
```

## How to Run the Project

1. Install Visual Studio.
2. Install SQL Server and SQL Server Management Studio.
3. Create the StudentDB database.
4. Execute the SQL table creation script.
5. Open the project in Visual Studio.
6. Install the required SQL client NuGet package.
7. Update the connection string with your SQL Server instance name.
8. Build and run the application.

## Learning Outcomes

- Understanding SQL Server database concepts.
- Learning ADO.NET connectivity.
- Implementing CRUD operations using C#.
- Executing SQL queries from C#.
- Understanding database integration in .NET applications.

## Author

**Mathivathanan M**

C# | .NET | SQL Server | ADO.NET
