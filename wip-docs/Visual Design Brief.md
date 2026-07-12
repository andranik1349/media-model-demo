# Media Model Homepage — Visual Design Brief

*Phase 4 visual-direction note. Captures the visual discovery discussion and serves as the build spec for the high-fidelity homepage prototype (`media-model-client-deliverables/homepage-prototype.html`). Also feeds the "what came out of discovery" section of the Phase 4 proposal deck. Everything here honors the locked strategy in [Design Concept.md](Design%20Concept.md) and the structure in [Information Architecture.md](Information%20Architecture.md) §7.*

---

## 1. The design problem (and the idea that resolves it)

Two visual reference streams sit in the project folder and pull in opposite directions:

- **Media Model's own campaign** (beekeeper, woodworker, "We know Armenia," fieldwork-becomes-adventure) is **bold and poster-like** — navy/yellow color-blocking, split-screen compositions, the silhouette cut-out device (flat-color figure paired with the real photo), a thick connector bar, slab headlines, strong Armenian photography.
- **The editorial web references** (the Wittig portfolio the client added) are **restrained and premium** — warm off-white canvas, oversized two-tone display type, generous air, minimal line-art data motifs, serif pull-quotes, quiet fixed side-rails.

**The idea:** a **restrained editorial canvas carrying bold, recurring brand beats.** The airy layout is the credibility spine the procurement-minded donor audience needs; the campaign's boldness returns as a deliberate rhythm rather than wallpaper. This maps exactly onto the two strategic rules already locked — *credibility before persuasion* and *accents, not wallpaper* (Design Concept §7) — and it does the job memory flags: **reunite the agency's strong identity with the website the original brief let go flat.**

Feel target: *bold beat → breathe → bold beat.* Never a wall of posters; never a timid white-and-blue brochure.

---

## 2. Strategic anchors this design must honor

- **Primary audience:** international orgs/donors (World Bank, UN, OECD, EU, EBRD, ADB) — procurement-minded, risk-averse. They must read rigor and restraint fast.
- **Core premise (verbatim):** *"We know Armenia — its people, markets, institutions, and land realities — making us a trusted partner for complex decisions."*
- **Tone:** human/evocative at the frame, rigorous/precise in the substance.
- **Primary CTA:** *Discuss a project* (enquiry/RFP). One clear macro-conversion, reachable throughout.
- **Structure:** the homepage sections from IA §7 — **ten sections here**, since IA §7's single "two service lines" block is presented as two separate sections (Research & Advisory §4, LARP §5). On the bold **asymmetric editorial grid** inherited from the Phase 3 wireframe (unequal 2–3 col spreads, staggered offsets — no single-column stacks, no uniform 3-up icon-card grids).

---

## 3. Color system

Load-bearing three-color system. **Yellow is a structural third color, not a garnish** — it appears as ground and fill often enough that removing it would break the design. Resist collapsing to navy/white/black.

| Token | Hex | Role |
|-------|-----|------|
| Navy | `#0f2873` | Structural type, hairline rules, the heavy base (§9 Contact), one silhouette voice |
| Yellow | `#fad75f` | Load-bearing accent **and** ground — stat band, section grounds, silhouette fills, connector bar, CTAs, the other silhouette voice |
| Off-white | `#f4f4f4` | Primary canvas — the airy editorial spine |
| White / near-black | `#ffffff` / ~`#141414` | Card grounds, body text where navy is too heavy |

Usage rule: the canvas is light; navy gives structure; **yellow does real work** at the beats (hero connector, stat band, one or both service-line grounds, talent nudge, contact CTA). Photography supplies warmth in full color.

---

## 4. Typography

- **Titles / display: Arvo** (Google Fonts, slab serif) — approximates the campaign's slab "We know Armenia" headlines. Used for hero, section openers, the evocative "frame" moments.
- **Body / substance: Sora** (Google Fonts) — service copy, project-card fields, metrics, navigation, the rigorous material.
- **Pull-quotes:** Arvo, with the grey→navy scrub-reveal borrowed from the reference.
- Loaded via a Google Fonts `<link>`; no other typefaces.

