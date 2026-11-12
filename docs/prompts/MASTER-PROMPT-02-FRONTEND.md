# MASTER PROMPT 02 — TELos SOFTWARE DEVELOPMENT
## COMPLETE FRONTEND ENGINEERING & IMPLEMENTATION

### ROLE

Act as a senior frontend architect, principal React developer, TypeScript engineer, UI implementation specialist, and accessibility engineer.

You are responsible for transforming the approved TELos UX/UI design blueprint into a complete, production-quality frontend application.

You must write actual working code, not just describe how the website should look.

---

# 1. PROJECT IDENTITY

**Project:** TELos Software Development

**Industry:** Software Development and Digital Solutions

**Target market:** Ethiopia and international clients.

**Website languages:**
- English (EN)
- Amharic (አማርኛ)

**Design direction:** A — Futuristic Technology.

### Brand characteristics

The website must communicate:
- Innovation.
- Software engineering excellence.
- Creativity.
- Reliability.
- Professionalism.
- Modern technology.

The experience must look like an established international software engineering company.

Do not make the website look like a generic AI website template.

# 2. REQUIRED TECHNOLOGY STACK

Use the following technologies:

| Technology | Purpose |
|---|---|
| React | Frontend framework |
| TypeScript | Type safety |
| Vite | Development and build tooling |
| Tailwind CSS | Styling |
| React Router | Page navigation |
| Motion for React | Animations |
| Lucide React | Icons |
| React Hook Form | Form management |
| Zod | Validation |
| Recharts | Dashboard charts |

Use compatible stable versions and configure the dependencies correctly.

Do not introduce unnecessary libraries.

# 3. VISUAL DESIGN SYSTEM

Implement the selected futuristic dark design.

### Color palette

Use the following starting palette:

- Main background: #080B14
- Secondary background: #0D1220
- Card background: #111827
- Primary blue: #3478F6
- Electric blue: #4EA5FF
- Cyan accent: #22D3EE
- Primary text: #F8FAFC
- Secondary text: #94A3B8
- Border: #243044
- Success: #22C55E
- Error: #EF4444

Use gradients selectively.

### Typography

Use:
- Inter for English.
- Noto Sans Ethiopic for Amharic.

Create a consistent typography hierarchy for:
- Hero headings.
- Section headings.
- Subheadings.
- Body text.
- Descriptions.
- Buttons.
- Labels.
- Metadata.

Do not use excessively large text that breaks mobile layouts.

### Visual effects

Implement:
- Subtle blue ambient glow.
- Sophisticated shadows.
- Fine borders.
- Soft gradient backgrounds.
- Carefully designed hover states.
- Smooth page transitions.
- Subtle background grid patterns where appropriate.
- Professional card interactions.

Avoid:
- Excessive glassmorphism.
- Random glowing circles.
- Excessive animation.
- Distracting backgrounds.
- Unnecessary visual effects.

The design must remain professional and readable.

# 4. BRAND AND NAVIGATION

Create a consistent TELos brand identity throughout the website.

Implement:
- Custom TELos text-based logo or SVG wordmark.
- Responsive navigation.
- Sticky header.
- Mobile navigation drawer.
- Active navigation states.
- Dropdown navigation.
- Language selector.
- Accessible navigation controls.
- Contact CTA.

The navigation should include:

Home | About | Services | Portfolio | Technologies | Blog | Contact

Primary button: **Start a Project**

# 5. COMPLETE PUBLIC WEBSITE

Implement all the following pages.

## A. HOME PAGE

Route: /

Build a premium homepage.

Sections:

1. Navigation.
2. Hero.
3. Company introduction.
4. Technology or credibility strip.
5. Services overview.
6. Featured projects.
7. Why choose TELos.
8. Development process.
9. Technologies.
10. Testimonials.
11. Frequently asked questions.
12. Project inquiry CTA.
13. Footer.

### Hero section

Use a strong headline such as:

"Engineering the Future Through Software."

Amharic version:

"በሶፍትዌር የወደፊቱን ዓለም እንገንባ።"

Description:

"We design and develop innovative digital products, modern websites and custom software solutions that help businesses grow."

Create the equivalent natural Amharic translation.

Hero actions:
- Start a Project.
- Explore Our Work.

Create a custom visual composition using CSS, SVG or appropriate graphics.

It may include:
- Abstract digital structures.
- Code-inspired visual elements.
- Subtle animated geometric shapes.
- Layered technology-inspired panels.

