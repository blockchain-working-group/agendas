# Blockchain Asset Policies and Control Models

**Status**: Draft

**Last updated**: 2026-07-31

**Scope**: Technical and governance controls over blockchain-based assets

**Companion documents**:
[Blockchain and DLT Platform Comparison Matrix](./BLOCKCHAIN_COMPARISON_MATRIX.md)
and [Public Sector Blockchain Use Cases](./PUBLIC_SECTOR_USE_CASES.md)

This reference highlights ways that a blockchain-based asset may be issued,
held, transferred, paused, frozen, burned, recovered, or reassigned. It gives
particular attention to Jurat and the BSV Association's Network Access Rules
(NAR) and Digital Asset Recovery (DAR) design because they illustrate different
ways to connect legal decisions to ledger state.

This is a comparison aid, not legal advice, an endorsement, or a conclusion
that a technical action changes legal title. A system's ability to freeze or
move a token does not by itself establish who owns the underlying legal right,
whether an order is valid in a particular jurisdiction, or whether other
participants will recognize the resulting ledger state.

## Start With the Asset, Not the Chain

An assessment should distinguish three things that are often called an
"asset":

1. A **native network asset**, such as BTC, BCH, BSV, ETH, SOL, XRP, XLM, ALGO,
   or HBAR.
2. An **issued token or application state**, whose issuer, contract, or token
   service may retain administrative powers.
3. An **off-chain legal right or item**, such as a dollar claim, license,
   security, title, physical object, or benefit represented by a token.

