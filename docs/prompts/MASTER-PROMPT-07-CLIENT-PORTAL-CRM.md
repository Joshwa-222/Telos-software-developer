# TELos SOFTWARE DEVELOPMENT — MASTER PROMPT 07
## Advanced Business Features, Client Portal, CRM, Automation & Growth Analytics

### 1. PROJECT OVERVIEW

Act as a senior full-stack software architect, SaaS developer, CRM engineer, UI/UX designer, database architect, and business automation specialist.

Your task is to extend the existing TELos Software Development platform with advanced business-management capabilities.

**Project:** TELos Software Development

**Existing frontend:** React, TypeScript, Vite, Tailwind CSS  
**Existing backend:** Node.js, Express, TypeScript  
**Existing database:** MongoDB and Mongoose  
**Existing administration:** Admin Dashboard and CMS  
**Design direction:** Futuristic Technology — premium dark interface with electric-blue accents  
**Languages:** English and Amharic

Continue from Prompts 01–06.

This phase must extend the existing application. It must not replace the current website, CMS, backend, authentication, or database.

### Main objectives

Build:

1. Secure Client Portal.
2. Customer Relationship Management (CRM).
3. Client project tracking.
4. Project milestone and task management.
5. Client document and file exchange.
6. Quote and proposal management.
7. Appointment and consultation booking.
8. Automated notifications and follow-ups.
9. Advanced business analytics.
10. Lead generation and conversion tools.
11. Optional AI-powered business assistance.
12. Advanced administrator controls.

**Important:** Build these as integrated modules within the existing TELos application, not as separate disconnected applications.

---

# 2. PROJECT INSPECTION AND INTEGRATION

Before implementation, inspect the existing repository and identify:

- Existing public pages.
- Existing Admin Dashboard.
- Existing authentication system.
- Existing administrator roles and permissions.
- Existing MongoDB models.
- Existing API routes and controllers.
- Existing CMS modules.
- Existing project and inquiry management.
- Existing file-upload system.
- Existing notification infrastructure.
- Existing English and Amharic localization.
- Existing deployment and environment configuration.

Reuse existing systems wherever possible.

### Integration rules

- Do not create a second authentication system.
- Do not create a second database.
- Do not duplicate existing projects, inquiries, users, or media models.
- Reuse the existing API client and error-handling architecture.
- Follow existing TypeScript conventions.
- Keep public website functionality working.
- Preserve existing administrative functionality.
- Add new models only when the existing data model cannot properly represent the required feature.
- Use migrations or safe schema changes when necessary.
- Do not use mock data as a replacement for real functionality.

Create a clear implementation plan based on the actual repository before making changes.

---

# 3. SECURE CLIENT PORTAL

Build a dedicated Client Portal where TELos customers can access their accounts and follow the progress of their projects.

### Client portal routes

Use the existing routing architecture. Suggested routes:

- `/portal/login`
- `/portal/register` if public registration is enabled.
- `/portal/dashboard`
- `/portal/projects`
- `/portal/projects/:id`
- `/portal/messages`
- `/portal/documents`
- `/portal/proposals`
- `/portal/profile`
- `/portal/notifications`

### Client dashboard

Display:

- Welcome message.
- Client account information.
- Active projects.
- Completed projects.
- Pending approvals.
- Upcoming project milestones.
- Recent project updates.
- Unread notifications.
- Recent client messages.

Only display data belonging to the authenticated client.

### Client account features

Allow clients to:

- View and update permitted profile information.
- Change their password.
- View their assigned projects.
- View approved project updates.
- View project milestones.
- Download permitted documents.
- Submit project feedback.
- Communicate with authorized TELos staff.
- Review proposals.
- Receive notifications.

Do not allow clients to access the Admin Dashboard.

Do not allow one client to view another client's private information, projects, messages, or files.

---

# 4. CLIENT AUTHENTICATION AND ACCOUNT MANAGEMENT

Integrate client authentication with the existing security architecture.

Support:

