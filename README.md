# 🏢 Employee Admin Portal – Enterprise Web API

A production-ready RESTful Web API built using **ASP.NET Core** and **Entity Framework Core** for managing employee records efficiently.

This API provides full CRUD functionality and follows enterprise-level development practices such as DTO usage, dependency injection, and RESTful standards.

---

## 📌 Project Overview

The Employee Admin Portal API allows:

- ✅ Create Employee
- ✅ Get All Employees
- ✅ Get Employee By ID
- ✅ Update Employee
- ✅ Delete Employee

Designed for scalable HR and enterprise backend systems.

---

## 🛠️ Technology Stack

- ASP.NET Core Web API
- Entity Framework Core
- SQL Server
- C#
- RESTful Architecture
- Dependency Injection

---

## 📁 Project Structure

```
EmployeeAdminPotal
│
├── Controllers
│   └── EmployeesController.cs
│
├── Data
│   └── ApplicationDbContext.cs
│
├── Models
│   ├── Entities
│   │   └── Employee.cs
│   ├── AddEmployeeDto.cs
│   └── UpdateEmployeeDto.cs
│
├── appsettings.json
└── Program.cs
```

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/EmployeeAdminPotal.git
cd EmployeeAdminPotal
```

---

### 2️⃣ Configure Database

Update `appsettings.json`:

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=YOUR_SERVER;Database=EmployeeDb;Trusted_Connection=True;TrustServerCertificate=True;"
}
```

---

### 3️⃣ Apply Migrations

Using Package Manager Console:

```bash
Add-Migration InitialCreate
Update-Database
```

Or using .NET CLI:

```bash
dotnet ef migrations add InitialCreate
dotnet ef database update
```

---

### 4️⃣ Run the Application

```bash
dotnet run
```

Default API URL:

```
https://localhost:5001
```

---

# 📡 API Endpoints

## 🔹 Get All Employees

**GET**
```
/api/employees
```

---

## 🔹 Get Employee By ID

**GET**
```
/api/employees/{id}
```

Example:
```
/api/employees/1
```

---

## 🔹 Create Employee

**POST**
```
/api/employees
```

Request Body:

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "9876543210",
  "salary": 50000
}
```

---

## 🔹 Update Employee

**PUT**
```
/api/employees/{id}
```

Request Body:

```json
{
  "name": "John Updated",
  "email": "johnupdated@example.com",
  "phone": "9876543211",
  "salary": 60000
}
```

---

## 🔹 Delete Employee

**DELETE**
```
/api/employees/{id}
```

---

# 🗃️ Employee Entity

```csharp
public class Employee
{
    public int Id { get; set; }
    public string Name { get; set; }
    public string Email { get; set; }
    public string Phone { get; set; }
    public decimal Salary { get; set; }
}
```

---

# 🔒 Enterprise Best Practices Used

- DTO Pattern
- Dependency Injection
- Clean RESTful Design
- Proper HTTP Status Codes
- Separation of Concerns
- Entity Framework Core Integration

---

# 📈 Future Enhancements

- JWT Authentication
- Role-Based Authorization
- Global Exception Handling Middleware
- Logging (Serilog)
- Pagination & Filtering
- Repository & Service Pattern
- Unit Testing (xUnit)
- Docker Support
- CI/CD Integration

---

# 👨‍💻 Author

**Saikat Ghosh**  
ASP.NET Core Developer  

---

⭐ If you like this project, please give it a star!
