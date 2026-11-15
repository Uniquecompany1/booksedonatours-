# Base44 prompt — Sedona Gift Cards app (clone of Lancaster Gift Cards, with audit fixes built in)

Paste this into Base44 as the build prompt for a NEW app (do not edit the Lancaster app).
Brand: Unique Sedona Experiences · Domain it will pair with: booksedonatours.com

---

Build a gift card store called "Sedona Gift Cards" for Unique Sedona Experiences, a Sedona, Arizona tour booking agency. It sells gift certificates for Sedona tours. Match a desert design theme: sandstone/cream background (#FAF5EE), rust/terracotta primary (#A44A24), dark brown text (#2B211C), serif headings.

## How it works (show these facts on the homepage, above the fold, not buried)
- Buyer picks a specific experience OR a dollar amount.
- The gift card is emailed to the PURCHASER within 24 hours.
- The recipient books their tour by phone at (717) 925-0891.
- Gift cards NEVER expire and have NO fees.
- All gift card sales are final (nonrefundable).

## Experiences to offer (buyer can also choose a custom dollar amount)
- Broken Arrow Jeep Tour — $146
- Half-Day Sedona Sightseeing Tour — $126
- Antelope Canyon & Horseshoe Bend Day Tour — $312
- Sedona Vortex Odyssey — $130
- Bliss Wine Tour (lunch included) — $125
- Private Lil' Rattler Jeep Tour — $159
- Grand Canyon Day Tour — $189
- Sedona Stargazing Tour — $127
- Verde Canyon Railroad — $186
- Boynton Canyon Trolley Tour — $26
Note in the UI: "Tour prices can change — if the tour costs more at booking, the recipient just pays the difference; if less, the balance stays on the card."

## Purchase flow requirements
1. Step 1: choose experience or dollar amount. Show a LIVE gift card preview that actually renders (card design with amount and experience name) as the buyer makes choices — the preview must update in real time.
2. Step 2: buyer details (name, email) with real form labels (not placeholder-only labels).
3. Step 3: review screen that repeats the key facts before payment: card emailed to the buyer within 24 hours; recipient books by phone at (717) 925-0891; never expires, no fees; all sales final.
4. Step 4: secure checkout (Stripe) and a confirmation screen + confirmation email repeating the same key facts and the phone number.
5. Every button must always be clickable or show a clear reason when disabled (e.g., "Enter an amount to continue") — never a silently disabled button.
6. Do not use nested interactive elements (no links inside clickable cards). All form fields need visible labels and focus states; the full flow must be keyboard-navigable.

## Pages
- Home: hero ("Give Sedona instead of stuff."), the how-it-works facts, experience list with prices, FAQ (expiry, fees, how to redeem, refunds, price changes).
- FAQ must state: redeem by phone only at (717) 925-0891; never expires; no fees; all sales final; issued by Unique Sedona Experiences, tours operated by local companies and fulfilled through Viator.
- Footer: Unique Sedona Experiences · booksedonatours.com · (717) 925-0891.

## After building
- Connect the custom domain when available; until then the base44.app URL is fine for testing only.
- The main site (booksedonatours.com/gift-cards.html) will link its "Buy a Gift Card" button here — keep the app URL stable once live.
