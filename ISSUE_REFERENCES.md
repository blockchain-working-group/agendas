# Issue References

Links gathered in GitHub issues, kept here so the issues can be closed without losing them.
Each section names the issue the links came from, so the original discussion is one click away.

This is an archive, not the curated list.
The curated list is [`docs/_data/resources.json`](docs/_data/resources.json), which renders as the [Resources page](https://blockchain-working-group.github.io/agendas/resources/) (see [RESOURCES.md](RESOURCES.md)).
Links checked on 2026-10-25; "unverified" means the site blocks automated checks and has no archived copy.

## Draft ACT-IAC blockchain primer ([#13](https://github.com/blockchain-working-group/agendas/issues/13))

- [DLT Blockchain Primer, 2023 final edits (.docx)](assets/files/DLT_Blockchain_Primer_2023_Finaledits.docx), the original draft in this repo.
- [blockchain-working-group/primer](https://github.com/blockchain-working-group/primer), the same document copied to its own repository for version-controlled review and comments.

## Potential use cases ([#14](https://github.com/blockchain-working-group/agendas/issues/14))

Deciding whether blockchain fits:

- [Do you need a Blockchain?](https://eprint.iacr.org/2017/375.pdf) (Wüst and Gervais, IACR ePrint 2017/375), a decision flowchart.
- [Flow diagram for deciding when to use blockchain in an IoT application](https://www.researchgate.net/figure/Flow-diagram-for-deciding-when-to-use-blockchain-in-an-IoT-application_fig2_325494976) (ResearchGate; unverified).
- Four questions from the thread: Do multiple groups need to establish trust?
  Do multiple parties share or update the same data?
  Is verification required?
  Can intermediaries be removed to reduce cost and complexity?

Use cases and examples:

- Voting: [US20200258338A1](https://patents.google.com/patent/US20200258338A1/en) (Google Patents).
- Decentralized authentication: [Planaria, decentralized auth](https://afomi.github.io/planaria/#/intro?id=decentralized-auth).
- Intellectual property: [From Web 2 to Web 3: harnessing blockchain technology for IP](https://www.euipo.europa.eu/en/news/from-web-2-to-web-3-harnessing-blockchain-technology-for-ip) (EUIPO).
- Securities settlement: [CNMV authorizes Securitize, the first DLT-based trading and settlement system in Spain](https://www.cnmv.es/webservices/verdocumento/ver?t=%7b44ec3466-5a78-4524-9c45-291209864197%7d) (CNMV, 2025).
- Fintech cohort: [DallasMeetup partners with the Texas Blockchain Council](https://www.dallasmeetup.com/news/dallasmeetup-partners-with-texas-blockchain-council-for-its-fintech-cohort) (2026).

Capabilities brainstormed in the thread: third-party attestation with a timestamp server, user login and authorization tokens, asset tokenization, micropayments (`HTTP 402`), after-the-fact reconciliation and auditability, a global event bus, triple-entry accounting, AI training-data accountability, and escrow.

## Minimal technical considerations for a public-agency pilot ([#15](https://github.com/blockchain-working-group/agendas/issues/15))

The checklist from this issue is published as "Starting a Blockchain POC — Minimum Requirements" on the [Participate page](https://blockchain-working-group.github.io/agendas/participate/).

Existing guidance:

- [ACT-IAC Blockchain Primer](https://www.actiac.org/documents/blockchain-primer) (unverified; see the #13 section for the repo copy).
- [GBA Blockchain Maturity Model](https://gbaglobal.org/bmm/).

ATO controls for consideration:

- [CCM v4.0 LOG-11: Transaction/Activity Logging](https://csf.tools/reference/cloud-controls-matrix/v4-0/log/log-11/)
- [NIST SP 800-53 r5 AU-2: Event Logging](https://csf.tools/reference/nist-sp-800-53/r5/au/au-2/)
- [NIST SP 800-53 r5 AU-14: Session Audit](https://csf.tools/reference/nist-sp-800-53/r5/au/au-14/)
- [NIST SP 800-53 r5 AU-16: Cross-Organizational Audit Logging](https://csf.tools/reference/nist-sp-800-53/r5/au/au-16/)

## List federal blockchain environments ([#23](https://github.com/blockchain-working-group/agendas/issues/23))

Questions the issue asked: Where do federal blockchain environments exist, in which agencies and divisions?
What is the status of each?
How does a staffer engage, and how does a vendor?

As of November 2025, no active federal blockchain environments were known to the group.
A GSA lab stakeholder was open to conversation, but a specific proposal, scope, and owner would be needed to proceed.

Costs and resources to consider for any environment (general considerations are covered in the [Blockchain Playbook](https://github.com/blockchain-working-group/blockchain-playbook), under the Selection Phase and Business Considerations):

- Infrastructure: cloud servers to run nodes of a given chain, blob storage for chain data, servers to listen for and distribute chain data to applications (pub/sub), and the documentation and compliance work of running any public system (ATOs and controls).
- People: training, and wallet management per device.
- Coordination: systems modification and integration, and data migrations.
