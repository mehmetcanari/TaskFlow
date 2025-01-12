<h1 align="center">TaskFlow API</h1>

###

<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/dot-net/dot-net-original.svg" height="40" alt="dot-net logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg" height="40" alt="csharp logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jetbrains/jetbrains-original.svg" height="40" alt="jetbrains logo"  />
</div>

###

<h2 align="center">TaskFlow API is a simple and efficient RESTful API built with .NET 9 using the Minimal API approach for managing tasks. It supports CRUD operations for task management, including creating, updating, deleting, and retrieving tasks. This API is designed for lightweight use with in-memory database for fast development and testing.</h2>

###

<h3 align="center">-FEATURES-<br><br>CRUD Operations: Create, Read, Update, Delete tasks<br><br>Minimal API: Efficient and easy-to-maintain API structure<br><br>DTO & Validation: Ensures data integrity and security with DTOs and validation<br><br>In-memory Database: Temporary storage for tasks using an in-memory list</h3>

###

<h2 align="left">Structure Markdown</h2>

###

<h3 align="left">📁 API/<br>├── 📁 Controllers/<br>│   ├── APIEndpoints.cs<br>│   ├── Program.cs<br>│   └── TaskFlowAPI.http<br>├── 📁 DTO/                                  <br>│   ├── CreateTodoDto.cs<br>│   ├── PatchTodoDto.cs<br>│   └── UpdateTodoDto.cs<br>└── 📁 Models/<br>    ├── TasksDatabase.cs<br>    └── TodoItem.cs</h3>

###

<h2 align="left">The API will be available at: <br>

</h2>

###

```http
http://localhost:5193
```

###

<h3 align="left">Retrieve all tasks. </h3>  
 

```http
GET http://localhost:5193/api/todos
```
###

<h3 align="left">

 Create a new task.
 </h3>
 
```http
POST localhost:5193/api/todos
Content-Type: application/json

{
    "Title": "Play Guitar",
    "Description": "Play Guitar for 30 minutes",
    "DueDate": "2029-07-01T00:00:00"
}
```

###

<h3 align="left">
  
Partial update a task.  
</h3>  

```http
PATCH http://localhost:5193/api/todos/1
Content-Type: application/json

{
    "IsCompleted": true,
    "DueDate": "2026-07-01T00:00:00"
}
```

###

<h3 align="left">
Fully update a task. </h3> 

```http
PUT localhost:5193/api/todos/1
Content-Type: application/json

{
    "Title": "Test Todo",
    "Description": "Sample Description",
    "isComplete": true,
    "DueDate": "2029-07-01T00:00:00"
}
```
###

<h3 align="left">
Delete a task. </h3> 

```http
DELETE localhost:5193/api/todos/1
```

