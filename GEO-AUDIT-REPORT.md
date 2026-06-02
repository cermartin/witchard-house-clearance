# GEO-SEO Audit Report
**Site:** https://witchard.vercel.app  
**Business:** Witchard House Clearance  
**Type:** Local Service — Hampshire, UK  
**Date:** 2 June 2026  

---

## Composite GEO Score: 41 / 100

| Category | Weight | Score | Weighted |
|----------|--------|-------|---------|
| AI Citability & Visibility | 25% | 38/100 | 9.5 |
| Brand Authority Signals | 20% | 20/100 | 4.0 |
| Content Quality & E-E-A-T | 20% | 52/100 | 10.4 |
| Technical Foundations | 15% | 58/100 | 8.7 |
| Structured Data | 10% | 55/100 | 5.5 |
| Platform Optimisation | 10% | 30/100 | 3.0 |
| **TOTAL** | 100% | — | **41.1** |

> Score will increase significantly once domain is live (`witchards.co.uk`) and indexing begins. Current low scores are partly a function of the site being on a Vercel subdomain with no backlink or brand signal history.

---

## 1. AI Citability & Visibility — 38/100

### What AI crawlers see
- **robots.txt:** Not found (404). No explicit allow/disallow rules. AI crawlers (GPTBot, ClaudeBot, PerplexityBot) will default to allowing access — this is fine, but an explicit `robots.txt` is strongly recommended.
- **llms.txt:** Not present. This file is the emerging standard for telling AI models what your site does and what content to prioritise.
- **Sitemap:** Not found. Single-page site so this is less critical, but a sitemap is still good practice.

### Citability assessment
The site has clear, factual, locally-specific content — which is good for AI citation. However:
- No FAQ section. FAQ-format content (Q&A pairs) is heavily cited by AI answer engines.
- No specific named staff/owner (the About section says "family team" but no names). AI models prefer attributable expertise.
- Pricing callout exists ("starts from a few hundred pounds") — good. But no specific price table for bedroom counts, despite this being agreed. This is a missed citability opportunity.
- No `<article>` or `<main>` semantic landmark — the content is in `<section>` tags which is acceptable but not optimal for passage extraction.

### AI crawler access
| Crawler | Status |
|---------|--------|
| GPTBot (OpenAI) | Allowed (no robots.txt restriction) |
| ClaudeBot (Anthropic) | Allowed |
| PerplexityBot | Allowed |
| Google-Extended | Allowed |

### Recommendations (Priority: HIGH)
1. Add `robots.txt` explicitly allowing all AI crawlers
2. Create `llms.txt` at site root (see template below)
3. Add a FAQ section — minimum 5 questions about house clearance in Hampshire
4. Add pricing table (1-bed / 2-bed / 3-bed estimates) — already agreed with client

---

## 2. Brand Authority Signals — 20/100

This is the weakest category and entirely expected for a brand-new business. No brand mentions exist yet on any AI-cited platform.

| Platform | Status |
|----------|--------|
| Google Business Profile | Not verified / not found |
| Facebook | `facebook.com/Witchardhomeclearances` — linked in site, existence unconfirmed |
| Instagram | `instagram.com/Witchardhomeclearances` — linked in site, existence unconfirmed |
| Reddit | No mentions |
| Trustpilot / Which? Trusted Traders | Not listed |
| Checkatrade / MyBuilder | Not listed |
| Wikipedia | Not applicable |

### Recommendations (Priority: HIGH)
1. **Google Business Profile** — single most impactful action for local AI visibility. Free. Required for "near me" queries in Google AIO and Maps.
2. **Trustpilot or Checkatrade** — even 2–3 reviews on a third-party platform dramatically increases AI citation likelihood for local service queries.
3. **Confirm socials exist** — the site links to Facebook/Instagram but it's unclear if the accounts are live. If not, either create them or remove the links.

---

## 3. Content Quality & E-E-A-T — 52/100

### What's good
- Clear service descriptions with specific detail (e.g. "oven cleaning not included")
- Local specificity throughout (New Alresford, Hampshire, named towns)
- Trust signals: EA reg number (CBDU640764), CRB checked, fully insured — all stated
- Sensible pricing context ("starts from a few hundred pounds") — prevents "what does it cost?" bounces
- Probate/estate clearance copy shows sensitivity — appropriate tone for this audience

### What's missing
- **No named person** — "family-run" is stated but no name is given. E-E-A-T (Experience, Expertise, Authoritativeness, Trust) requires a real human. Even just "Bill and Joe Witchard" in the About section would help significantly.
- **No years of experience / founding date** — vague "since day one" doesn't help AI models assess authority
- **No specific job examples** — even one or two sentences like "We recently cleared a 4-bedroom property in Winchester in a single day" signals real operational experience
- **Reviews section hidden** — understandable, but it means there's zero social proof currently visible

### Recommendations (Priority: MEDIUM)
1. Add owner name(s) to the About section
2. Add a founding year or "X years in Hampshire"
3. Add 1–2 short job vignettes to the About section
4. Reinstate reviews section as soon as first real review is collected

---

## 4. Technical Foundations — 58/100