Principle: slab (Arvo) carries feeling; Sora carries proof — the tone split made typographic.

---

## 5. Interaction vocabulary (recurring gestures, not one-off effects)

A small, reused set so the page feels composed:

1. **Portal-zoom reveal** — the hero (see §6).
2. **Silhouette-fills-with-photo** — the signature beat at §4 (Research & Advisory) and §8 (the collective). A flat-color silhouette resolves into the real photo on scroll/hover — the flat↔real relationship of the beekeeper/woodworker frames turned into a web gesture. *This is the single most honest translation of the campaign into an interface.*
3. **Drawn line geometry** — the brand's own `graph`/`infographic` SVGs draw themselves in on scroll (stroke animating) = "geometric rhythm / model the way" made literal. Quiet background structure.
4. **Connector bar** — the thick horizontal bar from the campaign, reused as divider/stat-rail/section link.
5. **Scrub reveal** — text shifts grey→navy as it enters (§2, pull-quotes). Restrained.

Motion discipline: tasteful fades/slides, controlled pinned zoom. No bouncy easing, **no long scroll-jacking sequence that traps the user.**

---

## 5A. Craft & motion standards

Adopted from the high-end-visual-design skill, filtered to what fits Media Model's restrained-institutional, geometric-slab identity. These raise the "agency-build" quality without fighting the brand.

**Adopt:**

- **Custom easing everywhere** — all transitions on a custom curve (e.g. `cubic-bezier(.32,.72,0,1)`); never `linear` or `ease-in-out`. Entrances ~600–800ms.
- **Entrance reveals** — elements fade-up on enter (`translate-y` + `opacity`, optional faint blur), via `IntersectionObserver`. Stagger on lists: featured rows, stat band, logo band, nav dropdown.
- **Depth, done right** — no harsh drop shadows, no generic 1px solid-gray borders. Hairlines = brand navy at ~8–12% opacity; shadows = soft, diffused, low-opacity ambient. Cards stay crisp with small radii (~2px, brand-native — not squircles).
- **CTA physics** — `active:scale(.98)` press feedback; the arrow nudges on hover (transform only).
- **Ultra-light icon strokes**; generous macro-whitespace (already the editorial spine — keep sections breathing).
- **Optional, kept minimal:** a very subtle fixed film-grain overlay (`opacity ~.03`, `pointer-events:none`) for paper tactility. Only if it doesn't muddy the clean editorial surface.

**Performance guardrails (hard rules):**

- Animate **only `transform` and `opacity`** — never width/height/top/left.
- **Portal-zoom implementation:** CSS scroll-driven animation (`animation-timeline: scroll()`) where supported; otherwise a **rAF-throttled passive scroll handler writing only `transform: scale()` / `opacity`.** No per-frame layout reads.
- `backdrop-blur` only on the fixed header/overlays, never on scrolling content. `will-change` sparingly. Honor `prefers-reduced-motion` on every gesture (§10).

**Explicitly rejected (would contradict locked decisions):** dark OLED / glassmorphism vibes; the floating glass-pill "Fluid Island" nav + screen-filling glass hamburger modal (too consumer-trendy for the donor audience — we keep the fixed slim header/side-rails); exaggerated squircle radii + "Double-Bezel" machined-card architecture (fights the geometric-slab identity); button-in-button circle-wrapped CTA arrow (plain `→` is more on-brand).

---

## 6. Hero — the portal-zoom (`/`)

Animates Media Model's *own* motif: the monastery window framing a valley in "We know Armenia" = the literal act of looking through a frame into Armenia. Not a borrowed gimmick.

- **Start:** a small **plain square aperture** (clean editorial frame — no window/skeuomorphic mockup) centered on the off-white canvas, full-color Armenian landscape inside.
- **Scroll:** the aperture zooms/grows, pulling the viewer *through* it until the photo fills the viewport.
- **Mid:** "We know Armenia" flies in (fade/slide, not bounce).
- **Settle:** full hero resolves — Arvo headline + supporting line (the concept-doc before→after copy) + single *Discuss a project* CTA + yellow connector bar.
- **Fallback:** reduced-motion / no-JS resolves straight to the full static hero.

