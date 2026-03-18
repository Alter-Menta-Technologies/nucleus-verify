Nucleus Verify

Signed proof that your code was reviewed. Independently verifiable. Forever.

🌐 verify.altermenta.com · ✉️ contact@altermenta.com · 🏢 Alter Menta Technologies

The problem no existing tool solves
The way software is written has changed permanently. AI generates thousands of lines in minutes. Code looks correct. Tests pass. But:

Does the code actually implement what it claims to implement?
Are the tests real, or do they pass without asserting anything?
Can you prove to your auditor, your customer, or your board what was reviewed, when, and by what engine — with a result they can independently verify?

Vulnerability scanners give you a list of findings. SAST tools give you a dashboard. Neither gives you proof. Nucleus does.

What Nucleus Verify produces
Every scan generates three permanent, cryptographically linked artifacts:
1. Ed25519-Signed Certificate

Tamper-evident and independently verifiable
Contains verdict, trust score, full scan scope, and findings summary
Portable: embed in a README, attach to a PR, send to a customer, hand to an auditor
Publicly verifiable at verify.altermenta.com/c/NV-XXXXXX
Available as a PDF download for compliance packages and security reviews

2. Deterministic Proof Pack

Same code + same seed = same hash, every time
Anyone can independently replay the proof pack and get the exact same result
Creates a cryptographic chain of custody no other tool in the market provides
Challengeable: if a customer or auditor disputes a result, they can verify it themselves

3. Tamper-Evident Verification History

Every scan supersedes the last, delta-tracked and cryptographically linked
Shows exactly what changed, what was introduced, and what was resolved between runs
A complete, independently verifiable history of every scan from day one
Built for auditors who need to demonstrate continuous verification over time


Verdicts
VerdictMeaning✓ VERIFIEDAll critical gates passed⚠ PARTIALSome gates passed — scope limitations noted✗ UNVERIFIEDOne or more critical gates failed
Every certificate includes honest scope disclosure — an explicit record of what Nucleus did not check. In a market full of tools that imply complete coverage, that honesty is itself a trust signal. Enterprise security teams know that any tool claiming 100% coverage is lying. Nucleus never does.

Engine quality
Tested against 50 of the most widely recognised open source repositories across 7 languages including Flask, Express, Django, Lodash, Gin, Tokio, and Underscore.
MetricResultRepositories benchmarked915Consistency errors0 — same code always produces the same hashFalse positive rate on Tier 1 repos0.0%Credibility killer findings0 across 50 reposBattery tests526 passed, 0 failedTotal tests2,955 passed, 0 failedOperator coverage431 / 432 operators verified
Determinism is mathematically guaranteed and cryptographically proven — not a claim.

Analysis depth
Standard operators — 432
Hand-written deterministic operators across 31 families, tuned for low false positives. These cover structural patterns, security posture, AI-specific risks, compliance patterns, and code quality that no other tool detects. Built with a comprehensive exception library covering known ecosystem patterns across every supported language.
Supported languages: Python · JavaScript · TypeScript · Go · Java · C · C++ · C# · Ruby · Rust · PHP · Swift · Kotlin · Scala · Dart · Shell · Perl · Lua · R — plus 65+ languages via Semgrep
Enhanced pack operators — 249
Nine specialist packs running in parallel. Each pack is independently scoped and opt-in.
Semgrep engine — 3,800+ rules
The Security Deep pack runs the full Semgrep open source ruleset — battle-tested rules maintained by the security community, covering every major framework and updated continuously.
CVE database — 250,238 known vulnerabilities
Synced from OSV across PyPI, npm, Go, crates.io, Maven, and NuGet. Every dependency checked against known vulnerabilities with CVSS scoring and fix availability.
CodeQL — enterprise tier
GitHub's own deep analysis engine. The most thorough static analysis available at any price point. Enterprise tier only. Always runs async with email delivery on completion.
Combined effective coverage: 250,000+ rules and vulnerabilities

The eight enhanced scan packs
Packs run in parallel — total scan time equals the slowest pack selected, not the sum of all packs.
PackWhat it analysesTime🔒 Security DeepOWASP Top 10, deep SAST, CWE mapping, Semgrep 3,800+ rules3–8 min📦 Dependency & Supply ChainCVE lookup (250K+ vulns), licence compliance, typosquatting, supply chain risk2–4 min⚖️ ComplianceGDPR, HIPAA, PCI-DSS, SOC2, DORA, FCA, PSD2, SWIFT CSP, ISO 27001, OWASP LLM, NIST AI RMF3–6 min🤖 AI Code TrustHallucination detection, AI drift, hollow code, LLM security patterns1–2 min📊 Code Quality & DebtTechnical debt scoring, dead code, cyclomatic complexity2–4 min🔏 Secrets DeepEntropy-based detection, 100 secret pattern families1–2 min📋 DocumentationREADME quality, contract vs implementation match, onboarding score1–2 min🧪 Test EffectivenessAssertion quality, assertion-less test detection, coverage estimation1–2 min🔬 CodeQL Deep (Enterprise)GitHub's analysis engine — finds what everything else misses15–90 min

Security Deep — what it covers

OWASP Top 10 — full coverage across all supported languages
CWE mapping — findings mapped to Common Weakness Enumeration identifiers
Injection — SQL, command, LDAP, XPath, template injection per framework
Authentication & session management — broken auth, weak session tokens, insecure defaults
Cryptography — weak algorithms, short key lengths, IV reuse, hardcoded keys
API security — auth bypass, rate limiting gaps, mass assignment, IDOR patterns
Framework-specific patterns — Django, Flask, FastAPI, Express, Spring, Gin, Next.js, React, and more
Language-specific deep dives — memory safety (C/C++, Rust), concurrency issues (Go, Java), prototype pollution (JavaScript)


