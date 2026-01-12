# MEForensics.net Website Template System
## Comprehensive Research-Based Template Outline

This document provides a complete guide to the MEForensics.net website structure, page templates, and content patterns. All templates follow SEO best practices, modern web design principles, and are optimized for forensic engineering service marketing.

---

## Site Architecture Overview

```
meforensics.net/
├── index.html                    # Interactive Sitemap Visualizer
├── home.html                     # Main Landing Page
├── about.html                    # Company Information & Team
├── contact.html                  # Contact Form & Intake
├── css/
│   └── styles.css               # Complete Design System
├── services/                     # Service Silo Pages
│   ├── forensic-engineering.html
│   ├── expert-witness.html
│   ├── condo-hoa-inspections.html
│   ├── disaster-response.html
│   └── drone-inspections.html
├── locations/                    # Location Hub Pages
│   ├── miami.html
│   ├── fort-lauderdale.html
│   ├── west-palm-beach.html
│   ├── orlando.html
│   ├── tampa.html
│   ├── naples.html
│   └── [20+ city pages]
└── resources/                    # Content/Article Clusters
    ├── legal-compliance/
    │   ├── sb4d-guide.html
    │   ├── chapter-558-claims.html
    │   └── daubert-standard.html
    ├── technology/
    │   ├── rov-vs-divers.html
    │   └── thermal-imaging.html
    └── disaster-recovery/
        ├── post-ian-lessons.html
        └── fema-elevation-certificates.html
```

---

## 1. HOME PAGE TEMPLATE

### Purpose
The home page serves as the primary conversion funnel entry point, establishing trust, demonstrating expertise, and guiding visitors to appropriate service pages.

### Structure

```
┌─────────────────────────────────────────────────────────────┐
│  HEADER (Fixed)                                              │
│  ┌─────────┐  ┌────────────────────────────┐  ┌───────────┐ │
│  │  Logo   │  │ Home | Services | Locations │  │ CTA Button│ │
│  └─────────┘  └────────────────────────────┘  └───────────┘ │
├─────────────────────────────────────────────────────────────┤
│  HERO SECTION (Full viewport height)                         │
│  ┌─────────────────────────────────────────────────────────┐│
│  │  Background Image (disaster/engineering scene)          ││
│  │  ┌─────────────────────────────────────────┐            ││
│  │  │ Badge: "Women Owned Business Enterprise"│            ││
│  │  │                                         │            ││
│  │  │ H1: "Disasters Happen—We're Here to Help"│           ││
│  │  │                                         │            ││
│  │  │ Subtitle: Value proposition             │            ││
│  │  │                                         │            ││
│  │  │ [Primary CTA] [Secondary CTA]           │            ││
│  │  │                                         │            ││
│  │  │ Trust Badges: FL PE | 24/7 | Multi-state│            ││
│  │  └─────────────────────────────────────────┘            ││
│  └─────────────────────────────────────────────────────────┘│
├─────────────────────────────────────────────────────────────┤
│  SERVICES OVERVIEW SECTION                                   │
│  ┌─────────────────────────────────────────────────────────┐│
│  │ Section Header: "Our Capabilities"                       ││
│  │ ┌─────────┐ ┌─────────┐ ┌─────────┐                     ││
│  │ │ Service │ │ Service │ │ Service │                     ││
│  │ │ Card 1  │ │ Card 2  │ │ Card 3  │                     ││
│  │ └─────────┘ └─────────┘ └─────────┘                     ││
│  │ ┌─────────┐ ┌─────────┐ ┌─────────┐                     ││
│  │ │ Service │ │ Service │ │ Service │                     ││
│  │ │ Card 4  │ │ Card 5  │ │ Card 6  │                     ││
│  │ └─────────┘ └─────────┘ └─────────┘                     ││
│  └─────────────────────────────────────────────────────────┘│
├─────────────────────────────────────────────────────────────┤
│  FLORIDA HORSESHOE SECTION                                   │
│  ┌─────────────────────────────────────────────────────────┐│
│  │ Section Header: "Service Coverage"                       ││
│  │ ┌───────────┐ ┌───────────┐ ┌───────────┐ ┌───────────┐ ││
│  │ │ Southeast │ │  Central  │ │ Tampa Bay │ │ Southwest │ ││
│  │ │ Miami     │ │ Orlando   │ │ Tampa     │ │ Naples    │ ││
│  │ │ Ft Lauder │ │ Kissimmee │ │ St Pete   │ │ Ft Myers  │ ││
│  │ │ WPB       │ │ Lakeland  │ │ Clearwater│ │ Sarasota  │ ││
│  │ └───────────┘ └───────────┘ └───────────┘ └───────────┘ ││
│  └─────────────────────────────────────────────────────────┘│
├─────────────────────────────────────────────────────────────┤
│  STATISTICS SECTION (Purple gradient)                        │
│  ┌─────────────────────────────────────────────────────────┐│
│  │  500+ Assessments | 250+ Testimonies | 20+ Cities | 24/7││
│  └─────────────────────────────────────────────────────────┘│
├─────────────────────────────────────────────────────────────┤
│  WHY CHOOSE US SECTION                                       │
│  ┌──────────────────────────────┐ ┌────────────────────────┐│
│  │ Content Column               │ │ Emergency Hotline Card ││
│  │ • Licensed PE multi-state    │ │                        ││
│  │ • Drone/ROV capabilities     │ │ (813) 555-1234         ││
│  │ • Rapid response             │ │                        ││
│  │ • Detailed reports           │ │                        ││
│  └──────────────────────────────┘ └────────────────────────┘│
├─────────────────────────────────────────────────────────────┤
│  CTA SECTION (Purple gradient)                               │
│  ┌─────────────────────────────────────────────────────────┐│
│  │ "Ready to Get Started?" + CTA Button                     ││
│  └─────────────────────────────────────────────────────────┘│
├─────────────────────────────────────────────────────────────┤
│  FOOTER                                                      │
│  ┌─────────────────────────────────────────────────────────┐│
│  │ Logo & Tagline | Services | Locations | Company | Legal ││
│  └─────────────────────────────────────────────────────────┘│
└─────────────────────────────────────────────────────────────┘
```

