
|Property|Value|
|---|---|
|Version|1.0|
|Status|Approved|
|Project Type|Personal Software Project|
|Initial Deployment|Local Environment|
|Primary Focus|Java Backend Development|

---

# 1. Project Overview

## 1.1 Purpose

The Personal Job Application Tracker is a web application designed to help users organize, manage and monitor their job search activities.

It provides a centralized platform for managing job opportunities, applications, recruitment stages, interviews, follow-ups and related documents.

The project also serves as a practical software engineering and portfolio project, with a primary focus on Java Backend Development and the Spring ecosystem.

## 1.2 Problem Statement

Managing multiple job applications can become difficult without a centralized tracking system.

Information such as company details, application dates, recruitment stages, interview schedules, recruiter feedback and submitted documents can become scattered across emails, spreadsheets and local files.

The application aims to solve this problem by bringing all relevant information together.

## 1.3 Objectives

- Centralize job application management.
    
- Track the complete recruitment lifecycle.
    
- Organize interviews and follow-up activities.
    
- Maintain and manage application-related documents.
    
- Provide search, filtering and reporting capabilities.
    
- Implement authentication and authorization.
    
- Gain practical experience with Java, Spring Boot, PostgreSQL and Spring Security.
    
- Develop a complete application suitable for a professional portfolio.

# 2. Target Users

The application will initially be used as a personal job search management tool.

The system will support user registration and authentication from the first functional release.

Each user must have access exclusively to their own applications and associated information.

The architecture should support future expansion and remote deployment.

# 3. Technology Stack

## 3.1 Backend

- Java 25
    
- Spring Boot 4.2
    
- Spring Web MVC
    
- Spring Data JPA
    
- Hibernate
    
- Spring Security
    
- Bean Validation
    
- Maven

## 3.2 Database

- PostgreSQL 17
    
- Docker
    
- Docker Compose

## 3.3 Frontend

- React
    
- JavaScript
    
- CSS

Frontend development will take place after the core backend implementation.

A simple, preferably ready-made UI template will be used to minimize unnecessary frontend design work.

## 3.4 Development Tools

- IntelliJ IDEA
    
- Git and GitHub
    
- Obsidian
    
- Docker Desktop

# 4. Functional Requirements

## 4.1 User Management and Authentication

The application must support:

- User registration.
    
- User login.
    
- User logout.
    
- Secure password storage.
    
- Authentication of users.
    
- Authorization and protected endpoints.
    
- User-specific data access.

Public registration must not allow users to assign themselves privileged roles.

The system must use Spring Security and an appropriate password hashing mechanism.

## 4.2 Job Application Management

Users must be able to create, view, update and delete job application records.

Each application should contain:

|Field|Required|
|---|---|
|Company|Yes|
|Job Title|Yes|
|Location|No|
|Job URL|No|
|Application Date|Conditional|
|Application Deadline|No|
|Status|Yes|
|Salary|No|
|Notes|No|
|Contact Person|No|

Application Date is required when an opportunity transitions to APPLIED.

Optional fields must not prevent a record from being created.

## 4.3 Wishlist Management

Users must be able to save interesting job opportunities before submitting an application.

Wishlist entries use the WISHLIST status.

Users can record deadlines, company information and other available details.

A wishlist entry must be convertible into an active application without creating a duplicate record.

## 4.4 Application Status Management

Supported statuses:

- WISHLIST
    
- APPLIED
    
- SCREENING
    
- INTERVIEW
    
- OFFER
    
- REJECTED
    
- WITHDRAWN

Users must be able to update application statuses.

Every status transition must be recorded, including:

- Previous status.
    
- New status.
    
- Date and time of change.

The complete status history must remain available while the application record exists.

## 4.5 Interview Management

Users must be able to create and manage multiple interviews associated with a job application.

Interview information:

- Interview Date.
    
- Interview Time.
    
- Interview Type.
    
- Location or Meeting Link.
    
- Contact Person.
    
- Notes.
    
- Outcome.

Interview types:

- HR Interview.
    
- Technical Interview.
    
- Coding Assessment.
    
- Behavioral Interview.
    
- Final Interview.
    
- Other.

Interview outcomes:

- Pending.
    
- Passed.
    
- Failed.
    
- Rescheduled.
    
- Cancelled.

## 4.6 Follow-up Management

Users must be able to create and manage follow-up activities associated with job applications.

Follow-ups must remain available even for rejected or withdrawn applications.

Information:

- Follow-up Date.
    
- Follow-up Type.
    
- Description / Notes.
    
- Completion Status.
    
- Response / Feedback.

Supported types:

- Application Status Inquiry.
    
- Interview Feedback Request.
    
- Rejection Feedback Request.
    
- Thank You Message.
    
