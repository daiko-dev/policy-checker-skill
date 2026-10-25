# policy-checker

A conversational skill that generates **complete, adapted legal documentation**
for any application — web, mobile, desktop, or SaaS. It behaves like a
technical legal advisor specialized in data protection and digital compliance:
it interviews you about your project, analyzes your codebase (if you share
one), decides which legal documents actually apply, drafts them in plain
language, and delivers a final compliance summary.

> ⚠️ **Not legal advice.** Every generated document includes a mandatory
> reminder to be reviewed by a licensed attorney in your jurisdiction before
> publication. This skill automates drafting, not legal judgment.

## What it generates

Depending on your project, the skill evaluates and drafts up to 25+ document
types, including:

| Category | Documents |
|---|---|
| Core terms & privacy | Terms of Service, Purchase & Subscription Terms, Privacy Policy, Cookie Policy + banner, in-app tracking notice (ATT) |
| Payments & commerce | Refund Policy, EULA |
| User content & community | DMCA / IP Infringement Policy, Community Guidelines, Content License Terms, Marketplace Seller/Buyer Terms |
| Consents & notices | Form consent texts (never pre-checked), email unsubscribe + footer, marketing/SMS consent, Legal Notice (Spain), age gate |
| Special & regulatory | AI/ML disclosure + Art. 22 GDPR clause, health/sensitive data notice, international transfers, professional services disclaimer, accessibility statement, DPA summary, breach notification, complaint channel |

Documents **not relevant to your project** are explicitly marked
`[DOES NOT APPLY + reason]` so you know nothing was silently skipped.

## How it works — 5 mandatory phases

1. **Interview** — Before generating anything, the skill asks about your
   project in logical blocks (app type, data collected, monetization,
   features, jurisdiction, commercial policies, store requirements). Questions
   come one block at a time, never all at once.
2. **Project analysis** *(optional)* — Paste code, a file tree, a PRD, a
   database schema, or a dependency list and the skill audits it against your
   answers: what data is *actually* collected, which third-party SDKs receive
   it, and where the compliance gaps are.
3. **Adaptive selection** — You get a checklist of every applicable and
   non-applicable document with reasons. **Nothing is drafted until you
   confirm.**
4. **Drafting** — Numbered, plain-language documents ready to publish, with
   placeholders for anything unknown (`[COMPANY NAME]`, `[CONTACT EMAIL]`,
   `[JURISDICTION]`, `[EFFECTIVE DATE]`) — the skill never invents legal
   facts.
5. **Compliance summary** — A final report: data minimization review,
   third-party/SDK inventory, detected risks with mitigations, and pending
   platform requirements (App Store, Google Play, Stripe, Meta, etc.).

See [examples/](examples/) for a real-shaped example session.

## Key guarantees

- **Never invents legal facts** — unknowns become placeholders, and you get a
  list of every placeholder to fill in.
- **Always disclaims** — every document ends with the attorney-review notice.
- **Refuses dark patterns** — asks for pre-checked boxes, hidden data
  collection, or buried unsubscribe links? The skill refuses, explains the
  legal risk, and offers the compliant alternative.
- **Coherent output** — all documents share the same definitions, contact
  details, and governing law.
- **Bilingual drafting** — works in English or Spanish; asks if the project
  needs both.

## Installation

### Claude Code (project or personal skills)

1. Copy the `policy-checker/` folder into your skills directory:

   ```bash
   # project-level (available in one project)
   mkdir -p .claude/skills
   cp -r policy-checker .claude/skills/

   # or personal-level (available everywhere)
   cp -r policy-checker ~/.claude/skills/
   ```

2. Start a new session and just ask, e.g.:

   > "Generate the legal docs for my app"

   or

   > "Check my app's legal compliance"

### Claude.ai / other environments

The skill is plain Markdown + YAML frontmatter — upload `policy-checker/`
with your skills provider, or paste the `SKILL.md` content as system
instructions and point it to the `references/` files.

## Usage tips

- **Prepare before you start:** know your company's country, where your users
  are, and which third-party services you use (Stripe, Firebase, Google
  Analytics, Mailchimp…). This shortens the interview a lot.
- **Share your project materials** (schema, dependency list, PRD) — the audit
  phase catches gaps like un-declared tracking or data you didn't know you
  were collecting.
- **Answer precisely about jurisdiction.** Governing law drives everything:
  GDPR sections, CCPA rights, COPPA age gates, Spanish Legal Notice, etc.
- **Save documents in `/legal` or `/public`** of your web project and link
  them from the footer, signup forms, and store listings.
- **Fill every placeholder before publishing** — the skill lists them all at
  the end.

## Repository structure

```
.
├── policy-checker/                  # the skill itself
│   ├── SKILL.md                     # core workflow + non-negotiable rules
│   └── references/                  # loaded per-phase by the skill
│       ├── interview-questions.md   # Phase 1 question bank (7 blocks)
│       ├── document-selection.md    # Phase 3 decision matrix (25+ docs)
│       ├── document-templates.md    # Phase 4 structural skeletons
│       ├── writing-rules.md         # drafting rules, placeholders, coherence
│       ├── jurisdictions.md         # GDPR/CCPA/COPPA/PIPEDA/LGPD/stores notes
│       └── compliance-checklist.md  # Phase 5 output format
├── examples/                        # example sessions and outputs
├── CONTRIBUTING.md
├── CHANGELOG.md
├── LICENSE
└── README.md
```

## Supported jurisdictions (built-in reference)

GDPR & UK GDPR · CCPA/CPRA (California) · COPPA (US children) · PIPEDA
(Canada) · LGPD (Brazil) · Spain-specific (LSSI, Legal Notice, AEPD) · US
federal (CAN-SPAM, TCPA, DMCA) · Apple App Store & Google Play requirements ·
EU AI Act transparency duties. Jurisdiction-specific clauses are added only
after you confirm where you and your users are — never assumed.

## FAQ

**Does this replace a lawyer?** No. It produces high-quality first drafts and
compliance reviews, but every document must be reviewed by a licensed attorney
in your jurisdiction before publication. The skill says so in every output.

**Can I use the generated documents commercially?** Yes — the output is
yours. Check the [LICENSE](LICENSE) for the skill's own code and references.

**What if my app serves users in many countries?** The skill drafts one
Privacy Policy with jurisdiction-specific sections (e.g., "Additional rights
for California residents") plus the broadest compliant baseline for terms.

**Does it store or send my data anywhere?** The skill is just instructions —
everything happens inside your AI session. Nothing is uploaded by the repo
itself.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) — issues and PRs for new
jurisdictions, document templates, and dark-pattern detection rules are very
welcome.

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

## License

[MIT](LICENSE) © daiko-dev