- Secure client login.
- Account verification where appropriate.
- Secure password reset.
- Logout.
- Session expiration.
- Account deactivation.
- Profile management.

### Account creation

Support one of these approaches based on the existing business workflow:

1. Administrators invite clients to create accounts.
2. Clients register through a public registration form, subject to verification and approval.

Make the approach configurable.

For invited clients:

- Generate a secure invitation.
- Set an expiration time.
- Validate the invitation on the backend.
- Prevent reuse of expired or consumed invitations.
- Never expose invitation secrets in logs.

For public registration, implement rate limiting, validation, and appropriate spam protection.

Do not automatically grant administrative privileges to clients.

### Client roles

Use clear role separation:

- Super Admin.
- Admin.
- Editor.
- Client.

The Client role must have access only to explicitly permitted client-facing functionality.

Enforce authorization on every protected backend endpoint.

---

# 5. CUSTOMER RELATIONSHIP MANAGEMENT (CRM)

Extend the existing inquiry management system into a practical CRM.

Do not duplicate existing inquiry records. Build on the existing lead and inquiry data model.

### CRM dashboard

Display:

- Total leads.
- New leads.
- Contacted leads.
- Qualified leads.
- Proposals sent.
- Won opportunities.
- Lost opportunities.
- Follow-ups due.
- Lead conversion rate, calculated from actual data.

### Lead management

Manage customer and potential-client information:

- Name.
- Email.
- Phone number.
- Company name.
- Requested service.
- Lead source.
- Budget range, where provided.
- Project description.
- Assigned administrator.
- Lead status.
- Priority.
- Creation date.
- Last contact date.
- Next follow-up date.

Do not invent client information.

### Lead pipeline

Implement these configurable stages:

1. New.
2. Contacted.
3. Qualified.
4. Proposal Sent.
5. Negotiation.
6. Won.
7. Lost.

Provide:

- Table view.
- Kanban pipeline view.
- Search.
- Date filters.
- Status filters.
- Assigned-user filters.
- Priority filters.
- Lead details.
- Internal notes.
- Follow-up tasks.

When an inquiry is converted into a client or project, preserve its history and relationships.

Prevent duplicate client records where practical by identifying matching email addresses or other reliable identifiers.

### CRM activity history

Record important activities:

- Lead created.
- Lead assigned.
- Status changed.
- Note added.
- Follow-up scheduled.
- Proposal sent.
- Lead converted.
- Lead closed.

Private CRM notes must never appear in public APIs or client-visible pages.

---

# 6. CLIENT PROJECT MANAGEMENT

Create a project management interface that connects the existing Projects CMS to client-specific work.

### Project information

Use the existing project model where possible.

Support:

- Project name.
- Client.
- Project description.
- Project category.
- Start date.
- Expected delivery date.
- Actual completion date.
- Project manager.
- Assigned team members.
- Project status.
- Progress indicator.
- Milestones.
- Related documents.

### Project statuses

Use configurable statuses such as:

- Planning.
- In Progress.
- On Hold.
- Under Review.
- Completed.
- Cancelled.

### Project dashboard

Authorized administrators can see all projects they are permitted to manage.

Clients can only see their assigned projects and information explicitly made visible to them.

### Project details page

Display:

- Overview.
- Project description.
- Progress.
- Current status.
- Timeline.
- Milestones.
- Approved deliverables.
- Client-visible updates.
- Relevant documents.
- Messages.

Do not expose internal administrator notes, private costs, confidential staff communications, or unrelated client information.

---

# 7. MILESTONE AND TASK MANAGEMENT

Implement project milestones and task tracking.

### Milestones

Each milestone should support:

- Title.
- Description.
- Project reference.
- Target date.
- Completion date.
- Status.
- Display order.
- Client visibility.
- Approval requirement, where appropriate.

### Task management

Support:

- Task title.
- Task description.
- Related project.
- Assigned administrator or staff member.
- Due date.
- Priority.
- Status.
- Completion date.

Suggested task statuses:

- To Do.
- In Progress.
- Under Review.
- Completed.

### Client visibility