- Other.

Users must be able to record feedback received from recruiters or employers.

## 4.7 Document Management

Users must be able to upload, organize and associate documents with job applications.

Supported document types:

- CV.
    
- Cover Letter.
    
- Certificate.
    
- Portfolio.
    
- Other.

Document information:

- Original File Name.
    
- Document Type.
    
- Storage Reference.
    
- Upload Date.
    
- Description.
    
- Version.

A document may be associated with multiple job applications.

Different versions of documents must be supported.

The system must distinguish between a document file and its association with a particular application, allowing users to identify which document version was submitted to each company.

Physical files will be stored outside the database. PostgreSQL will store document metadata and storage references.

Deleting an application must remove its document associations, but must not delete a physical file that is still associated with another application.

## 4.8 Dashboard

The application must provide an overview of job search activity.

Expected information:

- Total applications.
    
- Applications grouped by status.
    
- Wishlist opportunities.
    
- Upcoming interviews.
    
- Pending follow-ups.
    
- Approaching application deadlines.

A simple, preferably ready-made UI template will be used.

Development effort should focus on backend data retrieval and business logic rather than custom visual design.

## 4.9 Search, Filtering and Sorting

Users must be able to:

- Search by company.
    
- Search by job title.
    
- Filter by application status.
    
- Filter by date range.
    
- Combine multiple filters.
    
- Sort application results.
    
- Navigate results using pagination.

# 5. Security Requirements

Security is a core development objective and will be implemented as part of the initial functional release.

Requirements:

- Registration and login.
    
- Authentication and authorization.
    
- Secure password hashing.
    
- Role-based access control where appropriate.
    
- Securing REST endpoints.
    
- User-specific data ownership.
    
- Security testing.

The public registration process must assign the standard user role automatically.

Users must never be able to access or modify another user's data.

# 6. Non-Functional Requirements

## 6.1 Maintainability

The application must follow a clear separation of concerns and maintainable backend architecture.

## 6.2 Data Integrity

Application data and relationships must remain consistent.

## 6.3 Validation

User input must be validated before persistence.

## 6.4 Reliability

The application must handle errors appropriately and protect against accidental data loss.

## 6.5 Security

Sensitive information, credentials and uploaded documents must be handled securely.

## 6.6 Extensibility

The architecture should support future remote deployment and additional functionality.

# 7. Data Management and Deletion

Deleting a job application must also delete its dependent records:

- Interviews.
    
- Follow-ups.
    
- Status History.
    
- Document associations.

Physical document files must only be deleted when they are no longer referenced by any application.

Deleting an application must not delete documents shared with other applications.

# 8. Deployment Strategy

The initial application will run locally.

PostgreSQL will run in Docker using Docker Compose.

The Spring Boot backend will initially run locally during development.

The architecture must allow future deployment to a self-hosted homelab environment.

Remote access and production deployment are outside the initial deployment scope.

# 9. MVP Scope

The initial functional release will include:

1. User Registration and Authentication.
    
2. Job Application Management.
    
3. Wishlist Management.
    
4. Application Status Management and History.
    
5. Interview Management.
    
6. Follow-up Management.
    
7. Document Management.
    
8. Dashboard.
    
9. Search, Filtering, Sorting and Pagination.
    
10. Automated Testing.

The backend will be developed first, followed by the frontend.

Spring Security is part of the MVP and not a deferred enhancement.

# 10. Future Scope

Potential future enhancements:

- Automated reminders and notifications.
    
- Calendar integration.
    
- Advanced recruitment analytics.
    
- Additional dashboard statistics.
    
- Remote deployment.
    
- Additional user roles and permissions.
    
- More advanced document management.

# 11. Success Criteria

The project will be considered successful when:

- Users can register and authenticate securely.
    
- Users can manage their own job opportunities and applications.
    
- Recruitment progress can be tracked through status history.
    
- Interviews and follow-ups can be managed.
    
- Documents can be uploaded, stored and associated with applications.
    
- Search, filtering, sorting and pagination work correctly.
    
- The dashboard displays accurate information.
    
- The backend is covered by meaningful automated tests.
    
- The frontend communicates successfully with the backend REST API.
    
- The application can run locally using documented instructions.
    
- The repository and documentation are suitable for presentation on GitHub.

# 12. Development Principles

1. Implement features incrementally.
    
2. Understand technologies before using them.
    
3. Follow clean code and separation-of-concerns principles.
    
4. Write automated tests for implemented functionality.
    
5. Use Git commits at meaningful checkpoints.
    
6. Keep the Roadmap as the source of truth for project progress.
    
7. Prioritize practical Backend engineering experience.
    
8. Avoid unnecessary complexity.
    
9. Keep future extensibility in mind without overengineering the MVP.