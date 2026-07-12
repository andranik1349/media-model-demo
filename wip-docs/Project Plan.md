# Media Model Website — Project Plan

Working document that tracks the redesign of the Media Model website, from strategy through a high-fidelity homepage prototype. This is the master tracker; each phase produces its own standalone deliverable (see *Deliverables* below).

## Context

We were handed a document titled *Site structure (EN).md* that presents itself as a definitive brief. It is not. It mixes a rough sitemap, finished-sounding marketing copy, and a strong but unstructured project portfolio, and it is light on strategy and near-silent on SEO. It has real gaps (conflated pages, inconsistent service naming, placeholder contacts) and, more importantly, never establishes who the site is for or what it is trying to achieve. We are treating it as raw material, not a spec.

**Scope decisions (locked):**

- **Language:** English only for this engagement. The bilingual (ARM/ENG) question is set aside.
- **Deliverables:** One standalone document per phase. This plan stays lean and links out.
- **Primary audience:** International development organizations & donors (decided in Phase 1). Domestic private sector and government are secondary; talent is a distinct track.
- **Tone:** Balanced blend — human/evocative at the frame, rigorous/precise in the substance (decided in Phase 1).

**Core premise (locked — do not relitigate):**

> We know Armenia — its people, markets, institutions, and land realities — making us a trusted partner for complex decisions.

Everything downstream should ladder up to this. Strategy, IA, and copy can reshape *how* it's expressed, but the premise itself stays intact.

## Phases

### Phase 1 — Design Concept Doc
Establish the strategic foundation the original brief lacks: target audience(s) and their priorities, the site's mission and the primary action it should drive, positioning, and tone of voice. Grounded in the core premise and informed by the brand materials being shared alongside the brief.

- **Inputs:** Original brief, brand materials (Brand Guideline v1.0, Visual Concept Presentation, colors, SVG assets), core premise.
- **Output:** `Design Concept.md`
- **Status:** ✅ Complete & **approved by client** (2026-07-10). Audience and tone decided; positioning, mission, messaging, and voice defined; decisions log started for the Phase 4 proposal.

### Phase 2 — Sitemap & Information Architecture (with SEO)
Turn the concept into a proper IA: page hierarchy, navigation, URL structure, and page-level intent. Bring SEO in as a first-class concern — search intent, keyword/topic mapping, metadata approach, internal linking — since the current brief has almost none. Resolve the known structural problems (nav vs. content mismatches, conflated For Individuals / For Companies, service-name inconsistencies, what Insights and Partners actually require). Carry forward the open questions from the concept doc §8 (portfolio presentation, LARP prominence, Insights placement).

- **Inputs:** Phase 1 concept doc, original brief structure, portfolio content.
- **Output:** `Information Architecture.md`
- **Status:** ✅ Complete & **approved by client (2026-07-11)**. Full sitemap, nav, URL scheme, page-by-page IA, and SEO-ready foundations (structure only — not a keyword strategy; a future SEO team takes over) delivered. Original-brief problems audited (P1–P8) and each resolved. Carried-forward open questions decided: portfolio → top-level *Our Work* with featured tier + filters (D9); LARP → co-equal but not homepage-dominant (D10); Insights → reserved, out of nav (D11). Decisions log extended D7–D16 for the proposal deck. Five client review rounds incorporated (placeholder contacts, SEO-readiness-only scope, standalone Partners, rotating featured tier, two project-page templates, EN-at-root URL scheme); final consistency pass done. Phase 3 unblocked.

### Phase 3 — Homepage Structure & Wireframe
Develop a detailed section-by-section homepage wireframe. Take the original homepage content as the starting point, then augment and tweak it based on Phase 1 (audience, mission, tone) and Phase 2 (IA, SEO). Defines content blocks, hierarchy, and calls to action — structure and copy intent, not visual design. Phase 2 §7 already proposes a homepage block sequence to pressure-test.

