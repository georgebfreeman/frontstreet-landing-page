# FrontStreet — Investor Summary
### Domain: frontstreetapp.com

FrontStreet is a mobile-first marketplace and community platform purpose-built for Black artists in Boston — giving them a single app to showcase their portfolio, sell original work directly to collectors, and promote events, replacing the broken stack of Instagram, Eventbrite, Etsy, and WhatsApp they're currently duct-taping together.

---

## 1. The Problem

Black artists in Boston are systematically underserved by every platform they're forced to use. The infrastructure problem is real and quantified: Black artists represent just **1.2% of works in major US museum collections** despite comprising 13% of the population (Williams College / PLOS ONE). A deeper Artnet/Burns Halperin analysis of 31 museums over 12 years found Black Americans accounted for only 2.2% of acquisitions. Predominantly white institutions — just 2% of cultural organizations — capture nearly **60% of all arts funding** nationwide. The institutional pipeline is broken, and it has been for decades.

Today's digital alternatives fail these artists just as badly, for different reasons. Instagram suppresses Black creators algorithmically, offers no sales infrastructure, no event tools, and no cultural context — it was built for everyone, which in practice means it wasn't built for them. Artsy requires gallery representation and charges galleries $425+/month just to list, keeping individual emerging artists entirely off the platform. Eventbrite charges 10–14% in effective fees per ticket, a punishing rate for community-scale events with tight margins. No single platform combines artist profiles, event listings, and art sales — so every Boston Black artist manages at minimum four separate tools with no integration between them.

The market signal is there, and it's concrete. BAMS Fest — Boston's Art & Music Soul Festival — grew from 2,200 attendees in 2018 to over 10,600 by 2022 with **13,000–15,000 artist applications** and 60+ minority-owned businesses supported. It did all of this with no dedicated digital platform. Boston's Black community is approximately **180,000 residents (28.2% of the city)**, culturally anchored in Roxbury's Nubian Square, served by institutions like the National Center of Afro-American Artists and a pipeline of new investment including the planned 35,000 sq ft Greater Roxbury Arts & Cultural Center. The demand is proven. The infrastructure doesn't exist yet.

The consequence of inaction is more of the same: Black artists in Boston remain invisible to the collectors who want to find them, scatter their audience across platforms that don't serve them, and earn a fraction of what they would if they had the same digital infrastructure that every other category of creator takes for granted.

---

## 2. The Solution

FrontStreet is a single mobile app — iOS, Android, and web — that gives Black artists in Boston an integrated home for their work, their events, and their collector relationships. It's the platform that BAMS Fest, the National Center of Afro-American Artists, and the hundreds of artists applying to events in Boston don't have yet.

- **Artist Profiles & Portfolio** — Customizable profiles where artists display their work, bio, mediums, and available pieces with direct purchase capability, replacing the Instagram profile that was never designed for art sales.
- **Art Sales with Stripe Connect** — Collectors browse and buy artwork directly from artists at a 5–8% platform commission — the most artist-friendly rate in the market — with Stripe handling KYC, payment splitting, 1099-K generation, and fraud protection automatically.
- **Event Listings & RSVP** *(v2)* — A community calendar of exhibitions, pop-ups, workshops, and mixers with ticketing at 3% + $0.50, replacing Eventbrite's 10–14% fees for community-scale events.
- **Discovery Feed** *(v2)* — An algorithm built for fairness, not engagement metrics — ensuring all artists get equitable exposure rather than the suppression that characterises Instagram's feed for Black creators.
- **Featured & Boosted Placements** — Revenue stream for artists who want premium visibility, priced at $5–25 per boost — accessible to emerging artists, not just established ones.
- **Community by Design** — Hyper-local, Boston-first curation means every user in the app shares context. A collector in Jamaica Plain and an artist in Roxbury are in the same community, not lost in a global feed of millions.

FrontStreet charges artists 5–8% commission on sales. Saatchi Art takes 40%. Artfinder takes 40–45%. This isn't a marginal price difference — it's a structural commitment to the community the platform serves.

---

## 3. Target Customer

**Primary ICP:** Black visual artists based in Boston, MA who are actively creating and selling original work but lack a professional, culturally specific digital home for their practice.

**Characteristics:**
- Active on Instagram but frustrated by algorithmic suppression and zero sales/event infrastructure
- Selling through DMs, at pop-ups, or via personal website — no integrated collector management
- Hosts or participates in community events (exhibitions, open studios, pop-ups) currently listed on Eventbrite or promoted only via Instagram Stories
- Earns from art but not at scale — in the emerging-to-mid-career range ($500–$5,000 per piece)
- Connected to the Boston Black arts ecosystem: aware of BAMS Fest, Roxbury arts orgs, local galleries
- Values cultural authenticity over generic tech tools — would choose a platform built *for them* over a cheaper/more familiar general-purpose alternative
- Secondary audience: art collectors and enthusiasts of all backgrounds actively seeking to discover and purchase from Black Boston artists