### Key Content Elements

**Hero Section:**
- Dramatic background image (disaster scene, engineering work)
- WBE certification badge prominently displayed
- Headline emphasizing client-focused approach
- Geographic scope (Miami to Naples)
- Dual CTA: Form submit + Phone call
- Trust badges: Licensing, availability, coverage

**Service Cards (6 total):**
1. Forensic Engineering
2. Expert Witness & Legal
3. Condo & HOA (SB 4-D)
4. Disaster Response
5. Drone & ROV Inspections
6. Insurance Claims Support

---

## 2. SERVICE PAGE TEMPLATE

### Purpose
Service pages establish topical authority, target service-specific keywords, and convert visitors seeking specific engineering services.

### Structure

```
┌─────────────────────────────────────────────────────────────┐
│  HEADER                                                      │
├─────────────────────────────────────────────────────────────┤
│  PAGE HERO (Shorter than home)                               │
│  ┌─────────────────────────────────────────────────────────┐│
│  │ Breadcrumbs: Home > Services > [Service Name]           ││
│  │ Badge: "Core Service"                                   ││
│  │ H1: [Service Name] Services                             ││
│  │ Subtitle: Brief value proposition                       ││
│  └─────────────────────────────────────────────────────────┘│
├─────────────────────────────────────────────────────────────┤
│  MAIN CONTENT (2-column layout)                              │
│  ┌────────────────────────────────┐ ┌──────────────────────┐│
│  │ PRIMARY CONTENT                │ │ SIDEBAR              ││
│  │                                │ │                      ││
│  │ H2: What is [Service]?         │ │ Quick Contact CTA    ││
│  │ [Explanatory paragraph]        │ │                      ││
│  │                                │ │ Emergency Box        ││
│  │ H3: Our Specialties            │ │                      ││
│  │ ┌──────┐ ┌──────┐              │ │ Related Services     ││
│  │ │Spec 1│ │Spec 2│              │ │ • Link 1             ││
│  │ └──────┘ └──────┘              │ │ • Link 2             ││
│  │ ┌──────┐ ┌──────┐              │ │ • Link 3             ││
│  │ │Spec 3│ │Spec 4│              │ │                      ││
│  │ └──────┘ └──────┘              │ │                      ││
│  │                                │ │                      ││
│  │ H3: Our Process                │ │                      ││
│  │ 1. Site Investigation          │ │                      ││
│  │ 2. Document Review             │ │                      ││
│  │ 3. Engineering Analysis        │ │                      ││
│  │ 4. Expert Report               │ │                      ││
│  └────────────────────────────────┘ └──────────────────────┘│
├─────────────────────────────────────────────────────────────┤
│  CTA SECTION                                                 │
├─────────────────────────────────────────────────────────────┤
│  FOOTER                                                      │
└─────────────────────────────────────────────────────────────┘
```

