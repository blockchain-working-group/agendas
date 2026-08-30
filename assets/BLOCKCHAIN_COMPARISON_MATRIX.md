# Blockchain and DLT Platform Comparison Matrix
<!-- Inclusive comparison catalog; inclusion is not endorsement or preference. -->
<!-- Characteristics are aligned to GBA BMM elements where applicable. -->
<!-- This file is intended to evolve through working-group and industry participation. -->

**Last updated**: 2026-07-23
**Focus**: Public-sector evaluation with open industry participation
**Framework**: Characteristics aligned to [GBA BMM elements](https://gbaglobal.org/blockchain-maturity-model/)
**Related reference**: [Public Sector Blockchain Use Cases](./PUBLIC_SECTOR_USE_CASES.md)
**Asset policy reference**: [Blockchain Asset Policies and Control Models](./BLOCKCHAIN_ASSET_POLICIES.md)
**Community catalog**: [Working Group Sandbox (`/agendas/sandbox/`)](https://blockchain-working-group.github.io/agendas/sandbox/)

---

## Legend

| Symbol | Meaning |
|--------|---------|
| ✅ | Strong / native support |
| ⚠️ | Partial / requires configuration |
| ❌ | Weak / not supported |
| 🔬 | Experimental / emerging |
| — | Not applicable or insufficient data |

---

## Scope and Participation

This is an open comparison catalog, not a preferred-platform list. A platform's
inclusion means that it has come up in working-group discussion, appears in the
[Working Group Sandbox](https://blockchain-working-group.github.io/agendas/sandbox/),
or has been proposed as relevant to a public-sector use case. Inclusion does
not represent ACT-IAC, member, agency, or procurement endorsement.

Public networks, permissioned frameworks, DLT networks, and integration
platforms are listed together for discovery, but they should be compared within
the correct deployment category. A missing or pending assessment is an
invitation for sourced industry input, not a negative rating.

| Platform or ecosystem | Type | Inclusion basis | Assessment coverage |
|-----------------------|------|-----------------|---------------------|
| Ethereum Mainnet | Public programmable L1 | Sandbox; broad EVM ecosystem | Initial detailed assessment |
| F1R3FLY / RChain-derived stack | Decentralized compute and storage platform | Sandbox; participant interest | Queued for sourced assessment |
| Bitcoin (BTC) | Public proof-of-work UTXO network | Sandbox; Bitcoin-family baseline | Detailed assessment plus family comparison |
| Bitcoin Cash (BCH) | Public proof-of-work UTXO network | Sandbox; Bitcoin variant | Bitcoin-family comparison |
| Bitcoin SV (BSV) | Public proof-of-work UTXO network | Sandbox; Bitcoin variant and participant interest | Bitcoin-family comparison |
| Hyperledger Fabric | Permissioned DLT framework | Sandbox Hyperledger ecosystem | Initial detailed assessment |
| Hyperledger Besu | Public or permissioned EVM client | Sandbox Hyperledger ecosystem | Initial detailed assessment |
| Hyperledger Iroha | Permissioned DLT framework | Named in Sandbox Hyperledger ecosystem | Queued for sourced assessment |
| R3 Corda | Permissioned distributed-ledger platform | Regulated multi-party workflows | Initial detailed assessment |
| Algorand | Public programmable L1 | Existing matrix and participant research | Initial detailed assessment |
| Stellar | Public payments and asset network | Existing matrix and participant research | Initial detailed assessment |
| Polygon PoS | Public EVM-compatible Ethereum sidechain | Existing matrix and participant research | Initial detailed assessment |
| Solana | Public programmable L1 | Existing matrix and participant research | Initial detailed assessment |
| Hedera | Public hashgraph-based DLT network | Existing matrix and participant research | Initial detailed assessment |
| SIMBA Chain | Blockchain integration and service platform | Sandbox; government and defense focus | Queued for sourced assessment |
| Avalanche | Public network and configurable L1 platform | Matrix review candidate | Queued for sourced assessment |
| Hyperledger Indy | Identity-focused distributed-ledger software | Matrix review candidate; public-sector identity use cases | Queued for sourced assessment |
| XRP Ledger | Public payments, assets, and credential network | Matrix review candidate | Queued for sourced assessment |
| Canton Network | Privacy-enabled network for regulated assets and workflows | Matrix review candidate | Queued for sourced assessment |

Assessment coverage describes the state of this draft, not platform maturity.
Industry participants are encouraged to contribute source-dated corrections,
deployment evidence, and additional platforms.

## Bitcoin-Family Comparison

BTC, BCH, and BSV share historical roots and a proof-of-work UTXO model, but
they are separate networks with different scaling policies, application
approaches, governance communities, infrastructure, and risk profiles. They
should not be represented by one generic “Bitcoin” row.

| Network | Ecosystem emphasis | Scaling and application approach | Candidate public-sector patterns | Assessment caveat |
|---------|--------------------|----------------------------------|----------------------------------|-------------------|
| [Bitcoin (BTC)](https://bitcoin.org/en/how-it-works) | Peer-to-peer value transfer, settlement, and digital scarcity | Conservative base-layer design; Bitcoin Script; higher-layer and off-chain systems commonly used for additional capabilities | Public timestamp anchoring, payment acceptance, reserves or treasury policy research, and public-ledger analytics | General-purpose application logic and direct data storage are intentionally limited compared with programmable chains |
| [Bitcoin Cash (BCH)](https://documentation.cash/protocol/blockchain/block.html) | Peer-to-peer electronic cash and low-cost on-chain transactions | Larger blocks; UTXO-based Script with native token-aware operations | Payments, tokenized records, timestamping, and public-ledger analytics | Public-sector deployments, operational requirements, and support ecosystem require use-case-specific validation |
| [Bitcoin SV (BSV)](https://docs.bsvblockchain.org/) | High-volume on-chain transactions, data integrity, tokenization, and enterprise applications | UTXO-based Script; emphasis on large-block scaling, data transactions, overlay services, and the Teranode scaling roadmap | High-volume audit events, data-integrity proofs, payments, tokenized records, and supply-chain events | Throughput, node operations, governance, vendor support, and public-sector deployment evidence require independent validation |

---

## Initial Detailed Characteristics Matrix

The tables below preserve the original assessment set while sourced rows are
developed for the broader coverage register above. They are not a shortlist of
preferred platforms.

### BMM Element 1 — Distribution

| Chain | Node Distribution | Operator Independence | Hosting Concentration Risk |
|-------|------------------|-----------------------|---------------------------|
| Hyperledger Fabric | ⚠️ | ⚠️ Consortium-controlled | High if single org runs all nodes |
| Hyperledger Besu | ✅ (public) / ⚠️ (permissioned) | ⚠️ | Configurable |
| R3 Corda | ⚠️ | ⚠️ | Notary concentration risk |
| Algorand | ✅ | ✅ | Low; relay nodes globally distributed |
| Stellar | ✅ | ⚠️ | SDF influence on validators is notable |
| Ethereum | ✅ | ✅ | Low; 900K+ validators post-Merge |
| Polygon (PoS) | ⚠️ | ⚠️ | Validator set smaller than mainnet |
| Solana | ⚠️ | ⚠️ | High validator concentration by stake |
| Bitcoin (BTC) | ✅ | ⚠️ | Mining pool concentration risk |
| Hedera | ⚠️ | ⚠️ | 39-member governing council |

### BMM Element 2 — Governance

| Chain | Governance Model | On-Chain Governance | Upgrade Process | Public Sector Fit |
|-------|-----------------|--------------------|-----------------|--------------------|
| Hyperledger Fabric | Consortium agreement | ❌ | Channel config update | ✅ Configurable to agency policy |
| Hyperledger Besu | Consortium or public | ⚠️ | IBFT/QBFT voting | ✅ |
| R3 Corda | Network operator | ❌ | Network map service | ✅ Legal-grade governance docs |
| Algorand | Foundation + ARC proposals | 🔬 | On-chain voting emerging | ⚠️ |
| Stellar | SDF + Stellar Core | ❌ | Foundation-led | ⚠️ Centralized influence |
| Ethereum | EIP process + core devs | ❌ (off-chain) | Rough consensus + hardfork | ⚠️ Diffuse; hard to contract with |
| Polygon (PoS) | Polygon Labs + validators | ⚠️ | PIPs process | ⚠️ |
| Solana | Solana Labs dominant | ❌ | Labs-driven | ❌ Single entity risk |
| Bitcoin (BTC) | BIP process + node operators, developers, miners, and users | ❌ | BIP process, software adoption, and participant signaling | ⚠️ No single contracting authority; policy control remains external to the network |
| Hedera | Governing Council (39 orgs) | ❌ | Council vote | ✅ Most enterprise-legible governance |

### BMM Element 3 — Identity Management

| Chain | Identity Model | Permissioning | DID Support | KYC/AML Ready |
|-------|---------------|--------------|-------------|----------------|
| Hyperledger Fabric | MSP / X.509 certs | ✅ Native | ✅ via Aries | ✅ |
| Hyperledger Besu | Account-based | ✅ Permissioning API | ✅ via Aries | ✅ |
| R3 Corda | X.509 legal identity | ✅ | ⚠️ | ✅ |
| Algorand | Account-based | ⚠️ | ✅ via ARC standards | ⚠️ |
| Stellar | Account-based | ⚠️ SEP-0010 | ⚠️ | ⚠️ SEP-0012 KYC anchor |
| Ethereum | Account/EOA | ❌ native | ✅ ENS, ERC-725 | ⚠️ Layer 2 solutions required |
| Polygon (PoS) | Account-based | ❌ native | ✅ Polygon ID | ⚠️ |
| Solana | Account-based | ❌ | ⚠️ | ❌ |
| Bitcoin (BTC) | UTXO / address | ❌ native | ⚠️ External identity layers | ⚠️ External compliance controls and analytics |
| Hedera | Account-based + keys | ⚠️ | 🔬 | ⚠️ |

### BMM Element 4 — Interoperability

| Chain | Cross-Chain | Legacy System Integration | API Maturity | Standards Compliance |
|-------|------------|--------------------------|-------------|----------------------|
| Hyperledger Fabric | ⚠️ Weave / custom | ✅ REST, gRPC, event bus | ✅ | ✅ W3C, ISO |
| Hyperledger Besu | ✅ EVM bridges | ✅ JSON-RPC, REST | ✅ | ✅ |
| R3 Corda | ⚠️ | ✅ JDBC, messaging | ✅ | ✅ FIX, ISO 20022 |
| Algorand | ⚠️ | ✅ REST API | ✅ | ⚠️ |
| Stellar | ⚠️ | ✅ Horizon API | ✅ | ✅ ISO 20022 SEPs |
| Ethereum | ✅ Bridge ecosystem | ✅ JSON-RPC | ✅ | ✅ ERC standards |
| Polygon (PoS) | ✅ PoS bridge | ✅ | ✅ | ✅ ERC compatible |
| Solana | ⚠️ Wormhole | ⚠️ | ✅ | ⚠️ |
| Bitcoin (BTC) | ⚠️ Higher-layer protocols | ⚠️ RPC, APIs, and vendor services | ✅ Mature | ⚠️ Bitcoin standards and external specifications |
| Hedera | ⚠️ | ✅ REST, gRPC | ✅ | ⚠️ |

### BMM Element 5 — Performance

| Chain | TPS (approx) | Finality | Transaction Cost | Scalability Path |
|-------|-------------|---------|-----------------|-----------------|
| Hyperledger Fabric | 3,000–20,000 | ~1s | Near zero (permissioned) | Channels |
| Hyperledger Besu | ~1,000 (IBFT) | 2–5s | Near zero (permissioned) | Channels |
| R3 Corda | ~170 per notary | Notary-dependent | Near zero | Notary clusters |
| Algorand | ~6,000 | ~4.5s | ~$0.001 | PurePoS |
| Stellar | ~1,000 | 3–5s | ~$0.00001 | Limited |
| Ethereum | ~15–30 (L1) | ~12s L1 / ~1s L2 | Variable; L2 low | L2 rollups |
| Polygon (PoS) | ~7,000 | ~2s | ~$0.01 | zkEVM roadmap |
| Solana | ~65,000 theoretical | ~400ms | ~$0.00025 | Monolithic |
| Bitcoin (BTC) | ~7 | Probabilistic; confirmation target depends on risk | Variable | Payment channels and higher-layer protocols |
| Hedera | ~10,000+ | ~3–5s | ~$0.0001 | aBFT |

### BMM Element 6 — Privacy

| Chain | Private Transactions | PII Controls | GDPR Tooling | Confidential Compute |
|-------|---------------------|-------------|-------------|----------------------|
| Hyperledger Fabric | ✅ Private data collections | ✅ | ✅ | ✅ |
| Hyperledger Besu | ✅ Tessera / Orion | ✅ | ✅ | ⚠️ |
| R3 Corda | ✅ Need-to-know | ✅ | ✅ | ⚠️ |
| Algorand | ⚠️ | ⚠️ | ⚠️ | 🔬 |
| Stellar | ❌ | ⚠️ | ❌ | ❌ |
| Ethereum | ⚠️ ZK proofs available | ⚠️ | ⚠️ | 🔬 |
| Polygon (PoS) | ⚠️ | ⚠️ | ⚠️ | ✅ Polygon ID ZK |
| Solana | ❌ | ❌ | ❌ | ❌ |
| Bitcoin (BTC) | ⚠️ Public and pseudonymous transactions | ❌ native | ❌ native | ❌ native |
| Hedera | ⚠️ | ⚠️ | ⚠️ | ❌ |

### BMM Element 7 — Reliability

| Chain | Fork Resolution | Double-Spend Protection | Fraud Controls | Audit Trail |
|-------|----------------|------------------------|---------------|------------|
| Hyperledger Fabric | ✅ No forks (CFT/BFT) | ✅ | ✅ | ✅ |
| Hyperledger Besu | ✅ IBFT/QBFT | ✅ | ✅ | ✅ |
| R3 Corda | ✅ Notary-enforced | ✅ | ✅ | ✅ |
| Algorand | ✅ No forks (PurePoS) | ✅ | ⚠️ | ✅ |
| Stellar | ✅ FBA consensus | ✅ | ⚠️ | ✅ |
| Ethereum | ✅ Post-Merge | ✅ | ⚠️ | ✅ |
| Polygon (PoS) | ✅ | ✅ | ⚠️ | ✅ |
| Solana | ⚠️ History of outages | ✅ | ❌ | ✅ |
| Bitcoin (BTC) | ✅ Most-work chain rule | ✅ | ⚠️ External analytics and controls | ✅ |
| Hedera | ✅ aBFT | ✅ | ⚠️ | ✅ |

### BMM Element 8 — Resilience

| Chain | Outage History | Node Recovery | Geographic Distribution | Disaster Recovery Docs |
|-------|---------------|--------------|------------------------|------------------------|
| Hyperledger Fabric | ✅ | ✅ | ⚠️ Consortium-dependent | ✅ |
| Hyperledger Besu | ✅ | ✅ | ⚠️ | ✅ |
| R3 Corda | ✅ | ✅ | ⚠️ | ✅ |
| Algorand | ✅ | ✅ | ✅ | ✅ |
| Stellar | ✅ | ✅ | ✅ | ✅ |
| Ethereum | ✅ | ✅ | ✅ | ✅ |
| Polygon (PoS) | ⚠️ | ✅ | ✅ | ⚠️ |
| Solana | ❌ Multiple outages | ⚠️ | ✅ | ⚠️ |
| Bitcoin (BTC) | ✅ Long operating history | ✅ | ✅ | — |
| Hedera | ✅ | ✅ | ✅ | ✅ |

### BMM Element 9 — Security

| Chain | Audit History | Smart Contract Safety | Key Management | Known Exploits |
|-------|--------------|----------------------|---------------|----------------|
| Hyperledger Fabric | ✅ | ✅ Go/Java chaincode | ✅ HSM support | Minimal |
| Hyperledger Besu | ✅ | ⚠️ EVM risks | ✅ HSM support | Low |
| R3 Corda | ✅ | ✅ JVM sandbox | ✅ HSM support | Minimal |
| Algorand | ✅ | ⚠️ TEAL/AVM | ⚠️ | Low |
| Stellar | ✅ | ⚠️ Limited smart contracts | ⚠️ | Low |
| Ethereum | ✅ Extensive | ⚠️ EVM; many exploits in ecosystem | ⚠️ | High (ecosystem) |
| Polygon (PoS) | ✅ | ⚠️ EVM risks | ⚠️ | Medium (bridge exploits) |
| Solana | ⚠️ | ⚠️ Rust; complex model | ❌ | High (multiple exploits) |
| Bitcoin (BTC) | ✅ Extensive base-protocol review | ⚠️ Constrained Bitcoin Script | ✅ Mature custody and key-management ecosystem | Low at base protocol; application and custody risks are separate |
| Hedera | ✅ | ⚠️ EVM + Hedera services | ⚠️ | Low |

### BMM Element 10 — Infrastructure Sustainability

| Chain | Licensing | Commercial Support | Long-Term Viability | Energy Use |
|-------|----------|--------------------|--------------------|-----------| 
| Hyperledger Fabric | Apache 2.0 | ✅ IBM, AWS, Azure | ✅ LF Decentralized Trust | Low |
| Hyperledger Besu | Apache 2.0 | ✅ ConsenSys, AWS | ✅ LF Decentralized Trust | Low |
| R3 Corda | Apache 2.0 (OS) / Commercial | ✅ R3 enterprise | ✅ | Low |
| Algorand | MIT | ✅ Algorand Foundation | ✅ | Very low |
| Stellar | Apache 2.0 | ✅ SDF + partners | ✅ | Very low |
| Ethereum | Multiple open | ✅ Large ecosystem | ✅ | Low (PoS) |
| Polygon (PoS) | MIT / GPL | ✅ Polygon Labs | ⚠️ Evolving roadmap | Low |
| Solana | Apache 2.0 | ⚠️ Solana Labs | ⚠️ VC-dependent | Medium |
| Bitcoin (BTC) | MIT | ✅ Broad vendor ecosystem; no protocol owner | ✅ | High (PoW) |
| Hedera | Apache 2.0 | ✅ Council members | ✅ | Very low |

### BMM Element 11 — Synchronization

| Chain | Consensus Mechanism | Finality Type | Fork Possibility | BFT Tolerance |
|-------|--------------------|--------------|-----------------|--------------| 
| Hyperledger Fabric | CFT (Raft) / BFT (optional) | Deterministic | ❌ | ✅ |
| Hyperledger Besu | IBFT 2.0 / QBFT | Deterministic | ❌ | ✅ |
| R3 Corda | Notary-based (CFT/BFT) | Notary-final | ❌ | ✅ |
| Algorand | PurePoS (BA★) | Instant | ❌ | ✅ 1/3 |
| Stellar | Federated Byzantine Agreement | Fast | ❌ | ✅ |
| Ethereum | LMD-GHOST + Casper FFG | Probabilistic → Finalized | ⚠️ Rare | ✅ 1/3 |
| Polygon (PoS) | Heimdall + Bor (PoS) | Checkpoint-based | ⚠️ | ⚠️ |
| Solana | PoH + Tower BFT | Optimistic | ⚠️ | ⚠️ |
| Bitcoin (BTC) | Nakamoto PoW | Probabilistic | ✅ Possible | ⚠️ Security depends on majority hash power |
| Hedera | aBFT Hashgraph | Instant | ❌ | ✅ 1/3 |

---

## Additional Characteristics

### Public Sector Adoption Evidence

For use-case patterns, agency examples, and links to source material, see
[Public Sector Blockchain Use Cases](./PUBLIC_SECTOR_USE_CASES.md).
This initial table is incomplete; platforms in the coverage register remain in
scope while their deployment evidence is researched and sourced.

| Chain | US Federal | US State/Local | International Gov | CBDC Pilots |
|-------|-----------|---------------|-------------------|-------------|
| Hyperledger Fabric | ✅ DHS, DoD supply chain pilots | ✅ Multiple | ✅ Wide | ✅ |
| Hyperledger Besu | ✅ | ⚠️ | ✅ Baseline Protocol (EY) | ✅ |
| R3 Corda | ✅ DTCC, Fed pilots | ⚠️ | ✅ Wide financial | ✅ |
| Algorand | ⚠️ | ⚠️ | ✅ Marshall Islands SOV, Italy | ✅ |
| Stellar | ⚠️ | ⚠️ | ✅ Ukraine, SE Asia | ✅ |
| Ethereum | ⚠️ | ⚠️ | ✅ EU ESSIF, Colorado | ❌ |
| Polygon (PoS) | ⚠️ | ✅ Colorado Web3 credentials | ✅ | ⚠️ |
| Solana | ❌ | ❌ | ❌ | ❌ |
| Bitcoin (BTC) | ⚠️ Policy, enforcement, and analytics uses | ⚠️ State and local policy activity | ✅ El Salvador and other international policy activity | ❌ |
| Hedera | ⚠️ | ⚠️ | ✅ | ✅ |

### Permissioning Model

| Chain | Public | Private / Permissioned | Hybrid | Native Access Control |
|-------|--------|----------------------|--------|----------------------|
| Hyperledger Fabric | ❌ | ✅ | ✅ | ✅ |
| Hyperledger Besu | ✅ | ✅ | ✅ | ✅ |
| R3 Corda | ❌ | ✅ | ✅ | ✅ |
| Algorand | ✅ | ✅ | ✅ | ⚠️ |
| Stellar | ✅ | ⚠️ | ⚠️ | ⚠️ |
| Ethereum | ✅ | ❌ native | ⚠️ L2 | ❌ native |
| Polygon (PoS) | ✅ | ❌ native | ⚠️ | ❌ native |
| Solana | ✅ | ❌ | ❌ | ❌ |
| Bitcoin (BTC) | ✅ | ❌ native | ⚠️ Higher-layer and federated systems | ❌ native |
| Hedera | ✅ | ⚠️ | ⚠️ | ⚠️ |

### Smart Contract Capability

| Chain | Smart Contracts | Language(s) | EVM Compatible | Formal Verification |
|-------|----------------|------------|---------------|---------------------|
| Hyperledger Fabric | ✅ Chaincode | Go, Java, Node.js | ❌ | ⚠️ |
| Hyperledger Besu | ✅ | Solidity, Vyper | ✅ | ⚠️ |
| R3 Corda | ✅ CorDapps | Kotlin, Java | ❌ | ⚠️ |
| Algorand | ✅ | PyTeal, TEAL, AVM | ❌ | ⚠️ |
| Stellar | ✅ Soroban | Rust | ❌ | 🔬 |
| Ethereum | ✅ | Solidity, Vyper, Huff | ✅ | ⚠️ |
| Polygon (PoS) | ✅ | Solidity, Vyper | ✅ | ⚠️ |
| Solana | ✅ Programs | Rust, C | ❌ | ❌ |
| Bitcoin (BTC) | ⚠️ Constrained transaction programs | Bitcoin Script | ❌ | ⚠️ Script analysis and formally specified subsets |
| Hedera | ✅ | Solidity (EVM) + Hedera services | ✅ | ⚠️ |

---

## Asset Policy and Legal Control

Asset control is not a single chain-level characteristic. Native coins, issued
tokens, smart-contract assets, custodial accounts, and off-chain legal rights
can each have different policies. Freeze, pause, wipe, burn, clawback,
reassignment, court-order integration, and administrator upgrade powers must be
assessed for the specific asset—not inferred from a platform name.

See [Blockchain Asset Policies and Control
Models](./BLOCKCHAIN_ASSET_POLICIES.md) for the control-model taxonomy,
platform-level examples, public-sector requirements, and focused treatment of
Jurat and the BSV Association's Network Access Rules and Digital Asset Recovery
design.

## Columns to Add

The following characteristics are planned for future iterations:

- GBA BMM Assessment Status (assessed / not assessed / in progress)
- FedRAMP-adjacent certifications (SOC 2, ISO 27001, etc.)
- NIST alignment (SP 800-53, FIPS 140)
- DID/VC standard support (W3C DID, OpenID4VC)
- Token standard support (fungible, non-fungible, SBT)
- Asset type and authoritative record
- Retained issuer, contract, network, oracle, and custody controls
- Freeze, pause, burn, wipe, clawback, reassignment, and block-invalidation
  capabilities
- Court-order integration, due process, appeal, and conflicting-order handling
- Administrative-key security, revocability, disclosure, and audit evidence
- Cross-border regulatory status
- Open source health (contributor diversity, release cadence)
- Vendor lock-in risk
- Testnet/sandbox availability for procurement evaluation

---

*Inclusion is not endorsement or preference. Assessments are approximate and
subject to change through sourced working-group and industry contributions.
Verify against current documentation before procurement decisions.*
*Framework: [GBA Blockchain Maturity Model](https://gbaglobal.org/blockchain-maturity-model/)*
