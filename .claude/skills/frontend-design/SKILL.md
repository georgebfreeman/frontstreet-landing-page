---
name: frontend-design
description: Design high-converting SaaS and digital product landing pages using HTML, JS, and Tailwind CSS. Use this skill when the user asks to build landing pages, marketing pages, pricing pages, waitlist pages, or any conversion-focused web page for a digital product or SaaS.
license: Complete terms in LICENSE.txt
---

This skill guides creation of high-converting SaaS and digital product landing pages. Output production-ready HTML, JavaScript, and Tailwind CSS that follows proven conversion optimization patterns while maintaining clean, professional design.

The user provides landing page requirements: a product, feature, or offer to promote. They may include copy, brand guidelines, audience details, or technical constraints.

## Before You Generate

If the user has NOT provided the following, ask before generating:

1. **Product/Service**: What is it? One-line description.
2. **Target audience**: Who is the ideal customer?
3. **Primary conversion goal**: What should the visitor do? (sign up, start trial, join waitlist, book demo, buy)
4. **Key value proposition**: What is the #1 benefit or outcome?
5. **Social proof**: Any stats, testimonials, logos, or trust signals to include?
6. **Pricing**: Any pricing tiers or model to display?

If the user provides a reference (URL, screenshot, or description), extract these details from the reference instead of asking.

## Tech Stack

- **HTML5** — semantic, accessible markup
- **Tailwind CSS** (CDN) — utility-first styling, mobile-first responsive design
- **Vanilla JS** or lightweight frameworks (**Alpine.js**, **HTMX**) — for interactivity when needed
- Zero build step. Output should work by opening the HTML file in a browser.
- Use Google Fonts CDN for typography. Prefer clean, professional fonts suited to SaaS (e.g., DM Sans, Plus Jakarta Sans, Satoshi, General Sans, Manrope, Cabinet Grotesk). Pair a distinctive heading font with a readable body font.

## Landing Page Structure

Follow this proven high-converting section order. Include all sections for a full page, or generate individual sections on request.

### 1. Navigation
- Sticky/fixed top nav with logo, 3-5 anchor links, and a CTA button
- Mobile: hamburger menu with slide-out or dropdown
- Keep it minimal — navigation should not compete with the hero CTA

### 2. Hero Section (Above the Fold)
- **Headline**: Clear, benefit-driven, under 12 words. Answer "What do you get?"
- **Sub-headline**: Elaborate on the headline with specifics. Quantify results when possible ("Save 10 hours/week" > "Save time")
- **Primary CTA**: Action-oriented, specific ("Start your free trial" > "Submit"). High-contrast button, visually the loudest element on the page
- **Visual**: Product screenshot, short demo video embed, or illustration
- **Social proof snippet**: "Trusted by 10,000+ teams" or a row of client logos directly below the hero
- Everything above the fold must communicate: what it is, why it matters, what to do next

### 3. Logo Bar / Social Proof Bar
- Row of 4-8 client/partner logos in grayscale
- Optional: "Trusted by X,000+ companies" text above
- Immediately below the hero to establish credibility

### 4. Problem / Solution
- Frame the pain point the audience faces (2-3 short pain statements)
- Position the product as the solution
- Use icons or illustrations to reinforce each point

### 5. Features / Benefits
- Lead with benefits, support with features
- 3-6 feature blocks with icon, heading, and 1-2 sentence description
- Alternate layout: feature + screenshot side-by-side, alternating left/right
- Show what the feature does for the user, not what it is

### 6. Social Proof / Testimonials
- 2-3 testimonials with: full name, photo, company, role, specific result
- Card layout or quote format
- Place near or before a CTA for maximum impact

### 7. Pricing (when applicable)
- 3 tiers maximum. Visually highlight the recommended tier with a badge/border/scale
- Monthly/annual toggle (Alpine.js or vanilla JS)
- Each tier: name, price, feature list, distinct CTA button
- Keep it scannable — no walls of text

### 8. FAQ
- Accordion pattern (Alpine.js `x-show` or vanilla JS)
- 5-8 questions addressing common objections and reducing friction
- Direct, concise answers

### 9. Final CTA Section
- Repeat the primary call to action with reinforcing copy
- Different angle or urgency: "Ready to [outcome]?" or "Join X,000+ teams already using [Product]"
- Same CTA button style as hero for visual consistency

### 10. Footer
- Logo, brief tagline
- Link columns: Product, Company, Resources, Legal
- Social media links
- Copyright

## Conversion Optimization (Always Apply)

