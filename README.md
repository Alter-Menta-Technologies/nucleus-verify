# Nucleus Verify

> **Signed proof that your code was reviewed. Independently verifiable. Forever.**

🌐 [verify.altermenta.com](https://altermenta.com) · ✉️ contact@altermenta.com · 🏢 [Alter Menta Technologies](https://altermenta.com)

---

## The problem no existing tool solves

The way software is written has changed permanently. AI generates thousands of lines in minutes. Code looks correct. Tests pass. But:

- Does the code actually implement what it claims to implement?
- Are the tests real, or do they pass without asserting anything?
- Can you prove to your auditor, your customer, or your board *what* was reviewed, *when*, and *by what engine* — with a result they can independently verify?

Vulnerability scanners give you a list of findings. SAST tools give you a dashboard. Neither gives you **proof**. Nucleus does.

---

## What Nucleus Verify produces

Every scan generates three permanent, cryptographically linked artifacts:

### 1. Ed25519-Signed Certificate
- Tamper-evident and independently verifiable
- Contains verdict, trust score, full scan scope, and findings summary
- Portable: embed in a README, attach to a PR, send to a customer, hand to an auditor
- Publicly verifiable at `verify.altermenta.com/c/NV-XXXXXX`
- Available as a PDF download for compliance packages and security reviews

### 2. Deterministic Proof Pack
- Same code + same seed = same hash, every time
- Anyone can independently replay the proof pack and get the exact same result
- Creates a cryptographic chain of custody no other tool in the market provides
- Challengeable: if a customer or auditor disputes a result, they can verify it themselves

### 3. Tamper-Evident Verification Ledger
- Every scan supersedes the last, delta-tracked and cryptographically linked
- Shows exactly what changed, what was introduced, and what was resolved between runs
- A complete, independently verifiable history of every scan from day one
- Built for auditors who need to demonstrate continuous verification over time

---

## Verdicts

| Verdict | Meaning |
|---|---|
| ✓ VERIFIED | All critical gates passed |
| ⚠ PARTIAL | Some gates passed — scope limitations noted |
| ✗ UNVERIFIED | One or more critical gates failed |

Every certificate includes **honest scope disclosure** — an explicit record of what Nucleus did *not* check. In a market full of tools that imply complete coverage, that honesty is itself a trust signal. Enterprise security teams know that any tool claiming 100% coverage is lying. Nucleus never does.

---

## Analysis depth

### Native operators — 1,400+
Hand-written operators tuned for low false positives across 6 languages and 42 operator families. These cover structural patterns, logic contracts, security posture, and AI-specific risks that no other tool detects.

**Supported languages:** Python · JavaScript · TypeScript · Java · Go · Rust · C · C++

### Semgrep engine integration — 3,800+ rules
The Security Deep pack runs the full Semgrep open source ruleset — 3,800+ battle-tested rules maintained by the security community, covering every major framework and updated continuously.

### CVE database — 200,000+ known vulnerabilities
The Dependency pack queries OSV and NVD in real time. Every dependency in your project is checked against 200,000+ known vulnerabilities with CVSS scoring, fix availability, and age analysis.

### CodeQL — enterprise tier
GitHub's own deep analysis engine. Used internally by Google, Microsoft, and NASA. The most thorough static analysis available at any price point. Enterprise tier only. Always runs async with email delivery on completion.

### Combined effective coverage: 205,000+ rules and vulnerabilities

---

## The eight enhanced scan packs

Packs run in **parallel** — total scan time equals the slowest pack selected, not the sum of all packs.

| Pack | What it analyses | Operators / Rules | Time |
|---|---|---|---|
| 🔒 Security Deep | OWASP Top 10, deep SAST, CWE mapping, Semgrep 3,800+ rules | 180 operators + 3,800 Semgrep | 3–8 min |
| 📦 Dependency & Supply Chain | CVE lookup (200K+ vulns), licence compliance, typosquatting, dependency provenance | 120 operators | 2–4 min |
| ⚖️ Compliance | GDPR, HIPAA, PCI-DSS, SOC2 structural patterns | 200 operators | 3–6 min |
| 🤖 AI Code Trust | Hallucination detection, AI drift, hollow code, LLM security patterns | 80 operators | 1–2 min |
| 📊 Code Quality & Debt | Technical debt scoring, dead code, cyclomatic complexity | 90 operators | 2–4 min |
| 🔏 Secrets Deep | Entropy-based detection, 100 secret pattern families | 100 operators | 1–2 min |
| 📋 Documentation | README quality, contract vs implementation match, onboarding score | 60 operators | 1–2 min |
| 🧪 Test Effectiveness | Assertion quality, assertion-less test detection, coverage estimation | 70 operators | 1–2 min |
| 🔬 CodeQL Deep *(Enterprise)* | GitHub's analysis engine — finds what everything else misses | 500+ queries | 15–90 min |

---

## Security Deep — what it covers

- **OWASP Top 10** — full coverage across all supported languages
- **CWE mapping** — findings mapped to Common Weakness Enumeration identifiers
- **Injection** — SQL, command, LDAP, XPath, template injection per framework
- **Authentication & session management** — broken auth, weak session tokens, insecure defaults
- **Cryptography** — weak algorithms, short key lengths, IV reuse, hardcoded keys
- **API security** — auth bypass, rate limiting gaps, mass assignment, IDOR patterns
- **Framework-specific patterns** — Django, Flask, FastAPI, Express, Spring, Hibernate, Next.js, React, and more
- **Language-specific deep dives** — memory safety (C/C++, Rust), concurrency issues (Go, Java), prototype pollution (JavaScript)

---

## Dependency & Supply Chain — what it covers

- **CVE detection** — direct and transitive dependencies checked against 200,000+ vulnerabilities
- **CVSS scoring** — Critical / High / Medium / Low with fix availability
- **Unfixed CVE age** — flags vulnerabilities unfixed for over 12 months
- **Typosquatting** — Levenshtein distance analysis against top-1,000 packages per ecosystem
- **Licence compliance** — full SPDX matrix, GPL contamination detection, AGPL in commercial contexts
- **Supply chain risk** — single-maintainer packages, abandoned dependencies, install script inspection
- **Dependency depth** — flags packages more than 10 hops from root
- **Lockfile integrity** — lockfile vs manifest discrepancy, missing integrity hashes

---

## AI Code Trust — unique to Nucleus

No other verification tool was built for the AI code era. This pack detects risks that only exist in AI-generated codebases:

- **Hallucination detection** — code that claims to implement something but doesn't
- **AI drift** — README and documentation claims that don't match actual implementation
- **Hollow code** — structurally present but logically empty functions
- **Assertion-less tests** — tests written by AI that pass without verifying anything
- **LLM security patterns** — prompt injection vectors, unsafe model output handling, insecure API key management in AI-integrated code

---

## Compliance pack — structural pattern detection

200 operators covering the four major compliance frameworks. Every finding on the compliance certificate includes the framework reference, the structural pattern detected, and the file location.

| Framework | Coverage |
|---|---|
| GDPR | PII exposure patterns, consent mechanisms, data retention, right to erasure |
| HIPAA | PHI handling patterns, audit logging, access control, transmission security |
| PCI-DSS | Cardholder data patterns, cryptographic controls, network segmentation indicators |
| SOC2 | Access control patterns, logging completeness, change management indicators |

> **Important:** Nucleus detects structural compliance patterns. This is not a compliance certification and does not replace a qualified auditor. Certificate language makes this clear on every scan.

---

## Enterprise — tailored verification

For enterprise customers, Nucleus goes beyond the standard pack set:

### Custom operator development
Our team works with your security and compliance teams to build operators specific to your internal coding standards, proprietary frameworks, and regulatory requirements. Custom operators are YAML-defined, version-controlled, and scoped to your organisation only.

### Custom rule upload
Enterprise customers can upload their own Semgrep-compatible YAML rule sets. Your internal security standards enforced automatically on every scan.

### Private deployment options
Nucleus can be deployed to scan private repositories with no code leaving your controlled environment. We clone, scan, and delete. Nothing is retained.

### Compliance pack customisation
Standard compliance packs cover GDPR, HIPAA, PCI-DSS, and SOC2. Enterprise customers can request additional framework coverage — CMMC for defence contractors, DORA for financial services, ISO 27001 structural patterns, and more.

### Volume certificate management
Enterprise accounts include a verification ledger dashboard — every certificate issued across your organisation, searchable, filterable, and exportable for audit packages.

### Dedicated onboarding
Enterprise accounts include direct onboarding support, integration assistance for CI/CD pipelines, and a named contact for ongoing support.

---

## How it works
```
1. Submit any repository — public URL, private token, ZIP upload, or API
2. Select your enhanced scan packs — run what your situation requires
3. Packs execute in parallel — total time = slowest pack selected
4. Receive your signed certificate, proof pack, and ledger entry
5. Share the public verification URL — anyone can independently verify it
6. Every future scan links to the last — building your tamper-evident history
```

---

## Pricing

| Plan | Includes | Price |
|---|---|---|
| Free | Standard scan, signed certificate, proof pack | Free |
| Plus | + 1 enhanced pack trial | $20/month |
| Business | All 8 enhanced packs, full ledger, PDF certificates | $50/seat/month |
| Enterprise | Everything + CodeQL, custom operators, private deployment, SLA | Contact us |

---

## Who it's for

| Sector | Value |
|---|---|
| **Fintech & Payments** | PCI-DSS structural evidence. CVE detection in payment libraries. Signed certificates for customer security reviews |
| **Healthcare & Life Sciences** | HIPAA structural pattern detection. PHI exposure risk. Audit trail for every scan |
| **AI companies** | The only tool built specifically to verify AI-generated code at structural depth |
| **Defence & Government** | CMMC-aligned structural checks. Tamper-evident chain of custody from day one |
| **Pre-IPO SaaS** | SOC2 structural evidence. Accelerate enterprise customer security reviews with a portable signed artifact |
| **Legal Technology** | Data handling pattern detection. Evidence of due diligence for regulatory purposes |
| **Indie developers** | Ship with confidence. Put a signed certificate in your README |

---

## Get started

👉 **[verify.altermenta.com](https://altermenta.com)**

✉️ Enterprise enquiries: [contact@altermenta.com](mailto:contact@altermenta.com)

---

*Nucleus Verify is a product of [Alter Menta Technologies](https://altermenta.com) · London, United Kingdom*

*Built for the AI code era — and every line written before it.*
