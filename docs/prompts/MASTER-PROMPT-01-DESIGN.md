# TELos SOFTWARE DEVELOPMENT — MASTER PROMPT 01
## Product Design Strategy, UX Research, UI Architecture & Design System
### Phase 01 — Design Only (Reconstructed Working Edition)

> **Document status:** Reconstructed working edition based on the TELos project decisions and the requirements carried forward in Master Prompts 02–07. This is not a verbatim recovery of the original Prompt 01.

---

## 1. ROLE

Act as a principal product designer, senior UX strategist, UI/UX architect, design systems lead, accessibility specialist, and digital product consultant.

Your responsibility is to define the complete product experience and visual design blueprint for **TELos Software Development** before frontend implementation begins.

Do not write application code in this phase. Produce a precise, implementation-ready design specification that can be handed to the engineering phase.

## 2. PROJECT FOUNDATION

- **Product:** TELos Software Development
- **Industry:** Software development and digital solutions
- **Target market:** Ethiopia and international clients
- **Languages:** English and Amharic
- **Design direction:** Futuristic Technology — premium dark interface with electric-blue accents
- **Experience objective:** Present TELos as a credible, modern software engineering company, not a generic AI-generated template.

The product should communicate:
- Engineering competence.
- Innovation and creativity.
- Reliability and trust.
- Clarity and transparency.
- Professional service.
- Strong attention to detail.

Do not invent company history, staff counts, client names, awards, testimonials, years of experience, or project results. Use clearly labeled content placeholders wherever verified company information has not been supplied.

## 3. DESIGN GOALS AND SUCCESS CRITERIA

Create a cohesive experience that:
1. Explains what TELos does within seconds.
2. Makes services easy to understand and compare.
3. Demonstrates capability through genuine or clearly labeled demonstration work.
4. Guides visitors toward a project inquiry or consultation.
5. Works consistently in English and Amharic.
6. Provides accessible, responsive experiences across mobile, tablet, laptop, and desktop.
7. Establishes a reusable visual system for the public website, admin dashboard, and future client portal.
8. Can be implemented without major UX decisions being left to developers.

Prioritize usability, information hierarchy, readability, and conversion clarity over decorative effects.

## 4. VISUAL CONCEPT REVIEW

Evaluate these three possible visual directions before finalizing the selected direction.

### Concept A — Futuristic Technology (Selected)

A premium dark technology interface using deep navy surfaces, electric-blue and cyan accents, precise grid structures, restrained glow, and clear typography.

Characteristics:
- Dark, high-contrast foundation.
- Electric-blue primary actions.
- Cyan used sparingly for emphasis.
- Fine borders and controlled depth.
- Technical visual motifs used only when they support the content.
- Confident, spacious layouts.

### Concept B — Minimal Professional

A light or neutral interface with restrained color, strong typography, generous whitespace, and editorial layouts.

### Concept C — Creative Digital Studio

A more expressive direction with larger visual compositions, bold color accents, and more experimental section layouts.

### Selection rule

Use **Concept A — Futuristic Technology** as the final direction. Concepts B and C are comparison references only; do not mix them into the final system in a way that weakens consistency.

## 5. BRAND AND VISUAL IDENTITY

Develop a practical visual identity for TELos.

### Logo direction
- Use a clean TELos wordmark.
- Explore a simple geometric symbol that can work as a favicon and app icon.
- Keep the mark legible at small sizes.
- Provide light-background and dark-background variants if needed.
- Do not imitate another software company's logo.

### Color foundation

Use this palette as the initial design token proposal:

| Token | Value | Purpose |
|---|---|---|
| Main background | #080B14 | Main dark canvas |
| Secondary background | #0D1220 | Section and navigation surfaces |
| Card background | #111827 | Cards and panels |
| Primary blue | #3478F6 | Primary actions and links |
| Electric blue | #4EA5FF | Interactive emphasis |
| Cyan accent | #22D3EE | Secondary accent |
| Primary text | #F8FAFC | Main text |
| Secondary text | #94A3B8 | Supporting text |
| Border | #243044 | Dividers and outlines |
| Success | #22C55E | Positive status |
| Error | #EF4444 | Error status |