---

## 4. Value Proposition

> "I used to split everything across Instagram, Eventbrite, and my own website — and none of them actually talked to each other. With FrontStreet, my portfolio, my upcoming show, and my available work are all in one place. I sold two pieces in the first month just from people discovering me through the app. And the commission was so much lower than everywhere else that the math actually worked in my favor."

---

## 5. Key Features (MVP)

1. **Artist Profile & Portfolio** — A fully customizable artist page with cover image, bio, medium tags, follower count, and a 2-column portfolio grid — built on Quasar + Supabase with image storage via Supabase Storage + Cloudflare CDN for fast, cost-efficient delivery.
2. **Artwork Listings with Availability** — Artists upload up to 5 photos per piece with title, medium, dimensions, year, and price; a single toggle marks work as Available or Not for Sale, with the Available badge surfaced prominently to collectors.
3. **Direct Purchase via Stripe Connect** — Collectors purchase artwork through Stripe's hosted checkout (external browser, exempt from Apple's 30% commission); Stripe Express accounts handle artist KYC, automatic commission splitting, and 1099-K generation with no custom payment infrastructure required.
4. **Collector Browse & Discovery** — A curated home feed (Spotlighted Works carousel, Featured Artists row, section-headed scroll) built for purposeful discovery rather than infinite engagement optimisation — 17 MVP screens total.
5. **Search & Filtering** — Artists and artworks searchable by name, medium, and availability — built on Supabase PostgREST with a GIN-indexed `search_vector` column for fast full-text queries from day one.
6. **Artist Inquiry (Inquire CTA)** — A pre-filled contact form from any artwork detail page, letting collectors reach out directly about commissioning or purchasing work that isn't publicly available — the "Inquire" path alongside "Buy Now."

---

## 6. Business Model

**Pricing:**

- **Free — Artist Basic:** $0/mo — Full profile, portfolio upload (unlimited pieces), browse and discovery. No sales capability until Stripe Connect is onboarded.
- **Artist Pro:** $7/mo — Premium profile features, priority placement in search, analytics dashboard (v2), access to boosted listing slots.
- **Boosted Listings:** $10–25 per event or artwork — Paid featured placement in the discovery feed and Featured Artists row. One-time, not subscription.

**GTM Motion:**
- Founder-led supply-side acquisition: George personally onboards the first 10–15 Boston Black artists from his existing network, building initial portfolio density before opening to the public
- Launch event series: 2–3 physical pop-ups in Boston (Roxbury, South End, Cambridge) with in-app QR codes and on-site profile creation — each event creates content and drives both artist and collector signups simultaneously
- Waitlist conversion: existing landing page waitlist is the initial cohort; Tally intake form converts artist interest to active profiles
- Partnership with local arts institutions: BAMS Fest, NCAAA, GRACC, Castle of our Skins — community alignment that gives FrontStreet credibility no paid marketing could buy

**Revenue Goal:** Reach $2,500 MRR within 12 months of launch — driven by ~100 Pro subscribers ($700) + event/listing boosts ($750) + art sale commissions beginning month 6–12 ($1,000+) + local business partnerships ($500).

---

## 7. Competitive Landscape

| Competitor | Positioning | Price | Our Advantage |
|---|---|---|---|
| **Artsy** | World's largest online art marketplace; gallery-gated, elite global audience | $425+/mo for galleries; 10–15% commission | Artists list *directly* — no gallery required. 5–8% commission vs. 10–15%. Boston-specific curation vs. undifferentiated global feed. |
| **Instagram** | General-purpose social; de facto artist portfolio tool | Free (ad-supported) | No algorithmic suppression. Native sales and event infrastructure. Platform built *for* Black artists, not tolerating them as a segment. |
| **Eventbrite** | General event ticketing platform | ~10–14% effective fee per ticket | 3% + $0.50 ticketing fee (vs. $3.53 on a $20 ticket). Artist profiles integrated with event listings. Community-specific curation. |
| **Saatchi Art** | Global online gallery; open to individual artists | Free to list; **40% commission** on original sales | 5–8% commission vs. 40%. Hyper-local Boston focus vs. undifferentiated global inventory of 100,000+ works. Community identity vs. generic marketplace. |
| **Black Art In America (BAIA)** | Black art media brand with Shopify e-commerce | Not publicly disclosed; Shopify-based | Mobile-first app vs. desktop media site. Boston local focus vs. national/Atlanta HQ. Events + profiles + sales in one product vs. media + store only. No Boston presence. |

