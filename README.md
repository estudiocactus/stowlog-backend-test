# Stowlog API - Backend Developer Technical Test

## Introduction

Welcome to the Stowlog API technical test. This test is designed to evaluate your skills as a backend developer, specifically your proficiency with NestJS, TypeScript, MongoDB, and RESTful API design principles. Instead of modifying an existing codebase, you'll be building a simplified version of our API from scratch and deploying it to a cloud platform.



## Overview of Stowlog

Stowlog is a safety and compliance management system that helps organizations digitize their HSSE (Health, Safety, Security, and Environment) procedures. The platform includes features for managing safety inductions, visit appointments, permits to work, and more.



## Technical Test Requirements

### Technology Stack

You must use the following technologies:

- **Backend Framework**: NestJS
- **Database**: MongoDB
- **Authentication**: JWT
- **Documentation**: Swagger
- **Deployment**: Render (or similar platform of your choice, Fly.io, Railway...)

### Core Features to Implement

You are required to build a simplified version of the Stowlog API with the following modules:

#### 1. User Module

- User registration and authentication (JWT)
- User roles (Admin, Manager, Worker)
- User profile management

#### 2. Suspensions Module

- Create, read, update, delete (CRUD) operations for user suspensions
- Suspension history tracking
- Search functionality with filtering and pagination
- Email notification system when a user is suspended

#### 3. Facilities Module

- CRUD operations for facilities
- Assign users to facilities
- Facility member management

### Technical Requirements

1. **Architecture**
   - Follow NestJS best practices for module organization
   - Implement proper separation of concerns
   - Use dependency injection effectively

2. **API Design**
   - RESTful API endpoints
   - Proper request validation using DTOs and class-validator
   - Comprehensive error handling
   - Pagination for list endpoints

3. **Database**
   - MongoDB schemas using Mongoose
   - Proper indexing for performance
   - Data validation at the schema level

4. **Authentication & Authorization**
   - JWT-based authentication
   - Role-based access control
   - Protect routes based on user roles

5. **Documentation**
   - API documentation using Swagger
   - README with setup instructions
   - Code comments where necessary

6. **Testing**
   - Unit tests for services
   - Integration tests for controllers
   - Minimum 70% test coverage

7. **Deployment**
   - Deploy the application to Render (or similar platform)
   - Provide deployment instructions
   - Ensure the API is accessible online

### Bonus Points

- Implement caching for frequently accessed data
- Add logging middleware
- Implement rate limiting
- Set up CI/CD pipeline
- Add email verification for user registration



## Evaluation Criteria

Your submission will be evaluated based on:

1. **Code Quality (30%)**
   - Clean, readable, and well-organized code
   - Proper error handling
   - Following NestJS best practices

2. **Architecture (25%)**
   - Proper separation of concerns
   - Effective use of NestJS modules, services, and controllers
   - Appropriate use of dependency injection

3. **Functionality (25%)**
   - All requirements are implemented correctly
   - Edge cases are handled properly
   - Performance considerations

4. **Testing & Documentation (20%)**
   - Comprehensive tests
   - Clear API documentation
   - Well-documented code and README



## Submission Guidelines

1. Create a new GitHub repository for your project
2. Implement the required features
3. Deploy the application to Render (or similar platform)
4. Submit the following:
   - GitHub repository URL
   - Deployed application URL
   - README with:
     - Setup instructions
     - API documentation or Swagger URL
     - Brief explanation of your implementation
     - Any assumptions or design decisions you made
     - How you would improve the code further given more time



## Time Limit

You have 7 days to complete this test. Quality is more important than completing all requirements, so focus on delivering well-implemented features rather than rushing through all requirements.



## Database Setup

For the MongoDB database, we recommend using MongoDB Atlas's free tier:

1. Create a free MongoDB Atlas account at [https://www.mongodb.com/cloud/atlas](https://www.mongodb.com/cloud/atlas)
2. Set up a free M0 cluster
3. Configure network access to allow connections from anywhere (for simplicity in this test)
4. Create a database user
5. Use the connection string in your NestJS application's environment variables

This approach will ensure your application can be properly deployed to Render while maintaining database persistence.



## Email Notification Implementation

For this test, you should implement a simulated email service. Your implementation should:

- Log email details to the console (recipient, subject, content)
- Mark suspensions as having been notified after the "email" is sent
- Handle potential failures in the email sending process
- Be implemented as a separate service that follows NestJS best practices

You do NOT need to integrate with an actual email service provider for this test.



## Entity Relationship Diagram Example

[Open Diagram](https://www.mermaidchart.com/raw/bf561c6c-025d-4e87-a769-95fdc2bd9883?theme=light&version=v0.1&format=svg)



## Postman Collection Example

[Open Collection](https://.postman.co/workspace/My-Workspace~eb85a56d-6af4-424f-848a-7847304014b5/collection/9964216-bcf28ca4-0bc5-43f4-840f-ef64e04fe72f?action=share&creator=9964216)



## Project Structure Example

Here's a recommended project structure to help you get started:

stowlog-api/
├── src/
│   ├── common/
│   │   ├── decorators/
│   │   ├── filters/
│   │   ├── guards/
│   │   ├── interceptors/
│   │   └── utils/
│   ├── config/
│   │   ├── configuration.ts
│   │   └── validation.ts
│   ├── modules/
│   │   ├── auth/
│   │   │   ├── dto/
│   │   │   ├── guards/
│   │   │   ├── strategies/
│   │   │   ├── auth.controller.ts
│   │   │   ├── auth.module.ts
│   │   │   └── auth.service.ts
│   │   ├── users/
│   │   │   ├── dto/
│   │   │   ├── entities/
│   │   │   ├── users.controller.ts
│   │   │   ├── users.module.ts
│   │   │   └── users.service.ts
│   │   ├── suspensions/
│   │   │   ├── dto/
│   │   │   ├── entities/
│   │   │   ├── suspensions.controller.ts
│   │   │   ├── suspensions.module.ts
│   │   │   └── suspensions.service.ts
│   │   └── facilities/
│   │       ├── dto/
│   │       ├── entities/
│   │       ├── facilities.controller.ts
│   │       ├── facilities.module.ts
│   │       └── facilities.service.ts
│   ├── app.module.ts
│   └── main.ts
├── test/
│   ├── app.e2e-spec.ts
│   └── jest-e2e.json
├── .env.example
├── .gitignore
├── nest-cli.json
├── package.json
├── README.md
├── tsconfig.build.json
└── tsconfig.json



## Resources

- [NestJS Documentation](https://docs.nestjs.com/)
- [MongoDB Documentation](https://docs.mongodb.com/)
- [Render Documentation](https://render.com/docs)
- [JWT Authentication in NestJS](https://docs.nestjs.com/security/authentication)
- [Swagger in NestJS](https://docs.nestjs.com/openapi/introduction)

Good luck! We're looking forward to seeing your solution.
