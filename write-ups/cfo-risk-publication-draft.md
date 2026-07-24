# Blockchain Risk and Adoption in the Public Sector
## A Role-Based Guide Structured on the NIST Risk Management Framework

**Status: working draft — open for contribution.**
Tracked in [issue #50](https://github.com/blockchain-working-group/agendas/issues/50).
Timely context and motivating events are kept separate in the [scoping proposal](2026-07-10-cfo-publication-proposal.md) and the group's weekly updates, so this document can stay evergreen.
Open questions are marked throughout — they are invitations, not gaps.
If one speaks to your experience, claim it in the issue.

**Who this is for.**
Blockchain adoption in a public-sector body is not one person's decision — it moves through a chain of roles, each carrying a different piece of the same lifecycle.
This guide is written for that whole chain: Deputy Secretaries and Administrators who authorize; CFOs, CIOs, and Directors who own risk, systems, and programs; Project Managers and Directors who build; and the Analysts, Specialists, and Technicians who inventory, assess, and operate.
Part II maps each role to the steps it owns. No reader needs to read as though they were someone else — find your role, and the lifecycle tells you your part in it.

**Why NIST RMF.**
Public-sector agencies already work inside a risk vocabulary they know: the NIST Risk Management Framework (SP 800-37 Rev. 2).
Rather than invent a parallel framework for digital assets and blockchain systems, this guide runs the question through the RMF lifecycle these agencies already run for their information systems.
The payoff is shared language across roles: the exposure or use-case inventory becomes a *categorization* input, custody, counterparty, and security diligence become *control selection*, the "do no harm" memo becomes part of the *authorization* package, and the oversight cadence becomes *continuous monitoring*.
It also gives distinct roles a common map — a CFO, a CIO, and an authorizing Deputy Secretary can each find their step and see how their work hands off to the next.
This is a mapping, not a claim of compliance — RMF was written for information systems, and neither a digital asset holding nor a blockchain deployment is exactly a system. Where the analogy strains, we say so.

---

# Part I — Executive Summary (one page)

Blockchain and digital assets are entering the infrastructure that public agencies already depend on — as exposure that touches finance and operations from outside, and as systems agencies are now asked to build and adopt.
A public-sector leader does not need an opinion about the technology to have an obligation regarding it.
The duty of care is unchanged; the surface it applies to has grown.

The first obligation is **do no harm**.
Before any question of opportunity, the responsible official must be able to answer: where does my organization already touch this, and what could go wrong there?
Most organizations have exposure they have not inventoried — through vendors, allocations, unclaimed property, payment processors, or counterparties — and unexamined exposure is where failures start.

This guide runs that obligation through the **seven steps of the NIST Risk Management Framework**, each phrased as a question the responsible role answers about their own organization (Part II says which role owns which step):

1. **Prepare** — Who owns digital asset risk here, and what is our risk tolerance?
2. **Categorize** — Where do digital assets touch us, and how much would it matter if each went wrong?
3. **Select** — Which controls — custody, counterparty, compliance — do we require for each exposure?
4. **Implement** — Are those controls actually in place and documented?
5. **Assess** — Has someone independent confirmed the controls work?
6. **Authorize** — Has a named senior official accepted the residual risk, in writing?
7. **Monitor** — Who watches this continuously, and what does oversight see, how often?

The steps are ordered deliberately, as RMF orders them: you cannot select controls for exposure you have not categorized, cannot categorize exposure you have not inventoried in Prepare, and cannot authorize what has not been assessed.
Work from the bottom up; report from the top down.

Cutting across all seven steps are five **risk surfaces** — Exposure, Custody, Counterparty, Compliance, Governance — the specific places a finance organization gets hurt. The RMF steps are the *process*; the five surfaces are *what the process examines*. Part III presents the steps; each step names the surfaces it addresses.

The recommendation of this guide is modest and specific: **complete the Prepare and Categorize steps, then decide.**
An organization that has run the lifecycle can decline to hold a digital asset or build a ledger — and that is a defensible position, the RMF equivalent of a documented decision not to authorize.
An organization that has not holds a position by accident, and accident is not a defense.

---

# Part II — Overview for Leadership

## Who this is for: roles and the steps they own

Blockchain adoption is a relay, not a solo act. The RMF lifecycle is what hands the baton from one role to the next — an authorizing official cannot accept risk an analyst never categorized, and a project manager cannot implement controls a specialist never selected.
The table below assigns each role its center of gravity in the lifecycle. Roles overlap on purpose; the point is that everyone can find where they own the work and where they receive or hand off.

| Role | Center of gravity in the RMF lifecycle | What they own |
|---|---|---|
| **Deputy Secretaries / Administrators** | Authorize | Accepting residual risk on the record; the "go / no-go" at the right altitude. |
| **CFOs** | Prepare · Categorize · Authorize | Financial-exposure inventory, risk tolerance, fiduciary sign-off, total cost of ownership. |
| **CIOs** | Prepare · Select · Monitor | System ownership, control selection, security posture, continuous monitoring. |
| **Directors** (program/business) | Prepare · Monitor | Purpose and foundation, oversight cadence, organizational-change ownership. |
| **Project Managers / Directors** | Implement | Building and deploying the solution; delivery, devops, schedule, and dependencies. |
| **Analysts** | Categorize · Assess | Exposure and use-case inventory, impact/risk-tier rating, evaluation of findings. |
| **Specialists** (security, compliance, legal) | Select · Assess | Control design, regulatory mapping, independent assessment, formal verification. |
| **Technicians** | Implement · Monitor | Operating the system — key ceremonies, node ops, upgrades, monitoring instrumentation. |

Two things to notice.
First, **the same document serves every role** because they share one spine: a CFO reads Categorize as an exposure inventory, an analyst reads it as a risk-tiering task, and a Deputy Secretary reads its output as an input to Authorize.
Second, **no step belongs to only one role** — Prepare in particular is shared across the executive tier, because that is where accountability is assigned before anyone touches an asset or a ledger.
Each RMF step in Part III opens with a **"Who owns this step"** line so you can jump to your part.

> **Open question (for contributors):** Does this role-to-step mapping match how real agencies actually distribute this work? Corrections from practitioners — especially where a role we placed is wrong for your jurisdiction — would sharpen this table.


## Why this is a duty matter, not a technology matter

Every persona in the table above carries a duty that predates this technology: the authorizing official's duty to accept risk knowingly, the CIO's duty of due care over systems, the analyst's duty of accurate assessment.
For the CFO persona specifically, that duty is fiduciary — and it is worth stating plainly, because finance is where the obligation is oldest and most tested.

Fiduciary duty attaches to care, loyalty, and prudence in handling assets and obligations — not to any asset class in particular.
When an asset class moves from the periphery into regulated market infrastructure, the prudent-person standard moves with it.
"We don't do crypto" was once a complete risk posture; once tokenized instruments settle through the same market utilities as conventional securities, it no longer describes anything.
The same logic generalizes to the other roles: a duty of care does not exempt a technology because it is new — it attaches the moment the technology touches the organization's obligations.

Three shifts drive the change, stated here without dates because the direction — not the timing — is what matters:

- **Infrastructure convergence.** Tokenized versions of conventional instruments (government debt, funds, equities) are being handled by regulated clearing and settlement infrastructure, not just crypto-native venues.
- **Regulatory formalization.** Regimes for stablecoins, custody, and market structure are moving from enforcement actions and guidance toward formal rules — which means compliance obligations with dates and examiners.
- **Balance-sheet arrival.** Treasuries, pensions, and endowments — including public ones — are making explicit hold/don't-hold decisions, and those decisions are being reviewed by councils, boards, and rating agencies.

## What "do no harm" means operationally

Harm to a finance organization arrives through a small number of channels: loss of assets (custody failure, fraud, key loss), compliance failure (operating outside a license or rule), valuation and liquidity surprise (marking assets no one will buy at the mark), and reputational damage (being the cautionary headline).
Every recommendation in this guide traces back to closing one of those channels.
In RMF terms, these harm channels are the *impact* dimension of categorization: the reason a given exposure rates low, moderate, or high.
Nothing in this guide requires an organization to acquire, accept, or endorse any digital asset.

## Why borrow the NIST lifecycle at all

Three reasons, each practical:

- **It is already the house language.** The CISO and CIO run RMF on systems. A CFO who frames digital asset risk in the same lifecycle can borrow that machinery — authorizing officials, continuous monitoring, risk-acceptance memos — rather than standing up a parallel process the auditors have never seen.
- **It forces the ordering fiduciaries skip.** The single most common failure is deciding (authorizing) before inventorying (categorizing). RMF makes that sequence non-optional and legible to oversight.
- **It produces an audit trail by construction.** Each step yields an artifact — the categorization, the control set, the assessment, the authorization memo, the monitoring cadence. An examiner who asks "show me your basis" is asking for exactly these.

Where the mapping strains, we flag it. RMF categorizes *systems* by confidentiality/integrity/availability impact; a digital asset holding is categorized instead by financial-loss, compliance, and reputational impact. The lifecycle transfers; the impact taxonomy is re-specified for finance.

## The deeper shift: governance baked into the object

Everything above treats digital assets as exposure — something out there that touches the organization and must be inventoried.
But the concept underneath, and the reason this subject will not stay contained in the investment portfolio, is that blockchain allows **governance to become a property of the object itself** rather than of the institutions around it.

Today, a file is inert.
Its ownership lives in a database, its access rules in a directory service, its provenance in someone's memory or a contract, its transfer history in logs that can be edited or lost.
All of the governance is external to the thing being governed — which is why so much of information security, records management, and IP law is scaffolding built around objects that cannot defend themselves.

An attested object inverts that.
Consider what changes across domains a finance and risk leader already owns:

- **Information security** — What does it do to information security when a file is no longer merely a file, but an attested object with ownership, provenance, policy, transfer history, and enforceable access rules?
- **Digital goods** — What does it do to the web when digital goods can be scarce without relying on platform databases, legal fiction, or symbolic tokens pointing at copyable files?
- **Corporate security** — What does it do to corporate security when sensitive files can be restricted to trusted machines, threshold approval groups, and hardware-sealed access paths?
- **Government records** — What does it do to government records when a document can be designed so that transfer requires mandate, attribution, and verified terminals?
- **Intellectual property** — What does it do to intellectual property when the original digital object can be distinguished from every imitation, screenshot, transcription, or derivative copy by hash, chain, and possession state?
- **Markets** — What does it do to markets when information itself can become transferable property rather than endlessly copied data?

For the CFO, this cuts both ways, and it is why running the RMF lifecycle now is worth the effort.
In the present, the lifecycle governs objects whose controls are external — the organization supplies the custody, the compliance, the oversight.
As governance migrates into the object, the controls do not disappear; they become **design properties** — custody expressed as key policy, compliance as transfer rules, governance as threshold approvals baked into the asset itself.
An organization that has run the lifecycle will know what controls to demand of attested objects; one that has not will inherit whatever defaults its vendors chose.

This concept is developed fully in a companion draft, [From Copying Machine to Property Network](digital-possession-concept-draft.md), which makes the core claim directly: digital possession makes information capable of becoming property, shifting security from the perimeter to the object itself.

> **Open question (for contributors):** Which of these six domains is nearest-term for the public sector? Government records — where transfer requiring mandate, attribution, and verified terminals maps directly onto existing records law — is one candidate. Further open questions live in the companion draft.

## How to read the rest of this document

Part III walks the seven RMF steps in order.
Each step opens with **who owns it**, then covers: the question, why the responsible role must answer it, which of the five risk surfaces it addresses, specific actions, and the artifact the step produces (the "sign of maturity" — and, in RMF terms, the thing an assessor would ask to see).
Part IV translates the lifecycle into decision guardrails.
Part V widens the lens from risk to adoption — the fuller set of considerations for a body deciding whether to *build* a blockchain solution, mapped back onto the same seven steps.
The appendices hold material that dates quickly — regulatory perimeter maps, glossaries — and are expected to be revised on their own cycle.

> **Open question (for contributors):** Should this guide address the *revenue* side — fees, taxes, or seized assets arriving in digital form — as a distinct exposure class in Categorize, or is that a separate publication?

---

# Part III — Running the RMF Lifecycle on Digital Asset Risk

The seven steps below are the NIST RMF (SP 800-37 Rev. 2), re-specified for a finance organization's digital asset exposure.
Cross-cutting them are five **risk surfaces** — **Exposure, Custody, Counterparty, Compliance, Governance** — each named where the step that addresses it appears.

## Step 0 — Prepare: Who owns this risk, and what is our tolerance?

*Risk surface: Governance (foundational).*
**Who owns this step:** Deputy Secretaries / Administrators, CFOs, CIOs, and Directors, jointly — this is where the executive tier assigns accountability before anyone touches an asset or a ledger.

**Why a fiduciary must answer it.**
RMF's Prepare step exists because organizations that skip it improvise their risk posture under pressure.
For digital assets, Prepare is where the CFO establishes — before any exposure is examined — who is accountable, what the organization's risk tolerance is, and what "do no harm" will mean in practice here.
Skipping Prepare is how an agency ends up with a Bitcoin position and no one who will admit to owning the decision.

**Specific actions.**

- Name the accountable owner: one person responsible for digital asset risk across the lifecycle (the RMF "risk executive" analog).
- State the organization's risk tolerance for digital assets in writing, tied to the governing investment statute for public entities.
- Adopt the "do no harm" test as policy: any new digital asset activity must state, in writing, which harm channels (loss, compliance, valuation/liquidity, reputation) it opens and how each is closed.
- Establish the reporting relationship to the oversight body now, before there is anything to report.

**Sign of maturity / artifact.**
A named owner, a written risk-tolerance statement, and a policy that no digital asset activity proceeds without a do-no-harm memo.

> **Open question (for contributors):** What is the right "risk executive" placement in a small government — the CFO directly, a treasury committee, a joint CFO/CISO role? Examples from real jurisdictions would anchor this.

## Step 1 — Categorize: Where do digital assets touch us, and how much would each matter?

*Risk surfaces: Exposure (primary), with impact drawn from Custody, Compliance, and reputation.*
**Who owns this step:** Analysts do the inventory and impact/risk-tier rating; CFOs own the financial-exposure view; Specialists flag compliance impact. Deputy Secretaries and Directors receive the output.

**Why a fiduciary must answer it.**
This is the exposure inventory, and it is the load-bearing step.
Exposure you have not categorized cannot have controls selected, cannot be assessed, cannot be authorized, cannot be monitored.
Most organizations discover their first digital asset exposure involuntarily — an unclaimed-property escheatment, a vendor that settles in stablecoins, a pension fund's allocation, a seized asset in litigation.
RMF's discipline adds a second move beyond inventory: for each exposure, rate the impact if it went wrong (low / moderate / high), using the harm channels as the impact taxonomy.

**Specific actions.**

- Inventory direct holdings: investments, ETF positions, tokens held for any operational reason.
- Inventory indirect holdings: pension and endowment allocations, pooled investment vehicles, money market funds with tokenized instruments.
- Inventory obligational exposure: unclaimed property statutes covering custodial crypto accounts, assets received through forfeiture or escheatment, donations.
- Inventory operational exposure: vendors and payment processors that touch digital assets anywhere in your payment chain.
- For each item, assign an impact rating (low/moderate/high) against the harm channels — this is what turns an inventory into a categorization.
- Assign an owner: one named person accountable for keeping the inventory current.

**Sign of maturity / artifact.**
The categorized inventory exists, is dated, names an owner, carries an impact rating per item, and has survived one refresh cycle.
"We checked and found nothing" is a valid, documented result — the RMF equivalent of a categorization of "no exposure."

> **Open question (for contributors):** What does a practical categorized-inventory template look like for a small government (a county, a special district) versus a cabinet-level agency? A worked example from a real jurisdiction would anchor this step.

## Step 2 — Select: Which controls do we require for each exposure?

*Risk surfaces: Custody, Counterparty, Compliance.*
**Who owns this step:** CIOs and Specialists (security, compliance, legal) select the control set; CFOs weigh custody and counterparty controls for financial exposure.

**Why a fiduciary must answer it.**
RMF's Select step matches controls to the categorization: higher-impact exposures demand stronger controls.
For digital assets, the "control catalog" is the diligence you require before an exposure is acceptable — and it lives on three surfaces.

### Control family: Custody

Digital asset custody inverts a familiar assumption: possession of a key *is* possession of the asset, and there is no transfer agent to reverse a mistake.
The loss channel here is total and instantaneous.

- For every categorized exposure, document the custody arrangement: self-custody, qualified custodian, exchange, fund wrapper.
- For custodians, obtain and review: regulatory status, insurance and its exclusions, key-management practices (cold storage, multi-party controls), and what happens in the custodian's bankruptcy.
- For any self-custody, require dual control and documented key-recovery procedures reviewed by someone who did not design them.
- Prefer structures where a failure is survivable: segregated accounts over omnibus, bankruptcy-remote over general obligation.

### Control family: Counterparty

In conventional markets, the failure of an intermediary is cushioned by decades of resolution machinery.
In digital asset markets, intermediaries vary enormously in regulatory status, and the difference between a regulated trust company and an offshore venue is the difference between a workout and a write-off.

- Map every intermediary in the chain: brokers, exchanges, transfer agents, oracles, bridge operators, stablecoin issuers.
- For each, identify the primary regulator and what that regulator's perimeter actually covers — a money-transmitter license and a trust charter protect against different failures.
- Treat cross-chain bridges and other interoperability layers as counterparties, not plumbing; they concentrate risk and have a distinct failure history.
- Set concentration limits: no single intermediary should be able to take the whole position down.

### Control family: Compliance

The compliance perimeter is layered and moving: federal securities and commodities regimes, banking regulators, FinCEN/OFAC obligations, state licensing regimes, and — for public entities — investment statutes, procurement law, and audit standards written before any of this existed.
Fiduciary failure here rarely looks like malice; it looks like an activity that was legal when begun and unlicensed when examined.

- Assign regulatory ownership: one function accountable for tracking the perimeter as it applies to *your* inventory, not the industry generally.
- Map each inventory item and each counterparty to its applicable regimes, including state licensing where you or your vendors operate.
- For public entities: reconcile any digital asset activity against your investment statute and get the reconciliation in writing.
- Build comment-period participation into the compliance function — rules in formation are the cheapest place to manage future compliance cost.

**Sign of maturity / artifact.**
Every categorized exposure has a selected control set across all three families, with higher-impact items carrying stronger controls — the digital asset analog of a control baseline.

> **Open questions (for contributors):**
> - Custody: which state or federal precedents (RFPs, deposit-collateralization statutes, comptroller policies, approved-custodian lists) should this section cite as reusable control patterns?
> - Counterparty: how should an organization evaluate a *protocol* as a counterparty, where there is no legal entity to underwrite — is there a defensible fiduciary standard today, or is the answer "then don't"?
> - Compliance: what do GAO/state-auditor expectations look like for digital asset holdings?

## Step 3 — Implement: Are the controls actually in place?

*Risk surfaces: Custody, Counterparty, Compliance (as executed).*
**Who owns this step:** Project Managers / Directors lead delivery; Technicians execute (key ceremonies, node ops, configuration); Specialists confirm each control is deployed as designed.

**Why a fiduciary must answer it.**
Selecting a control and implementing it are different things, and the gap between them is where real losses live.
RMF's Implement step is about deployment and documentation: the custody arrangement is not just chosen but executed and evidenced; the concentration limit is not just set but enforced in the trading system; the statutory reconciliation is not just required but signed.

**Specific actions.**

- For each selected control, capture evidence of implementation: the custody agreement executed, the insurance certificate on file, the concentration limit configured, the reconciliation signed by counsel.
- Document *how* each control is deployed — the RMF requirement — so that Assess (next step) has something to check against.
- Close the gap between policy and practice: a control that exists only in a policy binder is not implemented.

**Sign of maturity / artifact.**
For every selected control there is documented evidence it is operating, sufficient for an independent assessor to verify without re-interviewing the person who set it up.

## Step 4 — Assess: Has someone independent confirmed the controls work?

*Risk surfaces: all five, verified.*
**Who owns this step:** Specialists and Analysts perform the independent assessment — pointedly *not* the same people who implemented the controls. Internal audit or an external assessor may stand in.

**Why a fiduciary must answer it.**
RMF separates Implement from Assess deliberately: the person who deploys a control should not be the only person who attests it works.
For digital assets, this is where the bankruptcy scenario gets *read by counsel* rather than filed, where the key-recovery procedure gets tested rather than assumed, where the counterparty map gets a second set of eyes.

**Specific actions.**

- Have an independent reviewer — internal audit, counsel, or an external assessor — confirm each control is in place and operating as intended.
- Specifically test the failure paths: read the custodian's bankruptcy terms, exercise (in a controlled way) the key-recovery procedure, confirm concentration limits actually trigger.
- Document findings and gaps; unresolved gaps carry into the authorization decision as residual risk.

**Sign of maturity / artifact.**
An assessment report, authored by someone other than the control owner, listing what was verified and what residual risk remains.

> **Open question (for contributors):** What working papers should a CFO have ready before the audit letter arrives, and how do GAO/state-auditor assessment expectations map onto this step?

## Step 5 — Authorize: Has a named official accepted the residual risk, in writing?

*Risk surface: Governance (decision).*
**Who owns this step:** Deputy Secretaries / Administrators as the authorizing officials; CFOs sign off on financial residual risk. This is the one step that must name a person, not a body.

**Why a fiduciary must answer it.**
This is the fiduciary heart of the framework and RMF's sharpest contribution.
An Authorization to Operate is a named senior official formally accepting residual risk on the record.
The recurring pattern in public-sector digital asset controversies is not bad analysis — it is decisions made at the wrong altitude, or with no one's name on them, surfaced to oversight after commitment rather than before.
RMF makes the accepting official explicit.

**Specific actions.**

- Define decision rights: who may authorize acquiring, accepting, holding, or disposing of a digital asset, and at what thresholds.
- Require an authorization package: the categorization, the selected controls, the assessment findings, the residual risk, and the do-no-harm memo — assembled into one decision record.
- Have the accountable official accept (or decline) the residual risk in writing. A documented "we decline to authorize" is a complete, defensible fiduciary act.
- Time the authorization *before* commitment, not after.

**Sign of maturity / artifact.**
A signed authorization decision — approve or decline — naming the accepting official and citing the assessment it rests on.

> **Open question (for contributors):** In public entities, who is the right "authorizing official" — the CFO, a treasury board, the governing council? How does that map to existing delegation-of-authority statutes?

## Step 6 — Monitor: Who watches this continuously, and what does oversight see?

*Risk surface: Governance (ongoing), refreshing all five surfaces.*
**Who owns this step:** CIOs and Directors own the monitoring cadence; Technicians run the instrumentation; Analysts refresh the categorization. Deputy Secretaries and CFOs are the standing audience.

**Why a fiduciary must answer it.**
RMF's insight is that authorization is not a finish line — risk drifts, regulations change, custodians fail, valuations move.
Continuous monitoring is what keeps the authorization honest.
Every step below Monitor produces information; monitoring determines whether that information keeps reaching the people whose duty depends on it.

**Specific actions.**

- Define the monitoring cadence: what the board, council, or oversight committee sees, how often, and in what form (the categorized inventory is the natural core artifact).
- Pre-commit escalation triggers: custody incident, counterparty distress, regulatory change touching the inventory, valuation move beyond a set band.
- Refresh the categorization on a fixed cycle — new exposures appear, impacts change.
- Rehearse one failure: a tabletop exercise on a custody or counterparty failure, before there is a real one.
- Report the *framework* to oversight, not just the transactions — on a fixed cadence, independent of whether any position exists.

**Sign of maturity / artifact.**
A running monitoring cadence with defined triggers, and an oversight body that has seen the lifecycle — not just the trades — at least once.

> **Open question (for contributors):** What is the right monitoring artifact for the *oversight body* itself — a one-page dashboard? A standing agenda item? Examples from boards or councils that do this well would be valuable.

---

# Part IV — Decision Guardrails

The lifecycle produces information; these guardrails turn it into defensible decisions. Each maps to an RMF step.

1. **Categorize before position.** No digital asset decision — including "no" — until the exposure inventory is categorized (Step 1). A refusal grounded in a categorization is prudence; a refusal grounded in unfamiliarity is luck.
2. **Survivability before yield.** In control Selection (Step 2), evaluate every arrangement by its failure mode first. If the custody or counterparty failure is not survivable, the yield discussion never starts.
3. **Perimeter before product.** Do not select a control set (Step 2) that accepts exposure through an intermediary whose regulator you cannot name.
4. **Independent assessment before authorization.** No authorization (Step 5) rests on the control owner's own word; Assess (Step 4) is a separate step for a reason.
5. **Written reconciliation for public funds.** For public entities, no authorization without a written reconciliation against the governing investment statute.
6. **A named official on the record.** Every authorization (Step 5) names the official accepting residual risk. "The organization decided" is not an authorization; a person authorizes.
7. **Oversight sees the lifecycle, not just the trades.** Monitor (Step 6) reports the seven-step picture on a fixed cadence, independent of whether any position exists.
8. **The do-no-harm memo.** Every new activity opens (in Prepare) with a memo naming the harm channels it opens and closing each — a discipline borrowed from clinical practice: first, state how this could hurt.

---

# Part V — Adoption Considerations (the fuller outline)

Parts III and IV run the *risk* lifecycle — the right lens when digital assets are exposure that touches the organization from outside.
But a public-sector body that decides to *build or adopt* a blockchain solution (a records registry, a grants-tracking ledger, a credentialing system) faces a wider set of questions.
This part sketches those dimensions as an outline, each mapped to where it lives in the RMF spine, so the document serves both the finance-risk reader and the agency deciding whether and how to adopt.
These are outline stubs — each is a candidate section, or its own companion piece.

## 1. Purpose — Why are we doing this at all?

The first and most easily skipped question. A blockchain adoption with no articulated purpose beyond "modernization" fails Prepare before it starts.
State the specific problem — shared state across organizations that don't trust a single custodian, tamper-evident records, disintermediated settlement — and the non-blockchain baseline it must beat.
*Maps to: Prepare (Step 0). The purpose statement is the input to risk tolerance.*

## 2. Foundation — What must be true before we begin?

The organizational, legal, and technical preconditions: statutory authority to operate the system, data-governance ownership, identity and key-management readiness, and the skills to run it.
Foundation is where most public-sector blockchain pilots quietly fail — the technology worked; the organization wasn't ready to hold the keys.
*Maps to: Prepare (Step 0).*

## 3. Use case classification — Risk tiers

Not every use case carries the same risk, and the framework should not treat them alike.
A tiering scheme — e.g. **low** (internal tamper-evident logging, no external value), **moderate** (inter-agency shared records, credentials), **high** (anything holding or moving value, or citizen-facing records of legal consequence) — sets how much of the lifecycle each use case must run.
This is the direct analog of RMF categorization applied to *systems being built*, not just *exposure being inventoried*.
*Maps to: Categorize (Step 1), extended from exposure to solution.*

> **Open question (for contributors):** What is the right tier definition and set of examples for public-sector blockchain use cases? A published tiering rubric would be one of this publication's most reusable artifacts.

## 4. Governance and security — Anchored in NIST publications

Where the "inspired by NIST" framing becomes concrete. Beyond RMF, NIST has a body of blockchain-specific guidance to build on rather than reinvent:

- **NISTIR 8202** — *Blockchain Technology Overview* (the foundational reference).
- **NISTIR 8301** — *Blockchain Networks: Token Design and Management Overview.*
- **NISTIR 8403** — *Blockchain for Access Control Systems.*
- **NISTIR 8408** — *Understanding Stablecoin Technology and Related Security Considerations.*
- **NISTIR 8472** — *Non-Fungible Token Security.*
- **NISTIR 8475** — *A Security Perspective on the Web3 Paradigm.*
- **SP 800-53** control families — as re-specified for a ledger's confidentiality/integrity/availability profile.

Governance covers on-chain and off-chain decision rights, upgrade/fork authority, node operation, and consensus participation; security covers key management, smart-contract assurance, and the consensus threat model.
*Maps to: Select and Implement (Steps 2–3) — this is the control catalog for a system, not just a holding.*

## 5. Decision framework — Should we use blockchain at all?

A gate before design: a structured "do we even need a blockchain" test (multiple writers who don't trust each other, need for a shared authoritative record, no acceptable trusted third party).
Most honest applications of this gate end in "a database is fine" — and saying so is a feature, the adoption analog of a documented decision not to authorize.
*Maps to: Prepare → Categorize (Steps 0–1).*

> **Open question (for contributors):** Which existing decision trees (DHS, GSA, GAO, academic) should this framework adopt or adapt rather than write fresh?

## 6. Decision architecture — Solution-agnostic

Once past the gate, the architecture choices — permissioned vs. permissionless, consensus mechanism, on-chain vs. off-chain data, public vs. private, hosted vs. self-run — stated as trade-offs, **not tied to any vendor or platform.**
The publication's credibility depends on staying solution-agnostic: it describes the decision axes and their consequences, and lets the agency choose.
*Maps to: Select (Step 2).*

## 7. DevOps — Building and operating the system

The operational reality most policy documents omit: deployment pipelines, node provisioning, key ceremony and rotation, upgrade and fork management, incident response, and monitoring.
Public-sector DevOps carries extra constraints (ATO processes, FedRAMP, continuous monitoring obligations) that intersect directly with RMF's later steps.
*Maps to: Implement and Monitor (Steps 3, 6).*

## 8. Testing — How do we know it works and stays working?

Smart-contract testing and formal verification, consensus and Byzantine-fault testing, data-integrity and migration testing, and — critically — the independent assessment that RMF requires before authorization.
Testing is where the adoption outline and the risk lifecycle share a step most cleanly.
*Maps to: Assess (Step 4).*

## 9. Cost of operations — Total cost of ownership

The number that decides most adoptions and is estimated least well: node infrastructure, key-management and HSM costs, transaction/gas costs where applicable, audit and assessment recurring costs, specialized staffing, and the cost of *exiting* or migrating off the platform.
A blockchain solution that is cheaper to build and ruinous to operate is a fiduciary trap.
*Maps to: Authorize (Step 5) — TCO is part of the residual-risk package the accepting official signs.*

> **Open question (for contributors):** What does a realistic multi-year TCO model look like for a moderate-tier public-sector ledger? A worked model would be high-value.

## 10. Organizational change — Will the institution actually adopt it?

The dimension that sinks technically sound projects: workflow redesign, role and skill changes, training, stakeholder buy-in across agencies, and the political economy of moving authority into a shared ledger.
Blockchain's core proposition — reducing reliance on a single trusted intermediary — is an organizational change before it is a technical one, and it threatens whoever *was* that intermediary.
*Maps to: cross-cutting, but anchored in Prepare (Step 0) and sustained through Monitor (Step 6).*

---

**How Part V relates to Parts III–IV.**
Parts III–IV are the *risk* view for the finance leader who mostly encounters digital assets as exposure.
Part V is the *adoption* view for the agency deciding whether to build.
They share one spine — the RMF lifecycle — which is the point: a CFO assessing a proposed blockchain grants system and a CISO authorizing it can use the same seven steps and the same tiering, and meet in the middle.

> **Open question (for contributors):** Should Part V be spun out as a standalone "Public-Sector Blockchain Adoption Guide" with the CFO risk guide (Parts I–IV) as its finance-specific companion? The two share the RMF spine deliberately so either split is clean.

---

# Open Questions — Standing Invitation to Contributors

Collected from the step sections, plus structural questions about the publication itself.
Claim one in [issue #50](https://github.com/blockchain-working-group/agendas/issues/50).

**Content questions**

- Prepare: the right "risk executive" placement for a small government (Step 0).
- Categorize: a worked categorized-inventory template, scaled for small governments vs. large agencies (Step 1).
- Select: reusable public-sector control precedents — RFPs, statutes, custodian policies (Step 2, Custody); a fiduciary standard for protocols with no legal entity (Step 2, Counterparty).
- Assess: audit-readiness expectations and working papers (Step 4).
- Authorize: who the right authorizing official is under existing delegation-of-authority law (Step 5).
- Monitor: the oversight body's artifact — what a board should actually see (Step 6).
- Scope: does the revenue side (fees, taxes, seized assets in digital form) belong here or in a companion piece?
- Mapping fidelity: where does the RMF analogy strain hardest, and should any step be renamed to avoid implying literal SP 800-37 compliance?
- Attested objects: which of the six domains (information security, digital goods, corporate security, government records, IP, markets) is nearest-term for the public sector? The concept now has a companion draft, [From Copying Machine to Property Network](digital-possession-concept-draft.md), with its own open questions.

**Publication questions**

- Audience boundary: is the role set in Part II complete for the public sector, and should it extend to regulated-industry counterparts (private-sector CFOs, CISOs, PMs) serving government markets?
- Role mapping: does the persona-to-RMF-step table match how agencies actually distribute this work, and where is it wrong?
- Form: single ~50-page publication, or a series releasing one RMF step (or phase) at a time?
- Review: do we convene a panel of practicing CFOs/comptrollers — and ideally an RMF/authorizing-official practitioner — to pressure-test the mapping before publication?
- Voice: how prescriptive can an ACT-IAC working group publication be — guidance, or checklist?

---

# Appendices (placeholders — maintained on their own revision cycle)

## Appendix A: Regulatory perimeter map (dated)

A table mapping asset types and activities to governing regimes and current rule status.
Feeds the Compliance control family in Step 2 (Select) and the escalation triggers in Step 6 (Monitor).
Deliberately excluded from the body so the guide stays evergreen; revise this appendix quarterly.
Seed material: the working group's weekly updates.

## Appendix B: Glossary

Plain-language definitions for the terms a CFO will encounter in vendor and counterparty diligence (custody terms, settlement terms, token classifications), plus the RMF terms used here (categorize, control baseline, authorization to operate, continuous monitoring) as re-specified for finance.

## Appendix C: The categorized exposure inventory template

The Step 1 (Categorize) artifact, ready to fill in — inventory columns plus an impact rating per item.

## Appendix D: RMF-to-finance mapping table

A one-page crosswalk: each of the seven RMF steps, its SP 800-37 purpose, the finance re-specification used here, the risk surface(s) it addresses, and the artifact it produces. The quick-reference companion to Part III.

## Appendix E: Sources and further reading

Standing references (NIST SP 800-37 Rev. 2, regulator portals, standards bodies, NCSL trackers) rather than news items.
