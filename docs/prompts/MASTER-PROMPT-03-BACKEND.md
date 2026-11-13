# TELos SOFTWARE DEVELOPMENT
# MASTER PROMPT 03 — COMPLETE BACKEND ENGINEERING

## 1. ROLE

Act as a senior backend engineer, software architect, API developer, database integration engineer and application security specialist.

Your task is to build a complete, scalable, secure backend for TELos Software Development.

This is a real full-stack business application, not a demonstration API.

The backend must support the public website and the administrative dashboard.

## 2. PROJECT INFORMATION

Company: TELos Software Development

Website languages:
- English
- Amharic

Frontend:
- React
- TypeScript
- Vite
- Tailwind CSS

Backend:
- Node.js
- Express.js
- TypeScript

Database:
- MongoDB
- Mongoose

Architecture:
- RESTful API
- Modular architecture
- MVC-inspired separation of concerns

## 3. BACKEND ARCHITECTURE

Create a maintainable backend structure.

Recommended:

server/
  src/
    config/
      database.ts
      environment.ts
    controllers/
    services/
    models/
    routes/
    middleware/
    validators/
    types/
    utils/
    constants/
    jobs/
    app.ts
    server.ts
  uploads/
  tests/
  .env.example
  package.json
  tsconfig.json
  README.md

Separate business logic from controllers.

Use:
- Controllers for HTTP requests and responses.
- Services for business logic.
- Models for database operations.
- Validators for request validation.
- Middleware for authentication and security.

## 4. DATABASE CONNECTION

Configure MongoDB using Mongoose.

Requirements:
- Environment-based connection string.
- Connection error handling.
- Connection status logging.
- Graceful server shutdown.
- Database health monitoring.
- Appropriate indexes.
- Consistent model validation.

Never hardcode database credentials.

Use environment variables:

PORT=
NODE_ENV=
MONGODB_URI=
JWT_SECRET=
JWT_EXPIRES_IN=
FRONTEND_URL=
ADMIN_ORIGIN=
UPLOAD_DIRECTORY=

Add a complete .env.example without real secrets.

## 5. AUTHENTICATION AND AUTHORIZATION

Build a secure administrator authentication system.

Features:
- Admin login.
- Secure password hashing using Argon2 or bcrypt.
- Short-lived access authentication.
- Secure refresh-token strategy.
- Logout.
- Session invalidation.
- Password change.
- Password reset workflow.
- Login attempt rate limiting.
- Role-based permissions.

Roles:

1. Super Admin.
2. Admin.
3. Editor.

Permissions:

Super Admin:
- Complete system access.
- Manage administrators.
- Manage roles.
- Manage website settings.
- View all content and inquiries.

Admin:
- Manage projects.
- Manage services.
- Manage inquiries.
- Manage blog posts.
- Manage team content.

Editor:
- Manage permitted content.
- No access to administrator management.

Security requirements:
- Never store plain-text passwords.
- Never expose password hashes.
- Never provide a public administrator registration endpoint.
- Protect admin routes on the server.
- Validate all authorization permissions.
- Use secure cookies where appropriate.
- Protect against CSRF where cookie-based authentication requires it.
- Use generic login errors.
- Never store secrets in frontend code.

Create the initial Super Admin through a secure setup script or controlled deployment process.

Do not create default public credentials.

## 6. PROJECT MANAGEMENT API

Create a Project model.

Fields:
- title
- slug
- shortDescription
- description
- category
- coverImage
- gallery
- technologies
- clientName
- projectUrl
- completionDate
- featured
- status
- SEO metadata
- createdAt
- updatedAt

API endpoints:

GET /api/projects
GET /api/projects/:slug
GET /api/admin/projects
POST /api/admin/projects
PUT /api/admin/projects/:id
DELETE /api/admin/projects/:id

Features:
- Search.
- Category filtering.
- Pagination.
- Featured projects.
- Draft and published states.
- Slug generation.
- Image management.