Dependency & Supply Chain — what it covers

CVE detection — direct and transitive dependencies checked against 250,238 known vulnerabilities
CVSS scoring — Critical / High / Medium / Low with fix availability
Unfixed CVE age — flags vulnerabilities unfixed for over 12 months
Typosquatting — Levenshtein distance analysis against top packages per ecosystem
Licence compliance — full SPDX matrix, GPL contamination detection, AGPL in commercial contexts
Supply chain risk — single-maintainer packages, abandoned dependencies, install script inspection
Lockfile integrity — lockfile vs manifest discrepancy, missing integrity hashes


AI Code Trust — unique to Nucleus
No other verification tool was built for the AI code era. This pack detects risks that only exist in AI-generated codebases:

Hallucination detection — code that claims to implement something but doesn't
AI drift — README and documentation claims that don't match actual implementation
Hollow code — structurally present but logically empty functions
Assertion-less tests — tests written by AI that pass without verifying anything
LLM security patterns — prompt injection vectors, unsafe model output handling, insecure API key management in AI-integrated code


Compliance pack — 11 frameworks
Structural pattern detection mapped to 11 compliance frameworks. Every finding on the compliance certificate includes the framework reference, the structural pattern detected, and the file location.
FrameworkJurisdictionGDPREuropean UnionHIPAAUnited StatesPCI-DSSGlobal FinancialSOC2GlobalDORAEuropean UnionFCA Operational ResilienceUnited KingdomPSD2 / Open BankingEU + UKSWIFT CSPGlobal FinancialISO 27001:2022GlobalOWASP LLM Top 10GlobalNIST AI RMF 1.0US / Global

Important: Nucleus detects structural compliance patterns. This is not a compliance certification and does not replace a qualified auditor. Certificate language makes this clear on every scan.


Verification gates
Every scan runs five gates. Verdicts are binary — a gate either passes or fails. No partial credit on critical gates.
GateWhat it checksgate_v2Detectable code structure — functions, classes, imports, routesgate_dDeterminism — same prompt + seed produces identical hash on replaycontractContract adherence — all claimed capabilities have supporting code evidencebuildBuild integrity — source files compile without syntax errorsgate_sStructural integrity — cross-file references and architecture consistency

Enterprise — tailored verification
For enterprise customers, Nucleus goes beyond the standard pack set:
Custom operator development
Our team works with your security and compliance teams to build operators specific to your internal coding standards, proprietary frameworks, and regulatory requirements. Custom operators are version-controlled and scoped to your organisation only.
Custom rule upload
Enterprise customers can upload their own Semgrep-compatible YAML rule sets. Your internal security standards enforced automatically on every scan.
Private deployment options
Nucleus can be deployed to scan private repositories with no code leaving your controlled environment. We clone, scan, and delete. Nothing is retained.
Compliance pack customisation
Standard compliance packs cover 11 frameworks. Enterprise customers can request additional coverage tailored to their regulatory environment.
Volume certificate management
Enterprise accounts include a verification history dashboard — every certificate issued across your organisation, searchable, filterable, and exportable for audit packages.
Dedicated onboarding
Enterprise accounts include direct onboarding support, CI/CD integration assistance, and a named contact for ongoing support.

How it works
1. Submit any repository — public URL, private token, ZIP upload, or API
2. Select your enhanced scan packs — run what your situation requires
3. Packs execute in parallel — total time = slowest pack selected
4. Receive your signed certificate, proof pack, and verification history entry
5. Share the public verification URL — anyone can independently verify it
6. Every future scan links to the last — building your tamper-evident history

Pricing
PlanIncludesPriceFreeStandard scan, proof pack, verification historyFreePlus+ Full result JSON, Report PDF, 1 enhanced pack trial$20/monthBusinessAll 8 enhanced packs, signed certificate PDF, full ledger$50/seat/monthEnterpriseEverything + CodeQL, custom operators, private deployment, SLAContact us

GitHub Action
Add verification to your CI/CD pipeline in one step:
yaml- name: Verify with Nucleus
  uses: altermenta/nucleus-verify-action@v1
  with:
    api_key: ${{ secrets.NUCLEUS_API_KEY }}
    repo: ${{ github.repository }}

Who it's for
SectorValueFintech & PaymentsPCI-DSS, DORA, FCA, PSD2, SWIFT structural evidence. CVE detection in payment libraries. Signed certificates for customer security reviewsHealthcare & Life SciencesHIPAA structural pattern detection. PHI exposure risk. Audit trail for every scanAI companiesThe only tool built specifically to verify AI-generated code at structural depthDefence & GovernmentTamper-evident chain of custody from day one. Independently verifiable resultsPre-IPO SaaSSOC2, ISO 27001 structural evidence. Accelerate enterprise customer security reviews with a portable signed artifactLegal TechnologyData handling pattern detection. Evidence of due diligence for regulatory purposesIndie developersShip with confidence. Put a signed certificate in your README

What Nucleus does not verify
Every certificate explicitly discloses what was not checked:

Semantic correctness of business logic
Runtime behaviour under production load
Dynamic security testing (fuzzing, DAST, penetration testing)
Runtime performance benchmarking
Concurrency correctness under load
Data integrity under concurrent writes

This disclosure is not a weakness. It is the honest boundary of what static structural verification can claim — and the reason the certificate means something.

Get started
verify.altermenta.com — scan your first repository free in under 60 seconds.

Nucleus Verify v1.1.1 · Deterministic verification for the AI era · Alter Menta Technologies Ltd · 124 City Road, London EC1V 2NX · Reg. 17036841
👉 **[verify.altermenta.com](https://altermenta.com)**

✉️ Enterprise enquiries: [contact@altermenta.com](mailto:contact@altermenta.com)