Define semantic tokens for backgrounds, text, borders, focus rings, interactive states, and status indicators. Verify contrast rather than assuming the palette is accessible.

### Typography
- English: Inter or a metrically compatible sans-serif.
- Amharic: Noto Sans Ethiopic.
- Define a consistent scale for display headings, page titles, section headings, body text, captions, labels, buttons, and metadata.
- Ensure Amharic line height, wrapping, and font rendering are explicitly tested.

### Shape, spacing, and elevation
Define:
- Spacing scale.
- Container widths.
- Responsive grid rules.
- Border-radius scale.
- Border treatments.
- Shadow and elevation levels.
- Icon sizing.
- Button heights and padding.
- Form-control dimensions.

Use glow and gradients sparingly. Avoid excessive glassmorphism, random glowing circles, over-animation, and low-contrast text.

## 6. INFORMATION ARCHITECTURE AND SITEMAP

Design the public website information architecture.

Recommended primary navigation:

- Home
- About
- Services
- Portfolio
- Technologies
- Process
- Blog
- Contact

Primary CTA: **Start a Project**

Plan the following public routes:

- /
- /about
- /services
- /services/:slug
- /portfolio
- /portfolio/:slug
- /technologies
- /process
- /team
- /careers
- /blog
- /blog/:slug
- /contact
- /request-project
- /faq
- /privacy
- /terms
- Not Found (404)

The final navigation may group secondary pages under About or other relevant menus, but every page must remain discoverable.

## 7. PUBLIC WEBSITE PAGE EXPERIENCE

For every page, define its purpose, target visitor questions, content hierarchy, primary action, secondary action, key components, responsive behavior, and empty/error states where relevant.

### A. Home page

Design a conversion-focused homepage with:
1. Header and primary navigation.
2. Hero section with a clear value proposition.
3. Primary CTA: Start a Project.
4. Secondary CTA: Explore Our Work.
5. Concise company introduction.
6. Services overview.
7. Featured projects or clearly labeled demonstration work.
8. Technologies overview, only using confirmed technologies.
9. Development process.
10. Reasons to work with TELos, without unsupported claims.
11. Testimonials section only when genuine approved testimonials exist.
12. FAQ preview.
13. Final project inquiry CTA.
14. Footer with contact and navigation links.

Possible hero headline:
**Engineering the Future Through Software.**

Possible Amharic headline:
**በሶፍትዌር የወደፊቱን ዓለም እንገንባ።**

Possible supporting description:
“We design and develop innovative digital products, modern websites and custom software solutions that help businesses grow.”

Treat these as draft copy that can be refined; provide natural Amharic localization rather than literal awkward translation.

### B. About page

Include:
- Company introduction.
- Mission.
- Vision.
- Core values.
- Company approach.
- Development philosophy.
- Team preview.
- Contact CTA.

Keep unknown company facts editable and clearly marked as content to be supplied.

### C. Services overview

Design clear service cards for:
1. Web Development.
2. Mobile Application Development.
3. Custom Software Development.
4. UI/UX Design.
5. E-commerce Development.
6. API Development and Integration.
7. Database Engineering.
8. Cloud and Deployment.
9. Website Maintenance.

Each card should include a title, concise description, relevant icon, key benefit, and Learn More action.

### D. Service detail template

Define a reusable page structure:
- Service-specific hero.
- Overview.
- Problems addressed.
- Features and deliverables.
- Benefits.
- Relevant technologies.
- Development approach.
- Related projects.
- FAQs.
- Project inquiry CTA.

### E. Portfolio and project details

Portfolio listing:
- Responsive project grid.
- Category filters.
- Search where useful.
- Featured project treatment.
- Project cards with image, title, category, short description, technologies, and View Project action.

Project detail:
- Project hero.
- Overview.
- Challenge.
- Solution.
- Technologies.
- Screenshots or gallery.
- Development approach.
- Related projects.
- Contact CTA.

Clearly distinguish real client work from demonstration projects. Never fabricate clients, outcomes, or metrics.

### F. Technologies page

Organize technologies into:
- Frontend.
- Backend.
- Mobile.
- Databases.
- Cloud and DevOps.
- UI/UX tools.