- **Inputs:** Phases 1–2, original homepage copy.
- **Output:** `homepage-wireframe.html` — an **interactive** low-fidelity wireframe (client preference), superseding the planned static `Homepage Wireframe.md`. Structure & copy intent only; IA rationale embedded as a toggle-able "Show IA notes" overlay instead of a separate spec doc.
- **Status:** ✅ Complete & **approved by client (2026-07-11)**. Nine-section homepage per IA §7, built on a **bold asymmetric editorial grid** (unequal 2–3 column spreads, staggered offsets — deliberately avoiding single-column stacks and uniform 3-up icon-card grids so Phase 4 inherits the bones). Minimal styling (grayscale + one functional accent; visuals are Phase 4). Real hover/interaction, dummy links, IA-annotation overlay. Cross-referenced against `Information Architecture.md` — nav, dropdowns, canonical service names, section order, featured projects, and D8/D9/D10/P4 rationale all consistent; one fix applied (credibility band's unsourced "11 regions" → "Nationwide", matching IA §7). Phase 4 unblocked.

### Phase 4 — Visual Discovery, Prototype & Client Proposal
Two deliverables that ship together at the end of the engagement.

First, focused visuals-and-aesthetics discovery (look, feel, references, informed by brand materials), then a high-fidelity HTML prototype of the homepage based on the Phase 3 wireframe.

Second, a **client-facing redesign proposal deck** that distills the whole workflow into a single presentation — the narrative that shows the client we reshaped their brief through a deliberate process, not on a whim. It walks through: strengths of the original doc; weak areas of the original doc; what came out of discovery (Phase 1); the new IA (Phase 2) with a rationale for each change and addition traced back to Phase 1 findings; and a segue/link into the high-fidelity prototype as the payoff.

- **Inputs:** Phases 1–3, brand/visual materials, original brief (for the before/after contrast).
- **Outputs:** Visual direction notes (`Visual Design Brief.md`) + `media-model-client-deliverables/homepage-prototype.html`; redesign proposal deck (`Redesign Proposal.pptx`).
- **Status:** 🔶 In progress. **Visual discovery + hi-fi prototype ✅ done** — `Visual Design Brief.md` (visual direction) and `media-model-client-deliverables/homepage-prototype.html` delivered. **Redesign proposal deck: plan ✅ complete & approved (2026-07-12)** — `Redesign Proposal — Deck Plan.md`; **build ⬜ pending** (dedicated session). Deck is a self-contained HTML file (discrete keyboard-nav slides), ~20–24 slides, before→why→after→proof arc; weaves the client-seen `v-0-examples/` v0 as the concrete "before"; builds with high-end-visual-design + theme-factory + design-taste-frontend + canvas-design.

## Deliverables

| Phase | Deliverable | Status |
|-------|-------------|--------|
| — | `Project Plan.md` (this doc) | ✅ In progress / living |
| 1 | `Design Concept.md` | ✅ Approved |
| 2 | `Information Architecture.md` | ✅ Approved |
| 3 | `homepage-wireframe.html` (interactive) | ✅ Approved |
| 4 | `Visual Design Brief.md` (visual direction) | ✅ Delivered |
| 4 | `homepage-prototype.html` (hi-fi) | ✅ Delivered |
| 4 | Redesign proposal deck (`Redesign Proposal.pptx`) | ⬜ Not started |

## Open questions / to resolve

- ~~**Brand materials**~~ — received and reviewed (Brand Guideline v1.0, Visual Concept Presentation, colors, SVG assets, inspiration layouts, photos). ✅
- ~~**Primary audience priority**~~ — decided in Phase 1: international orgs/donors primary. ✅
- ~~**Portfolio presentation**~~ — resolved in Phase 2 (D9): top-level *Our Work* with a curated featured tier + a filterable index (sector / client type / method). Client's proposed direction validated and specified. ✅
- ~~**LARP prominence**~~ — resolved in Phase 2 (D10): co-equal service line with its own page and portfolio filter, discoverable but not homepage-dominant. ✅
- ~~**SEO mapping**~~ — Phase 2 §8 lays SEO-*ready foundations* (clean URLs/slugs, one-topic-per-page, metadata slots, crawlable internal linking, technical hooks). Deliberately **not** a keyword strategy — that's a future SEO team's job; the goal is a structure they can build on without restructuring. ✅
- **Resolved by client (2026-07-11) — all Phase 2 open questions now closed:** contact details → placeholders through design (P4); *Partners* → kept a **standalone page** (not folded), room for SEO content later, fork **excluded from the Phase 4 proposal deck** (D14); featured-project selection → out of scope (rotating CMS/content decision; prototype uses 3–5 representative projects only); project-detail depth → out of scope — Phase 2 supplies **two project-page templates** (full case study + one-pager/article, D16), per-project assignment is a content decision; URL prefix → **English at root (no prefix), other languages under `/{lang}/`** (e.g. `/hy/`). Only Phase-3-facing item left is homepage section order, which Phase 3 handles by design.

## Progress log

- **2026-07-10** — Plan created. Scope locked (EN only, per-phase deliverables). Core premise agreed. Awaiting brand materials to begin Phase 1.
- **2026-07-10** — Added Phase 4 client-facing redesign proposal deck as a second deliverable.
- **2026-07-10** — Brand materials located in project folder. **Phase 1 complete:** `Design Concept.md` delivered. Decided primary audience (international orgs/donors) and tone (balanced blend); defined mission, positioning, value pillars, voice, and messaging hierarchy; started decisions log for the Phase 4 proposal. Phase 2 (IA + SEO) unblocked.
- **2026-07-10** — Client review on Phase 1: portfolio direction (featured sections + tags/filters) and the three characteristic inspiration layouts logged for later phases. **Phase 1 approved.** Next: Phase 2 (IA + SEO), to run in a fresh session.
- **2026-07-11** — **Phase 2 delivered:** `Information Architecture.md`. Audited original brief (8 structural problems, P1–P8) as the before/after basis for the proposal deck. New sitemap, 6-item primary nav, canonical URL scheme, canonical service taxonomy (fixes naming inconsistency), and page-by-page IA. SEO-ready foundations added from scratch (clean URLs, one-topic-per-page, metadata slots, internal-linking structure, technical hooks) — scoped as foundations for a future SEO team, not a keyword strategy. Resolved carried-forward open questions (portfolio D9, LARP D10, Insights D11) and extended the decisions log.
- **2026-07-11** — **Phase 3 copy pass:** restored the Design Concept §5 verbal assets that had thinned out of the wireframe, placed as *accents at the frames* (concept's "accents, not wallpaper" rule): "We know Armenia / we study it, measure it…" (hero), "Start Your Discovery Journey" (hero soft CTA — "Discuss a project" stays the primary hard CTA), "Model the Way" (collective), "fieldwork becomes adventure" (talent), "its warmth, its will, its way forward" (contact), "Discover the vision at mediamodel.am" (footer). No structural/IA change.
- **2026-07-11** — **Phase 3 complete & approved:** `homepage-wireframe.html` — interactive low-fi homepage wireframe (client asked for interactive over a static `.md`). Nine sections per IA §7 on an asymmetric editorial grid (unequal columns, staggered offsets, no uniform card grids), minimal styling, hover interactions, dummy links, and a toggle-able IA-notes overlay tying each section to its decision. Deliverable name changed from `Homepage Wireframe.md`. Cross-referenced against the IA doc — consistent; fixed one unsourced stat ("11 regions" → "Nationwide"). **Phase 4 unblocked** (visual discovery + hi-fi prototype, and the client proposal deck).
- **2026-07-11** — **Phase 2 review & approval.** Five client review rounds incorporated: contact details → placeholders (P4); SEO → readiness-only scope, not a strategy (D15); *Partners* → standalone page kept, excluded from the Phase 4 deck (D14); featured projects → rotating CMS slot, out of scope (D9); project detail → two page templates, per-project assignment out of scope (D16); URL prefix → EN at root, other languages under `/{lang}/`. Ran a final internal-consistency pass (fixed a P3→decision cross-ref, harmonized Partners/Impact roster wording). Decisions log now D7–D16. **Phase 2 approved.** Phase 3 (Homepage Wireframe) unblocked; only open item is the build-time EN-prefix toggle (non-blocking).
- **2026-07-12** — **Phase 4 (part 1) complete: visual discovery + hi-fi prototype delivered.** Visual discovery ran as a discussion → `Visual Design Brief.md` (the visual-direction deliverable): restrained light-editorial canvas carrying bold recurring brand beats; navy/yellow/off-white with **yellow load-bearing**; Arvo titles / Sora body; interaction vocabulary (portal-zoom hero animating the brand's own window-onto-Armenia motif, silhouette-fills-with-photo beat, drawn line-geometry, connector bar, scrub reveal); craft/motion standards filtered from the high-end-visual-design skill (custom easing, IntersectionObserver reveals, transform/opacity-only performance rules); copy deck + verbal-asset placement + guardrails. Brief cross-checked against the wireframe (copy/structure source) and the Design Concept §1 verbal palette. **Homepage layout change:** the two service lines are presented as **two separate full sections** (Research & Advisory §4 leads; LARP §5 its own but more compact/contrasting) rather than the wireframe's cramped 62/38 split — homepage is now 10 sections; **D10 preserved** via relative weight (client steer, 2026-07-12; trace-worthy for the proposal deck's before/after). Built to `media-model-client-deliverables/homepage-prototype.html` (self-contained single HTML). **Remaining Phase 4 deliverable: the redesign proposal deck (`Redesign Proposal.pptx`) — planned for a dedicated session.**