Do not use generic stock illustrations as the entire hero design.

## B. ABOUT PAGE

Route: /about

Sections:
- About TELos.
- Company introduction.
- Mission.
- Vision.
- Core values.
- Company approach.
- Development philosophy.
- Team presentation.
- Contact CTA.

Keep company-specific facts editable.

Do not invent employee numbers, years of experience or company achievements.

## C. SERVICES PAGE

Route: /services

Create a professional service overview.

Services:

1. Web Development.
2. Mobile Application Development.
3. Custom Software Development.
4. UI/UX Design.
5. E-commerce Development.
6. API Development and Integration.
7. Database Engineering.
8. Cloud and Deployment.
9. Website Maintenance.

Each service card should include:
- Distinctive icon.
- Service title.
- Short description.
- Key benefits.
- Learn More link.

Make the service content data-driven.

## D. SERVICE DETAILS

Route: /services/:slug

Implement a reusable service detail template.

Sections:
- Service-specific hero.
- Overview.
- Problems solved.
- Features.
- Benefits.
- Technology stack.
- Development approach.
- Related projects.
- FAQs.
- Project inquiry CTA.

Each service must have its own content.

## E. PORTFOLIO

Route: /portfolio

Create an attractive portfolio gallery.

Features:
- Grid layout.
- Project categories.
- Filtering.
- Search.
- Featured projects.
- Project preview cards.
- Responsive design.

Each project card must show:
- Project image.
- Project title.
- Category.
- Short description.
- Technologies.
- View Project action.

## F. PROJECT DETAILS

Route: /portfolio/:slug

Include:
- Project hero.
- Project overview.
- Challenge.
- Solution.
- Technologies.
- Project screenshots.
- Development approach.
- Related projects.
- Contact CTA.

Only use genuine project information supplied by the company or clearly identified demonstration projects.

## G. TECHNOLOGIES

Route: /technologies

Organize technologies into:
- Frontend.
- Backend.
- Mobile.
- Databases.
- Cloud and DevOps.
- UI/UX tools.

Use recognizable icons where available.

Do not claim TELos specializes in tools that the company has not confirmed using.

## H. OUR PROCESS

Route: /process

Show the development workflow:

1. Discovery.
2. Requirements Analysis.
3. Planning.
4. UI/UX Design.
5. Development.
6. Testing.
7. Deployment.
8. Maintenance.

Use a visually interesting timeline or process diagram.

## I. TEAM

Route: /team

Create reusable team profile cards.

Include:
- Profile image.
- Name.
- Position.
- Short biography.
- Social links.

Use placeholders until real team information is provided.

## J. CAREERS

Route: /careers

Create:
- Company culture introduction.
- Available opportunities.
- Career information.
- Application CTA.

Do not display fabricated open positions.

## K. BLOG

Routes:
- /blog
- /blog/:slug

Include:
- Article cards.
- Categories.
- Featured article.
- Search.
- Pagination.
- Reading time.
- Article detail.
- Related articles.

Use structured content that can later be managed through the admin dashboard.

## L. CONTACT

Route: /contact

Include:
- Contact introduction.
- Email information placeholder.
- Phone information placeholder.
- Location placeholder.
- Social media links.
- Contact form.
- Map section only when an actual company location is provided.

## M. REQUEST A PROJECT

Route: /request-project

Create a professional multi-step project inquiry form.

Fields:

Step 1:
- Full name.
- Email.
- Phone.
- Company.

Step 2:
- Project category.
- Project description.
- Required features.

Step 3:
- Budget range.
- Preferred timeline.
- Preferred contact method.

Step 4:
- Review details.
- Submit inquiry.

Implement:
- Validation.
- Progress indicator.
- Previous and next buttons.
- Error feedback.
- Success and failure states.

Do not claim an inquiry has reached the company until a real backend connection exists.

## N. FAQ

Route: /faq

Implement searchable or categorized accordion questions.

## O. LEGAL PAGES

Implement:
- /privacy
- /terms

Use editable legal-content placeholders rather than presenting invented legal approval.

## P. CUSTOM 404 PAGE

Design a futuristic but simple 404 page with a working return-home action.

# 6. BILINGUAL IMPLEMENTATION — IMPORTANT

English and Amharic must be fully integrated into the entire frontend.

This is not optional.

Implement a proper internationalization architecture.

Recommended library: i18next with react-i18next.

### Languages

English:
en

Amharic:
am

### Requirements

