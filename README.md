## SampleAPI - Minimal Web API with MongoDB

This project demonstrates how to create a minimal Web API using ASP.NET Core and integrate it with MongoDB for data storage. The implementation is based on the official tutorial and extended to support basic CRUD operations with MongoDB.

### Key Features

- **CRUD Operations**: Supports basic actions like Create, Read, Update, and Delete, providing full management capabilities for book collections.

- **MongoDB Integration**: Utilizes MongoDB as the database for efficient and scalable data storage.

- **Dependency Injection**: Configures services using ASP.NET Core's DI system.

- **Swagger Integration**: Provides an interactive UI for testing API endpoints.

### Requirements

- .NET 6.0 or later

- MongoDB installed locally or accessible remotely

- MongoDB Compass (optional for database management)

### Project Setup

1. Clone this repository:

   ```bash
   git clone https://github.com/PhamTrung1204/sampleapi.git
   ```

2. Open the project in Visual Studio.

3. Install necessary NuGet packages:

   ```bash
   dotnet add package MongoDB.Driver
   ```

4. Configure MongoDB settings in `appsettings.json`:

   ```json
   {
     "BookStoreDatabase": {
       "ConnectionString": "your_mongodb_connection_string",
       "DatabaseName": "BookStoreDB",
       "BooksCollectionName": "Books"
     }
   }
   ```

5. Build and run the application.

### API Endpoints

The following endpoints are available:

- `GET /api/Books`: Retrieves all books.
- `GET /api/Books/{id}`: Retrieves a specific book by ID.
- `POST /api/Books`: Adds a new book.
- `PUT /api/Books/{id}`: Updates an existing book.
- `DELETE /api/Books/{id}`: Deletes a book.

### How to Use

1. Run the application:

   ```bash
   dotnet run
   ```

2. Open Swagger UI in your browser:

   [https://localhost:7221/swagger/index.html](https://localhost:7221/swagger/index.html)

3. Use the Swagger interface to test API endpoints.

### Sample Data

The database includes the following initial documents:

```json
[
  {
    "Name": "Design Patterns",
    "Price": 54.93,
    "Category": "Computers",
    "Author": "Ralph Johnson"
  },
  {
    "Name": "Clean Code",
    "Price": 43.15,
    "Category": "Computers",
    "Author": "Robert C. Martin"
  }
]
```

### Achievements

- Successfully integrated MongoDB with ASP.NET Core.
- Developed a minimal Web API with CRUD operations.
- Gained experience in working with dependency injection and Swagger.

### Next Steps

- Add authentication and authorization.
- Implement a persistent database solution (e.g., Azure Cosmos DB or AWS DynamoDB).
- Create unit tests for API endpoints.

### Contributors

- **Trung Pham** ([GitHub](https://github.com/PhamTrung1204))

