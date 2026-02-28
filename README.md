# DUX_A1_CL

# Craigslist UK Redesign Project

## Table of Contents

1. [Aims and Justification for Website Development](#1-aims-and-justification-for-website-development)
2. [Target Audience, User Personas, User Stories, Tasks and Acceptance Criteria](#2-target-audience-user-personas-user-stories-tasks-and-acceptance-criteria)
3. [Design — Wireframes, Accessibility & Usability](#3-design--wireframes-accessibility--usability)
4. [Reflection on the Design Process](#4-reflection-on-the-design-process)
5. [Contributors](#5-contributors)
6. [References](#6-references)

---

## 1. Aims and Justification for Website Development

### Overview

Craigslist is a community-driven classifieds platform used for buying, selling, trading, and requesting or offering services at a local level. It handles listings for everyday items such as furniture, electronics, and odd jobs. Despite its wide reach, the current Craigslist UK website (london.craigslist.org) presents significant usability and accessibility deficiencies that hinder engagement and alienate large segments of the population.

The aim of this project is to investigate those deficiencies, justify the need for a redesigned website, and produce an improved design that addresses identified problems while remaining faithful to Craigslist's community-classifieds purpose.

To acheive this we will break it down into 3 parts: evaluation of business needs, and identified issues; Target Audience, User Personas, Stories ; Design Wireframes, Evaluate improved accessibility and usability

### Business Needs and Identified Issues

#### 1.1 Outdated Visual Design and Steep Learning Curve

The current Craigslist interface relies entirely on text-based navigation with no visual hierarchy, icons, or graphical signposting. PhD researcher Nihal Nayak (Harvard University) characterised the site as "out-of-fashion" with a steep learning curve (Nayak, 2019). Because so few modern websites use this style, new users must actively learn the interface rather than applying familiar web conventions — a direct violation of the usability principle of **consistency with external standards** (Nielsen, 1994).

![Screenshot 1: Homepage layout](/Screenshots/1.png)
> **Description:** Screenshot of london.craigslist.org homepage showing text-only layout, lack of sectional dividers, and absence of visual hierarchy.

#### 1.2 Non-Intuitive Search Functionality

The search box is positioned in the top-left corner beneath the page title. While visible, it contains no graphical button or icon to trigger a search. Users must know to press Enter/Return — an interaction pattern largely abandoned by modern web services. Competitor platforms eBay UK and Gumtree both use clearly labelled, graphically styled search buttons that align with established user expectations.

![Screenshot 2: Search bar comparison](/Screenshots/2.png)
> **Description:** Side-by-side comparison of Craigslist's search bar (no button) vs. eBay UK (prominent search buttons).

#### 1.3 Lack of Mobile Responsiveness

Craigslist does not implement responsive design patterns such as dropdown menus, collapsible navigation, or touch-optimised tap targets. A substantial and growing proportion of web traffic originates from mobile devices, particularly among younger demographics who prefer a mobile-first experience. The absence of responsive design means content overflows on small screens, elements fail to scale correctly even when browser zoom is applied, and touch targets are too small for reliable interaction.

![Screenshot 3: Mobile viewport](/Screenshots/3.png)
> **Description:** Annotated screenshot of Craigslist rendered on a mobile viewport, illustrating layout overflow and unscaled text elements.

#### 1.4 Poor Accessibility

The site uses inconsistent semantic landmark regions, provides minimal colour contrast differentiation between content areas, and offers no ARIA attributes or skip-navigation links. This makes the site difficult or impossible to use for people relying on screen readers, keyboard navigation, or assistive technologies — a failure to meet WCAG 2.1 Level AA standards (W3C, 2018).

The sites semantic landmark region has no deliniation between the topmost row, that selects the region, category allows access to posting and account information, and the search functions this means every time a screenreader or braile device goes over the header section they read both navigation information and site controls (region, category, post creation, and account information), instead of what should happen where navigation search and main are in three identifiable sections for those tools.

#### 1.5 Competitive Analysis Summary

| Feature                    | Craigslist UK | eBay UK | Gumtree |
| -------------------------- | ------------- | ------- | ------- |
| Graphical search button    | ✗            | ✓      | ✓      |
| Category icons             | ✗            | ✓      | ✓      |
| Mobile responsive layout   | ✗            | ✓      | ✓      |
| Visual section separation  | ✗            | ✓      | ✓      |
| Accessible colour contrast | ✗            | ✓      | Partial |
| Dropdown / hamburger menus | ✗            | ✓      | ✓      |

![Screenshot 4: Ebay Dynamic Modals](/Screenshots/4.png)
> **Description:** Screenshot of eBay UK homepage showing icons, responsive grid layout, and popup navigation menus.

#### 1.6 Analysis of eBay Iconography

eBay hosts their own dedicated design documentation site called the **eBay Playbook**, which is dedicated to showcasing how they as a business function and deliver their level of service.

The site has a whole page dedicated to eBay's iconography and their own icon library. This library includes purpose-built icons covering the majority of their product categories — headphones for electronics, a car for automotive, footwear, a t-shirt for clothing, a lamp shade for home furnishings, a bed frame for furniture, boats for leisure, and many more.

Unlike craigslist these icons are synonymous to the user have alternative text for screenreaders and are used across ebay apps, sites, pages, and services, and they are considered by ebay to be a **foundation** of their design. These icons and more can be found at [playbook.ebay.com/foundations/iconography/our-icons](https://playbook.ebay.com/foundations/iconography/our-icons)

![eBay Playbook Iconography](5.png)
> **Description:** Screenshot of ebay UK Playbook page on iconography, demonstrating eBay's structured icon library used across their platform for intuitive category navigation.

### Justification for Development

The evidence above demonstrates a clear and urgent business need for website redevelopment. The purpose behind the redesign is to:

* Reduce the learning curve for first-time and infrequent visitors by aligning with contemporary web design conventions.
* Improve accessibility to meet WCAG 2.1 Level AA standards, enabling use by people with disabilities.
* Introduce mobile-responsive layouts to capture and retain traffic from mobile users.
* Implement intuitive graphical navigation and prominent search functionality to reduce abandonment and improve conversion rates.
* Maintain Craigslist's community-classifieds identity while making it competitive against modern alternatives.

---

## 2. Target Audience, User Personas, User Stories, Tasks and Acceptance Criteria

### Target Audience

Craigslist UK serves a broad community of users across the UK who wish to buy, sell, trade, or seek/offer local services. Key audience segments include:

* **First-time visitors** exploring online classifieds for the first time or new to Craigslist specifically.
* **Returning visitors** who use the site periodically for specific needs (e.g., selling items every few months).
* **Frequent visitors** who rely on the platform regularly for business or personal activity.
* Additional segments include buyers, sellers, landlords, job seekers, and community members posting local events.

---

### Persona 1 — Sarah (First-Time Visitor)

| Attribute               | Detail                                                                                                                                   |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **Age**                 | 40                                                                                                                                       |
| **Occupation**          | Carer                                                                                                                                    |
| **Location**            | Hertfordshire                                                                                                                            |
| **Devices**             | iPhone (primary), Windows laptop                                                                                                         |
| **Tech comfort**        | Comfortable with basic web navigation; prefers graphical interfaces                                                                      |
| **Accessibility needs** | Dyslexia (uses screen reader / text-to-speech); occasional hand tremors (requires large touch targets); relies on voice search on mobile |

**Background:** Sarah has never used Craigslist before and is exploring online classifieds to source affordable second-hand furniture for a client. She is tech-savvy but prefers clear, visually structured layouts over text-heavy pages. She finds Craigslist's current interface overwhelming and has encountered issues with elements not scaling correctly when browser zoom is applied.

#### User Stories — Sarah

| #  | User Story                                                                                                                                                                                    |
| -- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| S1 | As a **first-time visitor**, I want to **search for second-hand furniture using a visible search button**, so that **I can find relevant listings without needing to know keyboard shortcuts**. |
| S2 | As a **user with dyslexia**, I want the **website to use clear, simple language with generous spacing and readable fonts**, so that **I can browse listings without cognitive overload**.        |
| S3 | As a **mobile user with hand tremors**, I want **large, clearly labelled buttons and touch targets**, so that **I can navigate the site reliably on my smartphone**.                            |

#### Tasks — Sarah

* Navigate to the homepage and locate the search bar.
* Enter a search term ("second-hand sofa") and initiate the search using an on-screen button (without pressing Enter).
* Filter results by location (Hertfordshire) and price range.
* Open a listing and view item details including images, price, description, and seller contact information.
* Use a screen reader or text-to-speech to access listing content.

#### Acceptance Criteria — Sarah

**S1 – Search functionality:**

> *Given* Sarah is on the homepage, *when* she types "sofa" into the search bar and taps the graphical search button, *then* she should be presented with a list of relevant local listings within 3 seconds, without needing to press Enter.

**S2 – Readability:**

> *Given* Sarah opens a listing page, *when* she reads the listing description, *then* all text must use a sans-serif font of at least 16px, with a line-height of at least 1.5, and a minimum colour contrast ratio of 4.5:1 (WCAG 2.1 AA).

**S3 – Touch targets:**

> *Given* Sarah is using the site on her iPhone, *when* she attempts to tap any button, link, or interactive element, *then* all tap targets must be a minimum of 44×44 CSS pixels in size (WCAG 2.1 Success Criterion 2.5.5).

---

### Persona 2 — Dexter (Returning Visitor)

| Attribute               | Detail                                                                                                                               |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| **Age**                 | 35                                                                                                                                   |
| **Occupation**          | Graphic Designer                                                                                                                     |
| **Location**            | London                                                                                                                               |
| **Devices**             | MacBook Pro (primary), Android tablet                                                                                                |
| **Tech comfort**        | High; experienced with web tools; critical of poor UI/UX                                                                             |
| **Accessibility needs** | Arthritis in hands (keyboard navigation preferred; difficulty with precise mouse control); deuteranopia (red-green colour blindness) |

**Background:** Dexter returns to Craigslist every few months to sell old electronics or look for items in familiar categories. He has browser extensions for magnification and high-contrast mode but wishes sites were accessible by default. He values auto-save on forms and struggles with small input fields. His design background means he quickly dismisses cluttered or outdated interfaces.

#### User Stories — Dexter

| #  | User Story                                                                                                                                                                                                                           |
| -- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| D1 | As a **returning visitor**, I want the **website to remember my preferred listing categories**, so that **I can get back to relevant content quickly without re-configuring my search each time**.                                      |
| D2 | As a **keyboard user**, I want to **navigate the entire site without a mouse**, so that **I can use the platform comfortably despite limited hand dexterity**.                                                                          |
| D3 | As a **user with deuteranopia**, I want **status indicators and important information to be conveyed through shape or text labels rather than colour alone**, so that **I do not miss critical information due to colour-coded cues**. |

#### Tasks — Dexter

* Log in to an existing account using keyboard navigation only (Tab, Enter, arrow keys).
* Navigate to the "Electronics" category using the keyboard and locate a previously posted listing.
* Create a new listing: enter title, description, price, and upload an image, with auto-save enabled.
* Review form validation messages that do not rely solely on red/green colour indicators.
* Submit the listing and receive a confirmation that is accessible via keyboard focus.

#### Acceptance Criteria — Dexter

**D1 – Returning user preferences:**

> *Given* Dexter has previously browsed the "Electronics" category, *when* he returns to the homepage, *then* the site should surface a "Recently Viewed" or "Your Categories" section that links back to Electronics without requiring a new search.

**D2 – Keyboard navigation:**

> *Given* Dexter is using keyboard-only navigation, *when* he tabs through the page, *then* every interactive element (links, buttons, inputs, dropdowns) must be reachable via Tab and operable via Enter/Space, with a clearly visible focus indicator at all times (WCAG 2.1 SC 2.4.7).

**D3 – Colour-independent information:**

> *Given* Dexter is viewing a form with validation errors, *when* an input fails validation, *then* the error must be communicated through a text label and/or icon — not through a colour change alone — ensuring it is perceivable to users with colour vision deficiencies (WCAG 2.1 SC 1.4.1).

---

### Persona 3 — [Third Persona — To Be Added by Group]

> *This section is reserved for the group's third user persona (e.g., a frequent visitor such as a small business owner or community organiser who uses Craigslist regularly). Add background, accessibility considerations, device information, user stories, tasks, and acceptance criteria following the same format as Personas 1 and 2.*

---

## 3. Design — Wireframes, Accessibility & Usability

> *This section will be completed following the creation of wireframe designs. It should include:*
>
> * *Wireframe images for at least 3 pages or page areas (desktop or mobile)*
> * *Annotations explaining specific design decisions with reference to WCAG 2.1, usability heuristics (e.g., Nielsen's 10 Usability Heuristics), and WAI-ARIA where applicable*
> * *Notes on how each design choice addresses the needs of the user personas above*

### 3.1 Design Principles Applied

The wireframes will be guided by the following standards and principles:

* **WCAG 2.1 Level AA** — minimum contrast ratios, keyboard navigability, focus indicators, text alternatives for non-text content, and no reliance on colour alone.
* **WAI-ARIA landmarks** — use of `<nav>`, `<main>`, `<aside>`, `<header>`, and `<footer>` semantic regions to support screen reader navigation.
* **Nielsen's Usability Heuristics** — particularly visibility of system status, consistency with external standards, error prevention, and recognition over recall.
* **Mobile-first responsive design** — layouts designed for small screens first and scaled up, with touch targets of at least 44×44px.

### 3.2 Page / Area 1 — Homepage

> *[Insert wireframe image here]*

**Design Notes:**

* Prominent search bar with a clearly labelled graphical search button, addressing Sarah's need to initiate search without keyboard shortcuts.
* Category grid using icons alongside text labels, reducing reliance on pure text navigation.
* Sufficient spacing between interactive elements to support users with hand tremors or motor impairments.
* "Recently Viewed" section for returning users such as Dexter.

### 3.3 Page / Area 2 — Search Results Page

> *[Insert wireframe image here]*

**Design Notes:**

* Filter panel accessible via keyboard with clearly labelled checkboxes and dropdowns.
* Results presented as cards with thumbnail images, title, price, and location — reducing cognitive load for users with dyslexia.
* Sorting and filtering controls do not rely on colour alone for active/inactive states.

### 3.4 Page / Area 3 — Post a Listing Form

> *[Insert wireframe image here]*

**Design Notes:**

* Large input fields with visible labels (not placeholder-only labels, which disappear on focus).
* Auto-save functionality at defined intervals to prevent data loss for users with slower input speeds.
* Validation errors displayed as inline text messages with icons, not colour alone.
* Clear progress indication for multi-step form submission.

---

## 4. Reflection on the Design Process

> *This section will be completed after wireframes are finalised. It should include:*
>
> * *A reflection on key decisions made during the design process*
> * *Challenges faced (e.g., balancing simplicity with accessibility requirements, adapting Craigslist's minimalist identity to modern standards)*
> * *Any iterations or changes made to initial designs in response to user persona requirements*
> * *Lessons learned about accessible and inclusive design*

---

## 5. Contributors

| Name        | Email                   |
| ----------- | ----------------------- |
| Kai Young   | ky25aaa@herts.ac.uk     |
| Will Cooper |                         |
| Daniel      |                         |

> *Update this table with actual emails. All Team Members have to have made commits to the repository*

---

## 6. References

Nayak, N. (2019) *A UI/UX Critique of Craigslist*. Medium. Available at: https://medium.com/@nihalnayak/a-ui-ux-critique-of-craigslist-e3b235824479 (Accessed: 8 February 2026).

Nielsen, J. (1994) '10 Usability Heuristics for User Interface Design', *Nielsen Norman Group*. Available at: https://www.nngroup.com/articles/ten-usability-heuristics/ (Accessed: 8 February 2026).

W3C (2018) *Web Content Accessibility Guidelines (WCAG) 2.1*. World Wide Web Consortium. Available at: https://www.w3.org/TR/WCAG21/ (Accessed: 8 February 2026).

'Craigslist: London, UK Jobs, Apartments, for Sale, Services, Community, and Events' (no date) *Craigslist*. Available at: https://london.craigslist.org/ (Accessed: 8 February 2026).

'eBay UK | Electronics, Cars, Fashion, Collectibles & More' (2024) *eBay UK*. Available at: https://www.ebay.co.uk/ (Accessed: 8 February 2026).

'Gumtree | Free Classified Ads from the #1 Classifieds Site in the UK' (no date) *Gumtree*. Available at: https://www.gumtree.com/ (Accessed: 8 February 2026).

Assignment 1 for DUX Kai, Will and Daniel - Remake of Craigslist UI (Craigslist London) to follow modern design principles, be accessible and open