# Example session — B2C web SaaS (fictional)

This is a **condensed, fictional** example of the skill's behavior. Company
details are invented placeholders.

---

## Phase 1 — Interview (user answers, condensed)

**App type:** "TaskFlow — web SaaS, B2C, individual users, email login, no
user content uploads, no user-to-user messaging."

**Data collected:** "Name, email, task content, and we connect Stripe for
subscriptions and Mailchimp for our newsletter. We use Google Analytics on
the marketing site."

**Monetization:** "Freemium: free plan, plus Pro at $9/month auto-renewing."

**Features:** "Transactional emails (welcome, receipts) via our own SMTP;
newsletter via Mailchimp. Stripe handles all payments. No ads."

**Jurisdiction:** "Company registered in Spain; users mostly in Spain and
the US."

**Commercial policies:** "14-day refund window for Pro, unused. We suspend
accounts after 3 failed payments."

**Mobile:** "No mobile app yet."

## Phase 2 — Project audit (user shares dependency list)

> User pasted `package.json` + DB schema excerpt.

**Skill findings:**

- `postgresql` schema includes `users.last_ip` and `users.birthdate` —
  **declared as collected but never used in code** → ⚠️ minimization risk,
  recommend removing or justifying.
- `analytics` package includes a Facebook Pixel alongside Google Analytics —
  **not mentioned in the interview** → ⚠️ adds "sale/share" exposure under
  CCPA and consent requirement under GDPR/ePrivacy.
- Mailchimp sends the newsletter but signup form has **one bundled
  checkbox** for terms + marketing → ⚠️ GDPR requires unbundling.
- Stripe is used correctly as processor (no card data stored directly) → ✅.

## Phase 3 — Adaptive selection (skill output, condensed)

| Document | Status |
|---|---|
| Terms of Service | **[APPLIES]** — all apps with users |
| Privacy Policy | **[APPLIES]** — processes personal data |
| Cookie Policy + Consent Banner | **[APPLIES]** — marketing site has Google Analytics + Facebook Pixel (non-essential cookies) |
| Purchase & Subscription Terms | **[APPLIES]** — auto-renewing Pro plan |
| Refund Policy | **[APPLIES]** — paid subscriptions with a stated 14-day window |
| Form consent texts | **[APPLIES]** — registration + newsletter forms; separate marketing checkbox required |
| Email unsubscribe + footer | **[APPLIES]** — newsletter via Mailchimp (transactional email footer recommended too) |
| Legal Notice (Spain) | **[APPLIES]** — company established in Spain (LSSI mandatory) |
| International data transfer notice | **[APPLIES]** — EU users' data processed by US-based processors (Stripe, Mailchimp, Google) |
| Marketing/SMS consent | **[APPLIES]** — newsletter opt-in; no SMS |
| Complaint channel notice | **[APPLIES]** — GDPR users (right to complain to AEPD) |
| Accessibility statement | **[APPLIES]** *(recommended)* — public web app |
| Community Guidelines | **[DOES NOT APPLY + reason]** — no user content or user interaction |
| DMCA / IP policy | **[DOES NOT APPLY + reason]** — no user uploads |
| Content License Terms | **[DOES NOT APPLY + reason]** — no uploads |
| EULA | **[DOES NOT APPLY + reason]** — pure web app, no distributed software |
| Marketplace Terms | **[DOES NOT APPLY + reason]** — single vendor |
| Age gate / minors clause | **[DOES NOT APPLY + reason]** — task tool for adults; state 18+/16+ minimum in ToS instead |
| AI/ML disclosure | **[DOES NOT APPLY + reason]** — no AI processing of user data |
| Health/sensitive data notice | **[DOES NOT APPLY + reason]** — none collected |
| ATT tracking notice | **[DOES NOT APPLY + reason]** — no iOS app |
| DPA summary | **[DOES NOT APPLY + reason]** — B2C, not processing customers' end-user data |

> **Skill:** "Confirm this list or tell me what to add/remove before I draft
> anything."

*(User confirms.)*

## Phase 4 — Drafting (excerpt of the Privacy Policy)

> ⚠️ The full document would be ~10 sections. Excerpt:

```
### PRIVACY POLICY — TaskFlow (excerpt)

1. INTRODUCTION

1.1. This Privacy Policy explains how TaskFlow S.L. ("we", "us") collects and
     uses your personal data when you use our web application at
     [WEBSITE URL] (the "Service").

1.2. Contact: [CONTACT EMAIL]. Registered address: [POSTAL ADDRESS], Spain.

2. DATA WE COLLECT

| Data | Source | Purpose | Legal basis | Retention |
|---|---|---|---|---|
| Name, email | Registration form | Account management, service delivery | Contract | While your account is active + [RETENTION PERIOD] |
| Task content | Your input | Providing the Service | Contract | While your account is active |
| Billing data | Stripe | Processing subscriptions | Contract | As required by tax law |
| Newsletter data | Signup form | Marketing emails | Consent | Until you unsubscribe |
| Usage data (cookies) | Google Analytics, Facebook Pixel | Site analytics and marketing measurement | Consent (cookies) | [RETENTION PERIOD] |

...
```

**Placeholders left for the user (skill's end-of-drafting list):**

- `[COMPANY NAME]` → legal name ("TaskFlow S.L." was confirmed in interview;
  replace if different)
- `[CONTACT EMAIL]`, `[POSTAL ADDRESS]`, `[WEBSITE URL]`
- `[RETENTION PERIOD]` (usage data, account data after deletion)
- `[DATE]` / `[EFFECTIVE DATE]`

## Phase 5 — Compliance summary (condensed)

- ✅ Refund window (14 days) stated and consistent between ToS and Refund
  Policy; EU statutory withdrawal rights preserved in the doc.
- ⚠️ **Remove or justify `users.birthdate`** — collected but unused
  (minimization violation risk under GDPR).
- ⚠️ **Unbundle the signup checkbox**: one checkbox for terms, a separate,
  unchecked one for the newsletter.
- ⚠️ **Facebook Pixel undeclared** → requires cookie consent banner
  classification and a "sale/share" review under CCPA (opt-out link).
- ⚠️ **Stripe/Mailchimp/Google (US) transfers** → state SCCs/DPF mechanism in
  the transfers section.
- ✅ Account suspension policy (3 failed payments) documented in ToS.
- 📋 Platform/store requirements: none (no mobile app). Add a Privacy Policy
  URL to the marketing site footer and the Stripe checkout description.

---

*Remember: all outputs require review by a licensed attorney in the governing
jurisdiction before publication.*