The portal replaces the split-screen silhouette *in the hero*; the silhouette beat moves down to §4 (Research & Advisory) and §8 (the collective). Result: cinematic entry → editorial substance → bold brand beats punctuating.

---

## 7. Section-by-section spec (IA §7 order)

| # | Section | Visual + interaction | Rhythm |
|---|---------|----------------------|--------|
| 1 | **Hero** | Portal-zoom reveal (§6). Full-color Armenia. Yellow connector bar. Single CTA. | Cinematic |
| 2 | **Premise + proof** | Editorial calm. Arvo two-tone line; the concept-doc before→after. Proof half scrub-reveals grey→navy. | Breathe |
| 3 | **Credibility band** | Connector bar → horizontal stat rail: 25+ · 150+ · 30+ · nationwide. `graph a.svg` line draws in behind. **Yellow ground.** Numbers **fade in (not count-up).** | Beat (quiet) |
| 4 | **Research & Advisory** | **Silhouette beat.** The primary service line, now its own full-width section (not cramped beside LARP). Category intro + the four sub-services as inline rows (canonical names) + a methods/rigor note. Silhouette-fills-with-photo device; light editorial ground with yellow accents. **Leads on scale/richness (D10).** → Services / sub-services. | Bold beat |
| 5 | **LARP** | Its own dedicated section, but **deliberately more compact and contrasting** — a navy (or yellow) ground, "Rare capability" badge, the consolidated Key Areas of Work, gov/IFI framing. Secondary weight keeps LARP **co-equal but not homepage-dominant (D10)**; the different treatment stops the two service sections reading as one long block. → LARP page. | Beat (secondary) |
| 6 | **Featured work** | Editorial, full color. Credibility-unit cards (name · client · period · method · sample). Asymmetric — one large marquee + smaller, no uniform grid. Cards lift on hover → Our Work filters. 3–5 representative projects (placeholders; featured tier is a rotating CMS slot — IA D9). | Breathe |
| 7 | **Who we work with** | Restrained client-logo band (World Bank, UNICEF, OECD, EBRD, ADB…), slow marquee, grayscale→color on hover. Due-diligence shortcut. | Breathe (low-drama) |
| 8 | **The collective** | **Silhouette beat.** The model/differentiator — *"a collective, not a fixed team."* Fieldwork/team photography illustrates it; aerial walking shot (parallax); optional `feet-sequence` as a "model the way" motif. → About/Collective. **("Fieldwork becomes adventure" belongs to §9, not here — talent is a separate track, D8.)** | Bold beat |
| 9 | **Talent nudge** | Small, quiet, **yellow accent.** This is where **"fieldwork becomes adventure"** lives. "Join the collective" → Careers. Deliberately off the primary CTA. | Whisper |
| 10 | **Contact + footer** | The one heavy-**navy** moment (earns it at the base). Yellow CTA, connector-bar echo, three-job footer (Navigate / Contact block / Identity strip — IA §4). Placeholder contact details. | Resolve |

Silhouette/bold beats land at **1-adjacent → 4 → 8**; **LARP (5) contrasts against R&A (4)** so the two service sections don't merge; 2/3/6/7 keep the premium editorial air. (Ten sections now — IA §7's single "two service lines" block is presented as two separate sections here; a Phase 4 layout choice, D10 preserved via relative weight.)

---

## 7A. Copy deck (content source: Phase 3 wireframe)

The wireframe is the source of truth for copy and content hierarchy; the prototype reuses this text (layout/aesthetics come from this brief, not the wireframe). Placeholders stay placeholders.

