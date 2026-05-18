# larspersson.com — Content & Build Spec

**For Claude Code.** Build target: a copy of the `Julia.github.io` template repo (template box is checked — use "Use this template", clean copy, no fork). The site is a single static `index.html` (Jekyll / GitHub Pages, no framework — do NOT introduce Next.js). Job: swap content and accent colour, keep the design system identical.

When in doubt, match Julia's `index.html` exactly. Only deviate where this file specifies.

---

## Decisions (locked)

- **Accent:** deep slate blue `#1e3a52`
- **LinkedIn:** https://www.linkedin.com/in/larsolovpersson-it-director/
- **Footer location:** Copenhagen, Denmark · Trelleborg, Sweden
- **Press email:** lars@larspersson.com
- **Logos available:** Scita, FlexIT, Green Frog — all three cards are logo'd (like Julia's Scita/WH2040 cards).
- **Press link:** OMIT it. Julia's hero has a top-right "Press kit →" link to `/press/`. Lars has no `/press` page yet — remove the link entirely, do not leave a dead one. Also delete `press.html` from the copied repo.

## Accent colour sweep — not a single variable

Julia's file hardcodes her teal in ~9 places. Replace ALL of them, or the slate blue will be inconsistent:

| What | Julia (teal) | Lars (slate blue) |
|---|---|---|
| `--accent` | `#0f766e` | `#1e3a52` |
| `--accent-light` | `rgba(15,118,110,0.08)` | `rgba(30,58,82,0.08)` |
| `.hero::before` gradient | `rgba(15,118,110,0.12)` | `rgba(30,58,82,0.12)` |
| `.hero-photo` bg + inset shadow | `rgba(15,118,110,0.06/0.02/0.08)` | `rgba(30,58,82,0.06/0.02/0.08)` |
| `.credential-note` colour | `#3d9690` | `#3a5a72` |
| `.links a.primary:hover` | `#0d6b63` | `#14283a` |
| `.links a.secondary:hover` | `rgba(15,118,110,0.15)` | `rgba(30,58,82,0.15)` |
| `.connect-card:hover` | `rgba(15,118,110,0.15)` | `rgba(30,58,82,0.15)` |
| `<meta name="theme-color">` | `#0f766e` | `#1e3a52` |

Leave the amber `.stat` badge (`#fdf6e3` / `#92400e`) as-is — it's a deliberate second accent and works fine against slate.

## Assets needed (Lars provides)

