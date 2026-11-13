# TELos SOFTWARE DEVELOPMENT — MASTER PROMPT 05
## ADMIN DASHBOARD, CONTENT MANAGEMENT SYSTEM (CMS) & BUSINESS OPERATIONS
### Phase 05 — Admin Application Implementation

## 1. ROLE AND OBJECTIVE

Act as a senior full-stack engineer, React/TypeScript architect, Express API developer, MongoDB data architect, security engineer and product designer.

Implement a complete, usable Admin Dashboard and CMS for TELos Software Development. This is an implementation phase: write working code, connect it to the existing database and API, and verify the actual behavior.

Do not return only a plan, mockup, prompt, or static dashboard.

## 2. PROJECT CONTEXT

- Product: TELos Software Development.
- Frontend: React, TypeScript, Vite, Tailwind CSS or the existing styling system, React Router.
- Backend: Node.js, Express and TypeScript.
- Database: MongoDB with Mongoose.
- Languages: English and Amharic.
- Design: Futuristic Technology; premium dark surfaces, electric-blue accents, restrained cyan highlights.
- Continue from Master Prompts 01–04.
- This phase must be integrated with the existing frontend, API, models and authentication.

## 3. NON-NEGOTIABLE INTEGRATION RULES

Before writing code, inspect the repository and report the actual frontend routes, backend entry points, API client, authentication mechanism, Mongoose models, existing inquiry handling, environment variables and test setup.

Preserve existing working features. Reuse the current authentication and database. Do not introduce a second database connection, second login system, duplicate inquiry records or parallel copies of existing models.

Use existing project conventions and dependency versions. Prefer adding small modules over rewriting the application. Never invent existing file paths or claim tests passed without running them.

## 4. ADMIN INFORMATION ARCHITECTURE

Create a responsive admin application with these navigation groups:

### Overview
- Dashboard

### Website CMS
- Projects
- Services
- Blog Articles
- Team
- Testimonials
- FAQs
- Website Content
- Media Library

### Customer Operations
- Inquiries / Leads

### Configuration
- Website Settings
- Administrators and Roles
- Activity Logs
- My Profile

Use a persistent desktop sidebar and an accessible mobile navigation drawer. Show the active page, breadcrumbs, account menu, notification entry point and logout action.

## 5. DASHBOARD

Create an overview screen with real database-backed information:
- Total inquiries.
- New and qualified inquiries.
- Published projects.
- Published services.
- Published blog posts.
- Pending content drafts.
- Recent inquiries.
- Recent administrative activity.
- Quick actions for creating content.

Charts must use real queried data and clearly labeled date ranges. Do not display invented statistics or hard-coded growth percentages. Provide loading, empty, error and permission-denied states.

## 6. CMS MODULES

All modules need list, detail, create, edit, publish/unpublish, delete or archive behavior as appropriate, validation, search/filtering, pagination where needed, confirmation dialogs and useful feedback.

### Projects
Fields: title, slug, summary, full description, category, cover image, gallery, technologies, live URL, repository URL, featured state, publication state and timestamps.

Distinguish real client projects from demonstration projects. Do not fabricate customers, delivery outcomes or performance metrics.

### Services
Fields: title, slug, description, icon, deliverables, ordering and publication state. The public services page must use published records from the API.

### Blog
Fields: title, slug, excerpt, rich body content, cover image, author, categories/tags, SEO title, SEO description, draft/published state, publish date and timestamps. Ensure unique slugs and safe rendering of submitted HTML/markdown.

### Team
Fields: name, job title, biography, profile image, skills, display order and publication state. Use only authorized, supplied staff information.

### Testimonials
Fields: client name, role/company (if provided), quote, optional image, approval state and display order. Unapproved testimonials must never appear publicly.

### FAQs
Fields: question, answer, category, display order and publication state. Published FAQs should be exposed through a public API.

### Website Content
Provide editable structured content for homepage hero, company introduction, mission, vision, CTA sections, footer information and public contact details. Maintain English and Amharic values separately. Never invent contact data or business claims.

