## Software Development Life Cycle (SDLC)
```
I am a software engineer and would like a detailed overview of the software development life cycle and how it can be applied to a project.  Please provide a summary of the key phases. Include best practices and methodologies that can be used in each phase.
```

## Asynchronous Programming in C#
```
Where in the C# documentation can i learn about threading and  asynchronous operations? I will need a link to the reference.
```
```
Summarize the key points at this link: https://learn.microsoft.com/en-us/dotnet/csharp/asynchronous-programming/async-scenarios and provide a real world example of how the async/await pattern can be used in a C# application.
```

## Data Generation
```
Generate a sample JSON array of 10 rows of sample data based on the following criteria:
- The data should include the following keys: 
employee ID (unique and random in the range 1 to 100),
department name (randomly assigned to one of the following departments: HR, Engineering, Sales),
first name,
last name,
hourly rate ($25.00 to $75.00, standard deviation of $7.65)
```

```
Generate a C# class in namespace 'Inventory.Models' to model the JSON schema.
```

```
Assuming the data is consumable over http://localhost:6543/employees, how would I consume this JSON data using C#? The employee data can be accessed using an HTTP GET request.
```
```
How would I consume the JSON data from the previous question using Postman?
```

## Service-Based Architecture Project Plan
```
Can you assist with developing a project plan for a service-based architecture using C# with ASP.NET and angular.io client side components. 
- It is important the the project plan adheres to best practices (SOLID principles), including security and testing. 
- I do not want to see any sample code in the response.
```

```
How would I design and implement the plan? Show me sample code with steps. Pause after each step to give me time to review and critique
```

## System Design
```
I am a leading a team of systems engineers. I need advise on how to plan, design, and implement the following tasks:
- Create a cloud environment using Azure.
- Set up a web server.
- Set up a load balancer for the web server.
- Set up a database server.
- Configure networking (e.g., VPC, subnets, security groups).
- Implement security measures for the infrastructure.
Include recommended tools an a proposed workflow for each task.
```

## Planning a Web-Based Invoicing Application
```
I am an experienced C# developer and need help planning a web-based invoicing application. I want to use ASP.NET Web API for the backend with ReactJS components for client-side rendering. The application should be able to:
- have a RESTful API for managing invoices and clients
- use a NoSQL database like MongoDB for data storage
- have invoice management logic that makes it easy to add and remove invoice items and clients
- generate reports for billing and ageing
- have a user-friendly interface for creating and managing invoices
- have a secure authentication and authorization system
- implement error handling and logging for better maintainability
Break down the requirements into smaller tasks and provide a project plan as part of your response. I don't need code, just a project plan. 
```
```
I also need help creating a test plan for the application that includes unit tests, integration tests, and end-to-end tests. My team has experience using MSTest. The application is built using C# with ASP.NET Core for the backend and ReactJS for the frontend. The test plan should include:
- Test objectives
- Test strategy
- Test environment
- Test schedule
- Test resources
- Test deliverables
```

## User Authentication
```
How can I securely handle user authentication for a .NET API service using JWT tokens? Please provide a sample implementation.
```

## Static Analysis
```
Explain how to perform local and remote static analysis .NET applications using GitHub CodeQL. We use Visual Studio for development and are not currently performing static analysis. We do have experience with GitHub Actions.
```

## SQL
```
Review and explain the following T-SQL stored procedure. 
- Suggest any enhancements that would improve performnce, security, and maintainability.  
- Provide a sample of the improved procedure.

CREATE PROCEDURE GetEmployeeDetailsByDepartment
    @DepartmentName NVARCHAR(MAX)
AS
BEGIN
    -- No error handling
    -- Dynamic SQL introduces SQL injection vulnerability
    DECLARE @Query NVARCHAR(MAX)
    SET @Query = 'SELECT e.id, e.HourlyRate, d.DepartmentName 
                  FROM HourlyEmployees e, Departments d 
                  WHERE e.id = d.EmployeeID 
                  AND d.DepartmentName = ''' + @DepartmentName + ''''

    EXEC(@Query) -- Executes the dynamic SQL
END
```

## TDD xUnit Test for Employees Class
```
Create a 'xUnit' unit test for a C# class 'Employees'.
The class has a method 'HighEarners' that returns a vector of employees who earn more than 100,000.
The employee class has a name and a salary. The method should return a vector of employees who earn more than 100,000.
Edge cases:
The test should include a test case where the vector is empty, and another where the vector has one employee. In both cases, the method should return an empty vector.
```

```
Modify the Employees class to include a HighEarners method accepts a function expression (lambda) strategy in the form: (double) => boolean.
Update the unit test class EmployeesTests to test the modified HighEarners method.
``` 