Public users must only access published projects.

## 7. SERVICES API

Create a Service model.

Fields:
- name
- slug
- shortDescription
- fullDescription
- icon
- coverImage
- features
- benefits
- technologies
- FAQs
- featured
- status
- sortOrder
- translations

Endpoints:

GET /api/services
GET /api/services/:slug
GET /api/admin/services
POST /api/admin/services
PUT /api/admin/services/:id
DELETE /api/admin/services/:id

Support English and Amharic content.

## 8. INQUIRIES AND CONTACT API

Create an Inquiry model.

Fields:
- fullName
- email
- phone
- company
- projectCategory
- budget
- timeline
- description
- attachments
- preferredContact
- status
- adminNotes
- createdAt
- updatedAt

Endpoints:

POST /api/inquiries
POST /api/contact
GET /api/admin/inquiries
GET /api/admin/inquiries/:id
PATCH /api/admin/inquiries/:id
DELETE /api/admin/inquiries/:id

Features:
- Server-side validation.
- Spam prevention.
- Rate limiting.
- Status management.
- Inquiry filtering.
- Pagination.
- Admin notes.
- Email notification integration readiness.

Inquiry statuses:
- New.
- In Progress.
- Contacted.
- Completed.
- Archived.

Never expose private inquiry information through public endpoints.

## 9. BLOG MANAGEMENT API

Create a Blog model.

Fields:
- title
- slug
- excerpt
- content
- coverImage
- author
- category
- tags
- language
- status
- publishedAt
- SEO metadata
- createdAt
- updatedAt

Endpoints:

GET /api/blog
GET /api/blog/:slug
GET /api/admin/blog
POST /api/admin/blog
PUT /api/admin/blog/:id
DELETE /api/admin/blog/:id

Features:
- Drafts.
- Publishing.
- Scheduling readiness.
- Search.
- Categories.
- Tags.
- Pagination.
- English and Amharic content.

## 10. TEAM MANAGEMENT API

Create a TeamMember model.

Fields:
- name
- position
- biography
- profileImage
- skills
- socialLinks
- sortOrder
- status

Endpoints:

GET /api/team
GET /api/admin/team
POST /api/admin/team
PUT /api/admin/team/:id
DELETE /api/admin/team/:id

## 11. TESTIMONIAL MANAGEMENT API

Create a Testimonial model.

Fields:
- clientName
- clientPosition
- company
- content
- profileImage
- rating
- featured
- status

Create public and protected admin endpoints.

Only approved testimonials should appear publicly.

Never manufacture customer reviews.

## 12. FAQ MANAGEMENT API

Create a FAQ model.

Fields:
- question
- answer
- category
- language
- sortOrder
- status

Implement public retrieval and protected CRUD operations.

## 13. WEBSITE SETTINGS API

Create a Settings model.

Manage:
- Company name.
- Company description.
- Logo.
- Contact email.
- Phone number.
- Business location.
- Social media links.
- Default language.
- Available languages.
- SEO defaults.
- Website configuration.

Endpoints:

GET /api/settings
GET /api/admin/settings
PUT /api/admin/settings

Public responses must not expose sensitive configuration.

## 14. MEDIA MANAGEMENT

Create a media upload service.

Support:
- Images.
- Project galleries.
- Team profile images.
- Blog cover images.
- Service images.

Requirements:
- File type validation.
- File size limits.
- Safe filenames.
- Image processing readiness.
- Secure upload authorization.
- Upload error handling.
- Delete unused media.
- Prevent executable file uploads.

Use a storage abstraction that supports local development and future cloud storage integration.

Never trust the original filename or client-provided MIME type alone.

## 15. DASHBOARD ANALYTICS API

Create:

GET /api/admin/dashboard/stats
GET /api/admin/dashboard/activity
GET /api/admin/dashboard/inquiries-chart
GET /api/admin/dashboard/projects-summary

Provide:
- Total projects.
- Published projects.
- Total services.
- Total inquiries.
- Unread inquiries.
- Recent activity.
- Inquiry trends.

