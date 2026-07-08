# Happy Trails Travel — Website Design

**Date:** 2026-06-29
**Status:** Approved

## Overview

A static marketing website for Happy Trails Travel, a travel agency run by an
agent with 20+ years of experience. The site introduces the business, presents
its services, and lets visitors send an inquiry via a Formspree-backed contact
form. Hosted on GitHub Pages.

### Business details

- **Name:** Happy Trails Travel
- **Tagline / description:** Travel agent with 20+ years of experience. Here to
  help you plan stress-free vacations, romantic getaways, destination weddings &
  much more!
- **Phone:** (515) 554-2798
- **Location:** Stuart, IA

## Stack & hosting

- Plain HTML5 + CSS3, no build step or framework.
- One shared stylesheet: `css/style.css`.
- Minimal vanilla JS for the mobile nav toggle only: `js/main.js`.
- Hosted on GitHub Pages from the root of the default branch.
- `.nojekyll` file at the repo root so all assets serve without Jekyll
  processing.

## Site structure (multi-page)

Each page shares the same header and footer markup (duplicated across files,
since there is no build/templating step).

1. **index.html — Home**
   - Hero: business name, tagline, primary CTA ("Plan Your Trip" → contact).
   - Short intro blurb.
   - Services preview: 4 cards linking to the Services page.
   - "Why choose us": 20+ years of experience, personal/stress-free planning.
   - Closing CTA to the contact page.

2. **about.html — About**
   - The agent's story and 20+ years of experience.
   - What working together looks like (personal, stress-free planning).

3. **services.html — Services**
   - Detailed section for each of the four offerings:
     - Stress-free Vacations
     - Romantic Getaways
     - Destination Weddings
     - Group & Cruise Travel
   - Each section: heading, short description, supporting image.

4. **contact.html — Contact**
   - Formspree inquiry form.
   - Phone and location details.

## Shared layout

- **Header:** sticky, responsive. Text logo "Happy Trails Travel" + nav links
  (Home / About / Services / Contact). Hamburger toggle on mobile that shows/
  hides the nav.
- **Footer:** phone `(515) 554-2798`, location `Stuart, IA`, copyright line.

## Visual style — Warm & adventurous

- Earthy green primary with terracotta accent; warm off-white background.
- Friendly, rounded cards; clear readable typography (a Google font with system
  fallback).
- Mobile-first responsive: single column on phones; multi-column grids on larger
  screens via CSS grid/flex and media queries.

## Contact form (Formspree)

- Method `POST` to a clearly-marked placeholder action:
  `https://formspree.io/f/YOUR_FORM_ID`, with an inline comment explaining what
  to replace after signing up at formspree.io.
- Fields:
  - Name (text, required)
  - Email (email, required)
  - Phone (tel, optional)
  - Trip type (select: Stress-free Vacation, Romantic Getaway, Destination
    Wedding, Group & Cruise Travel, Other)
  - Message (textarea, required)
- Submit button; standard Formspree success/redirect behavior (no custom JS
  handling required).

## Placeholders & assets

- `/images/` folder containing placeholder images (hero + per-service images)
  and a short `README` note listing which files to swap with real photos.
- Text-based logo for now (no logo file required).

## Out of scope (YAGNI)

- Booking engine, payments.
- CMS / blog / content management.
- Analytics.
- Custom domain (a `CNAME` file can be added later if desired).

## Success criteria

- All four pages render correctly and link to each other via the shared nav.
- Layout is usable and attractive on both mobile (~375px) and desktop.
- Contact form posts to Formspree once the placeholder endpoint is replaced.
- Site can be published on GitHub Pages with no build step.