Administrators must explicitly decide which milestones and updates are visible to clients.

Clients must not be able to modify internal task assignments or privileged project information.

### Progress calculation

Calculate progress using a clearly defined and consistent method.

For example, calculate milestone completion as:

Completed milestones divided by total milestones multiplied by 100.

Do not allow arbitrary progress numbers that contradict the actual project data unless an authorized manual-progress feature is intentionally implemented.

---

# 8. CLIENT DOCUMENT AND FILE MANAGEMENT

Create a secure document management system.

Support:

- Project documents.
- Proposals.
- Agreements.
- Briefs.
- Design previews.
- Approved deliverables.
- Other permitted project files.

### Document functionality

Administrators can:

- Upload files.
- Organize documents by project.
- Assign documents to clients.
- Set client visibility.
- Replace documents.
- Archive documents.
- Delete documents when permitted.

Clients can:

- View authorized documents.
- Download permitted documents.
- Upload files when explicitly allowed.
- View document descriptions and relevant metadata.

### Security requirements

- Validate MIME types and actual file content.
- Enforce upload-size limits.
- Generate safe unique filenames.
- Verify ownership and permission before downloads.
- Use private storage for sensitive documents.
- Avoid guessable public file URLs.
- Do not expose sensitive documents through public endpoints.
- Record relevant upload and download events where appropriate.
- Never accept executable or dangerous file types without a specific and justified requirement.

Use the existing media and storage infrastructure where possible.

---

# 9. QUOTATIONS AND PROPOSAL MANAGEMENT

Build a proposal management system connected to CRM leads and clients.

### Proposal details

Support:

- Proposal title.
- Proposal reference number.
- Client.
- Related inquiry or opportunity.
- Description.
- Services included.
- Deliverables.
- Estimated timeline.
- Pricing.
- Currency.
- Terms and conditions.
- Expiration date.
- Proposal status.

### Pricing configuration

Allow authorized administrators to configure supported currencies.

Do not hardcode currency assumptions throughout the application.

The system should support appropriate number formatting and configurable currency display.

### Proposal statuses

- Draft.
- Sent.
- Viewed, if reliable tracking is available.
- Accepted.
- Rejected.
- Expired.

### Proposal workflow

1. Administrator creates a proposal.
2. Proposal is associated with a lead or client.
3. Administrator reviews and sends it.
4. Client views the proposal through a secure link or authenticated portal.
5. Client accepts or rejects where this action is enabled.
6. The backend records the decision and timestamp.
7. The CRM pipeline can reflect the outcome.

Only authorized users can alter the proposal's financial information.

Keep a record of important proposal changes.

### PDF generation

Where feasible, provide a professional PDF proposal with:

- TELos branding.
- Client details.
- Proposal reference.
- Description.
- Deliverables.
- Pricing.
- Timeline.
- Terms.
- Contact information.

Ensure that generated PDFs display Amharic text correctly when Amharic content is included.

Do not claim a proposal has been sent merely because a PDF was generated.

---

# 10. APPOINTMENT AND CONSULTATION BOOKING

Create a consultation booking feature for potential clients.

### Public booking form

Allow visitors to submit:

- Name.
- Email.
- Phone number.
- Company, if applicable.
- Requested service.
- Preferred date.
- Preferred time.
- Time zone.
- Message.

Validate the form on the frontend and backend.

### Administrator scheduling

Administrators should be able to:

- View booking requests.
- Approve or reject requests.
- Propose an alternative time.
- Confirm appointments.
- Reschedule appointments.
- Cancel appointments.
- Add internal notes.
- Mark appointments as completed.

### Booking rules

- Avoid double booking where availability management is implemented.
- Store timestamps consistently.
- Display times in the configured business time zone.
- Make the time zone configurable; use Africa/Addis_Ababa as the initial business default only if appropriate.
- Use clear date and time formatting.
- Do not promise an appointment before it has been confirmed.

Provide a calendar view and a list view for administrators.

External calendar integrations should be optional and enabled only when their credentials and configuration are available.

---

# 11. NOTIFICATION AND AUTOMATION SYSTEM