Only present technologies confirmed by TELos as actual capabilities or label them as technologies under consideration.

### G. Process page

Present the delivery process:
1. Discovery.
2. Requirements Analysis.
3. Planning.
4. UI/UX Design.
5. Development.
6. Testing.
7. Deployment.
8. Maintenance.

Use a readable timeline or process diagram.

### H. Team and Careers

Create reusable team profile patterns with name, role, biography, image, skills, and social links. Use placeholders until real details are supplied.

Careers should show company culture and opportunities only when actual openings exist. Do not fabricate job vacancies.

### I. Blog

Define:
- Blog listing.
- Featured article.
- Category navigation.
- Search.
- Pagination.
- Article cards.
- Article detail layout.
- Reading time.
- Related articles.

### J. Contact and project inquiry

Contact page:
- Contact introduction.
- Verified email and phone placeholders.
- Location only when confirmed.
- Social links.
- Contact form.
- Map only when a real business location is provided.

Project inquiry flow:
- Step 1: Name, email, phone, company.
- Step 2: Project category, description, required features.
- Step 3: Budget range, timeline, preferred contact method.
- Step 4: Review and submit.

Define validation, progress indication, field help, error feedback, success state, and submission failure state. Do not imply successful delivery without a real backend integration.

### K. FAQ, legal pages, and 404

- FAQ: categorized or searchable accordion.
- Privacy and Terms: clearly editable legal-content placeholders, not claims of legal approval.
- 404: simple branded page with a working return-home action.

## 8. ADMIN DASHBOARD UX ARCHITECTURE

Design the administrative experience as a coherent content-management workspace. This phase defines UX and UI only; implementation belongs to a later engineering prompt.

### Proposed navigation groups

**Overview**
- Dashboard

**Website Content**
- Projects
- Services
- Blog
- Team
- Testimonials
- FAQs
- Website Content
- Media Library

**Customer Management**
- Inquiries

**Configuration**
- Website Settings
- Administrators and Roles
- Activity Logs
- My Profile

### Dashboard overview

Define:
- Key metric cards based on real data.
- Recent inquiries.
- Recent activity.
- Project summary.
- Quick actions.
- Useful empty states.

Never design fake analytics as if they were actual company data.

### CMS interaction patterns

Specify:
- List/table views.
- Search and filtering.
- Pagination.
- Create and edit forms.
- Draft/published states.
- Preview.
- Confirmation dialogs.
- Validation errors.
- Save feedback.
- Delete and archive behavior.
- Empty states.
- Loading states.
- Permission-denied states.

Create detailed layouts for project, service, blog, team, testimonial, FAQ, inquiry, media, settings, and administrator management screens.

## 9. INQUIRY MANAGEMENT UX

Design an inquiry workflow for administrators:
- Inquiry list.
- Status and priority indicators.
- Search and filters.
- Inquiry detail view.
- Customer contact information.
- Project requirements.
- Attachments.
- Internal notes.
- Assignment.
- Status updates.
- Follow-up information.

Separate private internal notes from customer-visible content.

## 10. RESPONSIVE DESIGN SPECIFICATION

Define layouts and interaction behavior for:
- Small mobile.
- Large mobile.
- Tablet.
- Laptop.
- Desktop and wide desktop.

Specify:
- Breakpoint strategy.
- Navigation collapse behavior.
- Grid changes.
- Typography scaling.
- Image cropping.
- Form layout.
- Admin sidebar behavior.
- Table overflow or mobile alternatives.
- Touch target sizes.

Do not merely shrink desktop screens. Redesign component behavior for narrow screens.

## 11. ACCESSIBILITY AND USABILITY

Follow WCAG 2.2 AA as the target.

Specify:
- Semantic heading structure.
- Keyboard navigation.
- Visible focus indicators.
- Accessible form labels and errors.
- Sufficient contrast.
- Alt text requirements.
- Reduced-motion support.
- Screen-reader labels.
- Accessible dialogs and menus.
- Logical focus order.
- Non-color status indicators.

Ensure bilingual text does not break layouts or controls.

## 12. INTERACTION AND MOTION GUIDELINES

