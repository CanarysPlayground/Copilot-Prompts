# Copilot Prompt Examples for Various Roles

This README provides a collection of prompts to use directly in Copilot sessions for different engineering roles and scenarios. Copy and use these prompts as needed.

---

## Inline Editor Comments

// Write a function to fetch list of copilot users using GitHub API.

// Write a Bubble Sort program that sorts exactly 5 numbers in ascending order.

---

## Prompt Engineering Prompts

**Generic Prompt:**
Write a Java class to store and display student details.

**Detailed Prompt:**
Create a class named Student with fields: name, age, and grade. Add a constructor to initialize the fields and add a method to display student details. In the main method, create a Student object and call the display method.

**Generic Prompt:**
Write a Dockerfile for a Node.js application.

**Detailed Prompt:**
Create a Dockerfile to run a Node.js app. Use the official Node.js LTS image as the base image. Copy package.json and install dependencies and copy the application source code and expose on port 3000. Define the command to run the app using 'node app.js'.

**Generic Prompt:**
Create a simple HTML page that shows a list of story book recommendations.

**Detailed Prompt:**
Create an HTML page that shows book recommendations with title, rating, description, and poster image for each Book.

---

## Role-Based Prompt

As a full stack developer, create a full-stack web application for a task management system using React for frontend and Node.js + Express for backend. Include user authentication, CRUD operations for tasks, and API routes. Suggest how to structure the project and define key classes and functions. And explain the entire application.

---

## Persona-Specific Use Cases

### Project Managers

**Prompts:**

Use Readme.md file

Recommend a technology stack suitable for implementing these requirements.

Generate functional and non-functional requirements for these high level requirements.

Provide me user stories and tasks to this file.

Share the best practices to develop e-commerce API application.

---

### Developer

**Prompts:**

Design a Spring Boot microservice to manage product inventory. Include REST endpoints, service classes, repositories using JPA, and model classes. Show how to organize the project and include unit tests using JUnit and Mockito and create a workspace for the application.

Explain how to implement and manage microservices using REST endpoints.

Create a full-stack web application for a task management system using Vue.js for the frontend and Django REST Framework for the backend. Implement features like user registration, login/logout using JWT authentication, and CRUD functionality for tasks.

Define RESTful API endpoints, Vue components, and how to manage state. Provide a suggested folder structure and highlight key models, views, and serializers.

Help me build a React web application for booking movie tickets. Use Redux for state management. Suggest component structure, utility functions, actions/reducers, and API integration flow.

Review the code and provide me comments so that my code would be more readable and understandable.

---

### API Developers

**Prompts:**

Review this product API and suggest how to optimize response structure for frontend performance. And add pagination and filtering to the product listing endpoint.

Use ProductsController.cs

Explain how to implement API versioning using custom request headers in spring Boot.

---

### UI Developers

**Prompts:**

Help me to create a ProductCard component with proper accessibility and responsive design.

Use ProductService.cs 

Create a TypeScript API service for product management that 
1. Uses axios with interceptors
2. Handles authentication with JWT tokens
3. Includes retry logic and error handling
4. Implements CRUD operations for products

Generate API test cases to validate all CRUD operations of the Products API with Mocking data.

---

### QA Engineers

**Prompts:**

/tests Generate unit tests for this function. Validate both success and failure, and include edge cases.

Generate manual test cases for each function in product controller based on acceptance criteria.

Use products-acceptance.md

Build automation test in Javascript for testing an e-commerce website's login, add to cart, and checkout flow. Define classes for page objects, utility functions, and test cases.

Create Cypress end-to-end tests for a React-based todo app. Write test cases for adding, deleting, marking complete, and filtering todos. Include folder structure, sample test cases, and configuration setup.

Design a JMeter test plan to load test the /api/tasks endpoint of a task management system. Simulate 100 concurrent users performing GET, POST, and DELETE requests over a 5-minute duration. Include assertions for response time < 2s and 95th percentile latency.

Create a Postman collection with tests for a REST API that manages tasks: POST /tasks, GET /tasks, PUT /tasks/:id, and DELETE /tasks/:id. Include tests for status code, response time, and response structure.

---

### Database Engineers

**Prompts:**

Design a MySQL database schema for an online learning platform with tables for users, courses, lessons, quizzes, enrollments, submissions, grades, and feedback. Ensure relationships are defined between instructors, students, and their respective learning activities. Include timestamps and foreign keys where appropriate.

Convert the Mysql database into Postgresql database.

Write MongoDB aggregation queries to:
- Count the number of completed tasks per user.
- Fetch tasks created within the last 15 days with high priority and include embedded project name.
- Perform a $lookup between users and comments collections.

Optimize my query for better performance while working with larger dataset.

Write a T-SQL stored procedure that takes a table name and column name as parameters and returns the count of NULL values for that column using dynamic SQL. Add input validation.

Create a project level database documentation.

---

### DevSecOps Engineers

**Prompts:**

Design a DevOps automation script using Python that automates Docker container builds, runs security scans with Trivy, and pushes to AWS ECR. Add relevant classes and functions, and list required dependencies.

Generate github actions workflow for creating a PR.

Generate terraform script to create Azure virtual machine by including subnet, network interface.

Update and create variables.tf and output.tf

Write a Docker file for python.

Write a yaml file for replicasets and pods.

Create a CI/CD pipeline in GitHub Actions for a Node.js application that includes stages for build, test, lint, security scan (using npm audit), and deployment to a staging environment. Ensure secrets are pulled securely from GitHub Secrets.

Write an ARM template to deploy an Azure App Service with app service plan.

Write a cloud formation template to create EC2 server.