### Service Pages Required

| Page | Primary Keywords | Specialty Focus |
|------|-----------------|-----------------|
| forensic-engineering.html | forensic engineering Florida, structural failure analysis | Failure analysis, origin & cause, fire damage, vehicle impact |
| expert-witness.html | expert witness engineer Florida, construction defect witness | Litigation support, Daubert testimony, umpire services |
| condo-hoa-inspections.html | condo milestone inspection Florida, SB 4-D inspection | Milestone inspections, SIRS, turnover reports |
| disaster-response.html | hurricane damage assessment, wind vs flood determination | Emergency response, insurance claims, damage documentation |
| drone-inspections.html | drone roof inspection, underwater ROV inspection | Aerial thermal imaging, marine structure inspection |

---

## 3. LOCATION HUB PAGE TEMPLATE

### Purpose
Location pages target geographic searches, establish local presence, and connect visitors to locally-relevant services.

### Structure

```
┌─────────────────────────────────────────────────────────────┐
│  HEADER                                                      │
├─────────────────────────────────────────────────────────────┤
│  PAGE HERO                                                   │
│  ┌─────────────────────────────────────────────────────────┐│
│  │ Breadcrumbs: Home > Locations > [City]                  ││
│  │ Badge: "[Region] Hub"                                   ││
│  │ H1: [City] Forensic Engineering Services                ││
│  │ Subtitle: Services for [County] and surrounding areas   ││
│  └─────────────────────────────────────────────────────────┘│
├─────────────────────────────────────────────────────────────┤
│  MAIN CONTENT (2-column)                                     │
│  ┌────────────────────────────────┐ ┌──────────────────────┐│
│  │ H2: Forensic Engineering in    │ │ Contact Sidebar      ││
│  │     [City] & [Region]          │ │                      ││
│  │                                │ │ Service Area Map     ││
│  │ [Local context paragraphs]     │ │ • County coverage    ││
│  │ - Unique local challenges      │ │ • Cities served list ││
│  │ - Regulatory considerations    │ │                      ││
│  │ - Recent local events          │ │ Other Locations      ││
│  │                                │ │ • City Link 1        ││
│  │ H3: Services in [City]         │ │ • City Link 2        ││
│  │ ┌──────┐ ┌──────┐              │ │ • City Link 3        ││
│  │ │Svc 1 │ │Svc 2 │              │ │                      ││
│  │ └──────┘ └──────┘              │ │                      ││
│  │ ┌──────┐ ┌──────┐              │ │                      ││
│  │ │Svc 3 │ │Svc 4 │              │ │                      ││
│  │ └──────┘ └──────┘              │ │                      ││
│  │ ┌──────┐ ┌──────┐              │ │                      ││
│  │ │Svc 5 │ │NICHE │ ← High Value│ │                      ││
│  │ └──────┘ └──────┘              │ │                      ││
│  │                                │ │                      ││
│  │ Why Choose Local Expertise?    │ │                      ││
│  │ • Local code knowledge         │ │                      ││
│  │ • Environment expertise        │ │                      ││
│  │ • Fast response times          │ │                      ││
│  │ • Local relationships          │ │                      ││
│  └────────────────────────────────┘ └──────────────────────┘│
├─────────────────────────────────────────────────────────────┤
│  CTA SECTION                                                 │
├─────────────────────────────────────────────────────────────┤
│  FOOTER                                                      │
└─────────────────────────────────────────────────────────────┘
```

