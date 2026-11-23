
**Version:** 1.0  
**Status:** Active  
**Source of Truth:** This document tracks the official development progress of the project.

---

# Phase 0 — Project Initialization

**Status:** Completed

- [x] Create GitHub repository
- [x] Clone repository locally
- [x] Generate Spring Boot project using Spring Initializr
- [x] Configure Maven and project dependencies
- [x] Configure PostgreSQL using Docker Compose
- [x] Create `.env` configuration
- [x] Configure database connection
- [x] Configure Git ignore rules
- [x] Verify Spring Boot application startup
- [x] Run Maven `clean verify` successfully
- [x] Create initial Git commit


---

# Phase 1 — Project Documentation

**Status:** In Progress

- [x] Define project objectives and scope 
- [x] Define functional requirements
- [x] Define non-functional requirements
- [x] Define initial technology stack 
- [x] Define MVP scope
- [x] Create PRD v1.0
- [x] Create Development Roadmap
- [x] Review and finalize project documentation 
- [x] Commit project documentation and Obsidian configuration changes

**Deliverables:**

- [x] `- `Product Requirements Document (PRD).md`` 
- [x] `- `Development Roadmap.md``


---

# Phase 2 — Architecture & Database Design

**Status:** Not Started

## 2.1 Application Architecture

- Understand layered architecture
    
- Define Controller, Service and Repository responsibilities
    
- Define package structure
    
- Define DTO strategy
    
- Define entity relationships
    
- Define exception handling strategy
    

## 2.2 Database Design

- Design User entity
    
- Design JobApplication entity
    
- Design ApplicationStatusHistory entity
    
- Design Interview entity
    
- Design FollowUp entity
    
- Design Document entity
    
- Design Document-Application association
    
- Define relationships and cardinality
    
- Define database constraints
    
- Review initial ER diagram
    

## 2.3 Database Implementation Preparation

- Understand JPA entity mapping
    
- Understand Hibernate
    
- Understand entity lifecycle
    
- Understand cascade operations
    
- Understand database migrations
    
- Select and configure a database migration strategy
    

**Deliverables:**

- Architecture documentation
    
- ER diagram
    
- Initial database design
    

**Estimated effort:** 4–6 days

---

# Phase 3 — Spring Security & User Management

**Status:** Not Started

## 3.1 Security Fundamentals

- Understand authentication vs authorization
    
- Understand Spring Security architecture
    
- Understand SecurityFilterChain
    
- Understand password hashing
    
- Understand BCrypt
    
- Understand security filters and request processing
    
- Evaluate session-based vs token-based authentication
    

## 3.2 User Management

- Implement User entity
    
- Implement User Repository
    
- Define user roles
    
- Implement registration DTOs
    
- Implement registration validation
    
- Implement user registration service
    
- Implement password hashing
    
- Implement registration endpoint
    
- Prevent public assignment of privileged roles
    

## 3.3 Authentication

- Configure Spring Security
    
- Implement login
    
- Implement logout
    
- Configure authentication mechanism
    
- Implement authentication failure handling
    
- Secure protected endpoints
    

## 3.4 Authorization

- Implement user-specific data ownership
    
- Prevent unauthorized access to other users' records
    
- Configure authorization rules
    
- Implement appropriate access-denied handling
    

## 3.5 Security Testing

- Test registration
    
- Test duplicate email handling
    
- Test password hashing
    
- Test login success and failure
    
- Test protected endpoints
    
- Test authorization boundaries
    

**Deliverable:** Functional user registration and authentication system.

**Estimated effort:** 5–8 days

---

# Phase 4 — Core Backend: Job Applications

**Status:** Not Started

## 4.1 Domain Model

- Implement JobApplication entity
    
- Implement application status representation
    
- Associate applications with users
    
- Implement JPA Repository
    
- Define application DTOs
    

## 4.2 Business Logic

- Implement application creation
    
- Implement application retrieval
    
- Implement application update
    
- Implement application deletion
    
- Implement application validation
    
- Implement Wishlist management
    
- Implement Wishlist-to-Applied transition
    
- Validate Application Date when transitioning to APPLIED
    
- Implement application status updates
    

## 4.3 Status History

- Implement ApplicationStatusHistory entity
    
- Automatically record status changes
    
- Record previous and new status
    
- Record date and time
    
- Implement status history retrieval
    

## 4.4 REST API

- Implement Job Application Controller
    
- Define REST endpoints
    
- Implement appropriate HTTP status codes
    
- Test application CRUD operations
    
- Test status transitions
    

**Deliverable:** Functional Job Application REST API.

**Estimated effort:** 6–9 days

---

# Phase 5 — Interviews & Follow-ups

**Status:** Not Started

## 5.1 Interview Management

- Implement Interview entity
    
- Associate interviews with applications
    
- Implement Interview Repository
    
- Implement Interview Service
    
- Implement interview creation
    
- Implement interview retrieval
    
- Implement interview updates
    
- Implement interview deletion
    
- Implement interview validation
    

## 5.2 Follow-up Management

- Implement FollowUp entity
    
- Associate follow-ups with applications
    
- Implement FollowUp Repository
    
- Implement FollowUp Service
    
- Implement follow-up creation
    
- Implement follow-up retrieval
    
- Implement follow-up updates
    
- Implement follow-up completion
    
- Support feedback requests for rejected applications
    

## 5.3 Testing

- Test interview operations
    
- Test follow-up operations
    
- Test application associations
    
- Test user ownership restrictions
    

**Deliverable:** Complete interview and follow-up management.