Implement a reusable notification system.

### Notification events

Support notifications for:

- New inquiry.
- Lead assignment.
- Upcoming follow-up.
- Proposal sent.
- Proposal accepted or rejected.
- Project status change.
- Milestone completed.
- Client message received.
- New document shared.
- Appointment request.
- Appointment confirmation.
- Appointment changes.

### In-app notifications

Provide:

- Notification list.
- Unread count.
- Mark as read.
- Mark all as read.
- Notification timestamps.
- Links to relevant records.

### Email notifications

Use the existing email provider or notification infrastructure.

If email configuration is not available, implement the email-service integration layer without pretending emails were sent.

Use configurable templates for:

- Inquiry confirmation.
- Appointment confirmation.
- Proposal notification.
- Client invitation.
- Password reset.
- Project update.

Provide English and Amharic templates where appropriate.

### Automation rules

Build a simple automation engine that allows authorized administrators to configure rules such as:

- Notify an administrator when a new inquiry arrives.
- Remind the assigned administrator about a follow-up.
- Notify a client when a visible milestone is completed.
- Notify a client when a proposal is available.
- Notify staff when an appointment is requested.

Include:

- Trigger.
- Conditions.
- Action.
- Enabled/disabled status.
- Execution history.
- Error status.

Use a reliable background job mechanism only if the project infrastructure supports it.

Do not create unreliable timer-based jobs inside an ordinary web request process.

Prevent duplicate notification delivery where possible using idempotency controls.

Do not create spam-like repeated messages.

---

# 12. ADVANCED BUSINESS ANALYTICS

Extend the existing Admin Dashboard with real business intelligence.

Use actual database information.

### Business metrics

Display:

- Total inquiries.
- Qualified leads.
- Lead conversion rate.
- Proposals sent.
- Accepted proposals.
- Active clients.
- Active projects.
- Completed projects.
- Upcoming milestones.
- Upcoming appointments.
- New client registrations.
- Returning clients, where reliable identification exists.

### Analytics charts

Implement:

1. Leads over time.
2. Inquiry sources.
3. Lead conversion funnel.
4. Projects by status.
5. Service demand.
6. Proposal outcomes.
7. Monthly project completions.
8. Appointment activity.

### Date filters

Provide:

- Last 7 days.
- Last 30 days.
- Last 90 days.
- Current month.
- Previous month.
- Custom range.

### Analytics rules

- Calculate metrics from actual stored records.
- Clearly define each metric.
- Avoid fake percentage increases.
- Handle missing historical data.
- Respect administrator permissions.
- Do not expose private client details in aggregated reports.

Provide CSV exports for authorized users where useful.

---

# 13. CLIENT COMMUNICATION CENTER

Implement secure messaging between clients and authorized TELos staff.

### Features

- Conversation list.
- Conversation details.
- Message history.
- Message timestamps.
- Read status.
- Related project reference.
- File attachments where permitted.
- Unread message indicators.

### Security

- Verify that the authenticated user belongs to the conversation.
- Verify the administrator's permission to access it.
- Prevent users from guessing IDs to access other conversations.
- Validate and scan attachments where supported.
- Limit attachment size.
- Keep internal staff notes separate from client-facing messages.

Do not expose messages through public endpoints.

Use the existing API and notification infrastructure.

Real-time messaging is optional. Implement it only when compatible with the current project architecture. A reliable polling or refresh-based approach is preferable to adding unnecessary infrastructure.

---

# 14. LEAD GENERATION AND WEBSITE CONVERSION TOOLS

Improve the existing public website's ability to convert visitors into potential clients.

### Contact and inquiry improvements

Provide:

- Better service selection.
- Project description field.
- Contact preference.
- Budget range, if appropriate.
- Preferred consultation time.
- Clear submission confirmation.
- Spam protection.
- Server-side validation.

### Call-to-action management

Allow authorized administrators to control:

- Homepage CTA text.
- CTA destination.
- Service-page CTA.
- Project-page CTA.
- Contact-page CTA.
- Consultation booking CTA.