### Media Library
Support upload, preview, search, metadata, alt text, replacement and removal. Validate size, extension and actual file type. Use safe filenames and private storage for non-public documents. Do not expose arbitrary local file paths or rely on guessable URLs.

## 7. INQUIRY MANAGEMENT

Build a usable inquiry workspace with:
- Search by name, email or message.
- Filters by status and creation date.
- Detail view with contact details and message.
- Status: New, Contacted, Qualified, Closed.
- Priority and assignment where supported.
- Private internal notes.
- Follow-up date.
- Activity history.

Keep private notes and administrative metadata out of public responses. Preserve inquiry history when converting an inquiry into a lead or project.

## 8. AUTHENTICATION, ROLES AND PERMISSIONS

Reuse the existing secure login and session strategy. Require authorization on every protected server endpoint; hiding a button in the frontend is not access control.

Define:
- Super Admin: full access including administrators and settings.
- Admin: operational and CMS access as explicitly granted.
- Editor: content creation and editing, without privileged settings.
- Read-only: view-only access to permitted modules.

Enforce role/permission checks server-side. Hash passwords with a suitable password hashing algorithm, rate-limit login, validate input, expire sessions and do not log secrets. Never embed credentials in source files or provide a hard-coded admin password.

## 9. API AND DATA LAYER

Create or extend typed REST endpoints for each collection. Use shared validation schemas where practical. Support:
- List with pagination, search, filtering and sorting.
- Read one record.
- Create.
- Update.
- Publish/unpublish.
- Delete or archive.

Validate all inputs on the backend. Whitelist writable fields; reject or strip unrecognized fields. Handle missing records, invalid IDs, duplicate slugs, database errors and unauthorized access with consistent responses.

Use indexes for common query fields such as slug, status, createdAt and email where justified. Use safe schema changes that preserve existing records.

## 10. UI/UX AND ACCESSIBILITY

Use the approved TELos design system:
- Main background #080B14.
- Secondary background #0D1220.
- Card background #111827.
- Primary blue #3478F6.
- Electric blue #4EA5FF.
- Cyan #22D3EE.
- Primary text #F8FAFC.
- Muted text #94A3B8.
- Border #243044.

Provide responsive tables or card alternatives, clear form labels, keyboard navigation, visible focus styles, appropriate contrast, semantic headings and accessible dialogs. Respect reduced-motion preferences.

English and Amharic are first-class. Test Ethiopian script rendering, long strings, responsive navigation and form layouts in both languages.

## 11. QUALITY AND SECURITY

- Validate on client and server.
- Protect against mass assignment.
- Prevent unauthorized object access.
- Escape or sanitize user-generated content before display.
- Do not expose stack traces, tokens or secrets.
- Use request size limits and rate limits.
- Protect public forms against spam where appropriate.
- Add audit events for sensitive administrative actions.
- Ensure destructive actions require confirmation.
- Never treat a successful frontend response as proof that an email or external integration completed.

## 12. TESTING AND ACCEPTANCE CRITERIA

Write and run tests for:
- Admin login success and failure.
- Role and permission enforcement.
- CRUD operations for every implemented content collection.
- Invalid input and missing record behavior.
- Public endpoints returning only published content.
- Inquiry submission and status changes.
- Responsive navigation and core forms.
- English and Amharic rendering.
- Production build and TypeScript checks.

Do not claim a test passes until its result has been observed. Record known test gaps honestly.

## 13. REQUIRED DELIVERABLES

Provide:
1. Integrated Admin Dashboard.
2. CMS screens and backend endpoints.
3. Database models and indexes.
4. Inquiry management.
5. Secure role and permission enforcement.
6. Responsive bilingual UI.
7. Validation and error handling.
8. Automated tests and CI checks.
9. Updated README and environment documentation.
10. A concise implementation report listing files changed, tests actually run, build result, remaining gaps and deployment prerequisites.

## FINAL COMMAND

Inspect the actual TELos repository and implement this phase in the existing codebase. Preserve existing features. Connect every implemented control to real backend behavior and MongoDB persistence. Do not stop after generating a dashboard design or static mock data.