- **Header:** MEDIA MODEL · "Research collective · since 2001". Nav: Services · Our Work · About · Partners · Contact · [Careers] · Search · EN / HY.
- **1 Hero:** kicker *"Since 2001 · Yerevan, Armenia"* · H1 **"We know Armenia."** · lead *"And that makes us a trusted partner for complex decisions — research, evaluation and land work, grounded in two decades of nationwide fieldwork."* · CTA *"Discuss a project"* + *"Explore our work"* · caption *"The premise — We study it, measure it, and help it move forward — its people, markets, institutions and land."*
- **2 Premise + proof:** *"One of Armenia's first research & advisory firms — a collective, not a fixed team, assembling the right expertise for each challenge."* + *"Since 2001 we've helped public institutions, private organizations and international agencies turn local knowledge into decisions…"* + *"From public opinion through to full-cycle land acquisition and resettlement, we cover ground few competitors can."* · tags: Sociologists · Economists · Statisticians · Legal specialists · Field teams.
- **3 Credibility:** "By the numbers" — **25+** years, since 2001 · **150+** projects delivered · **30+** experts in the network · **Nationwide** coverage across Armenia.
- **4 Research & Advisory:** *"Understand people, systems and change — data into insight, insight into action."* Sub-services: Social & Public Opinion · Market & Consumer · Monitoring, Evaluation & Impact · Policy Analysis & Advisory.
- **5 LARP:** badge *"Rare capability"* — *"Full-cycle LARP implementation on national infrastructure — legal, cadastral and stakeholder work, to RA law and international standards."* Key Areas of Work (consolidated). → LARP page.
- **6 Featured work:** lead **Regional Justice Survey, Armenia** — World Bank · Ipsos · 2019–2020 · Mixed methods · ~3,000 interviews. Then: Citizen / Population Survey (OECD · 2025 · CAPI · 900) · North–South Road Corridor — LARP (Gov. of Armenia · ADB · 2018–ongoing) · UNICEF E-Card Assistance — PDM (UNICEF Armenia · 2025 · phone survey). Link: *"All 150+ projects."* (Illustrative placeholders — rotating CMS slot, D9.)
- **7 Who we work with:** **"Trusted by the institutions that vet local partners."** Logos: World Bank · UNICEF · OECD · EU · Council of Europe · EBRD · ADB · UNHCR · Millennium Challenge Corp. · Save the Children · OSCE · Ameriabank · Ipsos → Partners.
- **8 The collective:** kicker "The model" · **"A collective, not a fixed team."** · *"We assemble the right specialists for each challenge — giving agility without sacrificing depth. Two decades of nationwide fieldwork sit behind every engagement."* · CTA "Meet the collective".
- **9 Talent nudge:** kicker "Work with us" · *"Researchers, analysts and early-career field staff — fieldwork becomes adventure."* · "Join the collective".
- **10 Contact:** **"Let's discuss your project in Armenia."** · *"A project enquiry, an RFP invitation, or an exploratory conversation — we'll respond quickly."* · form: Name · Organization · Project type (Research & Advisory / LARP, routes team) · Message · "Send enquiry".
- **Footer:** Navigate (full sitemap) · Contact (placeholder address/phone/email + mediamodel.am) · Identity (MEDIA MODEL · "Research collective · since 2001" · EN/HY) · © 2026 Media Model.

---

## 7C. Signature verbal assets — placement & discipline

The campaign's verbal palette (Design Concept §1). These are **accents at the frame**, rendered in Arvo; the Sora workhorse voice carries the substance. **Palette, not all at once** — don't wallpaper "We know Armenia," and treat the two extensions as *alternates*, one per placement.

