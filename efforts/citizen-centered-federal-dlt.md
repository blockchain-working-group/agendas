---
status: exploring
product: To be decided (a publication section, a playbook chapter, or a talk)
started_at: 2024-09-22
ended_at:
issue: https://github.com/blockchain-working-group/agendas/issues/31
---

# A Citizen-Centered Federal DLT (Working Draft)

> **Status: open thread, work in progress.**
> This is a starting point for discussion, not an official ACT-IAC or working group position.
> Contributions are welcome: add a question, challenge a claim, or fill in a gap.
>
> **How to contribute:** click the pencil icon on this file in GitHub to propose an edit (GitHub turns it into a pull request for review), or [open an issue](https://github.com/blockchain-working-group/agendas/issues/new) to discuss.
> New to GitHub? See the [README](../README.md#new-to-github).

Started by [@Dmicheal](https://github.com/Dmicheal) on November 2, 2025, in [issue #31](https://github.com/blockchain-working-group/agendas/issues/31), replying to these questions:

- In what ways is a federal DLT citizen-centered?
- Who would run it?
- Is it only federal, among two or more agencies, or does it extend to other trusted institutions or the public?
- What features would drive it, or be worth exploring?

The two replies are combined below, lightly reformatted from email, with the content unchanged.
It builds on the [Blockchain Playbook](https://github.com/blockchain-working-group/blockchain-playbook).

### Open questions

Good places to start contributing:

- What would "done" look like for this thread: a publication section, a playbook chapter, or a talk?
- Which of the models in section 2 is realistic today, and what would have to change for the others?
- Which existing federal programs (for example, mobile driver's licenses or Login.gov) already cover parts of the identity layer?

## 1. What makes a federal DLT "citizen-centered"?

A citizen-centered design means the ledger's architecture, governance, and data practices serve the individual first, not just the bureaucracy or private intermediaries.

| Design feature | Citizen-centered implication |
|---|---|
| Self-sovereign identity (SSI) | Citizens own and control their digital identity, not the agency. This allows selective disclosure and privacy-preserving authentication. |
| Transparency and auditability | Citizens can independently verify transactions (e.g., where their tax payment, benefits, or healthcare data flow). |
| Data minimization and consent | Only essential data are shared, and always with user consent, cryptographically verifiable. |
| Portability across agencies | Citizens don't repeatedly fill out forms. Their verified credentials can move securely across government systems. |
| Open participation | Citizens or civic tech developers can build tools or interfaces using open APIs or smart contracts (within regulated boundaries). |

The core idea: trust by design, not trust by authority.

## 2. Who would run the federal DLT?

That depends on governance philosophy.

| Model | Who runs it | Pros | Cons |
|---|---|---|---|
| Federal consortium ledger | Jointly run by agencies (e.g., Treasury, SSA, IRS, DHS) under a federal governance board | Strong interoperability, consistent standards | Bureaucratic, slower innovation |
| Hybrid with private validators | Public–private nodes (banks, universities, regulated firms) | Reduces single point of control, increases resilience | Complex trust framework, liability questions |
| Fully federal (centralized DLT) | Managed by one core federal agency (e.g., GSA, NIST, or Treasury) | Clear accountability, simpler to secure | Less resilient, possible over-centralization |
| Citizen node participation (future vision) | Citizens or civic organizations run read-only or validation nodes | Maximum transparency and resilience | Needs sophisticated privacy and regulatory guardrails |

The U.S. would likely start with a federated DLT consortium, governed by federal agencies but technically interoperable with "trusted partners."

## 3. Scope: federal-only or extended?

Think of it as a trust spectrum.

| Scope | Participants | Use cases |
|---|---|---|
| Intra-federal (narrow) | Only federal agencies | Identity, records, grants, supply chain |
| Inter-governmental (broader) | Federal, state, and local governments | Driver's license ↔ passport data, property tax ↔ IRS reconciliation |
| Federated public trust layer (broadest) | Adds trusted private institutions (banks, universities, healthcare providers) | Public identity, payment rails, credentials, ESG or compliance reporting |
| Publicly verifiable (open DLT) | The public can verify hashes or data proofs | Transparency and public accountability, with limited data exposure for privacy |

Realistically, the U.S. might evolve from intra-federal to inter-governmental to selective public trust extension, depending on policy maturity and cybersecurity confidence.

## 4. Features worth exploring

| Category | Potential feature | Why it matters |
|---|---|---|
| Identity layer | Decentralized digital ID (DID) system using SSI standards | Citizen-controlled identity is the foundation of trust |
| Access control | Role- and consent-based access via verifiable credentials | Data sovereignty and least-privilege enforcement |
| Privacy | Zero-knowledge proofs (ZKPs), selective disclosure | Enables transparency without exposing sensitive info |
| Governance | Multi-stakeholder, DAO-like structure (auditable rules) | Distributes decision-making power |
| Interoperability | Cross-ledger protocols (like Hyperledger Aries, W3C DIDComm) | Avoids vendor lock-in, supports agency independence |
| Smart contracts | Automated compliance and benefits issuance | Reduces bureaucracy, enforces fairness |
| Audit and transparency | Cryptographic proofs of public spending or grants | Boosts public trust and accountability |
| Disaster resilience | Distributed nodes across regions and agencies | Improves uptime and disaster recovery |

### Conceptual example: a Citizen Ledger ID (CLID)

- Issued once by a federal identity authority.
- Citizens use it to sign or verify actions (filing taxes, receiving benefits, or voting) without sharing raw data.
- Agencies verify authenticity via the DLT, not a central database lookup.
- A public dashboard shows aggregated, privacy-preserving stats of how funds or programs are running.

A citizen-centered federal DLT is not just about decentralization; it's about redistributing trust from hierarchical institutions to cryptographic, interoperable, transparent frameworks that still respect privacy, law, and security.
Done right, it could become the digital equivalent of the Constitution's checks and balances: trust engineered, not assumed.

## 5. Extending the Blockchain Playbook

The Playbook lays out five main pillars that any federal DLT must consider:

- **Mission alignment**: does blockchain add measurable value to the agency's mission?
- **Governance and legal compliance**: roles, responsibilities, and legal implications must be defined.
- **Technology selection**: interoperable, secure, standards-based, and scalable.
- **Data management and privacy**: protect citizen data through appropriate access and anonymization.
- **Performance and measurement**: define KPIs and success metrics early.

This sets up a trustable, federal-grade DLT backbone, but it is still largely institution-centered, focusing on inter-agency coordination.
A citizen-centered layer on top redefines who the primary user and beneficiary is.

| Federal Playbook focus | Citizen-centered extension |
|---|---|
| Inter-agency interoperability | Citizen identity and data portability across agencies |
| Security and compliance | Citizen control and consent verification |
| Ledger governance | Participatory governance and civic oversight |
| Data standards | Verifiable credentials and open APIs for citizen access |
| Efficiency metrics | Equity, accessibility, and trust metrics |

This reframes blockchain not just as infrastructure for agencies but as a civic utility, like a secure, digital "public square" for verified interactions between people and the state.

### Five citizen-centered pillars

1. **Digital self-sovereignty.**
   Citizens control their digital identity, verified credentials, and data-sharing permissions.
   Government systems verify authenticity without owning the underlying data (via decentralized identifiers and verifiable credentials).
2. **Participatory transparency.**
   Key government transactions (grants, budgets, procurements) are published as verifiable proofs on the ledger.
   Citizens or civic tech groups can audit without compromising security or privacy.
3. **Universal access and inclusion.**
   Every citizen has access to their own digital wallet for interacting with agencies (benefits, records, licenses) without needing specialized tech or intermediaries.
   Accessibility design ensures equity for low-bandwidth, low-literacy users.
4. **Civic governance participation.**
   Citizens can observe and comment on smart contract logic governing public resource flows.
   Governance could include a "public validator council" representing civic and academic institutions.
5. **Resilience through shared trust.**
   Nodes are distributed not only across agencies but also among trusted civic institutions (universities, certified NGOs, or regional governments).
   This decentralizes resilience and enhances cross-sector trust.

### Technical and governance features to add

| Category | Recommended enhancement | Why it matters |
|---|---|---|
| Identity layer | W3C-compliant DIDs and Verifiable Credentials managed by citizens | Replaces redundant identity verification cycles |
| Privacy | Zero-knowledge proofs and differential privacy | Enables public verifiability while protecting personal data |
| Governance | DAO-inspired "Federal Trust Council" with public reporting and versioning | Creates transparent change management for smart contracts and policies |
| Access layer | Citizen-facing "MyLedger.gov" portal and mobile wallet | Turns DLT from backend infrastructure into a front-end civic experience |
| Measurement | Trust Index: how transparent, accessible, and verifiable each agency's processes are | Encourages accountability through measurable trust metrics |

### Implementation spectrum

Each phase builds on the last.

1. **Federal integration (Playbook baseline)**: internal pilots in supply chain, record provenance, and payments, with a single-agency focus.
2. **Inter-agency and trusted partners**: shared ledger infrastructure across agencies (IRS, SSA, DHS), integrated with regulated private entities (banks, healthcare providers).
3. **Citizen interaction (citizen-centered DLT)**: citizens hold verifiable digital credentials, data exchange is consent-driven, and there is a transparent audit trail for how funds, benefits, or records move through the system.

### Conceptual architecture (layer model)

- Layer 0: cryptographic trust layer (DLT protocol, consensus, nodes)
- Layer 1: federal interoperability layer (agency-to-agency data and process flow)
- Layer 2: citizen identity and consent layer (SSI, verifiable credentials)
- Layer 3: application layer (public dashboards, wallets, and APIs)
- Layer 4: governance and oversight layer (smart policy contracts, civic audit, public reporting)

### Why this matters

Adding the citizen-centered layer turns federal trust from a compliance function into a living interface between citizens and the state.
It makes trust measurable, participation digital, and accountability verifiable: not just e-government, but verifiable government.