Use the existing CMS models and public APIs.

### Newsletter subscription

Implement a basic newsletter subscription system only if it fits the business requirements.

Support:

- Subscription form.
- Email validation.
- Consent.
- Confirmation process.
- Unsubscribe mechanism.
- Subscription status.
- Export of authorized subscriber data.

Do not send marketing emails without appropriate permission and an unsubscribe mechanism.

### Conversion tracking

Track useful events such as:

- Contact form submitted.
- Consultation requested.
- Proposal viewed.
- Proposal accepted.
- Newsletter subscription confirmed.

Do not collect unnecessary personal information or introduce invasive tracking.

---

# 15. OPTIONAL AI-POWERED BUSINESS ASSISTANT

Provide an optional AI integration layer, not a mandatory dependency.

Potential features:

- Drafting responses to inquiries.
- Summarizing long inquiry messages.
- Suggesting service categories.
- Drafting proposal descriptions.
- Summarizing project updates.
- Generating SEO descriptions.
- Suggesting blog outlines.

### AI safety and control

- AI-generated content must be reviewed before publication or sending.
- Do not automatically send AI-generated messages to clients without an explicitly configured approval workflow.
- Do not expose private client data to an external AI provider without appropriate authorization and configuration.
- Use environment variables for provider credentials.
- Do not hardcode API keys.
- Provide a fallback when the provider is unavailable.
- Keep AI features disabled until configured by an authorized administrator.

Do not invent an AI provider or pretend the service is connected when it is not.

---

# 16. ADMIN DASHBOARD NAVIGATION UPDATES

Extend the existing admin navigation with:

- Dashboard.
- Projects.
- Services.
- Inquiries.
- CRM & Leads.
- Clients.
- Client Projects.
- Milestones & Tasks.
- Proposals.
- Appointments.
- Messages.
- Blog.
- Team.
- Testimonials.
- FAQs.
- Media.
- Website Content.
- Notifications.
- Automation.
- Analytics.
- User Management.
- Activity Logs.
- Settings.
- My Profile.

Use grouped navigation to prevent overcrowding.

Hide or disable restricted menu items according to permissions, but always enforce permissions in the backend.

---

# 17. CLIENT PORTAL DESIGN

Use the established TELos visual identity.

The client portal should feel like a premium technology service platform.

### Client interface

Include:

- Responsive sidebar or navigation.
- Overview cards.
- Project progress visualization.
- Timeline.
- Document center.
- Proposal section.
- Messages.
- Notifications.
- Account settings.

Use the same design language as the main website and admin dashboard while making the client portal simpler and easier to use.

Provide empty states that explain what clients should expect when they have no active projects or documents.

Do not display unnecessary administrative controls to clients.

---

# 18. DATABASE AND DATA MODEL REQUIREMENTS

Inspect existing Prompt 03 and Prompt 04 models before creating or changing schemas.

Potential new collections may include:

- Clients.
- ClientInvitations.
- ProjectMilestones.
- ProjectTasks.
- Proposals.
- Appointments.
- Conversations.
- Messages.
- Notifications.
- AutomationRules.
- AutomationExecutions.
- NewsletterSubscriptions.

These are suggestions, not mandatory duplicate collections.

Reuse existing administrators, projects, inquiries, media, and activity-log models where possible.

### Data relationships

Design proper references between:

- Clients and projects.
- Clients and proposals.
- Projects and milestones.
- Projects and tasks.
- Clients and conversations.
- Conversations and messages.
- Users and notifications.
- Leads and proposals.
- Appointments and clients or leads.

### Data integrity

Implement:

- Mongoose schema validation.
- Appropriate indexes.
- Unique constraints where required.
- Pagination.
- Safe queries.
- Referential integrity checks.
- Timestamps.
- Proper handling of deleted or inactive records.

Use transactions when multiple database operations must succeed or fail together and the MongoDB deployment supports them.

Do not delete important business history unnecessarily.

Avoid storing duplicate copies of the same client or project information without a clear reason.

---

