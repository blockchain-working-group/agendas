# Blockchain Comparison Matrix
<!-- Public sector suitability prioritized. Characteristics aligned to GBA BMM elements. -->
<!-- This file is intended to evolve — add chains and columns as needed. -->

**Last updated**: 2026-04-02
**Focus**: Public sector suitability
**Framework**: Characteristics aligned to [GBA BMM elements](https://gbaglobal.org/blockchain-maturity-model/)

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

## Public Sector Suitability Tiers

| Chain | Tier | Notes |
|-------|------|-------|
| Hyperledger Fabric | **Tier 1** | Most deployed in government; permissioned; enterprise support ecosystem |
| Hyperledger Besu | **Tier 1** | EVM-compatible permissioned/public; used in regulated industries |
| R3 Corda | **Tier 1** | Built for regulated industries; legal-grade finality; strong in finance |
| Algorand | **Tier 2** | Carbon-neutral PoS; used in government digital ID and CBDC pilots |
| Stellar | **Tier 2** | Used in cross-border payments, financial inclusion, and government pilots |
| Ethereum (Mainnet) | **Tier 2** | Largest public ecosystem; PoS post-Merge; permissioning requires L2/rollup |
| Polygon (PoS) | **Tier 2** | EVM-compatible L2; lower cost; used in public records and credential pilots |
| Solana | **Tier 3** | High throughput; historically unstable; limited government adoption |
| Bitcoin | **Tier 3** | Anchor-only use case (timestamping); no smart contracts natively |
| Hedera Hashgraph | **Tier 2** | Governed by enterprise council; fast finality; CBDC and public sector pilots |

---

## Characteristics Matrix

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
| Bitcoin | ✅ | ⚠️ | Mining pool concentration risk |
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
| Bitcoin | BIP process + miners | ❌ | UASF / miner signaling | ❌ Not suited for enterprise governance |
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
| Bitcoin | UTXO / address | ❌ | ❌ | ❌ |
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
| Bitcoin | ❌ | ❌ | ⚠️ | ❌ |
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
| Bitcoin | ~7 | ~60 min (6 conf) | Variable | Lightning (off-chain) |
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
| Bitcoin | ❌ | ❌ | ❌ | ❌ |
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
| Bitcoin | ✅ Longest chain rule | ✅ | ❌ | ✅ |
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
| Bitcoin | ✅ Never down | ✅ | ✅ | — |
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
| Bitcoin | ✅ | — No Turing-complete SC | ✅ | Very low |
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
| Bitcoin | MIT | ❌ No commercial entity | ✅ | High (PoW) |
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
| Bitcoin | Nakamoto PoW | Probabilistic | ✅ Possible | ❌ 51% attack |
| Hedera | aBFT Hashgraph | Instant | ❌ | ✅ 1/3 |

---

## Additional Characteristics

### Public Sector Adoption Evidence

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
| Bitcoin | ❌ | ❌ | ⚠️ El Salvador | ❌ |
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
| Bitcoin | ✅ | ❌ | ❌ | ❌ |
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
| Bitcoin | ⚠️ Script only | Script | ❌ | ❌ |
| Hedera | ✅ | Solidity (EVM) + Hedera services | ✅ | ⚠️ |

---

## Columns to Add

The following characteristics are planned for future iterations:

- GBA BMM Assessment Status (assessed / not assessed / in progress)
- FedRAMP-adjacent certifications (SOC 2, ISO 27001, etc.)
- NIST alignment (SP 800-53, FIPS 140)
- DID/VC standard support (W3C DID, OpenID4VC)
- Token standard support (fungible, non-fungible, SBT)
- Cross-border regulatory status
- Open source health (contributor diversity, release cadence)
- Vendor lock-in risk
- Testnet/sandbox availability for procurement evaluation

---

*Assessments are approximate and subject to change. Verify against current documentation before procurement decisions.*
*Framework: [GBA Blockchain Maturity Model](https://gbaglobal.org/blockchain-maturity-model/)*