- Header photo — portrait, ~4:5 crop (Julia's is 1121×1403). Goes in `/images/`.
- Three logo files (Scita, FlexIT, Green Frog) in `/images/`.
- Favicon — slate-blue "LP" monogram, `.svg` + `.ico` in `/assets/`.
- Update `CNAME` to `larspersson.com`.
- Rewrite the JSON-LD Person schema for Lars (jobTitle, worksFor = Scita/FlexIT/Green Frog, address, sameAs, alumniOf = Lund University). Rewrite OG/Twitter meta. Keep `llms.txt` / `robots.txt`, update contents.

---

## SECTION 1 — Header

**Name:** Lars Persson

**Role / subtitle line:** Technical co-founder, Scita Health

**Positioning (pitch):** Building compliant, sovereign health data infrastructure across Sweden, Denmark, and the EU — designed for the regulatory path ahead. 25+ years in healthcare and enterprise IT.

**Pull quote (the `.why` italic block):** "Every decision has to be explainable, governable, and auditable."

**Link badges:** scita.health (primary) · flexit.tech · greenfrog.beer · LinkedIn · Email

---

## SECTION 2 — Building Now (three logo'd cards)

### Card 1 — Scita Health
**Role line:** Technical co-founder · Founding architect · Jul 2024 – Present

I'm not a software developer. I'm the one who makes sure the system holds together — technically, operationally, and regulatorily.

At Scita I designed the technical infrastructure for an AI-powered precision prevention platform for women navigating perimenopause and menopause. The AI layer is the core of it: a retrieval-grounded system that turns clinical evidence into personalised, explainable guidance — built so every output can be traced to a source and reviewed, never a black box. I built it on modern composable tools, architected from the start for the regulatory path ahead: intended as a Class IIb medical device under MDR, aligned with the EUDI Wallet for citizen-controlled health data, with AI governance built in rather than retrofitted.

Twenty-five years in regulated healthcare IT taught me what breaks at scale. The discipline is the same: every decision explainable, governable, auditable.

**Badges:** Xano · Claude API · n8n · Pinecone · RAG

### Card 2 — FlexIT
**Role line:** Founder · Active

Enterprise IT wisdom meets AI-era building. Advisory work for health and life-sciences ventures facing post-merger tech integration, AI readiness in regulated environments, compliance architecture (GDPR, MDR, ISO), and interim technical leadership through transitions. Also where I publish Field Notes — what I'm learning building with AI as a non-traditional developer.

**Badges:** Consulting · Advisory · GDPR · MDR · ISO · Field Notes

### Card 3 — Green Frog Brewery
**Role line:** Founder & Brewer · Trelleborg, Sweden

A small-batch craft brewery in Skåne. 13 varieties hand-brewed in 23-litre batches on Grainfather equipment — from classic pilsner and stout to an unusual low- and non-alcoholic line. Beer for special occasions that doesn't trade enjoyment for wellbeing. The same craft instinct that shapes everything else.

**Badges:** Hantverksöl · 13 varieties · NA/LA line · Bryggkurser

---

## SECTION 3 — Where I Stand

*Net-new section — not in Julia's template. Build fresh: full-width, single column, prose-led, NO card chrome. Quieter than the Building Now cards. Restrained.*

**Header:** Driving with Blågula Bilen

Since Russia invaded Ukraine in February 2022, I've volunteered with Blågula Bilen — a Swedish non-partisan, non-religious organisation founded by Take Aanstoot. Volunteers buy used 4×4s and trucks, fix them, fill them with equipment and medical supplies, and drive them to Ukraine, where both the vehicles and the cargo are donated to Ukrainian defence forces and civilian populations. As of early 2026, the organisation has delivered more than 1,400 vehicles.

Smart, proactive support for Ukraine is also smart, proactive defence for Scandinavia. Sovereign infrastructure, compliance, and resilience aren't abstractions — they're what holds when things break. The same instinct shapes the work at Scita and FlexIT.

**Inline link:** blagulabilen.se — about, donate, volunteer

**Ukrainian additions (Lars-specific, beyond Julia's template):**
- Inline Ukrainian flag SVG next to the heading
- Bicolour blue/yellow left stripe on the heading
- Italic Cyrillic subtitle under the heading: «Синьо-жовта машина» — the blue-and-yellow car
- Closing flag-coloured tribute card: "Слава Україні! Героям слава!"
- All Cyrillic text marked `lang="uk"`

---

## SECTION 4 — Track Record

**Framing line:**
25+ years in enterprise IT across healthcare, medtech, and manufacturing — post-merger integrations that can't fail, compliance frameworks that survive audits, legacy modernisation without burning down the house. The unsexy work that breaks at 3am.

**Roles** (same layout as Julia's Track Record: company + dates on the title row, one highlight line with the metric in `<strong>`):

- **European Life Care Group** — Interim CIO · 2023–2024 — Built the IT strategy behind expansion across **five European countries**; reported directly to CEO and board.
- **Occlutech** — IT Director · 2018–2022 — Standardised IT across international medical-device sites for a **40% efficiency gain**; migrated infrastructure to cloud at **99.9% uptime**. Management team member.
- **Attendo** — Deputy Head of IT · 2016–2018 — Ran Nordic IT governance across Sweden, Norway and Denmark — **14,000+ users** on standardised service delivery.
- **Icopal** — CIO · 2005–2014 — ERP transformation delivering **30% efficiency gain** and **25% cost reduction**; scaled IT across international sites.
- **Earlier** · 1994–2005 — CIO, Arjo (medtech) — 40% process automation. IT Manager, Lafarge Braas (manufacturing) — Nordic ERP implementation.

**Competency line (bottom):**
GDPR · MDR · ISO · Post-merger integration · Compliance architecture · AI-era building

*Note: Scita and FlexIT do NOT appear here — they're current and live in Building Now.*

---

## SECTION 5 — Connect (cards in Julia's "Connect" style)

### Card 1 — FlexIT
**Title:** Consulting & Field Notes
**Description:** Enterprise-grade systems in the AI era. Part professional practice, part public learning.
**Link:** flexit.tech · **Email:** lars@flexit.tech

### Card 2 — Green Frog Brewery
**Title:** Hantverksöl from Trelleborg
**Description:** Craft beer brewed in small batches with care. Same instinct, different domain.
**Link:** greenfrog.beer · **Email:** lars@greenfrog.beer

### Card 3 — Scita Health
**Title:** Precision prevention for women
**Description:** Technical co-founder.
**Link:** scita.health

**Direct email line below the cards:**
lars@flexit.tech

**Details block (optional — Julia has the equivalent):**
- **Education:** BSc Information Technology, Lund University
- **Certifications:** ITIL Foundation · AWS Cloud Practitioner · Certified Scrum Master · MIT Digital Transformation & AI · UGL
- **Languages:** Swedish (native) · English (fluent) · Danish (conversational)

---

## SECTION 6 — Footer

Copenhagen, Denmark · Trelleborg, Sweden · larspersson.com · References on request

---

## Out of scope for Claude Code (Lars does these in dashboards)

- DNS at Namecheap (A records → host)
- larspersson.eu → .com redirect via Cloudflare (currently handled by Vercel-native 308)
- SPF / DKIM / DMARC records (DKIM key generated in the email provider's admin console — confirm provider before copying the WH2040 template)
- lars@larspersson.com email forwarding
- Final voice pass on all copy (the above is a strong draft — Lars sharpens it)