# 19. API IMPLEMENTATION

Follow existing API conventions.

Suggested endpoint groups:

### Client portal

- `/api/client/auth`
- `/api/client/profile`
- `/api/client/dashboard`
- `/api/client/projects`
- `/api/client/documents`
- `/api/client/proposals`
- `/api/client/messages`
- `/api/client/notifications`

### CRM

- `/api/admin/crm/leads`
- `/api/admin/crm/activities`
- `/api/admin/crm/follow-ups`
- `/api/admin/crm/pipeline`

### Project tracking

- `/api/admin/project-management`
- `/api/admin/milestones`
- `/api/admin/tasks`

### Proposals

- `/api/admin/proposals`
- `/api/client/proposals`

### Appointments

- `/api/appointments`
- `/api/admin/appointments`

### Notifications and automation

- `/api/admin/notifications`
- `/api/client/notifications`
- `/api/admin/automation/rules`
- `/api/admin/automation/executions`

### Analytics

- `/api/admin/analytics/business`
- `/api/admin/analytics/leads`
- `/api/admin/analytics/projects`
- `/api/admin/analytics/proposals`

### Messaging

- `/api/client/conversations`
- `/api/admin/conversations`

These are proposed route groups. Reuse existing endpoint structures and naming conventions where they already exist.

Every endpoint must include the correct authentication, permission checks, input validation, and error handling.

Never allow a client to access records belonging to another client.

---

# 20. PERMISSIONS AND PRIVACY

Implement least-privilege access.

### Super Admin

- Full administrative control.
- User and permission management.
- System configuration.
- All authorized business data.
- Automation management.

### Admin

- Manage assigned business operations.
- Manage clients, leads, projects, tasks, proposals, and appointments according to permissions.
- Access permitted analytics.

### Editor

- Manage permitted public content.
- No access to restricted client financial records.
- No access to administrator management or security configuration.

### Client

- Access only their own account.
- Access only their own projects.
- Access only their own approved documents.
- Access only their own proposals.
- Access only their own conversations and notifications.
- Perform only actions explicitly allowed by the business workflow.

Enforce all restrictions on the backend.

Do not rely on hidden buttons or frontend route guards for security.

---

# 21. INTERNATIONALIZATION AND LOCALIZATION

Support English and Amharic across the new features.

Translate:

- Client portal.
- CRM.
- Appointment booking.
- Proposal interface.
- Project tracking.
- Notification messages.
- Form labels.
- Validation errors.
- Status indicators.
- Dashboard analytics.
- Email templates.
- Confirmation dialogs.

Ensure that:

- Amharic text displays correctly.
- Date and number formatting are appropriate.
- Currency formatting is configurable.
- Time zones are handled consistently.
- Language changes do not accidentally erase unsaved data.

Use the established localization architecture.

---

# 22. TESTING REQUIREMENTS

Test the actual end-to-end functionality.

### Client portal tests

- Client login.
- Client profile update.
- Client project access.
- Client document download.
- Client proposal review.
- Client message submission.
- Client notification access.
- Unauthorized cross-client access rejection.

### CRM tests

- Create lead.
- Update lead.
- Assign lead.
- Move lead through the pipeline.
- Add internal notes.
- Schedule follow-up.
- Convert lead to client.
- Verify activity history.

### Project tests

- Create project.
- Assign client.
- Create milestone.
- Update milestone.
- Complete task.
- Verify progress calculation.
- Verify client-visible content.
- Verify private notes remain private.

### Proposal tests

- Create proposal.
- Update proposal.
- Send proposal.
- Client views proposal.
- Client accepts or rejects.
- Verify proposal history.

### Appointment tests

- Submit booking request.
- Approve appointment.
- Reject appointment.
- Reschedule appointment.
- Check conflicting appointments where availability rules exist.

### Notification tests

- Trigger notification.
- Display unread count.
- Mark notification as read.
- Verify recipient authorization.
- Verify duplicate notifications are controlled.

### Security tests

