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
- Pages: `lp-weight-management/` (mobile-first, desktop two-column layer at 960px+).
  Current version: v0.7. Preview build: `preview/lp-weight-management-v0.7-preview.html`.
  v0.7 (content only, graphics pass later): "Get the base right" section after the approach (sleep / food and
  water / movement, daily additions, "treatment is a multiplier", 8-item readiness check); "What we check, in order"
  between doctors and programmes (body composition -> thyroid -> insulin resistance -> safety screening, plus
  where each result leads); review step = 1-month trial, weekly inches, monthly body comp; FAQs on inches vs kilos
  and after the goal; chat asks which basics are in place and names the missing ones.
  v0.6: NO section menu anywhere (rail and phone strip removed, per Rish). Chat is conversational: greetings,
  thanks, yes/no, "who are you", typed answers to the current question (e.g. "about 3 years"), Hinglish
  ("vajan kam nahi ho raha"), one-letter and swapped-letter typos, and a helpful fallback instead of a dead end.
  v0.5 adds: guided chat flow (ALIV team voice): concern -> how long -> what tried -> signs -> safety check
  (pregnancy, under 18, eating disorder) -> "worth checking" list -> tests + Listen. Plan. Review. -> doubts
  (injections, IV, diet, time, cost, clinics) -> hand-off: prefilled form (interest + hidden chat_summary) or
  WhatsApp with answers. Never asks name/phone, never shows a fee, never names drugs. Free text works at any step.
  Analytics events: chat_open, chat_concern, chat_reflect, chat_book, chat_whatsapp (gtag + fbq trackCustom).
  v0.4 adds: left section rail on wide screens (no button; fully transparent, names turn white over dark sections; current section in red #C8102E), chip strip under the
  top bar on phones; clinic gallery in About ALIV (lounge photo + Pune/Mumbai photo slots to fill);
  Safety and FAQ headings no longer sticky; research charts animate in (bars + numbers from 0, line flows from 0%).
  v0.3 adds: evidence text inline (no "More"), liquid-glass research cards, approach pyramid (labels inside,
  explanations right), structured programme cards (type, level, best for), "Listen. Plan. Review." illustrated
  story (doctor nods), and a guided weight-management chat assistant (rule-based; AI backend hook in code).

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

## Page rules from Rish (Nov 2026)
- Say "weight management", never "fat loss" (body-fat physiology wording is fine).
- Hero = the problem only. No ALIV mention, no booking button. Sell later in the page.
- Order: problem → evidence → research → approach → base (lifestyle) → safety → About ALIV (credentials + press)
  → doctors → what we check → programmes → how it works → FAQ → form → references → footer.
- Sticky side headings on desktop (not Safety or FAQ). No section menu of any kind on the page.
- Sticky Book bar appears only from the About ALIV section.
- Logos: img/logo/aliv-green.webp (light bg), aliv-white.webp (dark bg), aliv-blue.webp (spare).
- "How it works" mantra to keep across materials: Listen. Plan. Review.
- Two versions: v1 = static infographics (`<html data-motion="off">`); v2 = advanced animated (data-motion="on" + plugins).

## ALIV weight-management protocol (from the pre-consultation video, Nov 2026)
- Base of the pyramid: sleep 7-8 h, screens off 1 h before bed; water 3-4 L; protein >= 1 g/kg goal weight;
  meal order protein+fibre -> fats -> carbs; high-GI foods only at end of meals; 10-11 h eating window (9am-7pm),
  nuts/seeds between; morning water with moringa/cinnamon/turmeric; zone 2 incline walking 30-45 -> 60-75 min
  in one go + dead bugs; strength trainers judged on inches.
- Checks: body composition (BMI, fat vs muscle, visceral vs subcutaneous), thyroid (fix first; recheck 6 weeks;
  every 6-9 months with family history), insulin resistance (often missed), safety screening before medication.
- Process: 1-month trial (4-5 weekly sessions), inches weekly, body comp monthly, monthly review; goal 70-80%
  with support, then maintenance top-ups. "Treatment is a multiplier: x zero effort = zero." Inches over kilos.
- Kept OFF the page: drug names and doses, "3-5 kg a month", claims about pharma companies, microdosing organ
  benefits, "IV burns/flushes fat".

## Visual system (lp-weight-management)
- Scroll-triggered, once-only motion; all off under prefers-reduced-motion. No JS libraries.
- Components: live biomarker panel (hero), count-up credentials, press marquee, BMI cut-off infographic,
  animated trial bar/line charts (dark band), layered approach stack, programme cards, step progress line, team grid.

## Speed rules for every LP
- Self-host brand fonts in the LP folder (alivtherapy.in fonts send no CORS headers, so they break on other domains).
  Preload both woff2 files. No Google Fonts.
- Preload the hero image (small version under 700px, full version above). Team/inline images max 480px wide, WebP q~74.
- Clarity and the Meta Pixel library load after the page `load` event; gtag stays async. fbq calls queue, so nothing is lost.
- Animate only transform/opacity; pause infinite animations off-screen; respect prefers-reduced-motion.
- Baseline (Nov 2026, weight-management LP): ~140 KB first load on mobile, ~200 KB after a full scroll, CLS 0.

## Compliance rules for copy
- Every clinical claim gets a citation and an evidence label. No guarantees, no before/after.
- Never name or promote prescription drugs in copy (Indian ad rules + Meta/Google policy);
  medication = "doctor decides after assessment".
- No body-shaming / negative self-image hooks in weight-loss copy (Meta policy).

## Open items
- Clinic photos needed: Pune + Mumbai (reception, consultation room, body composition scan, exterior; Mumbai lounge).
  Confirm which city the infusion-lounge photo is from.
- WhatsApp number for chat hand-off: Rish to confirm (single constant WA_NUMBER in the chat script).
- Form backend must accept the new hidden field `chat_summary`.
- "Medically reviewed by [DOCTOR NAME]" placeholder on NAD+ and fat-loss pages.
- Confirm WhatsApp number = +91 77199 88811; founding year 2015 vs 2016.