1. Every visible navigation label must support both languages.
2. All page headings must be translated.
3. All paragraphs must have Amharic translations.
4. All buttons must be translated.
5. Form labels must be translated.
6. Validation messages must be translated.
7. Notifications must be translated.
8. Admin labels must be translated.
9. Error states must be translated.
10. Empty states must be translated.

Create separate translation files:

src/locales/en/
src/locales/am/

Use organized translation namespaces.

Suggested files:

- common.json
- navigation.json
- home.json
- about.json
- services.json
- portfolio.json
- contact.json
- forms.json
- admin.json

### Language switcher

Allow visitors to switch between:

EN | አማ

When the user changes language:
- Update the entire interface immediately.
- Preserve the current route when possible.
- Persist the preference in localStorage.
- Update document language metadata.
- Use appropriate Amharic fonts.
- Preserve the layout.

Important: Amharic is written left-to-right, so do not mistakenly switch the whole layout to RTL.

Use natural, understandable Amharic translations. Do not translate company names and technical product names unnecessarily.

Never show missing translation keys to visitors.

# 7. ADMIN DASHBOARD FRONTEND

Create the admin dashboard interface as a separate application experience.

Routes:

- /admin/login
- /admin/dashboard
- /admin/projects
- /admin/services
- /admin/inquiries
- /admin/blog
- /admin/team
- /admin/testimonials
- /admin/faqs
- /admin/media
- /admin/settings
- /admin/profile

### Admin layout

Implement:

- Responsive sidebar.
- Top navigation.
- TELos admin logo.
- Sidebar collapse.
- Breadcrumb navigation.
- Profile menu.
- Notifications area.
- Language selector.
- Main dashboard content.

### Dashboard overview

Display:
- Total projects.
- Total services.
- Total inquiries.
- Unread messages.
- Recent project activity.
- Recent inquiries.
- Project statistics chart.
- Inquiry trends.
- Content overview.

Use Recharts for appropriate charts.

### Project management UI

Create:
- Projects table.
- Search.
- Category filters.
- Status filters.
- Create project screen.
- Edit project screen.
- Project image upload interface.
- Delete confirmation dialog.

### Services management UI

Create:
- Services table.
- Add service.
- Edit service.
- Service descriptions.
- Service categories.
- Visibility controls.

### Inquiry management UI

Create:
- Inquiry list.
- Inquiry detail.
- Search.
- Status filters.
- Read/unread indicators.
- Archive interface.

### Blog management UI

Create:
- Article list.
- Article editor.
- Draft/published status.
- Category selection.
- Cover image interface.
- SEO field interface.

### Settings UI

Create:
- Company information.
- Website configuration.
- Contact details.
- Social media links.
- Default language.
- Theme settings.

Important: This phase implements the admin interface only. Do not pretend that frontend-only login forms provide real security. Real authentication, role permissions and server-side authorization will be implemented in later phases.

Clearly label demo data and preview functionality.

# 8. REUSABLE COMPONENT ARCHITECTURE

Build reusable components.

Examples:

Public components:
- Navbar.
- MobileMenu.
- Footer.
- HeroSection.
- SectionHeading.
- ServiceCard.
- ProjectCard.
- TechnologyCard.
- TeamCard.
- TestimonialCard.
- FAQAccordion.
- ContactForm.
- LanguageSwitcher.
- ThemeSwitcher.
- CTASection.

Admin components:
- AdminSidebar.
- AdminHeader.
- StatCard.
- DataTable.
- SearchBar.
- FilterDropdown.
- FormField.
- ConfirmDialog.
- NotificationToast.
- ChartCard.
- EmptyState.
- LoadingSkeleton.

Avoid duplicating the same component across multiple pages.

# 9. API-READY FRONTEND ARCHITECTURE

Prepare the frontend for future backend integration.

Create a structured API layer.

Example:

src/
  api/
    client.ts
    projects.ts
    services.ts
    inquiries.ts
    blog.ts
    team.ts
    settings.ts

Separate:
- API request logic.
- UI components.
- Data types.
- State management.
- Forms.
- Translation files.
- Utility functions.

Use typed interfaces for all data objects.

Create a replaceable mock data adapter for the development phase.

Support an environment variable:

VITE_API_BASE_URL

Allow the mock adapter to be switched off when the real API becomes available.

Do not place API endpoints throughout individual UI components.

Create consistent handling for:
- Loading.
- Success.
- Empty results.
- API failures.
- Network errors.

