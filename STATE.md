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

## Note on git history
As of this session, `index.html` has uncommitted changes (About section
photo swap) plus two new untracked asset files
(`assets/bill-and-joe.jpg/webp`) on top of the already-pushed reviews +
service-card-photo + nav-link + aggregateRating commit. Push to `master`
to deploy live via Vercel.
