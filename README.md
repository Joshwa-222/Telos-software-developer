# TELos Software Development
Bilingual English / Amharic software studio website and application foundation.

## Stack
- Frontend: React, TypeScript, Vite, React Router, Motion and Lucide.
- Backend: Node.js, Express, TypeScript, MongoDB and Mongoose.
- Security baseline: Helmet, CORS allowlist, Zod validation, rate limiting, bcrypt password hashing and signed JWTs.

## Requirements
Node.js 20+, npm 10+ and MongoDB.

## Local setup
1. Clone the repository.
2. Copy .env.example to backend/.env and update values.
3. Set MONGODB_URI and a random JWT_SECRET of at least 32 characters.
4. Set ADMIN_EMAIL and a strong ADMIN_PASSWORD (12+ characters) for first-run admin creation.
5. Run npm install at the repository root.
6. Run npm run dev.

Frontend: http://localhost:5173  
API health: http://localhost:5000/api/health  
Admin login: http://localhost:5173/admin

Never commit real credentials or use the example password in production.

## API routes
- GET /api/health
- POST /api/inquiries
- GET /api/services
- GET /api/projects
- GET /api/blog, /api/team, /api/testimonials and /api/faqs (published public content)
- POST /api/auth/login
- GET /api/admin/overview (protected)
- GET /api/admin/inquiries (protected)
- GET /api/admin/content/:kind (protected)
- POST /api/admin/content/:kind (protected)
- PATCH /api/admin/content/:kind/:id (protected)
- DELETE /api/admin/content/:kind/:id (protected)
- PATCH /api/admin/inquiries/:id/status (protected)

## Implemented in this initial foundation
Responsive bilingual public website, API-backed public service/project/article listings, public inquiry submission, MongoDB models, administrator login, protected dashboard metrics, CMS create/read/update/delete for Projects, Services, Blog, Team, Testimonials and FAQs, and inquiry review/status management.

## Not yet implemented
Private media storage and upload scanning, client portal, full CRM pipeline, proposals, appointment booking, email/notification automation, advanced analytics, complete role/permission editor, activity logs, automated application tests and production deployment. The Master Prompts 01–07 remain the extended product specification. Do not treat placeholder content or the initial admin view as a complete production CMS.

Before launch, configure secure production secrets, database backups, monitoring, private file storage, access controls, tests, domain and HTTPS. Verify all business contact details and replace all demo/placeholder portfolio content with approved factual content.