For preview-mode inquiry submissions, explicitly communicate that the backend is not connected and the inquiry has not been delivered.

# 10. RESPONSIVE DESIGN

The entire website must work correctly on:

- 320px mobile.
- 375px mobile.
- 425px mobile.
- 768px tablet.
- 1024px laptop.
- 1440px desktop.
- 1920px large screen.

Requirements:
- No horizontal overflow.
- No overlapping sections.
- No broken navigation.
- Responsive cards.
- Responsive forms.
- Responsive tables.
- Adapted mobile dashboard.
- Readable Amharic typography.
- Appropriate spacing on all devices.

Do not simply shrink desktop content.

# 11. ANIMATION AND INTERACTION

Use Motion for React where it adds genuine value.

Implement:
- Hero entrance animation.
- Subtle scroll reveals.
- Card hover effects.
- Smooth navigation transitions.
- Button interaction states.
- Mobile drawer animation.
- Accordion transitions.
- Loading feedback.
- Dashboard interaction feedback.

Respect prefers-reduced-motion.

Animations must never block navigation or reduce usability.

# 12. SEO AND PERFORMANCE

Implement:
- Page titles.
- Meta descriptions.
- Open Graph metadata.
- Canonical URL support.
- Semantic HTML.
- Descriptive image alternative text.
- Sitemap-ready route structure.
- Proper heading hierarchy.
- Image optimization.
- Lazy loading.
- Code splitting where useful.
- Efficient asset loading.

Use language-specific metadata for English and Amharic.

# 13. ACCESSIBILITY

Aim for WCAG 2.2 AA.

Include:
- Keyboard accessibility.
- Focus indicators.
- Accessible forms.
- Semantic landmarks.
- Proper labels.
- Appropriate contrast.
- Accessible dialogs.
- Screen reader-friendly feedback.
- Reduced motion support.

# 14. FILE STRUCTURE

Use a clean, maintainable structure.

Suggested architecture:

src/
  app/
    App.tsx
    router.tsx
    providers/
  assets/
  components/
    common/
    navigation/
    sections/
    forms/
    cards/
  layouts/
    PublicLayout.tsx
    AdminLayout.tsx
  pages/
    public/
    admin/
  api/
  data/
  hooks/
  locales/
    en/
    am/
  types/
  utils/
  styles/

public/
  images/
  icons/
  fonts/

Also create:
- README.md
- DESIGN.md
- .env.example

Adapt the architecture where necessary while preserving clear separation of concerns.

# 15. TESTING AND QUALITY CONTROL

Before finishing:

1. Run the development server.
2. Run TypeScript checks.
3. Run the production build.
4. Fix all compilation errors.
5. Test every route.
6. Test the language switcher.
7. Verify English translations.
8. Verify Amharic translations.
9. Test the navigation.
10. Test all forms.
11. Test mobile responsiveness.
12. Test admin navigation.
13. Check browser console errors.
14. Test loading and empty states.
15. Verify that no button is merely decorative when it claims to perform an action.

Use appropriate automated tests for important components and interactions.

# 16. STRICT IMPLEMENTATION RULES

- Build the real application.
- Do not return only sample JSX.
- Do not omit pages.
- Do not use lorem ipsum.
- Do not fabricate company details.
- Do not create fake testimonials.
- Do not invent completed business projects.
- Do not expose secrets or credentials.
- Do not hardcode admin passwords.
- Do not pretend frontend authentication is secure.
- Do not leave important buttons nonfunctional.
- Do not introduce unnecessary dependencies.
- Do not break existing project files without inspection.
- Keep code modular and maintainable.

If working inside an existing repository, inspect its structure first and preserve useful existing work.

# 17. FINAL DELIVERABLES

Deliver:

1. Complete React frontend.
2. All public pages.
3. All admin dashboard screens.
4. English language support.
5. Amharic language support.
6. Responsive mobile experience.
7. Reusable UI components.
8. API integration architecture.
9. Demo data adapter.
10. Form validation.
11. Animations.
12. SEO foundations.
13. Accessible interface.
14. README documentation.
15. Environment configuration example.
16. Successful production build.

### DEFINITION OF DONE

The project is complete only when the website runs, all required routes work, both languages work, the admin UI is navigable, responsive screens are verified, and the production build succeeds.

Do not start backend or database implementation in this phase.

**FINAL OBJECTIVE: Build the complete TELos Software Development frontend as a premium, futuristic, bilingual, fully responsive and API-ready web application.**