Use actual database records rather than invented statistics.

## 16. SECURITY MIDDLEWARE

Implement:

- Helmet.
- CORS allowlist.
- Rate limiting.
- Request validation.
- Central error handling.
- Secure authentication middleware.
- Role-based authorization.
- Request size limits.
- NoSQL injection protection.
- Secure HTTP headers.
- Audit logging.

Do not expose stack traces in production.

Do not log passwords, tokens, or sensitive inquiry details.

Validate and sanitize all incoming data.

## 17. API RESPONSE STANDARD

Use consistent JSON responses.

Success:

{
  "success": true,
  "message": "Operation successful",
  "data": {}
}

Failure:

{
  "success": false,
  "message": "A descriptive error occurred",
  "errors": []
}

Implement appropriate HTTP status codes.

Support:
- 200 OK.
- 201 Created.
- 400 Bad Request.
- 401 Unauthorized.
- 403 Forbidden.
- 404 Not Found.
- 409 Conflict.
- 422 Validation Error.
- 429 Too Many Requests.
- 500 Internal Server Error.

## 18. INTERNATIONALIZATION SUPPORT

The backend must support English and Amharic.

Use structured translated content where appropriate.

Example:

{
  "name": {
    "en": "Web Development",
    "am": "የድረ-ገጽ ልማት"
  }
}

Support language-aware content retrieval.

Do not assume that all business data is automatically translatable.

## 19. API DOCUMENTATION

Implement Swagger / OpenAPI documentation.

Provide:
- Endpoint descriptions.
- Request schemas.
- Response schemas.
- Authentication requirements.
- Error responses.
- Example requests.

Development documentation route:

/api/docs

Protect administrative information and avoid exposing production secrets.

## 20. TESTING

Use appropriate backend testing tools such as Vitest or Jest and Supertest.

Test:
- Database connection.
- Authentication.
- Authorization.
- Project CRUD.
- Service CRUD.
- Blog CRUD.
- Inquiry submissions.
- Form validation.
- File uploads.
- Rate limiting.
- Error handling.

Test both successful and failed requests.

## 21. FRONTEND INTEGRATION

Prepare the API to work with the React frontend from Prompt 02.

Use:
VITE_API_BASE_URL on the frontend.

Maintain consistent field names and response structures.

Provide API integration documentation.

Do not change frontend response assumptions without documenting the changes.

## 22. PRODUCTION READINESS

Prepare:
- Production environment configuration.
- Graceful shutdown.
- Logging.
- Health check.
- Database indexes.
- Deployment documentation.
- Backup strategy.
- Error monitoring readiness.
- Secure configuration.
- Production build.

Health endpoint:

GET /api/health

## 23. REQUIRED DELIVERABLES

Deliver a working backend containing:

1. Express server.
2. TypeScript configuration.
3. MongoDB connection.
4. Mongoose models.
5. Authentication.
6. Authorization.
7. Project APIs.
8. Service APIs.
9. Inquiry APIs.
10. Blog APIs.
11. Team APIs.
12. Testimonial APIs.
13. FAQ APIs.
14. Settings APIs.
15. Media management.
16. Dashboard analytics.
17. Security middleware.
18. Validation.
19. Error handling.
20. API documentation.
21. Automated tests.
22. .env.example.
23. README.md.

## 24. EXECUTION RULES

Before coding:
- Inspect the existing repository.
- Review the frontend API contracts.
- Identify missing dependencies.
- Check existing environment configuration.
- Preserve working frontend code.

Then implement the backend in logical stages.

Do not simply output code snippets.

Create the actual files in the project.

Run the server and automated tests.

Fix errors before completion.

Do not claim a feature is complete unless it has been implemented and tested.

### FINAL OBJECTIVE

Deliver a secure, modular, documented, tested and production-ready backend for TELos Software Development, ready for database optimization, full admin functionality and frontend integration in subsequent phases.