| Phrase | Where it lands | Register |
|--------|----------------|----------|
| **"We know Armenia."** | Hero H1 (the portal payoff) | Core |
| **"We know Armenia — we study it, measure it, and help it move forward."** | Hero supporting line / §2 premise — the *rigorous* extension (substance) | Frame → proof |
| **"We know Armenia — its warmth, its will, its way forward."** | One evocative moment only — §8 collective opener (or hero caption). The *warm* extension. Never stacked with the rigorous one. | Evocative |
| **"Model the Way"** | §8 the collective (the model/differentiator) and as the quiet label for the drawn line-geometry / "geometric rhythm" motif | Big brand idea |
| **"Fieldwork becomes adventure"** | §9 talent nudge (already placed) | Talent |
| **"Start Your Discovery Journey"** | Hero **scroll cue** into the portal-zoom (replaces the wireframe's plain "Scroll — the proof is one click away") | Evocative CTA |
| **"Discover the vision at — mediamodel.am"** | Footer / contact sign-off — echoes the campaign frames' closing line | Sign-off |

**CTA discipline (protect the macro-conversion, D3):** the hard primary CTA stays **"Discuss a project."** "Start Your Discovery Journey" and "Discover the vision at mediamodel.am" are *softer, evocative* cues — scroll prompt and sign-off — and must **not** replace the enquiry CTA. Evocative to pull attention; the rigorous CTA converts it.

---

## 7B. What we deliberately do NOT inherit from the wireframe

The wireframe drives copy/structure only. These wireframe traits are overridden by this brief:

- Placeholder accent blue `#2b3576` → brand navy `#0f2873`; neutral paper `#f5f4f1` → `#f4f4f4`.
- Its total absence of yellow → **yellow is load-bearing** here.
- `system-ui` type → **Arvo / Sora**.
- The 5/7 split-column hero → **portal-zoom hero overrides it**.
- The flat dark `#1a1a1a` footer → **brand navy**.
- Phase-3 wireframe chrome (the "Show IA notes" toggle, dashed section outlines, "Phase 3 wireframe" badge) → **dropped**; this is a client-facing hi-fi prototype.

---

## 8. Global shell

- **Slim fixed side-rails** (Wittig-style): logo top-left, primary nav, EN/HY switcher **stubbed** (present in markup, inactive — IA §9).
- **Primary nav** per IA §4: Home (logo) · Services · Our Work · About · Partners · Contact, with Careers set visually apart and a demoted Search icon. Services and Our Work carry dropdowns (IA §4).
- **Connector bar + drawn line geometry** as connective tissue between bands.
- Generous, consistent margins; asymmetric grid throughout.

---

## 9. Photography

- **Full-color, art-directed** — the real Armenian landscape/fieldwork imagery supplies the human warmth the strategy calls for; no duotone flattening.
- Sources in `photos/`: `We know Armenia` (hero/landscape), `Fieldwork Becomes Adventure` (§7), `Model the way`, `Research Collective`.
- Heavy image set — optimize; descriptive alt text (SEO hook per IA §8.5).

---

## 10. Build constraints

- **One self-contained HTML file** — all CSS/JS inline; only Google Fonts pulled via `<link>`. Output to `media-model-client-deliverables/homepage-prototype.html` for easy sharing.
- **Accessibility:** `prefers-reduced-motion` fallback on every animated gesture; no-JS resolves to full static content; keyboard-reachable; descriptive alt text.
- **Content = placeholders where IA says so:** 3–5 representative featured projects, placeholder contact details (IA P4/D9). Dummy links throughout.
- **Grid:** inherit the Phase 3 asymmetric editorial grid — no single-column stacks, no uniform 3-up icon-card grids.
- Responsive, mobile-first.

## 11. Guardrails — what to avoid

- Underusing yellow (the #1 temptation) — keep it load-bearing.
- AI-slop patterns: uniform 3-up icon cards, centered single-column stacks, generic gradient hero.
- Scroll-jacking that traps the user; bouncy/novelty motion.
- Letting warmth read as fluff on the substance sections; letting the page go flat navy/white/black.

---

## 12. Assets on hand

- **Brand SVGs** (`brand-assets-svg/`): `logo.svg`, `armenia-map-a.svg`, `eternity.svg`, `graph a/b/c.svg`, `infographic a/b.svg`, `feet-sequence/`.
- **Photos** (`photos/`): four themed sets (above).
- **Inspiration** (`inspiration-layouts/`): campaign frames (212926/212934/213031/213024) + editorial web refs (141151/141313) + the portal-zoom scroll reference (aerodynamics.nl).
- **Colors:** `colors-main.png`, `colors-shades.png`. Full brand system in `media model_Brand Guide line.pdf`.

---

*Locked micro-decisions: silhouette hover-reveal is in (§4/§7); stat band fades, no count-ups; Arvo titles / Sora body; yellow load-bearing; single self-contained HTML into `media-model-client-deliverables/`. Awaiting green light to build.*
