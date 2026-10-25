# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Planned

- Additional jurisdiction references (e.g., Australia Privacy Act, Japan APPI,
  South Korea PIPA).
- More example sessions in `examples/` (mobile app with children, marketplace).
- Optional packaged distribution (`.skill` file).

## [1.0.0] - 2026-10-25

### Added

- Initial release of the `policy-checker` skill.
- Mandatory 5-phase workflow: interview, project analysis, adaptive document
  selection, drafting, final compliance summary.
- 25+ document catalog with `[APPLIES] / [DOES NOT APPLY]` decision matrix:
  Terms of Service, Purchase & Subscription Terms, Privacy Policy, Cookie
  Policy + consent banner, ATT tracking notice, Refund Policy, EULA, DMCA /
  IP Infringement Policy, Community Guidelines, Content License Terms,
  Marketplace Terms, form consent texts, email unsubscribe/footer, marketing
  & SMS consent, Legal Notice (Spain), age gate, AI/ML disclosure with GDPR
  Art. 22 clause, sensitive data notice, international transfers notice,
  professional services disclaimer, accessibility statement, DPA summary,
  breach notification notice, complaint channel notice.
- Jurisdiction quick reference: GDPR/UK GDPR, CCPA/CPRA, COPPA, PIPEDA, LGPD,
  Spain (LSSI/AEPD), CAN-SPAM, TCPA, App Store / Google Play, EU AI Act.
- Non-negotiable rules: never invent legal facts, always attach the
  attorney-review disclaimer, refuse dark patterns and deceptive requests,
  keep all documents mutually coherent, draft in English or Spanish.
