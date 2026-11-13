# TELos SOFTWARE DEVELOPMENT — MASTER PROMPT 06
## Final Integration, Quality Assurance, Optimization & Production Deployment

### 1. ROLE

Act as a senior software architect, full-stack developer, DevOps engineer, cybersecurity specialist, QA engineer, and performance optimization expert.

Your mission is to take the existing TELos Software Development project and prepare it for production.

**Project:** TELos Software Development  
**Frontend:** Existing React + TypeScript + Vite application  
**Backend:** Existing Node.js + Express + TypeScript application  
**Database:** Existing MongoDB + Mongoose database  
**Design:** Futuristic Technology — premium dark interface with electric-blue accents  
**Languages:** English and Amharic

This is Prompt 06. Continue from the existing work completed in Prompts 01–05.

Do not rebuild the application from scratch.

---

# 2. COMPLETE PROJECT AUDIT

Before making changes, inspect the entire repository.

Review:

- Frontend architecture.
- Backend architecture.
- Database connection.
- Mongoose models.
- Authentication and authorization.
- Admin dashboard.
- CMS functionality.
- Public website pages.
- API integrations.
- Image and file storage.
- English and Amharic localization.
- Environment variables.
- Deployment configuration.
- Existing tests.
- Documentation.

Identify:

1. Broken features.
2. Missing integrations.
3. Duplicate code.
4. Unused dependencies.
5. TypeScript errors.
6. Security vulnerabilities.
7. Performance bottlenecks.
8. Incomplete functionality.
9. Deployment problems.
10. Mobile responsiveness issues.

Create a prioritized list of issues and fix them systematically.

Do not remove working features simply to simplify the codebase.

---

# 3. COMPLETE END-TO-END INTEGRATION

Verify that all parts of TELos work together.

### Public website

Test:

- Homepage.
- About page.
- Services page.
- Portfolio/projects page.
- Project details.
- Blog listing.
- Blog details.
- Team section.
- Testimonials.
- FAQs.
- Contact page.
- Navigation.
- Footer.
- Language switching.

### Admin dashboard

Test:

- Admin login.
- Dashboard overview.
- Project management.
- Service management.
- Inquiry management.
- Blog management.
- Team management.
- Testimonial management.
- FAQ management.
- Media library.
- Website content management.
- Website settings.
- Administrator management.
- Activity logs.
- Profile.
- Logout.

### Integration requirement

For every CMS module:

1. Create a record.
2. Save it to MongoDB.
3. Retrieve it through the admin API.
4. Edit it.
5. Verify the updated database record.
6. Publish it if applicable.
7. Verify the public website displays it.
8. Unpublish or delete it.
9. Verify the public website handles the change correctly.

No fake data or frontend-only functionality should be used as a substitute for actual integration.

---

# 4. COMPLETE API TESTING

Inspect every existing API endpoint.

Test:

- Correct HTTP methods.
- Correct request parameters.
- Correct response structures.
- Authentication requirements.
- Permission requirements.
- Validation.
- Error handling.
- Pagination.
- Filtering.
- Sorting.
- Database persistence.

Check for:

- Missing endpoints.
- Incorrect endpoint URLs.
- CORS failures.
- Broken frontend API connections.
- Incorrect API base URLs.
- Inconsistent response formats.
- Unexpected server errors.
- Unhandled asynchronous errors.

Use the project's existing testing framework or an appropriate API testing tool.

Create automated tests for important API workflows.

Never expose private database information or authentication secrets in API responses.

---

# 5. SECURITY AUDIT

Perform a security review of the entire application.

### Authentication

Verify:

- Password hashing.
- Secure login.
- Logout.
- Session expiration.
- Token renewal, if applicable.
- Password reset.
- Account status verification.
- Protection against brute-force login attempts.

### Authorization

Verify:

- Super Admin permissions.
- Admin permissions.
- Editor permissions.
- Protected backend endpoints.
- Direct API access restrictions.
- Prevention of privilege escalation.

### Application security

Review and protect against:

- Cross-site scripting (XSS).
- Cross-site request forgery (CSRF), where applicable.
- NoSQL injection.
- SQL injection if any SQL integration exists.
- Broken access control.
- Insecure file uploads.
- Sensitive data exposure.
- CORS misconfiguration.
- Weak security headers.
- Excessive API requests.
- Information leakage through error messages.

Use appropriate security middleware and configuration.

Do not disable security controls to make tests pass.

### Secrets management

