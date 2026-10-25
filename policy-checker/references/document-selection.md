# Document Selection Matrix (Phase 3)

Evaluate every document in the catalog against the interview answers and (if
provided) the project analysis. Present the full evaluated list to the user as
a checklist with `[APPLIES]` or `[DOES NOT APPLY + reason]` per item, and ask
for confirmation before drafting. The user may add or remove items; note any
user-added item and draft it with the same rules.

## Catalog

### Core terms and privacy

| Document | Applies when | Does not apply when |
|---|---|---|
| Terms of Use / Terms of Service | Always (any app with users) | Never — always applies |
| Purchase & Subscription Terms | Any paid plan, purchases, or subscriptions | Fully free app with no commerce |
| Privacy Policy | Any app that processes personal data | Only fully offline, zero-data app (practically never) |
| Cookie Policy + Consent Banner | Website with non-essential cookies (analytics, ads, embedded content) | Mobile app without web cookies (use in-app tracking notice instead) |
| In-app Tracking Notice (ATT) | iOS app that tracks users across other apps | Web-only or non-tracking iOS apps |

### Payments and commerce

| Document | Applies when | Does not apply when |
|---|---|---|
| Refund Policy | Any payments, subscriptions, or paid digital goods | No payments |
| EULA | Distributable software (mobile/desktop app binaries) | Pure web app |

### User content and community

| Document | Applies when | Does not apply when |
|---|---|---|
| IP Infringement / DMCA Policy | Users can upload content or post publicly; risk of hosting infringing material | No user content or all content is private and reviewed |
| Community Guidelines | Public or semi-public interaction (posts, comments, messaging, profiles) | No user interaction |
| Content License Terms | Users upload content (defines the license granted to the platform) | No uploads |
| Marketplace Seller/Buyer Terms | Marketplace with third-party sellers | Single-vendor store |

### Consents and notices

| Document | Applies when | Does not apply when |
|---|---|---|
| Form consent texts | Any form collecting personal data (registration, checkout, contact, newsletter) | No forms |
| Email unsubscribe + footer | Sending any marketing emails | Transactional-only emails (still recommend preference link) |
| Marketing/SMS consent | Marketing messages or SMS to users | No outbound marketing |
| Legal Notice | Company established in Spain (mandatory) or Spanish users | No Spain nexus |
| Age gate / minors clause | Minors may use the app, or age-restricted content | Strictly 18+ verified service |

### Special and regulatory

| Document | Applies when | Does not apply when |
|---|---|---|
| AI/ML disclosure + automated decisions | AI processing of user data, profiling, automated decisions with legal/equivalent effect (Art. 22 GDPR) | No AI/ML involvement |
| Health / sensitive data notice | Health, biometric, or other special-category data | None processed |
| International data transfer notice | Data crosses borders (e.g., EU users, US-hosted servers) | Data stays in-region |
| Professional services disclaimer | App offers health/legal/financial/other professional content | Pure entertainment or utility |
| Accessibility statement | Public web/app (recommended; required under EAA in EU, ADA risk in US) | Private internal tool |
| DPA summary | B2B SaaS processing customers' end-user data | No business customers |
| Security incident notification notice | Processing personal data at scale (recommended for B2B and sensitive data) | Trivial personal data |
| Complaint channel notice | GDPR/other laws grant complaint rights (mention supervisory authority) | No such regime applies |

## Presentation rules

- Show the checklist in the user's language, in the order above, grouped by
  section.
- For every `[DOES NOT APPLY]` item, give a one-line reason based on the
  confirmed profile (e.g., "Refund Policy — does not apply: the app has no
  payments").
- Explicitly ask: "Confirm this list or tell me what to add/remove before I
  draft anything."
- If the user asks for a document flagged as non-applicable, draft it anyway
  but restate why it seemed unnecessary.
