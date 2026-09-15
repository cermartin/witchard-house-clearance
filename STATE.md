# Witchard House Clearance — State

## Current status
Site is live at witchards.co.uk (Vercel, auto-deploys from
`github.com/cermartin/witchard-house-clearance` master on push). This
session closed out the two longest-open TODO items — photos and reviews
— using material Joe sent over Facebook/WhatsApp:

1. **Photos unblocked.** Joe sent van/team photos and a job-in-progress
   photo (clearing garden rubble/wood into the van, can't use a skip).
   Only the job photo was used: it directly matches the CW Garden
   Construction review (see below) and is now the Garden & Garage Clearance service card
   image, replacing its stock Unsplash photo. Compressed to matching
   JPEG+WebP pairs in `assets/` (`job-garden-clearance.*`, ~65-90KB,
   same pattern as the existing logo assets). The other photos (van cab
   selfies, 3 people in Witchard polos) were **not** used — About section
   copy says "just the two of us on every job" (Bill + Joe), and the
   third person is confirmed to be an occasional helper, not a team
   member, so using a 3-person photo there would visually contradict that
   claim. Left out entirely rather than risk overstating team size.
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

Both changes were confirmed with Martin before writing (team size /
helper-vs-member status, and whether both testimonials should go live)
per the project's "don't assume business facts" rule. Reviewed locally
with Playwright screenshots (desktop services grid, desktop + mobile
reviews section) before commit.

## What's done
- `TODO.md` items closed: job/van photos, reviews unhidden, `aggregateRating`.
- Local Python http.server used for the check has been shut down.

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
As of this session, `index.html` has uncommitted changes (reviews +
service card photo + nav link + aggregateRating schema) plus two new
untracked asset files (`assets/job-garden-clearance.jpg/webp`) — not yet
committed or pushed. Push to `master` to deploy live via Vercel.
