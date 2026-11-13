# TELos SOFTWARE DEVELOPMENT
# MASTER PROMPT 04 — ADVANCED DATABASE ENGINEERING & DATA ARCHITECTURE

## 1. YOUR ROLE

Act as a principal database architect, MongoDB specialist, Mongoose engineer, data security engineer and database performance specialist.

Your task is to design, implement, optimize and document the complete database system for TELos Software Development.

Do not merely create basic database schemas. Build a professional, reliable, maintainable database architecture suitable for a real software development business.

## 2. PROJECT CONTEXT

Company: TELos Software Development.

Website languages:
- English.
- Amharic.

Frontend:
- React.
- TypeScript.
- Vite.
- Tailwind CSS.

Backend:
- Node.js.
- Express.
- TypeScript.

Database:
- MongoDB.
- Mongoose.

Architecture:
- Full-stack application.
- REST API.
- Separate public website and private admin dashboard.

IMPORTANT:
Inspect the existing backend from Phase 03 before modifying anything.

Do not duplicate models or create incompatible database structures.

## 3. DATABASE ARCHITECTURE

Design a modular database architecture.

Use appropriate collections, references, embedded documents and indexes.

Avoid unnecessary data duplication.

Choose embedding or referencing according to access patterns and expected data growth.

Create a database relationship diagram using Mermaid.

Document the purpose of every collection.

## 4. REQUIRED COLLECTIONS

### A. Admin Users

Collection: admins

Fields:
- _id
- fullName
- email
- passwordHash
- role
- profileImage
- isActive
- isVerified
- lastLogin
- passwordChangedAt
- createdAt
- updatedAt

Requirements:
- Unique normalized email.
- Secure password storage.
- Role validation.
- Account status.
- No password exposure.
- Appropriate indexes.

Never store plain-text passwords.

### B. Projects

Collection: projects

Fields:
- _id
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
- translations
- seo
- createdBy
- updatedBy
- createdAt
- updatedAt

Requirements:
- Unique slug.
- Published and draft states.
- Featured project filtering.
- Category filtering.
- Search indexes.
- Pagination support.
- English and Amharic content.

### C. Services

Collection: services

Fields:
- _id
- name
- slug
- shortDescription
- fullDescription
- icon
- coverImage
- features
- benefits
- technologies
- faqs
- translations
- featured
- status
- sortOrder
- createdAt
- updatedAt

Requirements:
- Unique slug.
- Multilingual content.
- Display ordering.
- Search.
- Visibility management.

### D. Inquiries

Collection: inquiries

Fields:
- _id
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
- assignedTo
- createdAt
- updatedAt

Requirements:
- Private customer information.
- Status tracking.
- Inquiry assignment.
- Search and filtering.
- Date-based queries.
- Pagination.
- Appropriate indexes.

### E. Blog Posts

Collection: blogPosts

Fields:
- _id
- title
- slug
- excerpt
- content
- coverImage
- author
- category
- tags
- language
- translations
- status
- publishedAt
- seo
- createdAt
- updatedAt

Requirements:
- Unique slug.
- Draft and published states.
- Language filtering.
- Category filtering.
- Search.
- Publication scheduling readiness.

### F. Team Members

Collection: teamMembers

Fields:
- _id
- name
- position
- biography
- profileImage
- skills
- socialLinks
- sortOrder
- status
- createdAt
- updatedAt

### G. Testimonials

Collection: testimonials

Fields:
- _id
- clientName
- clientPosition
- company
- content
- profileImage
- rating
- featured
- status
- createdAt
- updatedAt

Only verified and approved testimonials should be published.

### H. FAQs

Collection: faqs

Fields:
- _id
- question
- answer
- category
- language
- translations
- sortOrder
- status
- createdAt
- updatedAt

### I. Website Settings

Collection: settings

Fields:
- _id
- companyName
- companyDescription
- logo
- contactEmail
- phone
- location
- socialLinks
- defaultLanguage
- supportedLanguages
- seoDefaults
- themeSettings
- updatedAt

Protect sensitive settings.

### J. Media Library

Collection: media

Fields:
- _id
- filename
- originalName
- storageProvider
- storageKey
- url
- mimeType
- size
- width
- height
- altText
- uploadedBy
- createdAt

Store media metadata in MongoDB, not large image files.

Use external object storage for actual media.

### K. Activity Logs

Collection: activityLogs

Fields:
- _id
- adminId
- action
- resource
- resourceId
- timestamp
- metadata
- ipAddress

Never log passwords, authentication tokens or sensitive customer information.

Restrict access to activity logs.

### L. Refresh Sessions

Collection: refreshSessions

Fields:
- _id
- adminId
- tokenHash
- expiresAt
- revokedAt
- createdAt
- lastUsedAt

Store only secure token hashes.

Implement appropriate expiration indexes.

## 5. DATABASE RELATIONSHIPS

Document these relationships:

- Admin → Projects.
- Admin → Services.
- Admin → Blog Posts.
- Admin → Media.
- Admin → Inquiries.
- Project → Media.
- Service → Related Projects.
- Blog Post → Author.
- Inquiry → Assigned Admin.
- Admin → Activity Logs.
- Admin → Refresh Sessions.