### Location Pages Matrix

| Region | Cities | Service Suite | High-Value Niche |
|--------|--------|---------------|------------------|
| Southeast | Miami, Fort Lauderdale, West Palm Beach, Boca Raton, Hialeah | Coastal Suite | High-Rise Recertification, Concrete Spalling, Historic Structures |
| Central | Orlando, Kissimmee, Winter Park, Lakeland, Altamonte Springs | Inland Suite | Theme Park Structures, Resort Engineering, Sinkhole Investigations |
| Tampa Bay | Tampa, St. Petersburg, Clearwater, New Port Richey, Brandon | Mixed | Commercial Roof, Foundation Repair, Flood Engineering |
| Southwest | Sarasota, Fort Myers, Naples, Cape Coral, Marco Island | Coastal Suite | Hurricane Ian Recovery, Luxury Waterfront, Canal Wall Failure |

### Coastal vs. Inland Service Suites

**Coastal Suite:**
- Structural Forensic Assessment
- Condo Milestone Inspection (SB 4-D)
- Expert Witness Services
- Flood vs. Wind Damage Claims
- Seawall & Marine Inspection

**Inland Suite:**
- Structural Forensic Assessment
- Expert Witness Services
- Roof Damage Assessment
- Sinkhole & Foundation Analysis
- Construction Defect Claims

---

## 4. RESOURCE/ARTICLE PAGE TEMPLATE

### Purpose
Resource articles establish thought leadership, target long-tail informational keywords, and nurture leads through educational content.

### Structure

```
┌─────────────────────────────────────────────────────────────┐
│  HEADER                                                      │
├─────────────────────────────────────────────────────────────┤
│  ARTICLE HERO (Compact)                                      │
│  ┌─────────────────────────────────────────────────────────┐│
│  │ Breadcrumbs: Home > Resources > [Category] > [Title]    ││
│  │ Badge: "[Category Name]"                                ││
│  │ H1: [Article Title]                                     ││
│  └─────────────────────────────────────────────────────────┘│
├─────────────────────────────────────────────────────────────┤
│  ARTICLE CONTENT (Centered, max-width 800px)                 │
│  ┌─────────────────────────────────────────────────────────┐│
│  │ Meta: Reading time | Date | Author                      ││
│  │ ─────────────────────────────────────                   ││
│  │                                                         ││
│  │ [Lead paragraph - bold/larger]                          ││
│  │                                                         ││
│  │ H2: Section Heading                                     ││
│  │ [Content paragraphs]                                    ││
│  │                                                         ││
│  │ ┌─ CALLOUT BOX ─────────────────────────────────────┐   ││
│  │ │ ⚠️ Important information highlighted               │   ││
│  │ └───────────────────────────────────────────────────┘   ││
│  │                                                         ││
│  │ H2: Another Section                                     ││
│  │ • Bullet list                                           ││
│  │ • With key points                                       ││
│  │                                                         ││
│  │ ┌─ TABLE ───────────────────────────────────────────┐   ││
│  │ │ Header 1 | Header 2 | Header 3                    │   ││
│  │ │ Data     | Data     | Data                        │   ││
│  │ └───────────────────────────────────────────────────┘   ││
│  │                                                         ││
│  │ H2: FAQ Section                                         ││
│  │ H3: Question 1                                          ││
│  │ [Answer]                                                ││
│  │                                                         ││
│  │ ┌─ INLINE CTA (Purple gradient) ────────────────────┐   ││
│  │ │ Need Help? Schedule Your Assessment               │   ││
│  │ │            [Request Quote Button]                 │   ││
│  │ └───────────────────────────────────────────────────┘   ││
│  └─────────────────────────────────────────────────────────┘│
├─────────────────────────────────────────────────────────────┤
│  RELATED ARTICLES SECTION                                    │
│  ┌─────────────────────────────────────────────────────────┐│
│  │ ┌─────────┐ ┌─────────┐ ┌─────────┐                     ││
│  │ │Related 1│ │Related 2│ │Related 3│                     ││
│  │ └─────────┘ └─────────┘ └─────────┘                     ││
│  └─────────────────────────────────────────────────────────┘│
├─────────────────────────────────────────────────────────────┤
│  FOOTER                                                      │
└─────────────────────────────────────────────────────────────┘
```

