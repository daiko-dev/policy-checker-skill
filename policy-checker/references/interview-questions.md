# Interview Question Bank (Phase 1)

Ask questions grouped by block, one block (or one logical group) at a time.
Never dump all questions at once. Omit any question already answered by the
project context. After each block, briefly confirm the answers and continue.

Language: interview in the user's language. If ambiguous, default to English
and offer Spanish.

## Block 1 — App type

- What kind of app is it: web, mobile, desktop, SaaS, API?
- Is it B2B, B2C, B2B2C, or a mix?
- Does it have user accounts (login/registration), or is it accountless?
- Is it a marketplace (multiple sellers), ecommerce, or a single-vendor store?
- Is there user-generated content (posts, reviews, uploads, comments)?
- Do users interact with each other (messaging, forums, social features)?

## Block 2 — Personal data collected

Audit against this list; ask about each item not already clarified:

- Identity: name, username, date of birth, gender.
- Contact: email, phone number, postal address.
- Payment: card data, billing address, invoices (note: card data should never
  be stored directly — expect a processor like Stripe).
- Location: precise geolocation, IP-based location, shipping address.
- Health or sensitive data: medical, biometric, religion, union membership,
  sexual orientation, criminal records.
- Minors' data: do users under 16 (or 13) use the app?
- Cookies / tracking: analytics, advertising pixels, session cookies,
  fingerprinting.
- Third-party SDKs: analytics, crash reporting, ads, auth providers, chat,
  push notifications (ask which services).
- AI/ML: do you process user data with AI models, train models on user data,
  or make automated decisions (scoring, profiling, moderation)?
- Content: photos, videos, documents, voice recordings uploaded by users.

## Block 3 — Monetization

- Is the app free, paid, freemium, or subscription-based?
- One-time purchases, subscriptions (ask: auto-renewing?), in-app purchases?
- Advertising (which networks, personalized or not)?
- Commissions or fees (marketplace/ecommerce)?
- Any paid trial periods, discounts, or refunds beyond legal minimums?

## Block 4 — Relevant features

- Outbound emails and/or push notifications (transactional? marketing?)?
- Payments and payouts (who pays whom, and through what processor)?
- User content uploads (who owns what, what is prohibited)?
- User-to-user messaging or public comments (moderation approach)?
- Geolocation features (background location? sharing with others?)
- Third-party integrations: Stripe, PayPal, Google (OAuth/Analytics/Firebase),
  Meta/Facebook, Mailchimp/SendGrid, AWS/GCP, OpenAI/other LLMs, etc.
- Data export or deletion features (self-service account deletion is required
  by major stores).

## Block 5 — Jurisdiction

- Where is the company/developer legally established (country)?
- Where are the users located (countries/regions)?
- Do you know which laws apply to you? (Explain: EU/EEA users → GDPR; UK →
  UK GDPR; California → CCPA/CPRA; other US states; Brazil → LGPD; Canada →
  PIPEDA; Spain additionally requires a Legal Notice and LSSI compliance.)
- Is a physical address for legal notices available, or use a placeholder?

## Block 6 — Commercial policies

- Desired refund policy: window length, conditions (used/unused), who pays
  return costs, digital goods (statutory withdrawal rights may apply in the EU).
- Conditions and notice for account suspension or termination.
- Price change policy for subscriptions (advance notice required in many
  jurisdictions).
- Dispute resolution preference (courts, arbitration, mediation)?

## Block 7 — Mobile stores (only for mobile apps)

- Which stores: Apple App Store, Google Play, both?
- iOS: does the app track users across apps (requires ATT prompt)?
- Does the app offer account creation AND in-app account deletion (required)?
- Subscriptions through the store's billing system (required for digital
  goods) or external payments (physical goods/services may use own processor)?
- Age rating of the app (4+/13+/17+ etc.)?

## Closing

Summarize the confirmed profile back to the user in a compact list and ask
them to correct anything wrong before moving to Phase 2.