*Artsy pricing: $425/mo per competitor analysis and third-party sources (verified March 2026). Saatchi Art commission: 40% per official help center (saatchiart.com, verified March 2026). Eventbrite effective fee rate: 10–14% per published fee structure (verified March 2026).*

---

## 8. Key Risks & Mitigations

| Risk | Mitigation |
|---|---|
| **Chicken-and-egg: no artists → no collectors → no artists** | Manually onboard first 10–15 artists before public launch. Artist profiles have standalone value as portfolio tools even with zero collectors — artists benefit from joining even if no sales happen immediately. George's existing network provides a warm start no competitor can replicate. |
| **Overbuilding before validating demand** | Hard feature freeze at 11 MVP features. Events, messaging, AI discovery feed, and wishlists are all v2. Build schedule is 12 weeks with specific milestones — no feature creep without explicit decision to delay launch. |
| **Solo founder bandwidth: code + design + marketing + community** | AI-assisted development (Claude, Copilot) reduces implementation time. Quasar's 80+ pre-built components eliminate custom UI engineering. Supabase Studio replaces custom admin build. The architecture was explicitly designed for one-person maintenance. |
| **App Store rejection delaying launch** | Prioritise PWA (web app) for initial launch — available immediately, no review process. Convert waitlist to web users before iOS/Android is approved. Physical art and event tickets are exempt from Apple's 30% commission; this is documented and defensible. |
| **Cultural trust: will artists actually adopt a new platform?** | George is a certified Boston artist with a City Vendor ID and Mayor's Office of Art & Culture certification. He is not an outsider building for a community — he is the community. Celebrity collectors in his personal network provide social proof. The trust moat is the product's primary competitive advantage. |
| **Monetisation too early kills community formation** | Months 1–3: free everything. Artist Pro tier and boosted listings launch only after 50+ active profiles and demonstrated collector engagement. Art sale commissions introduced at month 6–12 minimum, after real transaction volume exists. |

---

## 9. Success Metrics

**Week 4 — Validation Complete**
- 15 customer discovery interviews completed (10 artists, 5 collectors/patrons)
- 50 email signups on waitlist landing page
- 20 artist intake forms submitted via Tally
- Massachusetts Cultural Council grant application submitted (deadline April 30, 2026)

**Week 8 — Supply Side Live**
- 10 fully populated artist profiles with 50+ artworks listed across the platform
- Web version (PWA) deployed and publicly accessible at frontstreetapp.com
- End-to-end Stripe purchase flow tested with 3 real transactions
- iOS and Android builds submitted to App Store / Play Store review

**Week 12 — Soft Launch**
- App live on iOS and Android
- 50 active users (artists + collectors combined)
- 5 completed artwork purchases recorded
- 7-day user retention rate ≥ 30%
- At least 1 launch event hosted with documented in-app QR code signups

**Month 6 — Growth Signal**
- 150+ active users
- 25 Artist Pro subscribers ($175 MRR from subscriptions alone)
- 20+ completed artwork purchases (commission revenue beginning)
- Events feature (v2) in development based on validated demand
- MassChallenge or Google for Startups Black Founders Fund application submitted

---

## 10. Timeline Overview

- **Weeks 1–2 — Validate Before Building:** Customer discovery interviews, waitlist activation, Tally artist intake form, community Signal group. Do not write application code until 20 artist expressions of genuine interest are confirmed.
- **Weeks 3–7 — Build Supply Side:** Database schema + Supabase auth setup, artist profiles, artwork upload with image optimisation, Cloudflare CDN integration. Target: 10 fully populated profiles before moving to collector features.
- **Weeks 7–9 — Build Demand Side + Payments:** Collector browse feed, artwork detail pages, tag/medium filtering, Stripe Connect integration (artist onboarding + Checkout). End-to-end purchase flow tested before App Store submission.
- **Weeks 10–11 — Native App Builds:** Quasar → Capacitor → iOS (Xcode) + Android (Android Studio) builds. Device testing on physical hardware — not simulator only. Submit to both stores.
- **Week 12 — Launch:** PWA live if app stores still in review. Invite waitlist. Host first launch event. Begin post-launch iteration cycle based on real user behaviour.

---

*Sources: FrontStreet Market Research (March 2026), FrontStreet Technical Architecture (March 2026), FrontStreet UX/UI Document I (March 2026) — all available in this Obsidian vault. Competitor pricing verified March 2026: Artsy ($425+/mo, third-party sources); Saatchi Art (40% commission, saatchiart.com official help center); Eventbrite (10–14% effective fee, published fee structure); Art Basel/UBS 2025 Survey of Global Collecting; Grand View Research Online Art Market Report.*