Use ObjectId references where appropriate.

Use embedded subdocuments for small, closely related data.

Prevent unnecessary database joins.

## 6. INTERNATIONALIZATION DATA MODEL

The website must support English and Amharic.

Implement a consistent multilingual strategy.

Example:

{
  "title": {
    "en": "Web Development",
    "am": "የድረ-ገጽ ልማት"
  },
  "description": {
    "en": "Professional website development",
    "am": "ሙያዊ የድረ-ገጽ ልማት"
  }
}

Requirements:
- Consistent translation structure.
- English and Amharic validation.
- Language fallback.
- Search support.
- Avoid empty translated content being treated as valid.
- Preserve existing frontend API contracts.

Do not automatically translate customer-submitted inquiries.

## 7. INDEXING AND PERFORMANCE

Design appropriate indexes.

Include:
- Unique indexes for email and slug.
- Compound indexes for frequently used filters.
- Date indexes for inquiries.
- Status indexes.
- Language indexes.
- Category indexes.
- Text or search indexes where appropriate.
- TTL indexes for expiring refresh sessions.

Avoid indexing every field unnecessarily.

Explain the reason for each important index.

Use pagination for large datasets.

Use projections to avoid returning unnecessary sensitive fields.

Analyze query performance using MongoDB explain plans.

## 8. DATA VALIDATION AND INTEGRITY

Implement:
- Required field validation.
- Field type validation.
- String length limits.
- Email normalization.
- Unique constraints.
- Enum validation.
- Date validation.
- Reference validation.
- Slug uniqueness.
- Nested object validation.

Handle duplicate key errors properly.

Use database transactions when multiple related writes must succeed or fail together.

Avoid unbounded arrays in documents.

## 9. SECURITY

Implement database security best practices:

- Least-privilege database access.
- Environment-based credentials.
- Network access restrictions.
- No public database exposure.
- Secure backups.
- Sensitive field protection.
- Safe query construction.
- Input validation.
- Restricted administrative operations.
- Encryption in transit.
- Appropriate encryption at rest.

Never expose MongoDB credentials to the frontend.

Never return passwordHash or tokenHash in API responses.

## 10. DATABASE BACKUP AND RECOVERY

Prepare a database backup strategy.

Include:
- Scheduled backups.
- Backup retention policy.
- Recovery documentation.
- Restore testing.
- Production data protection.
- Recovery objectives.

Document the difference between a backup and a successfully tested recovery.

Do not claim backups are running unless an actual backup process is configured.

## 11. SEED DATA

Create a development-only database seeding script.

It should provide:
- Sample services.
- Clearly labeled demonstration projects.
- Sample blog articles.
- Sample FAQs.
- Sample team members.
- Development settings.

Requirements:
- Never insert fabricated real clients.
- Never insert fake verified testimonials.
- Never overwrite production data.
- Never seed a public default administrator password.
- Make the script safe to run repeatedly.

## 12. DATABASE MIGRATIONS AND VERSIONING

Create a database migration strategy.

Support:
- Schema changes.
- Data transformation.
- Version tracking.
- Safe migration execution.
- Rollback planning.
- Production migration documentation.

Do not make destructive schema changes without an explicit migration plan.

## 13. DATABASE MONITORING

Prepare monitoring for:
- Connection health.
- Query performance.
- Database size.
- Index usage.
- Slow queries.
- Failed database operations.
- Connection pool usage.

Integrate with the backend health endpoint.

Do not expose database internals publicly.

## 14. REQUIRED DELIVERABLES

Produce:

1. Complete MongoDB architecture.
2. Database relationship diagram.
3. All Mongoose models.
4. Schema validation.
5. Database indexes.
6. Model references.
7. Multilingual data structures.
8. Secure session storage.
9. Activity logging.
10. Media metadata model.
11. Development seed scripts.
12. Migration strategy.
13. Backup and restore documentation.
14. Database monitoring readiness.
15. DATABASE.md.
16. Updated README.md.
17. Database tests.

## 15. TESTING

Test:
- Database connection.
- Model validation.
- Unique constraints.
- References.
- Multilingual content.
- CRUD operations.
- Pagination.
- Search.
- Index behavior.
- Session expiration.
- Data protection.
- Seed script safety.

Use an isolated test database.

Never run destructive tests against production data.

## 16. EXECUTION RULES

Before implementation:

1. Inspect the existing repository.
2. Inspect Phase 03 backend models.
3. Compare the current models with the required architecture.
4. Identify missing collections.
5. Identify inconsistent field names.
6. Identify missing indexes.
7. Prepare a migration plan.

Then implement the database improvements.

Preserve working APIs and frontend compatibility.

Do not create duplicate models.

Do not destroy existing data.

Do not claim successful database operations without testing them.

### FINAL OBJECTIVE

Deliver a professionally engineered MongoDB database system for TELos Software Development, with secure data structures, efficient indexes, multilingual content, reliable relationships, backup readiness and complete technical documentation.