# 🌿 Bennet Pharmaceuticals — Official Website

<div align="center">

![Bennet Pharmaceuticals](https://bennetpharmaceuticals.com/bennet.png)

**A modern, fully redesigned single-page application for Bennet Pharmaceuticals Ltd.**  
*Healthy People, Healthy Nation — Est. 1996, Vadodara, Gujarat, India*

---

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Formspree](https://img.shields.io/badge/Formspree-ED5151?style=for-the-badge&logo=formspree&logoColor=white)](https://formspree.io)
[![Google Fonts](https://img.shields.io/badge/Google_Fonts-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://fonts.google.com)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Live Preview](#-live-preview)
- [Features](#-features)
- [Page Structure](#-page-structure)
- [Tech Stack](#-tech-stack)
- [Design System](#-design-system)
- [Sections Breakdown](#-sections-breakdown)
- [Sub-Pages (SPA Routing)](#-sub-pages-spa-routing)
- [Contact Form Setup](#-contact-form-setup)
- [File Structure](#-file-structure)
- [How to Run](#-how-to-run)
- [Customisation Guide](#-customisation-guide)
- [Credits](#-credits)

---

## 🌟 Overview

This is a **complete ground-up redesign** of the Bennet Pharmaceuticals website — transforming a static, generic template into a premium, animated, feature-rich **Single Page Application (SPA)** built with pure HTML, CSS, and JavaScript. No frameworks. No build tools. One file.

The redesign was built during an internship at Bennet Pharmaceuticals Ltd. with the goals of:

- Elevating brand perception to match a premium pharmaceutical company
- Fixing broken sections from the original site (zero-value stat counters, raw image dumps, missing interactivity)
- Adding a proper SPA navigation system with sub-pages for each capability
- Making the site fully responsive on all devices
- Integrating a working contact form that delivers enquiries directly to the company inbox

---

## 🖥️ Live Preview

> Open `bennet-pharmaceuticals.html` directly in any modern browser — no server required.

```bash
# Simply double-click the file, or open via terminal:
open bennet-pharmaceuticals.html         # macOS
start bennet-pharmaceuticals.html        # Windows
xdg-open bennet-pharmaceuticals.html     # Linux
```

---

## ✨ Features

### 🎨 Visual & UX
| Feature | Description |
|---|---|
| **Animated Hero** | Full-viewport dark navy hero with animated grid, glowing green orbs, floating stat pills, and staggered text fade-in |
| **Scroll Reveal** | Every section animates in on scroll with staggered delays using IntersectionObserver |
| **Flip Cards** | Core Values use a 3D CSS perspective flip animation — front shows icon + name, back reveals description |
| **Animated Counters** | Stats strip counts up from 0 using an eased cubic animation when scrolled into view |
| **Hover Zoom Gallery** | Life @ Bennet event photos zoom on hover and open in a full lightbox with keyboard navigation |
| **Testimonial Slider** | Auto-playing carousel with dot indicators, prev/next controls, and pause-on-hover |
| **SPA Navigation** | Full sub-page routing without any page reload — smooth scroll to top on every transition |
| **Sticky Nav** | Transparent at top, becomes solid navy with blur backdrop on scroll |
| **Dropdown Menu** | Click-toggled capabilities dropdown with outside-click-to-close behaviour |

### 📱 Responsive
- Fully responsive from 320px mobile to 4K desktop
- Fluid grid breakpoints at 1024px and 768px
- Mobile hamburger menu with full-screen overlay

### 📬 Contact
- Formspree integration — form submissions delivered to `jainvishesh2006@gmail.com`
- Graceful mailto fallback if network is unavailable
- Inline validation with colour-coded status messages

---

## 🗂️ Page Structure

The website is a **Single Page Application** — all content lives in one HTML file and pages are toggled via JavaScript. There are **5 total pages**:

```
📄 bennet-pharmaceuticals.html
│
├── 🏠 Home Page                  (main landing page)
│   ├── Hero
│   ├── Stats Strip
│   ├── About Us
│   ├── Core Values
│   ├── Capabilities Overview
│   ├── Leadership
│   ├── Life @ Bennet (Gallery)
│   ├── Testimonials
│   ├── Careers
│   └── Contact
│
├── 🔬 Innovation Sub-Page
├── 🏭 Manufacturing Sub-Page
├── 💊 Products Sub-Page          (9-tab medicine catalogue)
└── 🌐 Network Sub-Page
```

---

## 🛠️ Tech Stack

| Technology | Usage |
|---|---|
| **HTML5** | Semantic structure, SPA page containers |
| **CSS3** | Custom properties, Grid, Flexbox, 3D transforms, keyframe animations |
| **Vanilla JavaScript** | SPA routing, IntersectionObserver, testimonial slider, lightbox, counter animation, form submission |
| **Google Fonts** | `Cormorant Garamond` (headings) + `Nunito Sans` (body) |
| **Formspree** | Serverless contact form email delivery |
| **Unsplash** | Placeholder imagery for sub-pages |
| **Bennet CDN** | All real brand assets (logo, team photos, event gallery) served from `bennetpharmaceuticals.com` |

> **Zero dependencies** beyond Google Fonts and Formspree. No React, no jQuery, no build step.

---

## 🎨 Design System

### Colour Palette

```css
--green:        #AECA1D   /* Primary brand green — buttons, accents, highlights */
--green-dark:   #8CA418   /* Darker green — tags, labels, hover states */
--green-light:  #C5D84A   /* Lighter green — hero italic text, hero badges */
--green-pale:   #F2F7D8   /* Very light green — card backgrounds, chips */

--navy:         #1B2E4B   /* Primary dark — hero bg, footer, nav */
--navy-mid:     #243860   /* Mid navy — card gradients, dark overlays */
--navy-light:   #2E4472   /* Light navy — gradient endpoints */

--white:        #FFFFFF   /* Pure white */
--cream:        #F8FAF0   /* Off-white sections */
--text-muted:   #6B7A8D   /* Body copy, descriptions */
```

### Typography

| Role | Font | Weight | Size |
|---|---|---|---|
| Display / Hero | Cormorant Garamond | 300 (Light) | 4.8rem |
| Section Headings | Cormorant Garamond | 400 | 3rem |
| Sub-page Headings | Cormorant Garamond | 300 | 3.5rem |
| Card Headings | Cormorant Garamond | 600 | 1.2–1.5rem |
| Body Text | Nunito Sans | 400 | 1rem |
| Labels / Tags | Nunito Sans | 700 | 0.72–0.75rem |
| Navigation | Nunito Sans | 600 | 0.85rem |

### Spacing Scale
All padding uses `4rem` horizontal on desktop, stepping down to `2rem` on tablet and mobile.

---

## 📄 Sections Breakdown

### 1. 🦸 Hero
Full-viewport section with:
- Animated CSS grid background pattern
- Two radial gradient "orbs" for depth
- Left: badge + heading + subtitle + CTA buttons (staggered fade-up animation)
- Right: brand image card with two floating stat pills
- Scroll-down indicator with animated line

### 2. 📊 Stats Strip
Green background strip with 5 animated counters:
- 500+ SKUs & Products
- 500+ Sales Personnel
- 1,000+ Distributor Network
- 1,00,000+ Retail Outlets
- 15+ States Covered

> Counters use a cubic ease-out formula and trigger once when scrolled into view.

### 3. 🏢 About Us
Two-column layout:
- Left: real company photo with "30 Years of Trust" floating badge
- Right: brand story, certifications chips (WHO-GMP, ISO, Export Ready, etc.)

### 4. 💎 Core Values — Flip Cards
Five interactive flip cards with scroll-triggered entrance animation (staggered by 120ms each):
- **Front**: Icon + Value name
- **Back** (on hover): Full description on green background
- Values: Integrity · Collaboration · Empowerment · Excellence · Innovation

### 5. 🗂️ Capabilities Overview
Four clickable cards that route to dedicated sub-pages:
- 🔬 Innovation → Patent research, NIPER-A collaboration
- 🏭 Manufacturing → WHO-GMP, Contract Manufacturing, Export
- 💊 Products → 500+ SKUs across 9 specialist tabs
- 🌐 Network → 15+ states, 1,00,000+ retail outlets

### 6. 👥 Leadership
Four director cards with initials avatars, roles, and descriptions:
- Mr. J. K. Jain — Founder & Promoter Director
- Mr. Siddharth Jain — Technical Director
- Mrs. Vrushti Jain — Creative Director
- Mrs. Vaishali Jain — Director, Finance & Marketing

### 7. 🎉 Life @ Bennet
- Four culture pillars with real photos (hover zoom effect)
- 15-photo event gallery in masonry column layout
- Hover zoom on each photo
- Click any photo → full lightbox (arrow keys + Escape supported)

### 8. 💬 Testimonials — Auto-playing Slider
Four testimonial slides:
- Rajesh Kaushik — ZSM, Rajasthan
- Amit Kumar — RSM, UP & Bihar
- Priya Sharma — MR, Maharashtra
- Dr. Mahesh Verma — GP, Gujarat

> Auto-advances every 5 seconds. Pauses on hover. Dot indicators + prev/next buttons.

### 9. 💼 Careers
Two-column layout:
- Left: 4 perk cards (Career Growth, Learning, Health Benefits, Impactful Work)
- Right: Apply info box with both HR email addresses + team photo

**HR Contact:**
- `jobs.bennet@gmail.com`
- `hr@bennetpharmaceuticals.com`

### 10. 📬 Contact
- Left: company address, phone, 3 email addresses
- Right: contact form (Name, Email, Phone, Enquiry Type, Message) wired to Formspree

---

## 🔗 Sub-Pages (SPA Routing)

### How It Works
Each sub-page is a hidden `<div class="page">` that becomes visible when its route is activated. No page reload. Scroll resets to top on every navigation.

```javascript
function showPage(name) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.getElementById('page-' + name).classList.add('active');
  window.scrollTo({ top: 0, behavior: 'smooth' });
}
```

### 🔬 Innovation Page
- SALT Technology Patent — Lactoferrin 100mg enhanced bioavailability
- Silver Nanoparticles Patent — wound healing breakthrough
- NIPER-A (National Institute of Pharmaceutical Education and Research, Ahmedabad) research collaboration

### 🏭 Manufacturing Page
- WHO-GMP certified Baddi facility
- Three pillars: Global Standards · Uncompromising Quality · Advanced Technologies
- Contract Manufacturing card with contact details
- Global Exports card (Asia, Africa, Latin America)

### 💊 Products Page
9-tab medicine catalogue covering:

| Tab | Sample Products |
|---|---|
| General Physician | Azidep-500, Levonet-500, Actoferrin, Livalo, Dinsa Activ |
| Gynecologist | Terzo, Terzo-DS, Dinsa Activ-G |
| Paediatrician | Hynorax Drops, Nicet Suspension, Broxine Syrup |
| Surgeon | Granirex Inj, Anset Inj, Clid Inj, Ketopher Inj |
| Orthopedic | Ketopher-P, Dupox Gel, Dinsa Activ-OA |
| Dentist | Azidep-500, Clid-300, Dupox Gel |
| Ophthalmologist | Levonet Eye Drops, Azidep Eye Drops |
| Oncology | Granirex Inj, Anset Inj, Actoferrin |
| Dermatologist | Proticort-B, Dupox Gel, Actoferrin (Silver NP) |

### 🌐 Network Page
- 5 animated stat cards
- Community reach narrative
- Become a Distribution Partner CTA

---

## 📬 Contact Form Setup

The form uses **Formspree** — a serverless form backend that requires no server and works from local `file://` URLs.

### Current Setup
Form submissions are automatically sent to `jainvishesh2006@gmail.com` via the Formspree endpoint:
```
https://formspree.io/f/xdkogwrz
```

### If You Want to Change the Recipient Email
1. Go to [formspree.io](https://formspree.io) and create a free account
2. Create a new form and point it to your preferred email
3. Replace the endpoint URL in the JavaScript:
```javascript
const res = await fetch('https://formspree.io/f/YOUR_FORM_ID', { ... });
```

### Fields Captured
| Field | Type | Required |
|---|---|---|
| First Name | Text | ✅ |
| Last Name | Text | ❌ |
| Email Address | Email | ✅ |
| Phone Number | Tel | ❌ |
| Enquiry Type | Select | ❌ |
| Message | Textarea | ✅ |

### Fallback Behaviour
If Formspree fails (e.g. offline), the form automatically opens the user's mail app with all fields pre-filled as a `mailto:` link.

---

## 📁 File Structure

```
📦 bennet-pharmaceuticals/
│
└── 📄 bennet-pharmaceuticals.html     ← Everything lives here
    │
    ├── <head>
    │   ├── Google Fonts (Cormorant Garamond + Nunito Sans)
    │   └── <style> — ~700 lines of CSS
    │
    └── <body>
        ├── #lightbox                  ← Full-screen image viewer
        ├── <nav>                      ← Fixed navigation with dropdown
        │
        ├── #page-home                 ← Main landing page
        │   ├── #hero
        │   ├── #stats
        │   ├── #about
        │   ├── #values
        │   ├── #capabilities
        │   ├── #leadership
        │   ├── #life
        │   ├── #testimonials
        │   ├── #careers
        │   ├── #contact
        │   └── <footer>
        │
        ├── #page-innovation           ← Innovation sub-page
        ├── #page-manufacturing        ← Manufacturing sub-page
        ├── #page-products             ← Products sub-page (9 tabs)
        ├── #page-network              ← Network sub-page
        │
        └── <script>                   ← ~200 lines of vanilla JS
            ├── Gallery image injection
            ├── Lightbox open/close/navigate
            ├── Testimonial slider + autoplay
            ├── SPA routing (showPage / showSubpage)
            ├── Nav scroll behaviour
            ├── Mobile menu toggle
            ├── Product tab switching
            ├── Dropdown toggle
            ├── IntersectionObserver (reveal + values + counters)
            └── Contact form submit (Formspree + mailto fallback)
```

---

## 🚀 How to Run

### Option 1 — Open Locally (Instant)
Just double-click `bennet-pharmaceuticals.html`. Opens in your default browser immediately.

> ⚠️ If images don't load, it means your browser is blocking external URLs from `file://` context. Use Option 2.

### Option 2 — Local Server (Recommended for Development)

**Using Python (built-in):**
```bash
cd path/to/your/folder
python -m http.server 8080
# Open http://localhost:8080/bennet-pharmaceuticals.html
```

**Using Node.js:**
```bash
npx serve .
# Open the URL shown in terminal
```

**Using VS Code:**
Install the [Live Server extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer), right-click the file → *Open with Live Server*.

### Option 3 — Deploy (Free, Permanent URL)

**Netlify Drop** (easiest — no account needed for first deploy):
1. Go to [netlify.com/drop](https://app.netlify.com/drop)
2. Drag and drop the HTML file
3. Get a live URL instantly

**GitHub Pages:**
1. Push the file to a GitHub repo
2. Go to Settings → Pages → Deploy from branch
3. Your site is live at `https://username.github.io/repo-name`

---

## 🎛️ Customisation Guide

### Changing Colours
All colours are CSS custom properties at the top of the `<style>` tag:
```css
:root {
  --green:      #AECA1D;  /* Change this to update all green accents */
  --navy:       #1B2E4B;  /* Change this to update all dark backgrounds */
}
```

### Adding a New Testimonial
Find the `#testiSlides` div and add a new `.tcard` block:
```html
<div class="tcard">
  <div class="tcard-qmark">"</div>
  <div class="tcontent">
    <div class="tavatar-ph" style="display:flex">AB</div>
    <div>
      <div class="tstar">★★★★★</div>
      <p class="ttext">"Your testimonial quote here."</p>
      <div class="tauthor">Full Name</div>
      <div class="trole">Role — Region</div>
    </div>
  </div>
</div>
```

### Adding a New Medicine to the Products Page
Find the correct `#tab-XXX` div and add a `.med-card`:
```html
<div class="med-card">
  <div class="med-name">Brand Name</div>
  <div class="med-composition">Generic Name Xmg Tablets</div>
  <div class="med-type">Category</div>
</div>
```

### Adding a New Gallery Photo
Add to the `galleryImgs` array in the JavaScript:
```javascript
const galleryImgs = [
  'https://bennetpharmaceuticals.com/event1.jpg',
  // ... add your new image URL here
];
```

### Changing the Contact Form Email
Replace the Formspree endpoint with your own:
```javascript
const res = await fetch('https://formspree.io/f/YOUR_ID', { ... });
```

---

## 🌐 External Assets Used

| Asset | Source | Usage |
|---|---|---|
| Company Logo | `bennetpharmaceuticals.com/bennet.png` | Nav + Footer |
| About Photo | `bennetpharmaceuticals.com/about.png` | Hero, About, Manufacturing |
| Culture Photos | `bennetpharmaceuticals.com/learning1.jpg` etc. | Life @ Bennet pillars |
| Event Gallery | `bennetpharmaceuticals.com/event1–15.jpg` | Events gallery |
| Team Photo | `bennetpharmaceuticals.com/GroupPhoto1.jpg` | Careers section |
| Innovation Image | `images.unsplash.com` | Innovation sub-page hero |
| Fonts | Google Fonts CDN | Cormorant Garamond + Nunito Sans |
| Form Backend | Formspree | Contact form email delivery |

---

## 📞 Company Contact Information

| Type | Details |
|---|---|
| **Registered Office** | 608 B Wing, 6th Floor, Manubhai Tower, Sayajigunj, Vadodara, Gujarat 390005 |
| **Phone** | 0265 236 1750 |
| **General** | info@bennetpharmaceuticals.com |
| **Export** | Export@bennetpharmaceuticals.com |
| **Contract Mfg** | cm@bennetpharmaceuticals.com |
| **HR / Careers** | hr@bennetpharmaceuticals.com |
| **Jobs** | jobs.bennet@gmail.com |
| **LinkedIn** | [Bennet Pharmaceutical Ltd.](https://in.linkedin.com/company/bennet-pharmaceutical-ltd) |

---

## 🏆 Credits

| Role | Details |
|---|---|
| **Design & Development** | Vishesh Jain — Intern, Bennet Pharmaceuticals Ltd. |
| **Company** | Bennet Pharmaceuticals Ltd., Vadodara, Gujarat |
| **Built With** | Pure HTML5, CSS3, Vanilla JavaScript |
| **Fonts** | Google Fonts — Cormorant Garamond & Nunito Sans |
| **Form Backend** | Formspree (formspree.io) |
| **Icons** | Unicode Emoji |

---

<div align="center">

Made with 💚 during an internship at **Bennet Pharmaceuticals Ltd.**

*Healthy People, Healthy Nation*

© 2025 Bennet Pharmaceuticals Ltd. All Rights Reserved.

</div>
