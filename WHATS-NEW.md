# Peace4Paws site — update log (this build)

This build applies your wording-change tables, adds the new content you sent,
wires up the live adoptable-dog feed, and sets the events system to auto-archive.
Everything is still self-contained HTML (images baked in) so it runs by just
opening index.html — no server needed.

## Wording changes — APPLIED
- **Homepage:** every row from Homepage_Wording_Changes (alert bar, hero headline
  "Give a Dog a Second Chance", all three stat captions, who-we-are paragraph,
  "Change a Life", foster headline + paragraph, urgent-donation block, newsletter
  "Stay Connected"). The inline Venmo/Zelle/PayPal/check list was replaced with a
  link to the Donate page, per your note.
- **About / Adopt / Donate / Events / Foster / Volunteer / Stories / Memorials /
  Past Events:** every row from the Site Wording Change Tables applied, including
  softened emergency language, "Home Review", "Forever Home", grammar fixes, and
  the friendlier "Select any…" phrasing.
- **All internal notes removed** site-wide: every "add in admin", "live site",
  "drop in", "DRAFT", and AdoptAPet developer note is gone.

## New content — ADDED
- **About page:** real Mission Statement (the ahimsa origin story), a new
  "Real Rescue, Real Impact" stats band (294 dogs rescued in 2025 · 100% volunteer
  · helping since 2007 · foster-based), and a "The People Behind Peace4Paws"
  photo gallery built from the volunteer / rescue-moment images you sent.
- **Testimonials:** an "From Our Adopters" section on the homepage with the two
  adopter blurbs (Carol/Charlie, Cathy/Puddy) shown as little circle-photo cards,
  the adopter-spotlight style you described.
- **Past Events:** rebuilt from 5 placeholder cards to ALL 29 real events,
  newest-first, each with its real flier image and a recap (paraphrased from the
  summaries you provided). Click any card to open the full flier.
- **Memorials:** DRAFT notes removed; closing line softened. The Kyle and Anthony
  tributes remain as-is for you to confirm or swap for the family's exact words.

## Live systems — WIRED
- **Adoptable dogs (auto-updating, no admin work):** the homepage dog row and the
  Adopt page now embed Adopt-a-Pet's official Portable Pet List widget for shelter
  #86691. Dogs appear and drop off on their own as you update them on Adopt-a-Pet —
  no code or pet-ID editing needed. (This uses the public widget URL, so it does
  NOT require your Adopt-a-Pet login.) A fallback link to your Adopt-a-Pet search
  shows if the widget is blocked.
- **Events auto-archive:** the Events page now uses the same card style as Past
  Events. Add upcoming events to the `UPCOMING` list near the bottom of events.html
  (date, title, location, recap, optional flier). Cards show soonest-first; once a
  date passes, the card disappears on its own. When the list is empty, the
  "no events yet" message shows automatically. (For full auto-transfer INTO the
  Past Events page, that page is driven by its own list — when an event passes,
  move its entry into past-events.html. With the git-based CMS next step, both
  lists become point-and-click for non-technical staff.)

## Links cleaned up site-wide
- Footer "Our story" → About; "Recommended trainers" placeholder removed.
- Facebook / Instagram / YouTube wired to your real profiles.
- Every dead "#" link resolved (logos, hero buttons, donate buttons, card links).

## Still open / your call
- Confirm the two memorial tributes (or paste the family's exact words).
- Confirm the 294 / 2025 stat wording and the donate impact-amount wording.
- Decide nav grouping questions (Stories link vs dropdown; "Get Involved" group).
- Next infra step: add the git-based CMS (Decap/Pages CMS) so staff can edit
  photos, events, and text without touching code.