### Content Clusters

| Cluster | Articles | Target Keywords |
|---------|----------|-----------------|
| Legal & Compliance | SB 4-D Guide, Chapter 558 Claims, Daubert Standard | condo milestone inspection requirements, construction defect pre-suit, expert witness qualifications |
| Technology & Drones | ROV vs Divers, Thermal Imaging for Roofs | underwater drone inspection, thermal roof inspection |
| Disaster Recovery | Post-Ian Lessons, FEMA Elevation Certificates | hurricane damage engineering, flood elevation certificate |

---

## 5. DESIGN SYSTEM REFERENCE

### Color Palette

```css
/* Primary Brand */
--color-primary: #2D1B69;        /* Deep Purple */
--color-primary-light: #4A3D8A;  /* Medium Purple */
--color-accent: #7C3AED;         /* Vibrant Purple */
--color-highlight: #F59E0B;      /* Gold/Amber */

/* Status Colors */
--color-success: #10B981;        /* Green */
--color-danger: #EF4444;         /* Red */

/* Neutrals */
--color-text-primary: #1F2937;
--color-text-secondary: #6B7280;
--color-bg-primary: #FFFFFF;
--color-bg-secondary: #F9FAFB;
```

### Typography

```css
/* Display/Headlines */
--font-display: 'Playfair Display', serif;

/* Body Text */
--font-body: 'Inter', sans-serif;

/* Size Scale */
--font-size-xs: 0.75rem;   /* 12px */
--font-size-sm: 0.875rem;  /* 14px */
--font-size-base: 1rem;    /* 16px */
--font-size-lg: 1.125rem;  /* 18px */
--font-size-xl: 1.25rem;   /* 20px */
--font-size-2xl: 1.5rem;   /* 24px */
--font-size-3xl: 1.875rem; /* 30px */
--font-size-4xl: 2.25rem;  /* 36px */
```

### Component Library

| Component | Usage | States |
|-----------|-------|--------|
| `.btn--primary` | Main CTAs | Default, Hover, Active |
| `.btn--secondary` | Secondary actions | Default, Hover |
| `.btn--outline` | Tertiary actions | Default, Hover |
| `.service-card` | Service listings | Default, Hover |
| `.region-card` | Location listings | Default, Hover |
| `.card` | General content cards | Default, Hover |
| `.stat` | Statistics display | - |
| `.trust-badge` | Trust indicators | - |
| `.callout` | Highlighted info | Default, Warning |

---

## 6. SEO IMPLEMENTATION CHECKLIST

### Per-Page Requirements

- [ ] Unique, descriptive `<title>` tag (50-60 chars)
- [ ] Meta description (150-160 chars)
- [ ] H1 matching page topic (1 per page)
- [ ] Logical heading hierarchy (H1 → H2 → H3)
- [ ] Internal links to related pages
- [ ] Breadcrumb navigation
- [ ] Schema markup (LocalBusiness, Service, Article)
- [ ] Image alt text for all images
- [ ] Mobile-responsive layout
- [ ] Page load < 3 seconds

### URL Structure

```
meforensics.net/                          # Home
meforensics.net/services/[service-name].html
meforensics.net/locations/[city-name].html
meforensics.net/resources/[category]/[article-slug].html
meforensics.net/about.html
meforensics.net/contact.html
```

---

## Files Included in This Build

1. `index.html` - Interactive sitemap visualizer
2. `home.html` - Full home page with all sections
3. `css/styles.css` - Complete design system
4. `services/forensic-engineering.html` - Service page template
5. `locations/miami.html` - Location hub template
6. `resources/legal-compliance/sb4d-guide.html` - Article template
7. `contact.html` - Contact/intake form page
8. `about.html` - Company information page

All templates are production-ready and can be duplicated for additional pages.