- Keep credentials outside source code.
- Use environment variables.
- Provide a safe `.env.example`.
- Ensure `.env` files are excluded from Git.
- Never expose secrets through frontend environment variables.
- Never commit database credentials, private keys, or production tokens.

---

# 6. PERFORMANCE OPTIMIZATION

Improve performance without damaging existing functionality.

### Frontend optimization

Implement where appropriate:

- Code splitting.
- Lazy loading.
- Route-based loading.
- Image optimization.
- Responsive image sizes.
- Proper caching.
- Removal of unused dependencies.
- Reduction of unnecessary re-renders.
- Efficient state management.
- Efficient API requests.
- Optimized production builds.

### Backend optimization

Review:

- MongoDB query efficiency.
- Database indexes.
- Pagination.
- Request validation.
- API response sizes.
- Unnecessary database queries.
- Memory usage.
- Error handling.
- Connection pooling.
- Rate limiting.

### Image optimization

Ensure images:

- Have appropriate dimensions.
- Use modern formats when supported.
- Do not unnecessarily exceed display sizes.
- Have meaningful alternative text.
- Load efficiently on mobile connections.

Do not introduce a new image hosting provider unless the existing storage system requires it.

---

# 7. SEO AND PUBLIC WEBSITE QUALITY

Prepare the public website for search engines.

Implement and verify:

- Unique page titles.
- Meta descriptions.
- Canonical URLs where appropriate.
- Open Graph metadata.
- Social sharing previews.
- XML sitemap.
- Robots.txt.
- Correct heading hierarchy.
- Semantic HTML.
- Descriptive image alt text.
- Clean URL structures.
- Proper 404 page.
- Appropriate redirects.

### Bilingual SEO

Ensure English and Amharic pages have appropriate metadata.

Use correct language attributes and language-specific URLs if supported by the existing routing architecture.

Do not generate duplicate or misleading metadata.

Ensure unpublished content is not indexed as public content.

---

# 8. RESPONSIVENESS AND ACCESSIBILITY AUDIT

Test the website on:

- Desktop.
- Laptop.
- Tablet.
- Mobile.

Check:

- Navigation.
- Hero section.
- Cards.
- Images.
- Forms.
- Tables.
- Admin sidebar.
- Dialogs.
- Buttons.
- Footer.
- Language selector.

Fix:

- Horizontal overflow.
- Broken layouts.
- Overlapping text.
- Unusable mobile navigation.
- Small touch targets.
- Incorrect image cropping.
- Inconsistent spacing.

### Accessibility

Verify:

- Keyboard navigation.
- Visible focus indicators.
- Semantic page structure.
- Accessible forms.
- Form labels.
- Appropriate contrast.
- Accessible dialogs.
- Image alternative text.
- Screen-reader-friendly navigation.

---

# 9. ERROR HANDLING AND RELIABILITY

Implement reliable error handling across frontend and backend.

### Frontend

Handle:

- Network errors.
- Server errors.
- Invalid form submissions.
- Unauthorized access.
- Forbidden access.
- Missing records.
- Expired sessions.
- Upload failures.
- Empty search results.

Display clear messages rather than exposing technical stack traces.

### Backend

Implement:

- Centralized error handling.
- Consistent API responses.
- Request validation.
- Safe logging.
- Proper HTTP status codes.
- Graceful database failure handling.
- Process shutdown handling.
- Health-check endpoints.

Create a suitable health endpoint, for example:

`GET /api/health`

It should report application health without exposing sensitive configuration or database credentials.

---

# 10. DATABASE BACKUP AND DATA SAFETY

Prepare a safe database management strategy.

Implement or document:

- MongoDB backup procedure.
- Restore procedure.
- Backup frequency recommendations.
- Database access restrictions.
- Production database configuration.
- Index verification.
- Data migration procedure.
- Safe handling of database errors.

Do not automatically delete or overwrite production data.

Before performing destructive database operations, require explicit confirmation and ensure a backup exists.

---

# 11. ENVIRONMENT CONFIGURATION

Create and verify separate configurations for:

- Local development.
- Testing.
- Production.

Provide a `.env.example` file containing variable names and safe placeholder values only.

Include the required configuration for:

- MongoDB connection.
- Backend port.
- Frontend API base URL.
- Authentication secrets.
- CORS allowed origins.
- Upload or storage configuration.
- Application environment.
- Logging configuration.

Never insert real production credentials into the example file.

Make sure frontend and backend use the correct production URLs.

---

# 12. PRODUCTION DEPLOYMENT

Prepare TELos for production deployment.

First inspect the existing hosting setup and repository configuration.

