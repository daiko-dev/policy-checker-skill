# Final Compliance Checklist Format (Phase 5)

After drafting, deliver this summary in the user's language, tailored to the
confirmed profile. Every section must be filled with project-specific facts —
never generic filler. Mark each item ✅ (covered) / ⚠️ (gap or action needed)
/ ❌ (not applicable).

## 1. Data minimization review

For each personal data item collected:

| Data item | Purpose | Legal basis | Retention | Justified? |
|---|---|---|---|---|

- Flag any data item without a clear purpose or legal basis as ⚠️ and
  recommend removing it or clarifying the basis.
- Note any data the project analysis revealed that the user did not mention
  in the interview.

## 2. Third-party / SDK inventory

| Third party | What data they receive | Why | Data processing agreement needed? | Link to their privacy terms |
|---|---|---|---|---|

- Include auth providers, analytics, crash reporting, payments, email, ads,
  AI providers, hosting.
- Flag providers without a published DPA or with data-sharing concerns.

## 3. Detected legal risks and mitigations

For each risk: description, severity (high/medium/low), mitigation. Typical
risks to check:

- Missing consent mechanism for cookies/tracking.
- Emails without unsubscribe or with dark-pattern opt-out.
- Pre-checked marketing checkboxes or bundled consent.
- Automated decisions without human review route.
- Data requested but never used (minimization violation).
- No account deletion path (store rejection + GDPR Art. 17).
- International transfers without stated mechanism.
- Minors' data without age gate or parental consent.
- Marketing consent bundled with registration.
- Retention periods undefined.

## 4. Outstanding platform requirements

Only if applicable — list concrete pending actions:

- App Store / Google Play: privacy labels/data safety form alignment, ATT
  prompt, account deletion, age rating, privacy policy URL in store listing.
- Stripe/payments: required disclosures at checkout (price, renewal terms).
- Meta/Google Ads: consent signals needed if running personalized ads to EU
  users.
- Email provider: list hygiene (double opt-in recommended), sender address.

## 5. Open placeholders

List every placeholder left across the generated documents
(`[COMPANY NAME]`, `[CONTACT EMAIL]`, etc.) so the user can fill them before
publication, plus the standing reminder that a licensed attorney must review
everything before publication.
