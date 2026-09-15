# Witchard House Clearance — State

## Current status
Site is live at witchards.co.uk (Vercel, auto-deploys from
`github.com/cermartin/witchard-house-clearance` master on push). This
session closed out the two longest-open TODO items — photos and reviews
— using material Joe sent over Facebook/WhatsApp, across two rounds:

1. **Photos unblocked.** Joe sent van/team photos and a job-in-progress
   photo (clearing garden rubble/wood into the van, can't use a skip).
   The job photo directly matches the CW Garden Construction review (see
   below) and is now the Garden & Garage Clearance service card image,
   replacing its stock Unsplash photo (`assets/job-garden-clearance.*`).
   Of the remaining people photos, most show 3 people in Witchard polos —
   confirmed the third person is an occasional helper, not a team
   member, so those weren't used anywhere (would contradict the About
   copy's "just the two of us on every job"). One photo is genuinely just
   two people, Bill and Joe together in the van cab — confirmed with
   Martin this is really them, not Bill + the helper — so that one now
   replaces the generic 4-tile stat grid ("100% Family-run" etc.) in the
   About section (`assets/bill-and-joe.*`, 4:5 crop, `object-position`
   tuned to keep both faces in frame). Martin specifically suggested this
   placement on a follow-up message. All new photo assets compressed to
   matching JPEG+WebP pairs, same pattern as the existing logo assets.
2. **Reviews unblocked.** Two real reviews added, replacing the 3
   placeholder Sarah T./James H./Linda M. entries: Sally Holmes (Facebook
   comment, a care home manager thanking Witchard for helping a resident
   at Bailey House) and CW Garden Construction (Facebook message, a
   trade contractor praising price/speed/cleanliness on a skip-less
   rubble job — matches the new service card photo). The contractor's
   message had a typo ("defiantly" → "definitely") and was cut off
   mid-sentence in the screenshot Martin sent; typo corrected, quote
   ended cleanly at the visible text, nothing invented. Credited to the
   company name only, not the individual's name (Connor Walsh) — he
   asked to be posted under his company name, and Martin confirmed on
   2026-09-15 to drop the personal name from display entirely, not just
   lead with the company. `#reviews` section unhidden, "Reviews" added
   to nav. Removed the fabricated "5.0/5" score line since it wasn't
   backed by a real count; added `aggregateRating` schema (5.0,
   reviewCount: 2) since that's literally what's on the page now.

Every content decision (team size / helper-vs-member status, whether
both testimonials should go live, and confirming the two-person photo
was really Bill and Joe) was confirmed with Martin before writing, per
the project's "don't assume business facts" rule. Reviewed locally with
Playwright screenshots (desktop services grid, About section, desktop +
mobile reviews section, About photo at both viewport sizes) before each
commit. One CSS bug caught during testing: the About photo initially
used `height:100%` on the `img` with no defined parent height, which
rendered fine on the first load but broke (photo stretched to fill the
whole viewport) — fixed by putting `aspect-ratio:4/5` directly on the
`img` instead of relying on a percentage height from an unconstrained
parent.

## What's done
- `TODO.md` items closed: job/van photos, reviews unhidden, `aggregateRating`.
- About section photo added as a follow-up in the same session.
- Local Python http.server used for the checks has been shut down.

## Open / not done this session
- 5 of 6 service cards still use stock Unsplash images (only had one
  genuine job-in-progress photo to work with — the others were people
  photos, not tied to a specific service).
- Checkatrade / Trustpilot listing — still open, unrelated to this session.
- Two minor low-priority contrast items flagged in an earlier session but
  not fixed (grey "SCROLL" hint under hero, footer copyright line) — low
  severity, pick up if doing another accessibility pass.

## Next step
If Joe sends more job-specific photos (ideally one per remaining
service type), swap the remaining 5 stock service-card images. Otherwise
nothing blocking — next open item is Checkatrade/Trustpilot listing.

## 2026-09-15 (later) — FAQ section + About trim + Facebook link bug found
Martin felt the page was getting too long and floated splitting it into
multiple pages/tabs. Recommended against that for a single-visit local
service site (one-page keeps the phone number always in scroll reach,
existing nav anchors already act like tabs without page loads) and
suggested trimming + a collapsible FAQ instead. Martin agreed.

Drafted 8 FAQ questions for Joe, prefilled 2 draft answers only where the
site already said something equivalent (on-site presence, fixed pricing
from the How It Works copy) and left the rest blank rather than
guessing — nothing in `COMPANY.md` or `client-correspondence/` covered
booking lead time, item exclusions, donation/recycling split, single-item
jobs, or job refusals. Joe answered all 8 directly.

Built from his answers:
- New `#faq` section (between How It Works and About) using native
  `<details>/<summary>`, no JS — collapsed by default, "+" rotates to
  "×" on open. Added "FAQ" to nav and a matching `FAQPage` schema block
  (validated as well-formed JSON alongside the existing `LocalBusiness`
  block).
- About section trimmed from 3 paragraphs to 2 (dropped the "why we
  started this business" paragraph — Martin said there wasn't much more
  to say about the company beyond what's already up).
- About photo's aspect ratio changed from 4:5 to 4:3 (less tall) so the
  now-shorter text column and the photo balance better on desktop —
  previously the photo ran well past the text with `align-items:center`
  centering a short column against a very tall image.

Separately, Joe flagged that the Facebook button "takes me to a small
company page." Checked the href: it's
`facebook.com/groups/.../user/...`, a link to a user's profile inside a
group, not the actual Page. Don't have the real Page URL on file
anywhere, so didn't guess a replacement — added to `TODO.md` as
blocked-on-Joe, need to ask him for the correct link (appears 3 places:
schema `sameAs`, contact section, footer icon).

Reviewed locally with Playwright at desktop (1400px) and mobile (390px)
before commit — FAQ accordion open/closed states, About section balance,
no console errors.

## Note on git history
As of this session, `index.html` has uncommitted changes (FAQ section +
schema, About trim, About photo aspect-ratio tweak) — not yet committed
or pushed. Push to `master` to deploy live via Vercel. Still need to ask
Joe for the correct Facebook Page URL before that item can close.