Do not assume that the project must use a particular provider.

Use the user's selected hosting providers if they have already been configured.

If hosting has not been selected, prepare a deployment architecture suitable for:

- React frontend hosting.
- Node.js backend hosting.
- MongoDB Atlas or the existing managed MongoDB service.
- Secure media storage.
- HTTPS.
- Custom domain support.

### Frontend deployment

Verify:

- Production build succeeds.
- Correct API URL is configured.
- SPA routing works.
- Static assets load correctly.
- Environment variables are configured properly.
- Public pages do not depend on local development URLs.

### Backend deployment

Verify:

- Production start command works.
- MongoDB connection succeeds.
- Environment variables are configured.
- CORS allows only required origins.
- Health endpoint works.
- Authentication works.
- API endpoints work.
- File storage works.

### MongoDB production configuration

Verify:

- Database user has appropriate permissions.
- Network access is restricted.
- Connection string is stored securely.
- Production indexes are present.
- Backups are configured or documented.

### Domain and HTTPS

Prepare the application for:

- Custom domain connection.
- HTTPS.
- Secure cookies where applicable.
- Correct frontend/backend origin configuration.
- Appropriate redirect behavior.

Do not claim that deployment is complete unless the application has actually been deployed and verified.

---

# 13. CONTINUOUS INTEGRATION AND DEPLOYMENT

If appropriate for the existing GitHub repository, configure a GitHub Actions workflow.

The workflow should:

1. Install dependencies.
2. Run frontend checks.
3. Run backend checks.
4. Run tests.
5. Build the frontend.
6. Build the backend.
7. Report failures.

Only configure automated production deployment if the hosting provider and required secrets are available.

Never print deployment secrets in workflow logs.

Do not deploy untested code automatically.

---

# 14. FINAL TESTING CHECKLIST

Complete the following verification.

### Website

- [ ] Homepage works.
- [ ] About page works.
- [ ] Services page works.
- [ ] Projects page works.
- [ ] Project details work.
- [ ] Blog works.
- [ ] Team section works.
- [ ] Testimonials work.
- [ ] FAQs work.
- [ ] Contact form works.
- [ ] English language works.
- [ ] Amharic language works.
- [ ] Mobile layout works.

### CMS

- [ ] Admin login works.
- [ ] Dashboard statistics use real data.
- [ ] Project CRUD works.
- [ ] Service CRUD works.
- [ ] Inquiry management works.
- [ ] Blog management works.
- [ ] Team management works.
- [ ] Testimonial management works.
- [ ] FAQ management works.
- [ ] Media uploads work.
- [ ] Website content updates work.
- [ ] Website settings save correctly.
- [ ] Permissions work.
- [ ] Activity logs work.

### Technical

- [ ] Frontend production build passes.
- [ ] Backend production build passes.
- [ ] TypeScript checks pass.
- [ ] Relevant tests pass.
- [ ] MongoDB connection works.
- [ ] API integration works.
- [ ] CORS configuration works.
- [ ] No critical security issue remains.
- [ ] Production environment configuration is correct.
- [ ] Deployment has been verified, if deployment access is available.

---

# 15. FINAL DELIVERABLES

At the end of this phase, provide:

1. Fully integrated TELos website.
2. Fully integrated Admin Dashboard and CMS.
3. Verified frontend/backend communication.
4. Verified MongoDB persistence.
5. Security audit and fixes.
6. Performance improvements.
7. SEO implementation.
8. Responsive and accessibility improvements.
9. Production-ready environment configuration.
10. Database backup and restore instructions.
11. Deployment configuration.
12. Automated testing workflow where appropriate.
13. Updated README and technical documentation.

### Final implementation report

Provide a clear report with:

- What was inspected.
- Problems discovered.
- Problems fixed.
- Files created.
- Files modified.
- Security improvements.
- Performance improvements.
- Tests executed.
- Actual test results.
- Build results.
- Deployment status.
- Remaining issues.
- Exact next steps required from the project owner.

Do not claim that tests passed unless they were actually executed.

Do not claim that the site is live unless you verified the deployed URL.

---

# FINAL COMMAND

Inspect the existing TELos Software Development repository and continue from Prompts 01–05.

Perform a complete system integration, security audit, quality assurance process, performance optimization, and production deployment preparation.

Preserve all existing working features.

Fix actual problems instead of hiding them.

Make the website reliable, secure, responsive, bilingual, and ready for real users.

**The final objective is a complete, professionally engineered TELos Software Development platform—not just a visually impressive website.**