### What's good
- Mobile-responsive layout with sticky CTA on mobile
- `lang="en"` set on `<html>`
- Proper meta description (156 chars — good length)
- Title tag well-optimised: "Witchard House Clearance | Hampshire House Clearance Specialists"
- Inter font loaded via Google Fonts preconnect
- `loading="lazy"` on all service card images
- Security headers: `X-Content-Type-Options: nosniff` present
- Referrer policy set

### Issues
| Issue | Severity |
|-------|----------|
| No `robots.txt` | High |
| No `sitemap.xml` | Medium |
| No `canonical` meta tag | Medium |
| Schema URL still shows `witchard.vercel.app` — needs updating to `witchards.co.uk` | Medium |
| No `og:image` / Open Graph tags | Medium |
| No Twitter Card meta tags | Low |
| Emoji favicon (data URI SVG) — works but not ideal for all browsers | Low |
| Google Fonts external request — minor privacy/performance concern | Low |
| No `<main>` landmark element | Low |

### Recommendations (Priority: MEDIUM)
1. Add `robots.txt` (also fixes AI Citability category)
2. Add canonical tag pointing to the live domain
3. Add Open Graph tags (`og:title`, `og:description`, `og:image`, `og:url`)
4. Update schema JSON-LD `"url"` field when domain goes live

---

## 5. Structured Data — 55/100

### What's present
The site has a `LocalBusiness` JSON-LD schema block. This is well-implemented.

**Good:**
- `@type: LocalBusiness` — correct
- `name`, `description`, `telephone`, `email` — all present and accurate
- `address` with `addressLocality`, `addressRegion`, `addressCountry` — present
- `areaServed` — good list of Hampshire towns
- `openingHours: "Mo-Sa 08:00-18:00"` — correct
- `sameAs` — Facebook + Instagram URLs present
- EA reg number now in HTML (CBDU640764) — good

**Issues:**
- `"url": "https://witchard.vercel.app"` — needs updating to `witchards.co.uk`
- No `priceRange` context (shows `"££"` which is fine but `"priceRange": "£200-£1500"` would be more informative)
- No `image` property in schema
- Missing `hasOfferCatalog` with the 6 services listed — would enable rich results
- No `aggregateRating` (will be possible once reviews exist)

### Recommended schema additions

```json
"hasOfferCatalog": {
  "@type": "OfferCatalog",
  "name": "House Clearance Services",
  "itemListElement": [
    {"@type": "Offer", "itemOffered": {"@type": "Service", "name": "Full House Clearance"}},
    {"@type": "Offer", "itemOffered": {"@type": "Service", "name": "Partial Clearance"}},
    {"@type": "Offer", "itemOffered": {"@type": "Service", "name": "Post-Clearance Cleaning"}},
    {"@type": "Offer", "itemOffered": {"@type": "Service", "name": "Probate & Estate Clearance"}},
    {"@type": "Offer", "itemOffered": {"@type": "Service", "name": "Landlord & Rental Clearance"}},
    {"@type": "Offer", "itemOffered": {"@type": "Service", "name": "Garden & Garage Clearance"}}
  ]
}
```

---

## 6. Platform Optimisation — 30/100

| Platform | Status |
|----------|--------|
| Google AI Overviews | Poor — no GBP, no indexed domain yet |
| ChatGPT / Bing | Poor — no brand signals, no indexed domain |
| Perplexity | Poor — no brand signals |
| Google Maps | Not listed |
| Apple Maps | Not listed |

For a local service business, **Google Business Profile is 80% of this category**. Until that's set up, platform scores will remain low regardless of website quality.

---

## Priority Action Plan

### Immediate (do before pushing to `witchards.co.uk`)
| # | Action | Impact | Effort |
|---|--------|--------|--------|
| 1 | Connect domain (`witchards.co.uk`) | Critical | Low |
| 2 | Add `robots.txt` | High | 5 min |
| 3 | Add `llms.txt` | High | 10 min |
| 4 | Add Open Graph meta tags | Medium | 10 min |
| 5 | Add canonical tag | Medium | 2 min |
| 6 | Update schema URL | Medium | 2 min |
| 7 | Add `hasOfferCatalog` to schema | Medium | 5 min |

### Soon (first week live)
| # | Action | Impact | Effort |
|---|--------|--------|--------|
| 8 | Set up Google Business Profile | Critical | 30 min |
| 9 | Add owner name(s) to About section | High | 2 min |
| 10 | Add pricing table (1/2/3-bed estimates) | High | 20 min |
| 11 | Add FAQ section (5–8 questions) | High | 30 min |

### When reviews come in
| # | Action | Impact | Effort |
|---|--------|--------|--------|
| 12 | Unhide reviews section + add real reviews | High | 10 min |
| 13 | Add `aggregateRating` to schema | Medium | 5 min |
| 14 | List on Checkatrade / Trustpilot | Medium | 30 min |

---

## Quick Wins I Can Do Right Now

Items 2–7 above are all code changes in `index.html` — I can apply all of them immediately if you want.

- `robots.txt` — new file
- `llms.txt` — new file  
- Open Graph tags — 6 lines in `<head>`
- Canonical tag — 1 line in `<head>`
- Schema URL + `hasOfferCatalog` — edit existing JSON-LD block

Say the word and I'll apply all of them.