These are baked in by default:

- **Single conversion goal per page** — one primary CTA repeated 2-3 times at strategic points (hero, mid-page, final section)
- **Sticky CTA** — on mobile, a fixed bottom bar with the primary CTA after scrolling past the hero
- **Trust signals near CTAs** — place testimonial quotes, star ratings, or "No credit card required" adjacent to CTA buttons
- **Minimal form fields** — 3 fields max for signup forms (name, email, password or just email)
- **Contrast CTA buttons** — the CTA button must be the highest-contrast element on the page. It should break the color pattern
- **Specificity over vagueness** — use precise numbers ("12,847 teams", "4.9/5 from 2,300 reviews") not vague claims
- **Message match** — headline and CTA copy should mirror the language of the traffic source

## Mobile-First Design

All output must be mobile-first:

- Design for 375px viewport first, then scale up with Tailwind responsive prefixes (`sm:`, `md:`, `lg:`)
- Touch targets minimum 48x48px
- Stack pricing tiers vertically on mobile
- Hamburger nav on mobile with accessible toggle
- Test that hero headline + CTA are fully visible without scrolling on mobile
- Thumb-zone aware: primary CTAs in easy reach on mobile

## Interactive Elements

Add contextually based on the page type:

- **Scroll-triggered reveals** — fade-in/slide-up on scroll using Intersection Observer (vanilla JS). Subtle, purposeful.
- **Animated counters** — for stats sections (e.g., "10,000+ users" counting up on scroll)
- **Pricing toggle** — monthly/annual with Alpine.js or vanilla JS
- **FAQ accordion** — expand/collapse with smooth transitions
- **Hover states** — subtle scale, shadow, or color shifts on cards and buttons
- **Respect `prefers-reduced-motion`** — wrap animations in media query checks

Limit to 2-4 animations per page. Every animation must serve conversion, not decoration.

## Design Principles

- **Clean and professional** over flashy. Proven SaaS patterns that convert.
- **Visual hierarchy** — headline and CTA are the most prominent elements. Use size, weight, contrast, and whitespace to guide the eye.
- **Generous whitespace** — sections breathe. Padding between sections: `py-16` minimum, `py-20` to `py-24` preferred.
- **Consistent spacing rhythm** — use Tailwind's spacing scale consistently.
- **Color strategy** — cohesive palette with one dominant brand color, neutral backgrounds, and a high-contrast accent for CTAs. Define as CSS custom properties for easy theming.
- **Typography hierarchy** — clear distinction between headings (`text-4xl`/`text-5xl` bold), subheadings (`text-xl`/`text-2xl`), and body (`text-base`/`text-lg`). Line height and letter-spacing tuned for readability.
- **Card and section patterns** — subtle borders, soft shadows (`shadow-sm`, `shadow-md`), rounded corners for a polished feel.

## Landing Page Archetypes

Adapt structure based on the page type:

| Type | Focus | Key Sections |
|---|---|---|
| **Product Launch / Waitlist** | Collect signups | Hero with email capture, teaser visuals, countdown (optional), early-access incentive |
| **Sales / Free Trial** | Drive signups | Full structure: hero, features, social proof, pricing, FAQ, final CTA |
| **Feature-Focused** | Deep-dive one capability | Hero focused on the feature, use-case demos, before/after, testimonials from that use case |
| **Pricing-Focused** | Convert comparison shoppers | Hero with value prop, pricing table front-and-center, FAQ heavy on pricing Qs, ROI framing |
| **Comparison Page** | Win against competitors | Side-by-side feature table, switching incentives, competitor-specific testimonials |

## Anti-Patterns (Never Do These)

- Multiple competing CTAs with different goals on the same page
- Walls of text without visual breaks
- Vague headlines ("Welcome to our platform", "The best solution")
- CTA buttons that blend into the background
- Decorative animations that don't serve conversion
- More than 4 pricing tiers
- Forms with more than 3 fields on initial capture
- Missing mobile optimization
- No social proof anywhere on the page
- Generic stock photo heroes instead of product visuals

## Output Format

- Single HTML file with Tailwind CDN, Google Fonts, and inline `<script>` for JS
- If using Alpine.js, include via CDN `<script>` tag
- All styles via Tailwind utility classes + minimal `<style>` block for CSS custom properties and animations only
- Semantic HTML: `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`
- Accessible: proper heading hierarchy, alt text, ARIA labels on interactive elements, keyboard-navigable
- Include `<meta name="viewport">` and `<meta name="description">`