Define interaction states for:
- Default.
- Hover.
- Focus.
- Active.
- Disabled.
- Loading.
- Success.
- Error.

Motion should clarify state changes and navigation, not distract. Respect reduced-motion preferences. Avoid animation that harms readability or performance.

## 13. CONTENT AND LOCALIZATION RULES

English and Amharic are first-class languages.

Define:
- Language selector behavior.
- Translation completeness rules.
- Locale-aware text direction only where required.
- Font loading.
- Date and number formatting.
- Navigation label lengths.
- Translation fallback behavior.
- Language persistence.

Do not treat Amharic as a simple afterthought. Design for its actual text length and typography.

## 14. DESIGN SYSTEM DELIVERABLES

Provide a complete design specification containing:

1. Brand and visual direction.
2. Logo usage guidance.
3. Color tokens and semantic color roles.
4. Typography scale for English and Amharic.
5. Spacing and layout system.
6. Grid and container rules.
7. Buttons and links.
8. Form controls.
9. Cards and panels.
10. Navigation components.
11. Badges and status indicators.
12. Tables and pagination.
13. Dialogs and drawers.
14. Tabs and accordions.
15. Alerts and notifications.
16. Empty, loading, success, and error states.
17. Responsive behavior.
18. Accessibility requirements.
19. Motion guidelines.
20. Reusable component inventory.

## 15. REQUIRED DESIGN SCREENS

Create detailed screen specifications or high-fidelity mockups for:

### Public website
- Home desktop and mobile.
- About.
- Services listing.
- Service detail.
- Portfolio listing.
- Project detail.
- Technologies.
- Process.
- Blog listing.
- Blog article.
- Contact.
- Multi-step project inquiry.
- FAQ.
- 404.

### Admin dashboard
- Admin login.
- Dashboard overview.
- Project list and editor.
- Service list and editor.
- Inquiry list and detail.
- Blog list and editor.
- Team management.
- Testimonial management.
- FAQ management.
- Media library.
- Website content editor.
- Website settings.
- Administrator and role management.
- Activity logs.
- Profile.

For each screen, specify desktop and mobile behavior where appropriate.

## 16. DESIGN QUALITY REVIEW

Before finalizing, check:

- Is the value proposition immediately understandable?
- Is the primary CTA clear?
- Is navigation predictable?
- Are page layouts consistent?
- Are visual effects restrained?
- Is the text readable?
- Are English and Amharic both supported?
- Does every form have clear validation and feedback?
- Are empty and error states defined?
- Are mobile interactions usable?
- Are accessibility requirements addressed?
- Are all business claims supported by supplied facts?
- Can the engineering team implement the design without guessing?

Record unresolved questions and content dependencies rather than inventing answers.

## 17. STRICT PHASE 01 BOUNDARIES

This is a design and UX architecture phase only.

Do not:
- Build the React frontend.
- Write backend code.
- Create MongoDB models.
- Implement APIs.
- Implement authentication.
- Connect external services.
- Claim working functionality.
- Move into Prompt 02 implementation.

You may provide design annotations, user flows, component specifications, wireframes, and visual mockups as design deliverables.

## 18. FINAL HANDOFF

Deliver:
1. Product and UX strategy.
2. Approved visual direction.
3. Sitemap and navigation architecture.
4. Page-by-page content hierarchy.
5. Public website screen specifications.
6. Admin dashboard screen specifications.
7. User flows and inquiry journey.
8. Design system and component inventory.
9. Responsive design rules.
10. Accessibility checklist.
11. English and Amharic localization guidance.
12. Content placeholders and unresolved questions.
13. Engineering handoff notes for Master Prompt 02.

### FINAL COMMAND

Design the TELos Software Development digital product as a coherent, premium, bilingual software-company experience using the selected **Futuristic Technology** direction.

Complete the product strategy, UX architecture, page layouts, admin dashboard UX, and design system.

Keep this phase strictly design-only. Deliver a clear, detailed blueprint that the frontend engineering phase can implement without inventing missing UX decisions.

**The objective is a usable, credible, accessible, responsive TELos product experience—not merely an attractive collection of screens.**