- Verify role permissions.
- Verify client data isolation.
- Verify private document access.
- Verify file validation.
- Verify no sensitive information appears in public API responses.

Run the project's relevant unit, integration, and end-to-end tests.

Do not claim a feature works unless it has actually been tested.

---

# 23. PERFORMANCE AND RELIABILITY

Implement:

- Efficient MongoDB queries.
- Database indexes.
- Pagination.
- Search and filtering.
- Appropriate caching.
- Safe cache invalidation.
- Optimized images.
- Lazy loading.
- Reusable frontend components.
- Reliable background processing where required.
- Graceful handling of failed integrations.

Do not allow analytics queries to unnecessarily slow down the main application.

Keep private client data out of public caches.

---

# 24. IMPLEMENTATION ORDER

Implement this phase in a structured sequence:

**Step 1 — Repository inspection**

Review the existing work from Prompts 01–06.

**Step 2 — Data model planning**

Identify reusable schemas and determine which new business models are genuinely required.

**Step 3 — Client authentication**

Implement secure client account access and role separation.

**Step 4 — Client Portal**

Build the client dashboard, projects, documents, proposals, messages, and notifications.

**Step 5 — CRM**

Extend inquiry management into a complete lead pipeline.

**Step 6 — Project tracking**

Implement milestones, tasks, progress, and client-visible updates.

**Step 7 — Proposals**

Implement proposal creation, review, acceptance, and PDF generation.

**Step 8 — Appointments**

Implement consultation booking and administrator scheduling.

**Step 9 — Notifications and automation**

Implement reliable notification delivery and configurable automation.

**Step 10 — Analytics**

Add real business analytics based on database records.

**Step 11 — Lead generation**

Improve conversion tools and optional newsletter functionality.

**Step 12 — Optional AI integration**

Implement only when provider configuration and privacy controls are available.

**Step 13 — Testing and integration**

Test the complete client, admin, CRM, and public website workflows.

---

# 25. FINAL DELIVERABLES

At completion, provide:

1. Working Client Portal.
2. Client account management.
3. CRM and lead pipeline.
4. Client project tracking.
5. Milestone and task management.
6. Secure document management.
7. Proposal management.
8. Appointment booking.
9. Notification center.
10. Automation features.
11. Business analytics dashboard.
12. Lead generation improvements.
13. Optional AI integration layer.
14. English and Amharic support.
15. Updated API documentation.
16. Database changes and migration information.
17. Tests and actual results.
18. Updated README and deployment documentation.

### Final implementation report

Include:

- Features completed.
- Existing modules reused.
- New files created.
- Existing files modified.
- Database models added or changed.
- API endpoints added or reused.
- Security controls implemented.
- Tests executed.
- Actual test results.
- Environment variables required.
- Integrations requiring external credentials.
- Remaining limitations.

Do not expose credentials or private configuration values.

Do not claim deployment, email delivery, AI integration, or payment functionality unless the relevant integration has actually been configured and verified.

---

# 26. FINAL QUALITY STANDARD

TELos should now operate as a professional digital services business platform.

It should support the complete business journey:

**Visitor → Inquiry → Lead → Client → Proposal → Project → Milestones → Deliverables → Completion.**

The system must be:

- Secure.
- Reliable.
- Bilingual.
- Responsive.
- Maintainable.
- Connected to MongoDB.
- Integrated with the existing website and CMS.
- Easy for administrators to operate.
- Simple for clients to understand.

Do not overengineer the application or introduce unnecessary external services.

Prioritize real business functionality, data privacy, and maintainability over decorative features.

# FINAL COMMAND

Inspect the existing TELos Software Development repository and continue from Prompts 01–06.

Implement Prompt 07 as a complete advanced business platform with a secure Client Portal, CRM, project tracking, proposals, appointments, notifications, automation, and business analytics.

Connect every implemented feature to the existing frontend, backend, authentication, and MongoDB database.

Preserve all existing working functionality.

Test real workflows with actual database persistence.

**Do not build a collection of attractive screens. Build a connected business system that TELos can actually use to manage clients, leads, projects, and customer relationships.**