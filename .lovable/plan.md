# Hassan Wali — Dark Portfolio Website

A single-page dark portfolio for Hassan Wali, freelance full stack web developer based in Pakistan. All content in English except client reviews (Roman Urdu).

## Design

- **Background**: deep black `#0a0a0a` with charcoal `#111111` cards/surfaces
- **Text**: white / light gray
- **Accent**: electric blue `#3B82F6` for buttons, links, highlights, glows (matches the neon blue in Hassan's portrait)
- **Typography**: Space Grotesk for headings, DM Sans for body (loaded via Google Fonts `<link>` in root head)
- **Feel**: clean, minimal, professional; subtle scroll-reveal animations, smooth scrolling, soft blue glow accents; mobile-first responsive
- Photo used: uploaded portrait (`Tech_Workspace_Portrait_with_Neon_Accents.png`), served via Lovable Assets CDN pointer

## Sections (one scrolling page, `/`)

1. **Nav** — fixed top bar: name/logo left; links (Services, Projects, Pricing, Contact) right, collapsing to a mobile menu
2. **Hero** — Hassan's portrait photo beside the text block; heading "Hassan Wali", subtitle "Full Stack Web Developer & App Builder", line "I build fast, modern websites that grow your business." CTA "Let's Work Together" → WhatsApp (wa.me/923474054450)
3. **Services** — 6 cards: Landing Pages, Portfolio Websites, Business Websites, Ecommerce Websites, Full Stack Web Apps, Mobile Apps (each with an icon and one-line description)
4. **Projects** — 3 cards, each with name, type, live-link button, price tag:
   - Kamran Cloth House — E-commerce — kamranclothhouse.pk — Rs 30,000
   - Bannu Masala — Business website — bannumasala.com — Rs 30,000
   - Northlinks Broadband — Static business website — northlinksbroadband.vercel.app — Rs 8,000
   - Card images: styled placeholder covers (subtle gradient/pattern with project initial), no fake screenshots
5. **Reviews** — 3 testimonial cards written in Roman Urdu, attributed to real clients:
   - Kamran Khan (Kamran Cloth House)
   - Hassan Irfan (Bannu Masala)
   - Abdul Qadir Jan (Northlinks Broadband)
   - 5-star rating display, quote about delivery/quality/support
6. **Pricing** — simple table/cards:
   - Static/Landing Page: Rs 5,000–8,000
   - Business Website: Rs 15,000–25,000
   - Ecommerce/Full Stack: Rs 30,000+
   - Mobile App: Custom quote
7. **Contact** — heading "Ready to start your project?", WhatsApp button (wa.me/923474054450), plus location note "Based in Pakistan" and response-time reassurance
8. **Footer** — "© 2026 Hassan Wali — All rights reserved", nav links, WhatsApp link

## Technical notes

- Single route `src/routes/index.tsx` with full `head()` metadata (title, description, og tags, twitter card); no more "Lovable App" placeholder
- Sections are stacked blocks on the scrolling page; nav links smooth-scroll to each section (in-page anchors only, no hash-as-content)
- Photo uploaded via `lovable-assets` to CDN, referenced by its `.asset.json` pointer URL (also usable as og:image via its absolute asset URL)
- Animations: CSS/IntersectionObserver-based fade-up on scroll, hover lift on cards — no heavy libraries
- All colors as design tokens in `src/styles.css` (`@theme inline`), no hardcoded color utilities in components