**Estimated effort:** 4–6 days

---

# Phase 6 — Document Management

**Status:** Not Started

## 6.1 Java File Handling

- Understand Java File I/O
    
- Understand `java.nio.file`
    
- Understand file paths and directories
    
- Understand file storage and retrieval
    
- Understand Spring MultipartFile
    
- Understand file validation and security
    

## 6.2 Document Backend

- Implement Document entity
    
- Implement document-application association
    
- Define document metadata
    
- Configure document storage location
    
- Implement file upload
    
- Implement file retrieval
    
- Implement file download
    
- Implement document association with multiple applications
    
- Implement document version management
    
- Validate file types
    
- Validate file sizes
    
- Protect documents from unauthorized access
    

## 6.3 File Lifecycle

- Implement safe document deletion
    
- Prevent deletion of shared documents
    
- Handle orphaned document files
    
- Test document association and deletion scenarios
    

**Deliverable:** Functional document storage and management system.

**Estimated effort:** 5–8 days

---

# Phase 7 — Search, Filtering & Pagination

**Status:** Not Started

- Understand Spring Data JPA query methods
    
- Understand JPQL
    
- Understand Specifications and dynamic queries
    
- Implement company search
    
- Implement job title search
    
- Implement status filtering
    
- Implement date range filtering
    
- Support combined filters
    
- Implement sorting
    
- Implement pagination
    
- Test search and filtering
    
- Verify user-specific query restrictions
    

**Deliverable:** Searchable and filterable application database.

**Estimated effort:** 3–5 days

---

# Phase 8 — Dashboard Backend

**Status:** Not Started

- Define dashboard data requirements
    
- Implement application statistics
    
- Implement applications grouped by status
    
- Implement upcoming interviews retrieval
    
- Implement pending follow-ups retrieval
    
- Implement approaching deadlines retrieval
    
- Implement dashboard REST endpoints
    
- Verify calculations and user-specific results
    

**Deliverable:** Dashboard REST API.

**Estimated effort:** 2–3 days

---

# Phase 9 — Testing & Backend Refinement

**Status:** Not Started

## 9.1 Automated Testing

- Write repository tests
    
- Write service unit tests
    
- Write controller integration tests
    
- Write validation tests
    
- Write security tests
    
- Test complete application workflows
    
- Test document handling
    
- Test deletion and relationship integrity
    

## 9.2 Backend Refinement

- Review package structure
    
- Review separation of concerns
    
- Review exception handling
    
- Review database queries
    
- Review security configuration
    
- Review technical debt
    
- Update API documentation
    
- Prepare backend README
    

**Deliverable:** Tested and documented backend.

**Estimated effort:** 4–6 days

---

# Phase 10 — Frontend Development

**Status:** Not Started

## 10.1 Frontend Setup

- Create React application
    
- Configure project structure
    
- Configure API communication
    
- Select a simple dashboard UI template
    
- Configure frontend environment variables
    

## 10.2 Authentication UI

- Implement registration page
    
- Implement login page
    
- Implement logout functionality
    
- Handle authentication state
    
- Handle unauthorized responses
    

## 10.3 Application Management UI

- Implement application dashboard
    
- Implement application listing
    
- Implement application creation form
    
- Implement application editing
    
- Implement application details
    
- Implement status updates
    
- Implement Wishlist view
    
- Implement search and filtering
    

## 10.4 Additional Features

- Implement interview management UI
    
- Implement follow-up management UI
    
- Implement document management UI
    
- Implement status history view
    
- Implement dashboard statistics
    
- Implement upcoming activity sections
    

**Deliverable:** Functional React frontend.

**Estimated effort:** 8–12 days

---

# Phase 11 — Integration & Finalization

**Status:** Not Started

## 11.1 Integration

- Connect frontend with backend
    
- Verify authentication workflow
    
- Verify complete job application workflow
    
- Verify interview and follow-up workflows
    
- Verify document upload and retrieval
    
- Verify dashboard data
    
- Test complete user experience
    

## 11.2 Final Review

- Fix identified bugs
    
- Review security and validation
    
- Review application performance
    
- Update README
    
- Document installation and execution
    
- Prepare GitHub repository
    
- Prepare portfolio project showcase
    

**Deliverable:** Complete Personal Job Application Tracker.

**Estimated effort:** 4–6 days

---

# Phase 12 — Homelab Deployment (Future)

**Status:** Future Scope

- Prepare production configuration
    
- Containerize Spring Boot backend
    
- Configure Docker Compose for full application
    
- Configure persistent storage
    
- Configure production environment variables
    
- Review authentication and security settings
    
- Deploy to homelab
    
- Configure reverse proxy and HTTPS
    
- Test remote access
    

**Deliverable:** Self-hosted application.

---

# Development Rules

1. Work milestone by milestone and task by task.
    
2. Do not skip tasks without understanding and completing them.
    
3. Learn unfamiliar concepts before implementing them.
    
4. The developer writes the implementation; the mentor explains, guides and reviews.
    
5. Implement automated tests alongside features.
    
6. Use Git commits at meaningful checkpoints.
    
7. Update this roadmap whenever a task is completed.
    
8. Do not mark tasks complete before implementation and review.
    
9. Keep the PRD and this Roadmap as the project's source of truth.
    
10. Avoid unnecessary complexity and premature optimization.
    

---

# Progress Tracking

**Current Phase:** Phase 1 — Project Documentation

**Next Task:** Complete and review the Roadmap.

**Last Completed Git Commit:** `2dade53`

**Next Git Checkpoint:** Project documentation and Obsidian configuration.