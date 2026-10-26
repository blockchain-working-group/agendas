---
status: drafting
product: A short brief on tamper-evident logs and SP 800-53, then a sample OSCAL component definition
started_at: 2023-09-22
ended_at:
issue: https://github.com/blockchain-working-group/agendas/issues/7
---

# Immutable Logs and NIST SP 800-53 Controls

> **Status: member contribution, draft.**
> This is not an official ACT-IAC or working group position, and it is not compliance guidance.
> It was written by Ryan Wold ([@afomi](https://github.com/afomi)) for [issue #7](https://github.com/blockchain-working-group/agendas/issues/7) and first shared as a [gist](https://gist.github.com/afomi/f616597f098cf5abcdddde5d97e25cfc) on October 4, 2024.
> This version, revised October 2026, tones down claims the original stated too strongly and adds a note on OSCAL.

Public-sector organizations can strengthen the integrity of their audit logs by making them **tamper-evident**: any change or deletion after the fact can be detected.
A blockchain can provide that evidence.
It supports several NIST SP 800-53 controls, but it does not satisfy any of them on its own.

## The pattern: anchor the logs, don't store them on chain

The agency keeps its detailed logs in an authorized, access-controlled log store.
At regular intervals it publishes a cryptographic hash (or a Merkle root covering many log entries) to a blockchain.
Later, anyone with the logs can recompute the hash and compare it to the anchored value.
A match shows the logs are unchanged since they were anchored; a mismatch or a missing entry shows they were not.

Raw security logs and personal information should generally stay off public chains.
Only the hashes go on chain.
See "Event Log Anchoring" in the [glossary](https://blockchain-working-group.github.io/agendas/glossary/).

## Controls this can support

Each control still needs the agency's own policy, process, and implementation.
Anchoring adds evidence to each one.

1. **[AU-2: Event Logging](https://csf.tools/reference/nist-sp-800-53/r5/au/au-2/)**
   - The control: decide which events to log, and log them.
   - What anchoring adds: proof that the record of logged events has not been trimmed or rewritten since it was anchored.
     The agency still decides which events are logged.

2. **[AU-3: Content of Audit Records](https://csf.tools/reference/nist-sp-800-53/r5/au/au-3/)**
   - The control: audit records include what happened, when, where, the source, the outcome, and who was involved.
   - What anchoring adds: proof that a record's content is the same as when it was anchored.
     It says nothing about whether the content was complete in the first place.

3. **[AU-6: Audit Record Review, Analysis, and Reporting](https://csf.tools/reference/nist-sp-800-53/r5/au/au-6/)**
   - The control: review and analyze audit records for unusual activity, and report findings.
   - What anchoring adds: reviewers and auditors can verify that the logs in front of them match what was anchored, without trusting the system that holds them.

4. **[AU-9: Protection of Audit Information](https://csf.tools/reference/nist-sp-800-53/r5/au/au-9/)**
   - The control: protect audit information and tools from unauthorized access, modification, and deletion.
   - What anchoring adds: detection of modification or deletion, closest to the [AU-9(3) Cryptographic Protection](https://csf.tools/reference/nist-sp-800-53/r5/au/au-9/au-9-3/) enhancement.
     It does not prevent tampering in the log store, so access controls on that store are still required.

5. **[AU-10: Non-repudiation](https://csf.tools/reference/nist-sp-800-53/r5/au/au-10/)**
   - The control: provide evidence that an individual performed a given action.
   - What anchoring adds: a timestamped, independently verifiable record that a signed entry existed.
     Non-repudiation also depends on binding keys to identities and protecting those keys.

6. **[CM-3: Configuration Change Control](https://csf.tools/reference/nist-sp-800-53/r5/cm/cm-3/)**
   - The control: manage, approve, and record changes to system configuration.
   - What anchoring adds: a change history that can't be quietly edited later, which helps when tracing or reversing unauthorized changes.

## Why tamper-evidence matters

- **Security:** an intruder who edits or deletes logs to hide their activity can be detected.
- **Compliance:** auditors get evidence of log integrity that doesn't depend on trusting the log store's administrators.
- **Accountability:** actions recorded in anchored logs are hard to dispute later.
- **Incident response:** investigators can confirm the log data they rely on is authentic.
- **Trust:** stakeholders can verify integrity themselves instead of taking it on faith.

## What this does not do

- It does not satisfy any control by itself.
  Agencies still need defined event types, a protected log store, identity and key binding, a retention policy, review workflows, and privacy safeguards.
- It does not make logs undeletable.
  It makes deletion detectable.
- It adds its own risks to manage, such as signing-key management, the availability of the chain, and its dependencies.
  These belong in the system's risk assessment like any other dependency.

## Next: making this reusable with OSCAL

The mapping above is prose, so every agency that wants it has to re-read it and rewrite it into its own security plan.
NIST's [Open Security Controls Assessment Language (OSCAL)](https://pages.nist.gov/OSCAL/) expresses the same information as machine-readable data (JSON, XML, or YAML).
NIST publishes the [SP 800-53 catalog itself in OSCAL](https://github.com/usnistgov/oscal-content).

Two OSCAL [models](https://pages.nist.gov/OSCAL/learn/concepts/layer/) fit this work:

- A [component definition](https://pages.nist.gov/OSCAL/learn/concepts/layer/implementation/component-definition/) describes a reusable capability, such as "audit log anchoring", and states which controls it supports and how.
  The six controls above are a first draft of one.
- A [profile](https://pages.nist.gov/OSCAL/learn/concepts/layer/control/profile/) selects and tailors controls from a catalog.
  A distributed-ledger "overlay" (a tailored set of SP 800-53 controls for systems that use a blockchain) would be a profile.

An agency's system security plan can then import both, so the next agency starts from shared, versioned data instead of a blank page.
Writing a sample component definition for log anchoring would be a good next working-group exercise.
