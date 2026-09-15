# Witchard Website — Todo

## Do now (code fixes)
- [x] Add `robots.txt`
- [x] Add `llms.txt`
- [x] Add Open Graph meta tags
- [x] Add canonical tag
- [x] Update schema URL to `witchards.co.uk`
- [x] Add `hasOfferCatalog` to schema

## Needs Joe / Martin
- [x] Connect domain (`witchards.co.uk`) on Spaceship → Vercel
- [x] Set up Google Business Profile (needs verification)
- [x] Add owner name(s) to About section — Joe confirmed 2026-09-12: Bill and Joe Witchard
- [x] Pricing table — not applicable, confirmed dynamic/quoted-by-call only (2026-09-11); site copy already reflects this correctly
- [x] Confirm Facebook + Instagram accounts are live
- [x] Job/van photos: Joe sent real photos 2026-09-15. Garden & Garage Clearance service card now uses a real job photo (clearing rubble into the van, matches the CW Garden Construction review below). About section now uses a real Bill + Joe photo (in the van together) in place of the generic stat-tile grid. Other 5 service-card images left as stock (only had one usable job-in-progress shot; the rest were van/team lifestyle photos not tied to a specific service).
- [ ] **BLOCKED ON JOE** — Facebook link is wrong. Joe flagged 2026-09-15 that the Facebook button "takes me to a small company page" — current href (`facebook.com/groups/.../user/...`) is a link to a user's profile inside a Facebook group, not the actual Witchard Home Clearances Page. Need the real Page URL from Joe (appears in 3 places in `index.html`: schema `sameAs`, contact section Facebook link, footer social icon).

## When reviews come in
- [x] Unhide reviews section + add real reviews — 2 real Facebook reviews added 2026-09-15 (Sally Holmes / Bailey House, CW Garden Construction — credited to company name only, not the individual, per his request). Placeholder Sarah T./James H./Linda M. reviews removed.
- [x] Add `aggregateRating` to schema — added (5.0, reviewCount 2, reflects the two real reviews only)
- [ ] List on Checkatrade / Trustpilot

## Site refresh / upgrade (from 2026-09-11 review)
- [x] Optimize/compress hero + nav logo image — split into separate nav (small) and hero (larger) WebP+JPEG assets in `assets/`, old 107KB Snapchat JPEG no longer referenced in HTML
- [x] Fix `og:image` — now a proper 1200×630 `assets/og-image.jpg` (logo centred on navy background) instead of the cropped wide banner
- [x] Toned down hero entrance animation (removed scale/slide "pop", shortened to a plain fade) — read as more calm/credible for a two-man family business, less "SaaS launch"
- [x] About section + stat tile updated to say father-and-son explicitly, not generic "family team" (owner names still pending — see item above)
- [x] Service card photos — Garden & Garage card now uses a real job photo (see above)
- [x] About section photo — stat-tile grid replaced with a real Bill + Joe photo (see above)
- [x] Page felt too long (Martin's feedback 2026-09-15) — trimmed About from 3 paragraphs to 2, added a collapsible FAQ section (8 Q&As from Joe, `<details>/<summary>`, no JS needed) between How It Works and About to answer common questions without adding permanent scroll weight. FAQPage schema added alongside the existing LocalBusiness schema.

## Done
- [x] Real phone number (07706 559151)
- [x] Real email (witchardhomeclearances@yahoo.com)
- [x] Facebook + Instagram URLs
- [x] Remove contact form → phone/email CTAs
- [x] Step 1 copy updated (no form reference)
- [x] Reviews section hidden
- [x] Opening hours (Mon–Sat 8am–6pm)
- [x] Pricing callout in How It Works
- [x] Logo (Snapchat photo)
- [x] EA Waste Carrier licence (CBDU640764) added
