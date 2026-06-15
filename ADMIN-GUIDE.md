# Peace4Paws Website — Admin & Editing Guide

This is a **static website** (plain HTML files). It loads instantly, costs nothing
to host, and most day-to-day content already updates on its own. Here's what's
self-updating, what you edit directly, and the recommended next step for letting
non-technical volunteers edit without touching code.

## 1. What updates ON ITS OWN (no work needed)

- **Adoptable dogs** (Home + Adopt pages): pulled live from your Adopt-a-Pet
  account (shelter #86691). When you add, update, or adopt out a dog on
  Adopt-a-Pet, the website list changes automatically. You never edit the site
  for this.
- **Applications** (Adopt / Foster / Volunteer): these are your Jotform forms.
  Edit the forms in Jotform; the website just links to them.
- **Donations**: Zeffy, PayPal, Venmo, Zelle, and the Square shop are all external
  links. Manage them in those accounts; the website just points to them.

## 2. What you edit in the FILES

These need a small text edit in the HTML (or, better, the CMS in section 4).

### Upcoming events  (events.html)
Near the bottom of `events.html` there's a clearly-marked list called `UPCOMING`.
Add an event like this:

    var UPCOMING = [
      { date:"2026-10-03", title:"Pawsfest 2026",
        loc:"Grace Episcopal Church, Westwood, NJ",
        recap:"Our annual fall festival of adoptions, food, and fun.",
        img:"" }
    ];

- Events show **soonest first** automatically.
- When an event's **date passes, it disappears on its own**.
- When the list is empty, a friendly "no events yet" message shows automatically.

### Past events  (past-events.html)
Each past event is a card that opens its flier. To add one, copy an existing
card block and change the date, title, location, recap, and image.

### Text & photos on the other pages
Headlines, paragraphs, and photos live directly in each page's HTML. Photos are
embedded in the file. Editing these by hand is possible but fiddly — this is
exactly what the CMS in section 4 solves.

## 3. Quick reference — where things live

- Home ............... index.html
- Adopt ............. adopt.html  (adoption steps, then live dog feed)
- Foster ............ foster.html
- Volunteer ......... volunteer.html
- About ............. about.html  (mission, stats, team photos)
- Stories ........... stories.html  (Happy Tails)
- Memorials ......... memorials.html
- Events ............ events.html  (upcoming, auto-archives)
- Past Events ....... past-events.html
- Donate ............ donate.html  (all giving options + Square shop)

## 4. RECOMMENDED next step: point-and-click editing for volunteers

To let non-technical staff change photos, events, and text **without code**, add a
free git-based CMS on top of this same site after it's on GitHub + Cloudflare:

- **Decap CMS** (decapcms.org) or **Pages CMS** (pagescms.org) — both are free,
  run on the same GitHub repo, and give volunteers a simple admin login with
  forms and image uploaders. No new hosting cost.

This is a follow-up project once the site is live. The deployment steps below get
the site online first.
