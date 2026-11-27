# ALIV Marketing — working memory

## Landing pages (`landing-pages/`)
- Template = live page https://www.alivtherapy.in/lp-nad-plus/ (single-file HTML, inline CSS/JS).
- Structure: nav → hero (+disclaimer) → "what is / why" with accordion → evidence-tiered claims
  (Strong / Mixed / Early) → approach/routes → band image → 3 next steps → safety → Why ALIV
  (doctors photo) → enquiry form (name, phone, city, interest) → FAQ → numbered references
  (PubMed-verified) → footer → sticky mobile CTA.
- Brand tokens: forest green #075330 ink, teal #0C544D/#17766B, yellow #F2C200 = only CTA colour,
  blue #1257A8 = links only. Fonts: Avenir Heavy (display), Gordita (body).
- Tracking IDs reused on every LP: Clarity uxteeaz5rs, Google Ads AW-11058315015, Meta Pixel 429598552784651.
- Pages: `lp-fat-loss/` (mobile-first, desktop two-column layer at 960px+).

## Brand facts (from alivtherapy.in, Nov 2026)
- Homepage: "Pioneering Regenerative Medicine & Longevity Since 2016" (therapy pages say "since 2015": unresolved).
- Panel (about-us): Rishi Tandulwadkar (Founder & CEO), Dr Rajesh Tandulwadkar (Gastro Surgeon & Liver Expert),
  Dr Sunita Tandulwadkar (ObGyn & Infertility), Dr Ramesh Bhonde (Scientific Expert), Dr Sattyasheel Naik (Ortho),
  Dr Samta Singhania (ObGyn), Dr Sattyajeet Naik, Dr Labhdy Nirmal (Head & Neck Cancer Surgeon),
  Dr Sonali Dhomane (Infertility), Chandra Venkitaraman (Medical Counselor). Headshots: /assets_web/images/doctor/*.webp
- Press ("As featured on"): Femina, Mid-day, Pune Times, Pune Mirror, BioSpectrum, Sakal, Women Shine, APN News, Dainik.
- Selling points: ICU/paediatric-trained nurses, super-specialised founding doctors, pharma-grade imported ingredients.
- Fat-loss products: Trim & Tone Elixir (IV, L-carnitine + B-complex), FatLoss Max (tirzepatide-based),
  Advanced Metabolic Reset (microdose tirzepatide, NAD+, Tesamorelin; diagnostics HOMA-IR, ApoB, Lp(a), hs-CRP,
  HbA1c, liver enzymes, FibroScan, body composition). Also IV League membership, corporate plans, Gift of Health.

## Visual system (lp-fat-loss)
- Scroll-triggered, once-only motion; all off under prefers-reduced-motion. No JS libraries.
- Components: live biomarker panel (hero), count-up credentials, press marquee, BMI cut-off infographic,
  animated trial bar/line charts (dark band), layered approach stack, programme cards, step progress line, team grid.

## Compliance rules for copy
- Every clinical claim gets a citation and an evidence label. No guarantees, no before/after.
- Never name or promote prescription drugs in copy (Indian ad rules + Meta/Google policy);
  medication = "doctor decides after assessment".
- No body-shaming / negative self-image hooks in weight-loss copy (Meta policy).

## Open items
- "Medically reviewed by [DOCTOR NAME]" placeholder on NAD+ and fat-loss pages.
- Fat-loss page needs img/hero.webp and img/band.jpg; confirm WhatsApp number = +91 77199 88811.
