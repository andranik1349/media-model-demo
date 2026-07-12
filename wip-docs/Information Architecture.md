# Media Model Website — Information Architecture & SEO

*Phase 2 deliverable. Turns the Phase 1 strategy into a buildable structure: page hierarchy, navigation, URL scheme, and page-level intent, with **SEO-readiness** brought in as a first-class concern (foundations an SEO team can build on — not a keyword strategy). Every structural choice traces back to the [Design Concept](Design%20Concept.md) — primarily the primary audience (international orgs/donors), the mission (prove rigor + local knowledge to an unfamiliar buyer), and the experience principles in §7 of that doc.*

Scope for this engagement is **English only**, though the structure is designed to accept an Armenian layer later (see §9). The core premise is fixed:

> **We know Armenia — its people, markets, institutions, and land realities — making us a trusted partner for complex decisions.**

This document also resolves the open questions carried forward from the concept doc §8 — portfolio presentation, LARP prominence, and Insights placement (SEO, the fourth item deferred there, is handled as its own concern in §8) — and records each IA decision in the log (§10) so the Phase 4 proposal deck can show the reasoning.

---

## 1. What this phase inherits and must fix

The original brief (*Site structure (EN).md*) is raw material, not a spec. Before proposing a new structure, it's worth naming precisely what is broken in the old one, because the Phase 4 proposal deck is built on this before/after contrast. Each problem below is resolved by a specific decision later in this document.

| # | Problem in the original brief | Why it hurts the primary audience | Resolved by |
|---|-------------------------------|-----------------------------------|-------------|
| P1 | **Nav vs. content mismatch.** The menu lists *Work With Us → For Individuals / For Companies*, but the page content splits into a *talent* pitch (recruitment) and a *For Companies* pitch (client sales). Two opposite jobs live under one recruitment-sounding label. | A procurement-minded client looking to hire Media Model would never click "Work With Us" — it reads as a careers link. The client-facing "For Companies" copy is buried where buyers won't find it. | §4 nav split: a client path (*Services* / *Contact*) and a separate *Careers* path (§3, D8). |
| P2 | **The portfolio — the strongest asset — is a flat dump.** 60+ dated, named-client projects sit as long scrolling lists inside *About → Our Impact*, four subsections deep, with no filtering and no featured tier. | The evidence a risk-averse buyer needs to see first is buried behind an "About" click and an internal jump. Best work (World Bank, UNICEF, OECD) is visually equal to a 2002 newspaper study. | §6 portfolio architecture: dedicated top-level *Our Work*, featured tier + tag/filter system (D9). |
| P3 | **Service naming is inconsistent across the doc.** "Policy Analysis & Strategic Advisory" (menu) vs. "Policy Analysis & Advisory" (services page); "Monitoring, Evaluation & Impact Assessment" vs. "Monitoring & Evaluation (M&E)"; LARP sub-items differ between home and services. | Inconsistent names read as carelessness to a standards-driven reader and fracture SEO (the same service competes with itself under two strings). | §5 canonical service taxonomy (one name per service, D12). |
| P4 | **Placeholder / missing contact details.** Phone, email, website all blank; address is "Google Map" with no value. | Contact is the primary conversion. A blank contact page kills the macro-conversion the whole site exists to drive. | §7 Contact page spec; **placeholders used through design**, real values swap in at launch (2026-07-11). |
| P5 | **Structure isn't SEO-ready.** URLs undefined, no metadata slots, no one-topic-per-page logic, no internal-linking structure. | An SEO team would have to restructure the site before starting; and the buyer who Googles a capability + "Armenia" finds nothing. Phase 2 lays foundations, not a keyword strategy. | §8 SEO-ready foundations. |
| P6 | **"About" is overloaded.** Our Story, Our Philosophy, Our Collective, *and* the entire project portfolio all sit under About — mixing identity, values, team, and evidence. | Dilutes both jobs: the identity story is interrupted by data, and the evidence is hidden inside identity. | §5 sitemap: portfolio promoted out; About tightened to identity + people. |
| P7 | **Insights is defined-but-hidden with no plan.** Listed in the menu, marked "hidden, not active in the initial phase," never specified. | An orphaned nav item creates a dead link risk and an unclear roadmap. | §6 decision: keep out of nav, reserve URL, no orphan link (D11). |
| P8 | **Home mixes weak and strong signals with no credibility tier.** The homepage leads with a mood image and a paragraph of "we, we, we" copy; the 25+ years / 150+ projects / named-client proof lives pages away under Our Impact. | Credibility must license the reading early (concept §7). The current order asks a skeptical buyer to trust before seeing proof. | §7 Home spec: credibility band + featured work near the top. |