Those layers can have different owners, controllers, governing terms, and
remedies. [NISTIR 8301, *Blockchain Networks: Token Design and Management
Overview*](https://www.nist.gov/publications/blockchain-networks-token-design-and-management-overview)
provides a government reference for native and non-native token models,
custody, transactions, and supporting infrastructure.

## Control-Model Taxonomy

| Control model | Who can act | Typical actions | Examples | Principal policy question |
|---------------|-------------|-----------------|----------|---------------------------|
| Bearer or key-authorized asset | Holder of the required keys or script conditions | Transfer or authorize a spend | Native BTC and BCH under ordinary network rules | What remedy exists when keys are lost, stolen, or compelled? |
| Issuer or token-service control | Issuer-designated keys or roles | Mint, authorize, freeze, wipe, pause, or claw back | Algorand ASAs, Stellar issued assets, XRPL issued tokens, Hedera Token Service, Solana tokens, USDC, and USDT | Were retained powers disclosed, limited, secured, and made revocable where appropriate? |
| Smart-contract or application control | Contract roles, governance, multisig, or upgrade administrator | Pause, allowlist, denylist, burn, replace, or change policy | ERC-20 and ERC-721 implementations; ERC-3643 regulated tokens; EVM applications | Is the control in the base network or only in this contract, and can an upgrade expand it? |
| Permissioned-network policy | Consortium members, identified operators, or endorsing organizations | Admit participants, approve transactions, change rules, or correct application state | Hyperledger Fabric, Besu permissioned deployments, Corda | Which organizations must agree, and under which operating agreement? |
| Custody or intermediary control | Exchange, custodian, wallet provider, transfer agent, or escrow | Freeze an account, block withdrawal, recover keys, or comply with process | Hosted wallets and regulated service providers | Does the control reach the on-chain asset, only the customer account, or both? |
| Network-operator directive | Association or other governance body and participating nodes | Freeze or reassign outputs; reject transactions or blocks | BSV NAR and DAR | Which nodes are bound, what legal event triggers action, and could nodes diverge? |
| Court-oracle or arbitrator bridge | Court or tribunal plus an oracle, execution key, or opted-in contract | Attest to a decision and trigger a freeze, transfer, escrow release, or other remedy | Jurat, UKJT Digital Dispute Resolution Rules, and ERC-792 arbitrable contracts | How are jurisdiction, authenticity, due process, appeal, and bridge failure handled? |
| Protocol-native managed asset | Defined administrator or law-enforcement roles constrained by consensus rules | Freeze, seize, issue, or perform other recorded management actions | NIST/Prometheus managed-cryptocurrency research prototypes | Are the administrator's powers narrow, transparent, reviewable, and protected by checks and balances? |

The layers may be combined. For example, a court may order a custodian to
freeze an account, an issuer to exercise a token clawback, or a network
participant to follow a protocol-specific recovery process. Those are
different technical paths even when they respond to the same legal event.

## Highlight: BSV Network Access Rules and Digital Asset Recovery

### What the published model says

The [BSV Association Network Access Rules](https://nar.bsvblockchain.org/)
describe the relationship between the Association and nodes governed by those
rules. Under [Part III — Enforcement
Rules](https://nar.bsvblockchain.org/network-access-rules/part-iii-enforcement-rules),
the Association may issue a Directive following a defined enforcement event or
a direct or indirect decision event. The Rules describe qualifying decisions
as having force of law, being recognized, or being enforceable in England and
Wales or Switzerland, together with other subject-matter requirements.

The published Rules limit a Directive to one or more listed steps:

- freeze specified coins in unspent transaction outputs;
- blacklist or whitelist specified peer IP addresses;
- reassign frozen coins; or
- invalidate specified blocks.

The current [BSV Digital Asset Recovery protocol
reference](https://protocol.bsvblockchain.org/concepts/digital-asset-recovery)
describes DAR as a use of the network Alert System. It says nodes maintain
freeze and recovery orders, a freeze makes named UTXOs unspendable, and a
recovery order reassigns funds to a recovery UTXO. The reference says BSV node
software ships with the functionality, while the off-chain legal processes
that drive it are outside the protocol reference's scope.

### How to classify it

NAR/DAR is not an issuer clawback field attached to a particular token. It is a
network-governance and node-enforcement design that can affect BSV UTXOs. It
should therefore be assessed separately from:

- ordinary private-key or script-authorized spending;
- an issuer's control over a token carried on BSV;
- an exchange or custodian freezing a customer account; and
- the rules of BTC or BCH, which are separate networks.

### Questions requiring independent validation

- Which production nodes are subject to the NAR, and what portion of block
  production and transaction processing do they represent?
- How is a Directive authenticated, published, audited, corrected, stayed, or
  withdrawn?
- What notice and opportunity to contest an action exist before and after an
  emergency freeze?
- How are conflicting orders, appeals, reversals, and differences among
  jurisdictions handled?
- How are the Alert System and directive-signing keys protected, rotated, and
  recovered?
- What happens when nodes, wallets, exchanges, or applications do not recognize
  the same freeze or reassignment?
- Could enforcement produce divergent ledger views, a chain split, stranded
  transactions, or incompatible accounting records?
- Which completed production recoveries can be verified from court records,
  directives, transaction data, and independent operational evidence?

The NAR and protocol pages establish the Association's published rules and
technical design. They should not be treated, without further legal and
factual review, as proof that every node is bound or that every jurisdiction
will recognize a resulting reassignment.

## Highlight: Jurat and the Jurat Transaction Chain

### Earlier JTC design

Jurat's current description of the [Jurat Transaction Chain
(JTC)](https://jurat.io/jtc/) calls it an earlier proof-of-concept Bitcoin fork
with protocol-level legal enforcement. Jurat describes a process in which a
claimant generated a request identifier, presented it in litigation, and
Jurat-enabled witness nodes observed an authenticated court-docket entry so
miners could execute the corresponding action. The vendor's
[recovery-process explanation](https://jurat.io/how-can-you-recover-stolen-crypto-with-jurat/)
lists freezes and return of coins as example actions.

JTC is a separate network. Jurat is not a native property of BTC, BCH, or BSV,
and the historical JTC implementation should not be attributed to any of those
networks.

### Current direction described by Jurat

Jurat's current site says the project has pivoted from JTC to modular,
EVM-compatible smart contracts. It describes an oracle network as a witness
layer for court and tribunal events and application contracts that opt in to
legal-enforcement logic. This changes the control model from a Bitcoin-derived
consensus feature to an application or token-contract feature on an EVM
network.

Because these statements come from Jurat, a platform assessment should label
each capability as historical, deployed, pilot, proposed, or in development
and validate it against current code, audits, network deployments, and primary
court records.

### Questions requiring independent validation

- Which specific chain, contract version, asset, court system, and oracle set
  are in scope?
- What exact action can the deployed contract take: pause, freeze, burn,
  transfer, upgrade, or something else?
- Does the asset holder opt in with clear notice, and can the policy change
  after acquisition?
- How does the system verify jurisdiction, finality, authenticity, scope, and
  continuing validity of an order?
- How are sealed matters, personal data, mistaken identity, stays, appeals,
  vacatur, and conflicting decisions handled?
- Can an oracle, administrator, upgrade key, or contract role act without a
  court event?
- What independent evidence shows that the legal and technical process operated
  as described?

## Additional Paths From Legal Decisions to Ledger State

The connection is normally a pipeline rather than a single feature:

1. A court, regulator, arbitrator, issuer, or other authorized body makes a
   decision.
2. A person or system authenticates the decision and determines its scope.
3. A key, contract role, oracle, custodian, issuer, asset agent, or node
   directive translates it into a transaction or validation rule.
4. The ledger records the resulting freeze, transfer, burn, reissuance, state
   change, or ordinary signed transaction.

The following examples illustrate different implementations. Only some
authenticate the legal decision themselves; several merely provide a technical
power that an authorized actor may exercise after completing an off-chain legal
review.

| Pattern and example | Decision-to-ledger connection | Ledger effect | Evidence and limitation |
|---------------------|-------------------------------|---------------|-------------------------|
| **Court-authorized issuer action — Tether/USDT** | A federal seizure warrant is served through the issuer, which can act through its token administration mechanism | Freeze followed by an issuer-facilitated transfer to a law-enforcement-controlled wallet | A concrete production example: the [Department of Justice reports](https://www.justice.gov/usao-ndoh/pr/united-states-seeks-forfeit-200000-tether-usdt-cryptocurrency-valued-200000) that Tether first froze 200,000 USDT and later transferred it under a federal warrant; this does not establish the same capability for other tokens |
| **Issuer blocklist — Circle/USDC** | Circle evaluates a government instruction and invokes its retained issuer controls | Block on-chain transfers to and from an address; a legal order may also affect redemption or associated reserves | Circle's [USDC Terms](https://www.circle.com/legal/usdc-terms) describe blocklisting and legal-order freezes; the issuer, rather than the base blockchain, authenticates and executes the instruction |
| **Tribunal execution key — UKJT Digital Dispute Resolution Rules** | Parties incorporate rules into an on-chain relationship and authorize an arbitrator to use a private key when implementing a decision | Any transaction or contract action permitted by the delegated key and agreement | The [UKJT rules](https://lawtechuk.io/ukjt/digital-dispute-resolution-rules/) expressly contemplate arbitrators implementing decisions directly on-chain; this is an opt-in arbitral framework, not a universal court power |
| **Arbitrator-contract callback — ERC-792 and Kleros** | An arbitrator returns a ruling to an arbitrable smart contract, whose ruling function performs the programmed outcome | Escrow release, permission-list change, or another application-defined state transition | [ERC-792 documentation](https://developer.kleros.io/en/stable/) defines the interface; a decentralized ruling is not automatically a state-court judgment and may still require ordinary legal recognition for off-chain enforcement |
| **Regulated-token transfer agent — ERC-3643** | An appointed owner or agent acts after an external legal, regulatory, compliance, or key-recovery determination | Address or partial-balance freeze, pause, burn, wallet recovery, or forced transfer | [ERC-3643](https://eips.ethereum.org/EIPS/eip-3643) standardizes the controls and their event history but does not itself authenticate a court order |
| **Protocol asset controller — Polymesh** | An asset owner or authorized agent invokes protocol-level asset controls after a regulatory or legal determination | Freeze an asset or perform a controller transfer that overrides many normal transfer restrictions | [Polymesh documentation](https://developers.polymesh.network/core/assets/) identifies regulatory and legal-enforcement scenarios; authority and process remain configuration- and issuer-specific |
| **Court order enforced through custody or recovered keys** | Authorities serve a custodian or obtain control of the required private keys, then create an ordinary valid transaction | Transfer to an agency-controlled wallet without changing consensus or token rules | [Department of Justice guidance](https://www.justice.gov/media/1266016/dl?inline=) describes both hosted-wallet process and transfers from seized unhosted wallets; this is often the applicable path for native bearer assets |
| **Protocol-native managed currency — NIST/Prometheus research** | Identity-proofed administrator and law-enforcement roles are embedded in a blockchain design, with consensus constraining and recording their actions | Account freeze, fund seizure, issuance, and other defined management transactions | NIST and Prometheus Computing built a Bitcoin-derived [working prototype](https://csrc.nist.gov/pubs/conference/2019/11/24/implementing-a-protocol-native-managed-cryptocurre/final) following earlier [managed-currency architecture research](https://csrc.nist.gov/pubs/conference/2018/08/01/managed-blockchain-based-cryptocurrencies/final); it is research evidence, not a production network |

These examples should not be collapsed into one “reversibility” score. A
custodian moving assets with an existing key, an issuer executing a forced
transfer, an arbitrator calling a contract, and nodes changing transaction
validity have materially different governance, finality, and systemic effects.

## Platform-Level Asset Controls

This table identifies available control mechanisms, not a preferred level of
reversibility. A platform can support both tightly controlled and
holder-controlled assets depending on configuration.

| Platform or model | Native asset | Issued-asset or application controls | Assessment note |
|-------------------|--------------|--------------------------------------|-----------------|
| Bitcoin (BTC) | Ordinary native-asset transfers use keys and Bitcoin Script; no standard issuer freeze or clawback authority | Overlay protocols, custodians, and applications may add their own controls | Do not infer an on-chain confiscation capability from an exchange's account freeze |
| Bitcoin Cash (BCH) | Ordinary native BCH transfers use keys and Script; no standard issuer freeze or clawback authority | Token and application policy depends on the selected protocol and contract design | Assess native BCH separately from an issued token |
| Bitcoin SV (BSV) | UTXO-based native asset plus the published NAR/DAR node-enforcement model | Token and overlay protocols may add issuer or application controls | Review NAR/DAR adoption, legal trigger, node behavior, and divergence risk |
| Ethereum, Polygon, Besu, and other EVM environments | A base network's native asset is distinct from an issued token | Token contracts can implement role-based mint/burn, pause, denylist, clawback-like transfer, or upgrade functions; none should be assumed from the ERC label alone | Inspect deployed bytecode, proxy and upgrade paths, roles, multisig, delays, and events; [OpenZeppelin documents common access-control](https://docs.openzeppelin.com/contracts/5.x/access-control) and [pausable-token patterns](https://docs.openzeppelin.com/contracts/5.x/api/token/erc20#ERC20Pausable) |
| ERC-3643 regulated EVM tokens | The EVM network's native asset is separate | Permissioned token agents can freeze addresses or balances, pause, burn, recover a lost wallet, and force transfers | Confirm the deployed implementation, appointed agents, governing instrument, and decision-authentication process; see [ERC-3643](https://eips.ethereum.org/EIPS/eip-3643) |
| Algorand | ALGO is distinct from an Algorand Standard Asset (ASA) | ASAs can designate manager, reserve, freeze, and clawback addresses; the freeze and clawback addresses can affect holder accounts | Record whether each authority exists and whether it can be changed or permanently removed; see [Algorand asset operations](https://dev.algorand.co/concepts/assets/asset-operations/) |
| Stellar | XLM has no issuer; issued assets have an identified issuer | Issuers can require authorization, revoke authorization to freeze an asset, and enable clawback that burns an amount from a holder | Record issuer flags and whether powers were irreversibly disabled; see [Stellar asset controls](https://developers.stellar.org/docs/tokens/control-asset-access) and [clawbacks](https://developers.stellar.org/docs/build/guides/transactions/clawbacks) |
| XRP Ledger | Native XRP is not an issued token | Issuers can configure freeze and clawback for eligible trust-line tokens and Multi-Purpose Tokens | XRP itself cannot be clawed back; see [XRPL clawback documentation](https://xrpl.org/docs/concepts/tokens/fungible-tokens/clawing-back-tokens) |
| Hedera | HBAR is distinct from a Hedera Token Service token | Token keys can govern administration, KYC, freeze, wipe, supply, fees, pause, and metadata | Determine which keys were set and whether the token is immutable; see [Hedera TokenUpdate](https://docs.hedera.com/hedera/sdks-and-apis/hedera-api/token-service/tokenupdate) and [TokenWipeAccount](https://docs.hedera.com/hedera/sdks-and-apis/hedera-api/token-service/tokenwipeaccount) |
| Solana | SOL is distinct from an SPL token | Token mints can retain mint and freeze authorities; Token-2022 adds policy-oriented extensions such as a default account state | Identify the token program and every retained authority; see [SPL Token basics](https://solana.com/docs/tokens/basics) and [Token-2022 default state](https://solana.com/docs/tokens/extensions/default-state) |
| Polymesh | POLYX is distinct from an issued asset | Asset owners and agents can apply compliance rules, freeze assets, and perform controller transfers | Treat issuer identity, agent permissions, legal authority, and controller-transfer audit history as part of the asset assessment; see [Polymesh assets](https://developers.polymesh.network/core/assets/) |
| Hyperledger Fabric | No required global native asset model | Membership, ACL, endorsement, modification, and chaincode rules can define who may create or change asset state | The consortium agreement and application logic are part of the asset policy; see [Fabric policies](https://hyperledger-fabric.readthedocs.io/en/latest/policies/policies.html) |
| Corda and other permissioned workflow ledgers | Deployment-specific | Contract rules, participants, notaries, identity, and network governance determine valid state transitions | Review the legal agreement and CorDapp or application rules; do not assume a global freeze or clawback feature |

Platforms in the broader comparison catalog that are not listed here remain in
scope. Their asset-policy rows should be added when current primary sources and
a specific asset model have been identified.

## Public-Sector Policy Requirements

For any asset that carries value, eligibility, title, authority, or a claim on
an off-chain item, document the following before selecting a platform:

| Requirement | Questions to answer |
|-------------|---------------------|
| Asset and authoritative record | What exactly does the token represent? Is the ledger, an agency system, a registrar, or a legal instrument authoritative? |
| Control authority | Which issuer, agency, contractor, consortium, node operator, custodian, court, tribunal, oracle, or key holder can act? |
| Available actions | Can the controller deny issuance, freeze, pause, wipe, burn, reassign, reverse, invalidate a block, or alter the governing code? |
| Trigger and evidence | Is action based on statute, regulation, program rule, contract, sanctions list, fraud determination, court order, arbitration, or administrator discretion? |
| Due process and redress | What notice, hearing, emergency process, appeal, correction, compensation, and restoration mechanisms apply? |
| Jurisdiction and conflicts | Which law and forum govern? How are foreign, state, federal, tribal, or conflicting orders recognized? |
| Administrative security | Are powers separated, least-privileged, multisignature-controlled, time-delayed, logged, monitored, rotated, and recoverable? |
| Holder disclosure | Can a holder discover all controls before acquisition? Can powers be added, upgraded, delegated, or permanently removed? |
| Privacy and records | What order, identity, case, or asset data becomes public? How are sealing, retention, disclosure, and correction handled? |
| Ecosystem effect | Will wallets, custodians, exchanges, bridges, indexers, auditors, and downstream systems recognize the action? |
| Continuity and failure | What happens if an issuer, oracle, administrator, vendor, court feed, or network association becomes unavailable or compromised? |
| Evidence and maturity | Is the capability documented, testable, audited, deployed, and supported by independently verifiable cases? |

Federal technical and compliance references help frame—but do not answer—these
questions:

- [NISTIR 8202, *Blockchain Technology
  Overview*](https://www.nist.gov/publications/blockchain-technology-overview)
  describes blockchains as tamper evident and tamper resistant rather than
  absolutely immutable.
- [NISTIR 8301, *Blockchain Networks: Token Design and Management
  Overview*](https://www.nist.gov/publications/blockchain-networks-token-design-and-management-overview)
  separates token, wallet, transaction, interface, and protocol concerns.
- [GAO-22-104625, *Blockchain: Emerging Technology Offers Benefits for Some
  Applications but Faces
  Challenges*](https://www.gao.gov/products/gao-22-104625)
  identifies governance, legal, regulatory, privacy, security, and
  interoperability challenges.
- [OFAC's virtual-currency industry
  guidance](https://home.treasury.gov/news/press-releases/jy0410) makes clear
  that sanctions obligations can apply to virtual-currency activity. That
  compliance obligation does not prescribe one technical remedy or make a
  protocol-level reassignment necessary.
- NIST and Prometheus Computing's [protocol-native managed-cryptocurrency
  prototype](https://csrc.nist.gov/pubs/conference/2019/11/24/implementing-a-protocol-native-managed-cryptocurre/final)
  and NIST's [consensus-enforced managed-currency
  architecture](https://csrc.nist.gov/pubs/conference/2018/08/01/managed-blockchain-based-cryptocurrencies/final)
  examine transparent, constrained administrative powers, including
  law-enforcement-related freezing and seizure. These are research results,
  not federal policy or production endorsements.

## Fields to Add to Platform and Use-Case Assessments

- Asset type: native, issued, smart-contract, credential, NFT, or off-chain
  claim.
- Authoritative record and governing legal instrument.
- Controller and source of authority.
- Freeze, pause, burn, wipe, clawback, reassignment, and block-invalidation
  capabilities.
- Court-order, tribunal, sanctions, and administrative-action integration.
- Revocability of each control and whether new controls can be added by upgrade.
- Key custody, multisignature threshold, separation of duties, time delay, and
  emergency process.
- Holder notice, public event log, directive publication, and audit evidence.
- Appeal, correction, restoration, and conflicting-order procedure.
- Production adoption, source date, version, audit status, and independent
  deployment evidence.

## Maintenance Notes

- Prefer protocol specifications, code, governing rules, statutes, regulations,
  court dockets, and agency publications over marketing descriptions.
- Attribute a claim to its source. Jurat's site describes Jurat's model; BSV
  Association publications describe the NAR/DAR model.
- Record whether a capability is historical, proposed, experimental, shipped
  but inactive, deployed, or independently demonstrated.
- Recheck links, rule versions, software releases, network adoption, and legal
  status before relying on this draft for policy or acquisition decisions.
- Treat inclusion as an invitation for sourced correction and industry input,
  not endorsement or preference.
