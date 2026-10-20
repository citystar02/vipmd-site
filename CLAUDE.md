# vipmd-site — VipMD Cardiology website

Live at https://vipmd.com via GitHub Pages (main branch, / root, custom domain + enforced HTTPS).
Deploy = push to main. Changes are live in ~1 minute. CNAME file must never be deleted.

NOTE: This is a PUBLIC repo. Site code only. Never commit strategy documents, pricing,
payer rates, patient data, or internal notes. The full brand strategy doc
(VipMD_Cardiology_Brand_Identity_v3_FINAL.md) lives outside this repo — ask Ty to attach it.

## Stack

Hand-written static HTML, one self-contained file per page (inline CSS/JS, no build step,
no framework). Fonts via Google Fonts. Keep it this way.

## Design tokens (from index.html — reuse exactly)

- Paper `#FDFBF7` (background) · Catalina Navy `#113757` (ink) · Navy Deep `#0C2A43`
- Amaranth `#487b9b` (links/accents) · Heartbeat Coral `#D14B36` / `#B53E2C` (call CTAs ONLY)
- Gold Whisper `#F4EDDF` (tinted bands) · line `#E5DFD3`
- Display: Bricolage Grotesque · Body: Fira Sans, 19px floor (audience is 65+, mobile)
- Signature elements: status strip (top), giant tappable phone number, sticky mobile call bar

## Site facts (single source of truth)

- Name: VipMD Cardiology & Primary Care
- Address: 4000 Physicians Blvd, Bldg E, Ste 101, Bakersfield, CA 93301
- Phone: (661) 327-0807 — the phone call is THE conversion event on every page
- Tagline: "Heart answers without the wait" / ES: "Respuestas para su corazón, sin la espera."

## Copy rules (non-negotiable)

1. Access claim is "most patients seen within the week" — never "48 hours", "1–2 days",
   or "days, not weeks/months" in published copy.
2. Every CTA routes to evaluation ("Call today", "Get seen") — NEVER to a specific test,
   and never "free screening" or any inducement language (Medicare compliance).
3. "No referral needed" appears ONLY inside the insurance-clarity module (see index.html),
   never as a headline or page title.
4. Pair every access promise with the team-care framing (NP seen first, cardiologist reads
   every study) — copy block exists in index.html.
5. No interventional/procedural claims (cath, stents, ablation). No competitor names.
6. Spanish is human-register, local idiom — extend the data-i18n dictionary pattern in
   index.html; every patient-facing page ships EN + ES.
7. One quantified claim allowed on provider page only: patient seen this week / urgent
   findings called same day / written report within 5 business days.

## Phase 1 pages to build (priority order)

1. /getting-seen/ — access page: how it works, what to bring, insurance-clarity module
2. /cardiology-testing/ hub + echocardiogram, stress-testing, nuclear-cardiology,
   vascular-ultrasound, heart-monitoring (resource tone: what it is → what it shows →
   how to prepare → how fast → CTA to evaluation)
3. /patient-resources/ — test prep, forms, what to bring, results timeline
4. /for-providers/ — referral info, the 3-part provider promise, back-line (English only)
5. /es/ mirror of every patient-facing page
6. /our-team/, /insurance-and-payment/, /contact/, /about/

Keep nav consistent with index.html; add real <nav> once interior pages exist.
Each page: own <title>, meta description, canonical, and FAQPage/MedicalClinic JSON-LD
where it fits. Update og:url per page.
