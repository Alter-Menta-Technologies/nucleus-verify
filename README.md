# Nucleus Verify

**Signed proof that your code was reviewed. Independently verifiable. Forever.**

[![Verified by Nucleus](https://verify.altermenta.com/badge/NV-078123)](https://verify.altermenta.com/c/NV-078123)

🌐 [verify.altermenta.com](https://verify.altermenta.com) · ✉️ [contact@altermenta.com](mailto:contact@altermenta.com) · 🏢 [Alter Menta Technologies](https://altermenta.com)

---

## The problem

AI writes code faster than anyone can review it. Code looks correct. Tests pass. But three questions remain unanswered:

- **Does it actually do what it claims?** Hollow functions, assertion-less tests, and hallucinated implementations are invisible to linters.
- **Can you prove it was reviewed?** Not a dashboard. Not a score. An independently verifiable artifact that anyone — an auditor, a customer, a board — can check themselves.
- **What changed between versions?** A cryptographic chain of custody showing exactly what was introduced, resolved, or unchanged across every scan.

Vulnerability scanners give you a list. SAST tools give you a dashboard. Neither gives you **proof**.

---

## What a scan produces

Every scan generates three permanently linked artifacts:

### Ed25519-Signed Certificate
A tamper-evident certificate containing the verdict, trust score, full scan scope, and findings summary. Embed it in a README, attach it to a PR, send it to a customer, or hand it to an auditor. Publicly verifiable at `verify.altermenta.com/c/NV-XXXXXX`. Available as a PDF download for compliance packages.

### Deterministic Proof Pack
Same code + same seed = same hash, every time. Anyone can independently replay the proof pack and arrive at the exact same result. This creates a cryptographic chain of custody that no other tool in the market provides. If a customer disputes a result, they can verify it themselves.

### Tamper-Evident Verification History
Every scan supersedes the last — delta-tracked and cryptographically linked. The history shows exactly what changed, what was introduced, and what was resolved between runs. Built for auditors who need to demonstrate continuous verification over time.

---

## Verdicts

| Verdict | Meaning |
|---|---|
| ✓ **VERIFIED** | All five critical gates passed |
| ⚠ **PARTIAL** | Most gates passed — scope limitations noted |
| ✗ **UNVERIFIED** | One or more critical gates failed |

Every certificate explicitly discloses what Nucleus did **not** check. In a market full of tools that imply complete coverage, that honesty is itself a trust signal.

---

## Verification gates

Five gates run on every scan. Each is binary — pass or fail, no partial credit.

| Gate | What it checks |
|---|---|
| `gate_v2` | Detectable code structure — functions, classes, imports, routes |
| `gate_d` | Determinism — same prompt and seed produces identical hash on replay |
| `contract` | Contract adherence — all claimed capabilities have supporting code evidence |
| `build` | Build integrity — source files compile without syntax errors |
| `gate_s` | Structural integrity — cross-file references and architecture consistency |

---

## Engine quality

Tested against 50 of the most widely recognised open source repositories — Flask, Django, Express, Lodash, Gin, Tokio, Underscore, and more.

| Metric | Result |
|---|---|
| Repositories benchmarked | 915 |
| Consistency errors | **0** |
| False positive rate on Tier 1 repos | **0.0%** |
| Credibility killer findings across 50 repos | **0** |
| Battery tests | 526 passed, 0 failed |
| Total tests | 2,955 passed, 0 failed |
| Operators verified | 431 / 432 |

Determinism is mathematically guaranteed and cryptographically proven — not a claim. The same code always produces the same hash. 915 repositories confirm this with zero exceptions.

---

## Analysis depth

### Standard scan — 432 operators across 31 families

Hand-written deterministic operators covering:

- **Security** — injection, authentication, cryptography, session management, secrets, API surface
- **AI code risks** — hallucination, hollow code, assertion-less tests, LLM security patterns
- **Compliance patterns** — mapped to 11 frameworks across every finding
- **Code quality** — complexity, dead code, error handling, scaffolding detection
- **Supply chain** — CVE detection, typosquatting, lockfile integrity, licence compliance
- **Infrastructure** — CI/CD, Kubernetes, secrets in config, hardcoded credentials

**Supported languages:** Python · JavaScript · TypeScript · Go · Java · C · C++ · C# · Ruby · Rust · PHP · Swift · Kotlin · Scala · Dart · Shell · Perl · Lua · R — plus 65+ via Semgrep

### Enhanced packs — 249 additional operators

Nine specialist packs that run in parallel. Total scan time equals the slowest pack selected, not the sum.

| Pack | Focus | Time |
|---|---|---|
| 🔒 **Security Deep** | OWASP Top 10, CWE mapping, Semgrep 3,800+ rules | 3–8 min |
| 📦 **Dependency & Supply Chain** | 250,238 CVEs, licence compliance, supply chain risk | 2–4 min |
| ⚖️ **Compliance** | 11 frameworks — GDPR, HIPAA, PCI-DSS, DORA, FCA, PSD2, SWIFT CSP, ISO 27001, SOC2, OWASP LLM, NIST AI RMF | 3–6 min |
| 🤖 **AI Code Trust** | Hallucination, AI drift, hollow code, LLM security | 1–2 min |
| 📊 **Code Quality & Debt** | Technical debt scoring, dead code, cyclomatic complexity | 2–4 min |
| 🔏 **Secrets Deep** | Entropy-based detection, 100 secret pattern families | 1–2 min |
| 📋 **Documentation** | README quality, contract vs implementation match, onboarding score | 1–2 min |
| 🧪 **Test Effectiveness** | Assertion quality, assertion-less test detection, coverage estimation | 1–2 min |
| 🔬 **CodeQL Deep** *(Enterprise)* | GitHub's analysis engine — finds what everything else misses | 15–90 min |

### CVE database — 250,238 vulnerabilities

Synced from OSV across PyPI, npm, Go, crates.io, Maven, and NuGet. Every dependency checked against known vulnerabilities with CVSS scoring and fix availability.

---

## Compliance coverage

11 frameworks mapped to findings automatically on every standard scan. No additional configuration required.

| Framework | Jurisdiction | In Force |
|---|---|---|
| GDPR | European Union | 2018 |
| HIPAA | United States | 1996 |
| PCI-DSS v4.0 | Global Financial | 2024 |
| SOC2 | Global | — |
| DORA | European Union | January 2025 |
| FCA Operational Resilience | United Kingdom | 2022 |
| PSD2 / Open Banking | EU + UK | 2018 |
| SWIFT CSP CSCF v2024 | Global Financial | 2024 |
| ISO 27001:2022 | Global | 2022 |
| OWASP LLM Top 10 | Global | 2025 |
| NIST AI RMF 1.0 | US / Global | 2023 |

> Nucleus detects structural compliance patterns. This is not a compliance certification and does not replace a qualified auditor. Every certificate makes this explicit.

---

## How it works

```
1. Submit — public URL, private token, ZIP upload, or API
2. Select packs — choose what your situation requires
3. Scan — packs run in parallel, results in minutes
4. Receive — signed certificate, proof pack, verification history entry
5. Share — public verification URL anyone can independently check
6. Repeat — every future scan links to the last, building your chain of custody
```

---

## GitHub Action

Add verification to your CI/CD pipeline in one step:

```yaml
- name: Verify with Nucleus
  uses: altermenta/nucleus-verify-action@v1
  with:
    api_key: ${{ secrets.NUCLEUS_API_KEY }}
    repo: ${{ github.repository }}
```

---

## Pricing

| Plan | What's included | Price |
|---|---|---|
| **Free** | Standard scan · Proof pack · Verification history | Free |
| **Plus** | + Full result JSON · Report PDF · 1 enhanced pack trial | $20 / month |
| **Business** | All 8 enhanced packs · Signed certificate PDF · Full ledger | $50 / seat / month |
| **Enterprise** | Everything + CodeQL · Custom operators · Private deployment · SLA | Contact us |

---

## Enterprise

For organisations that need to go further:

- **Custom operators** — built to your internal coding standards, proprietary frameworks, and regulatory requirements. Version-controlled and scoped to your organisation only.
- **Custom rule upload** — upload your own Semgrep-compatible YAML rule sets. Your internal security standards enforced automatically on every scan.
- **Private deployment** — scan private repositories with no code leaving your controlled environment. Clone, scan, delete. Nothing retained.
- **Extended compliance** — additional framework coverage beyond the standard 11, including bespoke regulatory requirements.
- **Volume certificate management** — every certificate issued across your organisation, searchable, filterable, and exportable for audit packages.
- **Dedicated onboarding** — direct support, CI/CD integration assistance, and a named contact.

---

## Who it's for

| Sector | Why Nucleus |
|---|---|
| **Fintech & Payments** | DORA, FCA, PSD2, SWIFT CSP structural evidence. CVE detection in payment libraries. Signed certificates for customer security reviews. |
| **Healthcare & Life Sciences** | HIPAA structural pattern detection. PHI exposure risk. Audit trail for every scan. |
| **AI companies** | The only verification tool built specifically for AI-generated code. Detects hollow functions, assertion-less tests, and hallucinated implementations. |
| **Defence & Government** | Tamper-evident chain of custody from day one. Independently verifiable results. |
| **Pre-IPO SaaS** | SOC2, ISO 27001 structural evidence. Accelerate enterprise security reviews with a portable signed artifact. |
| **Indie developers** | Ship with confidence. Put a signed certificate in your README. |

---

## What Nucleus does not verify

Every certificate explicitly discloses the boundaries of what static structural verification can claim:

- Semantic correctness of business logic
- Runtime behaviour under production load
- Dynamic security testing (fuzzing, DAST, penetration testing)
- Runtime performance benchmarking
- Concurrency correctness under load
- Data integrity under concurrent writes

This is not a weakness. It is why the certificate means something.

---

## Get started

**[verify.altermenta.com](https://verify.altermenta.com)** — scan your first repository free in under 60 seconds.

---

*Nucleus Verify v1.1.1 · Deterministic verification for the AI era*
*Alter Menta Technologies Ltd · 124 City Road, London EC1V 2NX · Reg. 17036841*