**What the original brief gets right** (carry forward, don't lose in the redesign — the proposal deck should credit these):

- The **two-service-line structure** (Research & Advisory + LARP) is sound and is a real differentiator; we keep it.
- The **portfolio content itself** — dated, named-client, method-tagged projects — is gold-standard proof. The problem is presentation, not substance.
- The **"Our Impact" metrics** (25+ years, 150+ projects, 30+ experts, nationwide) are exactly the credibility signals the audience wants; we promote them, not discard them.
- The **collective concept** and the talent/"fieldwork becomes adventure" story are distinctive; we keep them, just on their own path.

---

## 2. IA principles (from strategy to structure)

The experience principles in Design Concept §7 translate into these structural rules. Every page and link decision below is testable against them.

1. **Evidence within one click of home.** Proof (featured projects, metrics, client roster) is reachable from the homepage without a search or a deep drill. *Our Work* is top-level nav, not buried in About.
2. **Credibility before persuasion, top to bottom.** On any given page, verifiable specifics (dates, clients, sample sizes, standards) appear before or alongside evocative framing — never after a wall of mood.
3. **One canonical home for every concept.** Each service, each project, each idea has exactly one URL that owns it. Everything else links to that home. This serves both the reader (no ambiguity) and SEO (no cannibalization).
4. **Separate the two jobs.** Winning clients and recruiting the collective are different funnels with different CTAs. They share a brand but not a path.
5. **Shallow and legible.** Target a maximum depth of **3 clicks** from home to any project detail. The "geometric rhythm / model the way" identity argues for an ordered, predictable structure — structure itself is a credibility signal.
6. **Structurally bilingual-ready.** URLs, templates, and navigation are designed so an `/hy/` Armenian layer can be added later without rework (§9), even though only English ships now.

---

## 3. Audience-to-path mapping

Each audience from the concept doc gets a deliberate entry point and primary path. This is what the nav and homepage are optimized to route.

| Audience | Entry angle | Primary path through the site | Primary CTA |
|----------|-------------|-------------------------------|-------------|
| **International orgs / donors** (primary) | Rigor + track record + local access | Home → *Our Work* (featured + filter by client type/method) → *Services* (Research & Advisory) → *Contact* | "Discuss a project" / RFP enquiry |
| **Domestic private sector** (secondary) | Local market insight + commercial relevance + speed | Home → *Services* (Market & Consumer) → *Our Work* (filter: private sector) → *Contact* | "Discuss a project" |
| **Government / public institutions** (secondary) | Neutrality + legal/institutional competence + delivery at scale | Home → *Services* (LARP) → *Our Work* (filter: LARP) → *Contact* | "Discuss a project" |
| **Talent — the collective** (distinct track) | Belonging + growth + "fieldwork becomes adventure" | Home (footer/secondary) → *Careers* → enquiry | "Join the collective" (separate form) |

**D8 — the client/talent split is the backbone of the nav.** The single biggest structural fix. The old "Work With Us" conflation (P1) is replaced by: a **client journey** carried by *Services* + *Our Work* + *Contact*, and a **talent journey** isolated in *Careers*, reachable but never competing for share of voice on the primary path. The "For Companies" content from the old brief is not a page — it is absorbed into *Services* intro and *Contact*, where buyers actually are.

---

## 4. Global navigation & shell

### Primary navigation (header)

```
Home  |  Services  |  Our Work  |  About  |  Partners  |  Contact          [Careers]  [Search]
```

- **Six primary items**, ordered by the primary buyer's decision sequence: understand the offer (*Services*) → check the proof (*Our Work*) → vet the firm (*About*) → see who trusts us (*Partners*) → act (*Contact*). *Home* is the logo. *Partners* is kept as a standalone page (§5).
- **Services** and **Our Work** are the two load-bearing items for conversion and carry dropdowns (below).
- **Careers** sits visually apart (right-aligned, lighter weight) — present for the talent audience, deliberately de-emphasized so it doesn't read as the primary action (D8).
- **Search** is retained from the brief (the old home listed a search bar) but demoted to an icon; it matters mostly once the portfolio is large.
- **Language switcher (EN / HY)** — built into the shell now, English-only active, Armenian stubbed (§9). Present in markup, not yet a live toggle.

**Services dropdown** (mirrors the canonical taxonomy, §5):

```
Services
├── Research & Advisory
│   ├── Social & Public Opinion Research
│   ├── Market & Consumer Research
│   ├── Monitoring, Evaluation & Impact
│   └── Policy Analysis & Advisory
└── Land Acquisition & Resettlement (LARP)
```

**Our Work dropdown** (fast routes into the filtered portfolio):

```
Our Work
├── Featured projects
├── Research projects
├── LARP projects
└── Browse by sector / client / method   →  filter view
```

**About dropdown** (tightened — portfolio removed, per P6):

```
About
├── Our Story
├── Our Collective   (people, network, expertise)
└── Impact & Numbers (metrics + who-we-work-with band → Partners)
```

*Our Philosophy* from the old brief collapses **into Our Story** (values + how-we-work + vision/mission read as one identity narrative; splitting them created four thin pages). *Our Impact* splits: the **metrics** stay in About as "Impact & Numbers" (with a light who-we-work-with band that links to the standalone *Partners* page); the **project portfolio** is promoted to top-level *Our Work* (D9).

### Footer (global)

Three-job footer, consistent site-wide:

- **Navigate** — full sitemap links (all primary + secondary pages, including *Careers* and, later, *Insights*).
- **Contact block** — address (with map link), phone, email, mediamodel.am — the details the brief left blank (P4). Present on every page so the conversion path is always one scroll away.
- **Identity strip** — logo, "research collective / since 2001", approved descriptors, ©, and the language switcher echo.

---

## 5. Sitemap & canonical service taxonomy

### Full sitemap

```
Home  /
│
├── Services  /services/
│   ├── Research & Advisory              /services/research-advisory/
│   │   ├── Social & Public Opinion Research      /services/research-advisory/social-public-opinion/
│   │   ├── Market & Consumer Research            /services/research-advisory/market-consumer/
│   │   ├── Monitoring, Evaluation & Impact       /services/research-advisory/monitoring-evaluation/
│   │   └── Policy Analysis & Advisory            /services/research-advisory/policy-advisory/
│   └── Land Acquisition & Resettlement (LARP)    /services/larp/
│
├── Our Work  /our-work/
│   ├── (featured + filterable index — sector / client type / method)
│   ├── Research projects (filter view)           /our-work/research/
│   ├── LARP projects (filter view)               /our-work/larp/
│   └── Project detail (2 templates: case study / one-pager)  /our-work/{project-slug}/
│
├── About  /about/
│   ├── Our Story        /about/  (values, how we work, vision & mission fold in here)
│   ├── Our Collective   /about/collective/
│   └── Impact & Numbers /about/impact/  (metrics + who-we-work-with band → Partners)
│
├── Careers  /careers/   (the "collective" / talent track — formerly "Work With Us → For Individuals")
│
├── Contact  /contact/
│
├── Partners  /partners/   (standalone page — client & partner logos now, room for SEO content later — see note)
│
└── Insights  /insights/   (reserved, NOT in nav, not built this phase — D11)
```

**Depth check:** Home → Our Work → project detail = 2 clicks. Home → Services → sub-service = 2 clicks. Nothing the primary audience needs exceeds the 3-click rule (principle 5).

**Note on Partners.** Retained as a **standalone page in primary nav** (as in the original brief). It starts as a partner/client logo wall but is given its own URL and template deliberately, so it can be **enriched with SEO-relevant content later** (partnership descriptions, named-relationship context, links into related work). *About → Impact & Numbers* keeps a lighter "who we work with" credibility band that links through to Partners, so the two don't fully duplicate: Impact frames the numbers, Partners owns the relationships. *(Decision 2026-07-11 — kept standalone rather than folded.)*

### Canonical service taxonomy (fixes P3)

One name per service, used identically in nav, page titles, URLs, and body copy. This is the single source of truth; the old brief's variants are retired.

| Canonical service name | Retired variants (from old brief) | URL slug |
|------------------------|-----------------------------------|----------|
| Social & Public Opinion Research | "Social & Public Opinion Research" | `social-public-opinion` |
| Market & Consumer Research | "Market & Consumer Insights" / "Market & Consumer Research" | `market-consumer` |
| Monitoring, Evaluation & Impact | "Monitoring, Evaluation & Impact Assessment" / "Monitoring & Evaluation (M&E)" | `monitoring-evaluation` |
| Policy Analysis & Advisory | "Policy Analysis & Strategic Advisory" / "Policy Analysis & Advisory" | `policy-advisory` |
| Land Acquisition & Resettlement (LARP) | LARP sub-items listed inconsistently on home vs. services | `larp` |

The LARP page consolidates the three inconsistent home-page sub-items ("End-to-End LARP Implementation", "Stakeholder Coordination & Institutional Engagement", "Stakeholder Engagement & Consultation") into the single, cleaner "Key Areas of Work" list already present on the services page — one canonical description.

---

## 6. Resolving the carried-forward open questions

### D9 — Portfolio presentation: dedicated *Our Work* with a featured tier + filters

**Decision.** Promote the portfolio out of *About* to a **top-level *Our Work*** section with two layers:

1. **A curated featured tier** — a small set of marquee projects surfaced on both the homepage and the top of *Our Work*, so the best work is seen first and never sits visually equal to a minor 2002 study (fixes P2/P8). This is a **managed, rotating CMS slot**, not a fixed list baked into the IA: which projects appear is a content decision the client makes and changes over time. Any specific projects named in this doc or the prototype (e.g., World Bank Regional Justice Survey, OECD Citizen Survey, UNICEF programmes, North–South Corridor LARP) are **illustrative placeholders** to show the slot working — the wireframe/prototype will use 3–5 representative projects, and the production selection is out of scope here.
2. **A filterable full index** — every project as a card, filterable by a controlled taxonomy (below). This preserves the depth of the 60+ list without the data-dump problem.

**Portfolio taxonomy (filters).** Three orthogonal axes, each derivable from the existing project data, so filtering requires no new content — only tagging:

- **Sector / theme:** Public Policy & Governance · Market & Consumer · Social Development & Infrastructure · Monitoring & Evaluation · Land Acquisition & Resettlement.
- **Client type:** International development org · Government / public · Private sector · Prime contractor (subcontracted fieldwork).
- **Method:** CAPI · CATI · Face-to-face survey · Focus groups (FGD) · In-depth interviews · Panel / longitudinal · Mixed methods · Impact evaluation.

**Project card = the credibility unit.** Each card carries exactly the fields the buyer scans for: project name · client (named) · period (dated) · scope · method · sample size / coverage. These are the specifics the concept doc says must do the boasting. Behind the card, project detail is provided by **two page templates** — a **full case study** (Template A) for flagship engagements and a **short one-pager/article** (Template B) for the long tail (see §7). Phase 2 supplies both templates; *which* project uses which (or stays card-only) is a per-project content/CMS decision, out of scope for this exercise.

This directly implements the client's own proposed direction from concept §8 and validates it: featured sections + tags/filters, now specified as an architecture.

### D10 — LARP prominence: co-equal service line, government/IFI-targeted, not homepage-dominant

**Decision.** LARP is presented as a **co-equal second service line** — its own top-level entry under *Services* (`/services/larp/`) and its own portfolio filter — but it does **not** get equal share of voice on the homepage, which is optimized for the primary international-research buyer.

**Rationale.** LARP is a genuine differentiator (few research houses do full-cycle land acquisition) and serves the government/IFI audience, so it must be easy to find and fully specified for those who need it. But foregrounding it on the homepage would muddy the primary narrative aimed at research/evaluation buyers. Resolution: **discoverable and complete, not dominant.** The homepage gives LARP a single clear entry (one of two service cards); the depth lives on its own page and portfolio filter. This satisfies the concept doc's open question by scoping *where* LARP leads (its own page, the government path, IFI infrastructure searches) versus where it supports (homepage as one of two lines).

### D11 — Insights: reserved, out of nav, no orphan link

**Decision.** *Insights* stays out of primary navigation and is not built this phase (consistent with the brief and concept §3/§8). We **reserve the `/insights/` URL** and template slot so a future thought-leadership layer can be added without restructuring, but we do **not** place an orphaned/dead nav link (fixes P7). If/when content exists, Insights enters via the footer first, then earns nav placement. This keeps the site's job clear — it converts on enquiry, not content consumption (concept D3).

---

## 7. Page-by-page IA

For each page: its **job**, its **key content blocks in order**, its **primary internal links**, and the **one topic it owns** (illustrative — see the §8 scope note; the SEO team validates the exact terms). Copy is intent, not final wording (that's Phase 3).

### Home — `/`
**Job:** In one screen and one scroll, convince a skeptical, unfamiliar international buyer that Media Model pairs defensible rigor with unmatched local knowledge, and route them to enquire.
**Blocks (in order):**
1. **Hero** — Armenia image + "We know Armenia" framing (human frame). Single primary CTA: *Discuss a project*.
2. **Premise + proof pairing** — the core-premise line immediately substantiated (concept §5 before→after model).
3. **Credibility band** — 25+ years · 150+ projects · 30+ experts · nationwide (promoted from Our Impact; licenses the reading — fixes P8).
4. **Two service lines** — Research & Advisory / LARP, as two clear cards → Services.
5. **Featured work** — 3–5 marquee, named-client projects → Our Work (evidence within one click — principle 1).
6. **Who we work with** — client/partner logo band (World Bank, UNICEF, OECD, EBRD, ADB…) as a due-diligence shortcut.
7. **The collective, briefly** — one band on the model, linking to About → Our Collective.
8. **Talent nudge** (secondary) — small "Join the collective" → Careers, kept off the primary CTA.
9. **Contact CTA + footer.**
**Internal links out:** Services (both lines), Our Work (featured + all), About/Collective, Careers, Contact.
**Topic (illustrative):** brand + primary category — "Media Model", "research and advisory Armenia", "research collective Armenia".

### Services (index) — `/services/`
**Job:** Frame the two-line offer and route to the right sub-service; absorb the old "For Companies" client pitch.
**Blocks:** intro (collective, tailored, research-to-implementation) → two service-line cards → light proof strip (relevant featured projects) → Contact CTA.
**Links:** four Research & Advisory sub-pages, LARP page, Our Work (filtered), Contact.
**Topic (illustrative):** "research and advisory services Armenia", "market research company Armenia".

### Research & Advisory — `/services/research-advisory/`
**Job:** Own the research-buyer category and distribute to the four sub-services.
**Blocks:** category intro → four sub-service summaries (canonical names) → methods/quality-control note (rigor signal) → related featured projects → Contact CTA.
**Links:** four sub-service pages, Our Work (research filter), Contact.
**Topic (illustrative):** "social research Armenia", "public opinion research Armenia", head term for the cluster.

### Sub-service pages ×4 — `/services/research-advisory/{slug}/`
**Job:** Convert on a specific need; rank for specific-intent searches.
**Blocks (template):** what it is (plain) → what you get / what it de-risks (outcome-oriented, "you") → methods & capabilities (CAPI/CATI/qual, sampling, QC — the rigor substance) → 2–3 relevant projects (auto-pulled by tag) → Contact CTA.
**Links:** parent Research & Advisory, tagged projects in Our Work, Contact.
**Topics owned (illustrative — one per sub-service):**
- Social & Public Opinion → "public opinion survey Armenia", "CAPI survey Armenia".
- Market & Consumer → "market research Armenia", "consumer research Yerevan".
- Monitoring, Evaluation & Impact → "monitoring and evaluation Armenia", "impact evaluation Armenia".
- Policy Analysis & Advisory → "policy research Armenia", "policy analysis Armenia".

### LARP — `/services/larp/`
**Job:** Fully specify the differentiator for government/IFI buyers; rank for a low-competition, high-value niche.
**Blocks:** what LARP is + standards framing (RA legislation + international policy — neutrality/competence signals) → Key Areas of Work (the consolidated canonical list) → flagship projects (North–South Corridor, Kajaran–Agarak) → institutional-coordination note → Contact CTA.
**Links:** Our Work (LARP filter), flagship project details, Contact.
**Topic (illustrative):** "land acquisition and resettlement Armenia", "LARP Armenia", "resettlement consultant Armenia" (near-zero competition, high intent).

### Our Work (index) — `/our-work/`
**Job:** The proof engine. Let a buyer confirm comparable, credible, recent experience fast.
**Blocks:** featured tier (marquee cards) → filter controls (sector / client type / method) → full card grid → CTA to Contact.
**Links:** every project card → detail or expanded card; Services (cross-link by theme); Contact.
**Topic (illustrative):** "research projects Armenia", long-tail via individual project pages (named clients + methods).

### Project detail — `/our-work/{project-slug}/`
**Job:** Deep proof for a specific comparable engagement; long-tail SEO. Phase 2 defines the **structure — two page templates**; which project uses which (or stays card-only) is a content/CMS decision, out of scope here.

**Template A — Full case study** (for flagship engagements that merit depth):
**Blocks:** title · client · period · scope · method · sample/coverage → context/challenge → approach & methodology → outcome/what it de-risked → related projects/service → Contact CTA.

**Template B — Short one-pager / article** (for the long tail — a compact, consistent record):
**Blocks:** title · client · period · scope · method · sample/coverage → a short paragraph of narrative → related service → Contact CTA.

**Topic (illustrative):** highly specific long-tail (e.g., "Regional Justice Survey Armenia World Bank").

### About → Our Story — `/about/`
**Job:** Establish identity and trust; fold in philosophy/values/vision/mission as one narrative.
**Blocks:** founding + evolution (2001 → 2012 LARP expansion) → values & how we work (from old Our Philosophy) → vision & mission → link to Collective and Impact.
**Topic (illustrative):** "about Media Model", "research company Armenia since 2001".

### About → Our Collective — `/about/collective/`
**Job:** Explain the collective model and the breadth of expertise (the differentiator).
**Blocks:** "a collective, not a team" → disciplines in the network (sociologists, economists, statisticians, legal, field) → how expertise is assembled per challenge → Careers nudge.
**Topic (illustrative):** "research collective Armenia", "research experts Armenia".

### About → Impact & Numbers — `/about/impact/`
**Job:** Concentrate the credibility signals (metrics + a who-we-work-with band) in one linkable place; the full relationships live on *Partners*.
**Blocks:** key metrics (25+/150+/30+/nationwide) → areas of impact (5 sectors) → a "who we work with" credibility band (highlight logos) that links through to the standalone *Partners* page → CTA into Our Work.
**Topic (illustrative):** "Media Model clients", credibility/entity signals.

### Partners — `/partners/`
**Job:** Own the partner/client relationships as a trust signal; a standalone page with room to grow into SEO-relevant content.
**Blocks:** intro (the range of institutions we work with — public, private, international) → partner/client logo wall (grouped: international dev orgs · government · private sector · prime contractors) → *(room to grow)* short relationship/partnership write-ups and links into related *Our Work* projects → Contact CTA.
**Links:** Our Work (by client type), About → Impact & Numbers, Contact.
**Topic (illustrative):** "Media Model partners", "Media Model clients Armenia" (a natural home for future relationship-led SEO content).

### Careers — `/careers/`
**Job:** The talent funnel, fully separated from the client path (D8). "Fieldwork becomes adventure."
**Blocks:** the collective as a place to work → who we look for (experienced + early-career) → what you gain → separate enquiry ("Join the collective", distinct from client contact).
**Topic (illustrative):** "research jobs Armenia", "fieldwork jobs Armenia".

### Contact — `/contact/`
**Job:** Convert. This is the macro-conversion; it must not have gaps (fixes P4).
**Blocks:** "Get in Touch" → enquiry form (name, org, project type, message; project-type field routes research vs. LARP) → **required real details:** address + map, phone, email, mediamodel.am → office/hours if relevant.
**Content note:** phone/email/address are blank in the brief. **Decision (2026-07-11): use placeholders** for the wireframe and prototype — real values swap in at launch and don't block design.
**Topic (illustrative):** "contact Media Model", "research firm Armenia contact".

---

## 8. SEO-ready foundations (not a full SEO strategy)

**Scope note.** Phase 2 does *not* run keyword research or commit to a ranking strategy — that is a future SEO team's job. What Phase 2 owns is making the IA and page structure **SEO-friendly**: clean URLs, a logical hierarchy, one clear topic per page, and the content slots (titles, metadata, headings, internal links) an SEO specialist needs. The test is simple — an SEO team should be able to take over and add their usual work *without* having to restructure the site first, and the site shouldn't fall apart the moment they start. The brief offered none of this (P5); the sections below are the foundations we commit to, plus illustrative examples the SEO team can accept, tune, or replace.

### 8.1 The foundations we commit to

These are structural and belong to the IA — they ship as part of Phase 2's thinking, not as recommendations for later:

- **Clean, human-readable, stable URLs / slugs** — the scheme in §5. No IDs, no query-string pages in the primary path.
- **One topic per page, one H1 per page**, with a logical heading hierarchy — so no two pages compete for the same topic (the anti-cannibalization rule below).
- **Metadata slots on every template** — title, description, canonical, OpenGraph — present in the markup with sensible defaults, ready for the SEO team to populate properly.
- **A crawlable internal-linking structure** — hub-and-spoke, footer sitemap, no orphans (§8.4).
- **Technical hooks in place** — XML sitemap, robots.txt, alt text, mobile-first templates, HTTPS, and `hreflang` scaffolding for the future Armenian layer (§9).

### 8.2 One topic per page (the anti-cannibalization map)

The load-bearing IA decision for SEO: each page **owns one topic**, so pages don't compete with each other and the SEO team inherits a clean slate. The map below assigns that single topic per page. **The example terms are illustrative** — a plausible "capability + Armenia" framing to show the topic each page should own — not committed keyword targets. The SEO team validates, refines, or swaps them; the *structure* (one topic, one owning page) is what Phase 2 fixes.

| Page | Topic it owns | Illustrative terms (for the SEO team to validate) |
|------|---------------|---------------------------------------------------|
| Home | Firm / brand | Media Model, research collective Armenia |
| Services / Research & Advisory | The research offer overall | research and advisory services Armenia |
| Sub-service: Social & Public Opinion | Public-opinion research | public opinion survey Armenia, CAPI survey |
| Sub-service: Market & Consumer | Market research | market research Armenia, consumer research |
| Sub-service: Monitoring, Evaluation & Impact | M&E | monitoring and evaluation Armenia, impact evaluation |
| Sub-service: Policy Analysis & Advisory | Policy research | policy research Armenia, policy analysis |
| Services: LARP | Land acquisition & resettlement | land acquisition and resettlement Armenia, LARP |
| Our Work | Proof / project experience | research projects Armenia (+ per-project long-tail) |
| About / Impact | Firm trust & credibility | research company Armenia since 2001, Media Model clients |
| Careers | Talent | research jobs Armenia, fieldwork jobs Armenia |

Rule (principle 3): the broad term belongs to the index page; the specific topics to the leaf pages. Sub-service pages must not all point at "research Armenia" — that would have them cannibalize each other. This is enforced by structure, independent of whichever exact keywords the SEO team lands on.

### 8.3 Metadata pattern (defaults, tunable)

Every template exposes these slots, pre-filled with sensible defaults so nothing ships blank — all tunable by the SEO team:

- **Title tag pattern:** `{Page topic} in Armenia | Media Model` (front-load the topic; keep < ~60 chars).
- **Meta description slot:** one sentence of capability + one proof specific (named client / sample scale) + soft CTA, ≤ ~155 chars, in the concept-doc voice (proof, not adjectives).
- **H1 = the page's one topic**, exactly once per page, matching the canonical taxonomy name (reinforces the P3 fix).
- **Structured-data hooks (schema.org):** `Organization` on Home/About, `Service` on service pages, optional project markup on project pages — scaffolding for the SEO team to complete.
- **Canonical tags** self-referencing on every page. Important for *Our Work*: expose filters as crawlable static paths (`/our-work/research/`, `/our-work/larp/`) rather than indexable `?sector=` permutations, so filtering can't spawn duplicate pages.
- **OpenGraph/Twitter** slots on featured project and service pages.

### 8.4 Internal-linking structure

Internal links are both an IA concern (how a reader moves) and the SEO team's circulatory system. Phase 2 fixes the structure; the SEO team tunes anchors and emphasis:

- **Hub-and-spoke per service.** Each Research & Advisory sub-service links up to the category hub and down to its tagged projects; the hub links to all four. LARP is its own hub → LARP projects.
- **Projects link to the service they prove, and vice versa.** A CAPI public-opinion project links to the Social & Public Opinion sub-service; that sub-service pulls in 2–3 such projects. Ties proof to offer bidirectionally (concept: evidence converts).
- **Featured projects surfaced from Home and Services**, not only from Our Work — so buyer attention (and link equity) reaches the best pages fast (principle 1).
- **Contact reachable from every page** (footer + per-page CTA) — the conversion target is never more than a scroll away (fixes the buried-CTA half of P1/P4).
- **Descriptive anchor text**, never "click here" — so links describe their destination.
- **No orphans.** Every published page is linked from at least the footer sitemap. Insights, while reserved, gets no link until it has content (D11) — no dead/orphan link.

### 8.5 Technical hooks handed to the SEO team

Structural requirements the IA assumes and leaves in place for the SEO team to build on: the clean slug scheme (§5), one H1 per page, logical heading hierarchy, XML sitemap + robots.txt, optimized imagery (the photo set is heavy), descriptive alt text on the Armenia/fieldwork imagery, mobile-first responsive templates, HTTPS on mediamodel.am, and `hreflang` scaffolding for the future Armenian layer (§9). None of these require design decisions; they're foundations that keep the site from fighting an SEO team later.

---

## 9. Bilingual-ready structure (English-only now)

English ships this phase, but the structure must not make an Armenian layer painful (concept §7, principle 6):

- **URL strategy (decided):** **English (default) lives at the root — no language prefix.** Armenian and any languages added later take a `/{lang}/` prefix (`/hy/…`, `/ru/…`) with mirrored slugs. So `/services/larp/` is the English page; `/hy/services/larp/` is its Armenian pair.
- **`hreflang` anticipated:** metadata scaffolding assumes future `en`/`hy` pairs so the switch is additive, not a re-architecture.
- **Navigation & templates language-agnostic:** the EN/HY switcher lives in the shell now (inactive); labels and slugs are variables, not hard-coded, so a translation layer drops in.
- **Content model separates structure from copy:** page templates (blocks, taxonomy, links) are defined independently of the English strings, so Armenian content reuses the same IA.

---

## 10. Decisions log (Phase 2 additions for the proposal deck)

Continues the Design Concept §9 log. Each entry is a change the Phase 4 proposal must justify, traced to a Phase 1 finding or an original-brief problem.

| # | Decision | Rationale | Traces to |
|---|----------|-----------|-----------|
| D7 | Portfolio promoted to top-level *Our Work* (out of About) | It's the primary audience's key decision input and the strongest asset; burying it under About contradicts "evidence within reach" | Concept D5; problem P2/P6 |
| D8 | Nav split into a client path (Services/Our Work/Contact) and a separate *Careers* track; old "Work With Us" retired | Winning clients and recruiting the collective are different jobs; the old label hid the client pitch and mislabeled the buyer path | Concept D4; problem P1 |
| D9 | Portfolio = featured tier + filterable index (sector/client type/method) | Surfaces best work without losing depth; implements and validates the client's proposed direction | Concept §8 open Q; problem P2 |
| D10 | LARP = co-equal service line, discoverable but not homepage-dominant | Real differentiator for gov/IFI buyers, but homepage stays optimized for the primary research buyer | Concept §8 open Q; audience model |
| D11 | Insights reserved (URL + slot), kept out of nav, no orphan link | Site converts on enquiry not content; avoids a dead nav item while preserving a future path | Concept D3; problem P7 |
| D12 | Canonical service taxonomy — one name per service across nav/URL/copy | Inconsistent naming reads as careless to a standards-driven reader and splits SEO signals | Problem P3 |
| D13 | *Our Philosophy* folds into *Our Story*; *Our Impact* splits (metrics→About, projects→Our Work) | Four thin identity pages became one coherent story; evidence moved to where it converts | Problem P6 |
| D14 | *Partners* kept as a **standalone page in primary nav** (not folded) — logo wall now, room for SEO content later | Client steer; a dedicated URL can be enriched into relationship-led SEO content; Impact & Numbers keeps a lighter "who we work with" band that links to it | Original brief; client decision 2026-07-11. **Internal decision — exclude from the Phase 4 proposal deck** (no change vs. the original brief, so nothing to justify to the client) |
| D15 | IA and page structure made SEO-*ready* (clean URLs, one topic per page, metadata slots, crawlable linking) — foundations only, not a keyword strategy | Phase 2's job is to hand a future SEO team a structure they can build on without restructuring; keyword research is theirs | Problem P5 |
| D16 | Two project-page templates — full case study + short one-pager/article — instead of a single detail page or per-project bespoke work | The original brief had no project pages at all (flat lists); two templates give depth where it's earned and a consistent, non-thin record for the long tail. Per-project assignment is a content/CMS decision, not IA | Problem P2; original brief |

---

## 11. Open questions carried into Phase 3

- ~~**Partners page (D14):**~~ resolved — *Partners* stays a **standalone page** (kept as in the original brief; room to enrich with SEO content later). Not folded. This fork is an internal call and is **excluded from the Phase 4 proposal deck** (no change from the original brief to justify).
- ~~**Contact details (P4):**~~ resolved — use placeholders through wireframe/prototype; real phone, email, and address swap in at launch (not a design blocker).
- ~~**Featured-project selection:**~~ not an IA decision. The featured tier is a **rotating CMS slot** (§6/D9); the wireframe and prototype use 3–5 representative projects purely to show the slot working. What lands there in production is a content/CMS decision the client owns and changes over time — out of scope for this exercise.
- ~~**Project-detail depth:**~~ not an IA decision. Phase 2 provides the **structure — two project-page templates** (full case study + short one-pager/article; §7, D16). Which project uses which, or stays card-only, is a per-project content/CMS call, out of scope here.
- ~~**Root vs. `/en/` URL prefix (§9):**~~ decided — English (default) at the root, no prefix; other languages take a `/{lang}/` prefix later (e.g., `/hy/`).
- **Homepage section order (into Phase 3):** §7 proposes a sequence; the wireframe phase will pressure-test the exact block order and CTA placement.

---

*Inputs: [Design Concept.md](Design%20Concept.md) (Phase 1); Site structure (EN).md (original brief, as raw material); project portfolio. Prepared as the structural foundation for Phase 3 (Homepage Structure & Wireframe) and as source material for the Phase 4 client proposal deck.*
