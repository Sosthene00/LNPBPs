# LNP/BP Specifications

LNP/BP stands for "Bitcoin Protocol / Lightning Network Protocol". This set of specifications covers standards & best
practices for Layer 2, 3 solutions (and above) in cases when they do not require soft- or hard-forks on the Bitcoin
blockchain level and are not directly related to issues covered in Lightning Network RFCs (BOLTs).

Basically, LNP/BPs cover everything that can be anchored to Bitcoin transactions, defines primitives for L2+ solution
design and describes complex use cases which can be built from some primitives. This allows such solutions as financial
assets, storage, messaging, computing and different forms of secondary markets leveraging Bitcoin security model and
Bitcoin as a method of payment/medium of exchange.

Criteria for a LNP/BP specification proposal:
* Should not be covered by existing or proposed BIPs
* Should not cause soft- or hard-fork in Bitcoin blockchain (but may depend on soft-forks from an existing BIP proposals)
* Should not distort Bitcoin miner's economic incentives
* Should not pollute Bitcoin blockchain with unnecessary non-transaction related data or have to maintain such pollution
  as low as possible
* Should not be covered by existing or proposed BOLTs
* Must not require a utility or security tokens to function (but may enable creation of digital assets or tokenized
physical goods)
* Must not depend on non-bitcoin blockchains (but may be applicable to bitcoin-compatible blockchains)


## List of current LNP/BP proposals

No | Layer | Vertical | Title | Author(s) | Type | Status
------:| ----- | -------- | ----- | ----- | ---- | ------
[1](lnpbp-0001.md) | Transaction (1) | Bitcoin protocol | Key tweaking: collision-resistant elliptic curve-based commitments | Maxim Orlovsky et al | Standard | Final
[2](lnpbp-0002.md) | Transaction (1) | Bitcoin protocol | Deterministic embedding of cryptographic ommitments into transaction output scriptPubkey | Maxim Orlovsky et al | Standard | Proposal
[3](lnpbp-0003.md) | Transaction (1) | Bitcoin protocol | Deterministic definition of transaction output containing cryptographic commitment | Giacomo Zucco et al | Standard | Proposal
[4](lnpbp-0004.md) | Client-validated data (3) | Cryptographic primitives | Multi-message commitment scheme with zero-knowledge provable unique properties | Maxim Orlovsky | Standard | Proposal
[5](lnpbp-0005.md) | Transaction graph (2) | Bitcoin protocol | Universal short Bitcoin identifiers for blocks, transactions and their inputs & outputs | Christian Decker et al | Standard | Proposal
6 | Transaction (1) | Bitcoin protocol | Deterministic bitcoin commitments | Maxim Orlovsky | Standard | Draft
7 | Client-validated data (3) | Consensus layer | Strict encoding | Peter Todd, Maxim Orlovsky | Standard | Planned
[8](https://petertodd.org/2016/commitments-and-single-use-seals) | Client-validated data (3) | Cryptographic primitives | Single-use-seals | Peter Todd, Maxim Orlovsky | Informational | Draft
[9](https://diyhpl.us/wiki/transcripts/scalingbitcoin/milan/client-side-validation/) | Client-validated data (3) | Consensus layer | Client-side validation | Peter Todd, Maxim Orlovsky | Informational | Draft
[10](lnpbp-0010.md) | Transaction graph (2) | Bitcoin protocol | Bitcoin transaction output-based single-use-seals with pay-to-contract commitments | Peter Todd et al | Standard | Proposal
[11](lnpbp-0011.md) | Client-validated graphs (4) | Smart contracts | RGB: Client-validated confidential smart contracts using bitcoin transaction graphs for Bitcoin and Lightning Network | Maxim Orlovsky et al | Informational | Proposal
12 | Client-validated graphs (4) | Consensus layer | RGB Schema: client-side validation rules for RGB smart contracts | Maxim Orlovsky | Standard | Planned
13 | Client-validated graphs (4) | Consensus layer | RGB client-side verification and data serialization | Maxim Orlovsky | Standard | Planned
14 | Client-validated data (3) | Smart contracts | Bech32 encoding for client-validated data | Maxim Orlovsky | Standard | Planned
[15](lnpbp-0015.md) | OSI Session (i5) | Internet2 | Handshake and encryption in network communications based on Noise_XK (BOLT-8 extract) | Multiple peers | Standard | Proposal
16 | OSI Session (i5) | Internet2 | LNP handshake over WebSockets | Maxim Orlovsky | Standard | Planned
17 | OSI Session (i5) | Internet2 | LNP handshake over ZMQ sockets | Maxim Orlovsky | Standard | Planned
[18](lnpbp-0018.md) | OSI Transport (i4) | Internet2 | Native message framing protocol (BOLT-8 extract) | Multiple peers | Standard | Planned
[19](https://github.com/internet2-org/rust-internet2/tree/master/microservices/src) | OSI Presentation (i6) | Internet2 | ZMQ-based RPC and ESB protocols for microservices | Multiple peers | Standard | Planned
[20](lnpbp-0020.md) | Application (5) | Smart contracts | RGB fungible assets schema (RGB-20) | Multiple peers | Standard | Final
[21](lnpbp-0021.md) | Application (5) | Smart contracts | RGB schema for NFTs representing ownership rights (RGB-21) | Maxim Orlovsky | Standard | Proposal
[22](https://github.com/LNP-BP/LNPBPs/issues/29) | Application (5) | Smart contracts | RGB reputation and identity schema (RGB-22) | Maxim Orlovsky, Sabina Sachtachtinskagia | Standard | Draft
23 | Application (5) | Smart contracts | RGB verifiably-unique history log for auditable data (RGB-23) | Maxim Orlovsky, Giacomo Zucco | Standard | Planned
24 | Application (5) | Smart contracts | RGB-24 schema for decentralized global name system (DGNS) | Maxim Orlovsky | Standard | Planned
30 | Application (5) | Smart contracts | RGB-wrapped native blockchain assets schema (RGB-30) | Maxim Orlovsky | Standard | Planned
25-29, 31 | Reserved | | For the future use by RGB schemata
[32](https://github.com/LNP-BP/descriptor-wallet/blob/master/src/bip32/pubkeychain.rs) | Application (5) | Bitcoin | BIP-32 derivation path extension for read-only wallets | Maxim Orlovsky | Standard | Draft
[33](https://github.com/LNP-BP/LNPBPs/issues/24) | Client-validated data (3) | Lightning network protocol | Lightspeed: micropayments for Lightning Network | Maxim Orlovsky | Draft
[34](https://github.com/storm-org/storm-spec) | Client-validated data (3) | Cryptographic primitives | Zero-knowledge arguments for data persistance using probabalistical checkable proofs | Maxim Orlovsky | Standard | Draft
[35](https://github.com/LNP-BP/LNPBPs/pull/97) | OSI Application (i7) | Lightning network protocol | Biffrost: LN message extensions for RGB data propagation | Maxim Orlovsky | Standard | Planned
[36](https://github.com/LNP-BP/LNPBPs/issues/21) | OSI Presentation (i6) | API | Recommendations for API design | Maxim Orlovsky | Informational | Draft
[37](https://github.com/LNP-BP/LNPBPs/pull/23/files) | Application (5) | Smart contracts | Invoicing formats for RGB-20 fungible assets schema | Alekos Filini | Standard | Rejected
[38](https://github.com/LNP-BP/FAQ/blob/master/Presentation%20slides/Universal%20LNP-BP%20invoices.pdf) | Application (5) | Smart contracts | Universal LNP/BP invoices supporting Bitcoin, LN & RGB | Maxim Orlovsky | Standard | Draft
[39](lnpbp-0010.md) | Transaction graph (2) | Bitcoin protocol | Bitcoin transaction output-based single-use-seals with sign-to-contract commitments | Maxim Orlovsky et al | Standard | Planned
[40](https://github.com/storm-org/storm-spec) | Transaction graph (2) | State channels | Storm: trustless storage with escrow contracts | Maxim Orlovsky | Standard | Draft
41 | OSI Application (i7) | Lightning network protocol | Lightning network message extensions for Storm | Maxim Orlovsky | Standard | Planned
[42](https://github.com/internet2-org/rust-internet2/blob/master/addr/src/encoding.rs) | OSI Application (i7) | Internet2 | Uniform encoding for internet2 addresses | Maxim Orlovsky | Draft
[43](https://lists.linuxfoundation.org/pipermail/bitcoin-dev/2021-February/018381.html) | Application (5) | Smart contracts | RGB-enabled BIP43 purpose field & identity system | Maxim Orlovsky | Standard | Draft
[44](https://github.com/LNP-BP/descriptor-wallet/blob/master/src/descriptor/script.rs) | Application (5) | Smart contracts | Script templating: BIP-32 & LNPBP-43 key derivations within for non-miniscript-compatible Bitcoin scripts | Maxim Orlovsky | Standard | Draft
45 | OSI Application (i7) | Lightning network protocol | Lightning network message extensions for decentralized exchange functionality | Maxim Orlovsky | Standard | Planned
[46](https://github.com/LNP-BP/LNPBPs/pull/98) | OSI Application (i7) | Lightning network protocol | Channel funding with RGB assets | Maxim Orlovsky | Standard | Draft
47 | OSI Application (i7) | Lightning network protocol | Multipeer lightning channels | Maxim Orlovsky | Standard | Planned
48 | OSI Application (i7) | Lightning network protocol | Bilateral channel funding | Maxim Orlovsky | Standard | Draft
49 | OSI Application (i7) | Lightning network protocol | Synchronized multi-hop state updates via delegation in Lightning network | Maxim Orlovsky, Christian Decker | Standard | Planned
50 | OSI Application (i7) | Lightning network protocol | Channel transaction structure negotiation using PSBTs (generalized LN) | Maxim Orlovsky, Christian Decker | Standard | Planned
51 | OSI Application (i7)| Lightning network protocol | Decentralized naming & name resolution system | Maxim Orlovsky | Standard | Planned
52-57 | Reserved | | For the future use by lightning network protocol extensions
[58](https://github.com/pandoracore/typhon-spec) | Client-validated data (3) | Cryptographic primitives | Apophis: distributed elliptic curve-based key creation with shared secrets | Maxim Orlovsky | Standard | Draft
[59](https://github.com/pandoracore/typhon-spec) | Transaction graph (2) | Bitcoin protocol | Typhon: trustless Bitcoin sidechains | Maxim Orlovsky | Standard | Draft
[60](https://github.com/pandoracore/ibiss-spec) | Client-validated data (3) | Game theory | Ibiss: incentive-based interactive anonymous settlement scheme for computation integrity arguments | Maxim Orlovsky, Sabina Sachtachtinskagia | Informational | Draft
[61](https://github.com/pandoracore/ibiss-spec) | Client-validated data (3) | Game theory | Toth: incentive-based interactive settlement scheme for computation integrity arguments with reputation | Maxim Orlovsky, Sabina Sachtachtinskagia | Informational | Draft
[62](https://github.com/pandoracore/prometheus-spec) | Transaction graph (2) | Smart contracts | Prometheus: trustless multiparty computing with escrow & arbitration using Ibiss protocol on bitcoin blockchain | Maxim Orlovsky | Standard | Draft
63 | Application (5) | Smart contracts | Prometheus+: trustless multiparty computing with escrow & arbitration using Ibiss2 protocol over LN with tokenized RGB reputation | Maxim Orlovsky | Standard | Planned
100 | Transaction graph (2) | Bitcoin protocol | Scalable & confidential single-use-seal commitment layer 1 | Standard | Brainstorming

### Invited or planned proposals to join LNP/BP standards family

1. Discreet log contracts: deterministic transaction structure, embedding into lightning network, wire protocols
    - [Specification effort](https://github.com/discreetlogcontracts/dlcspecs)
    - [Lightning Discreet Log Contract Channels](https://hackmd.io/@lpQxZaCeTG6OJZI3awxQPQ/LN-DLC)
2. Different [pre-Schnorr schemes for scriptless scripts](https://lists.linuxfoundation.org/pipermail/lightning-dev/2019-November/002316.html)
3. Generalized lightning network standartisation and related [eltoo](https://lists.linuxfoundation.org/pipermail/bitcoin-dev/2018-April/015907.html) and [PTLC](https://suredbits.com/payment-points-part-2-stuckless-payments/) proposals
4. Micropayments:
    - [LSAT Authentication and Payments for the Lightning-Native Web](https://lightning.engineering/posts/2020-03-30-lsat/) by Olaoluwa Osuntokun


## Layers for LNP/BP proposals:

No | Title | Description | Examples
--:| ----- | ----------- | ---------
1  | Transaction | Data or protocols defined for a single bitcoin transaction (both off-chain and on-chain) | Cryptographic primitives, advanced multisignature schemes, transaction structure
2  | Transaction graph | Data and protocols defined on a transaction graph | Blockchains, sidechains, state channels
3  | Client-validated data | Protocols and formats for off-chain data (persistent or ephemeral) | Cryptographic primitives, serialization
4  | Client-validated graphs | Protocols and formats for off-chain graph structures | Complex commitment schemes, schemata
5  | Application | Specific high-level applications build of underlying layers | Assets, audit, storage, computing, messaging, decentralized exchanges and marketplaces

Additionally to these layers there is a set of network protocol layers organized according to [ISO OSI model](https://en.wikipedia.org/wiki/OSI_model#Layer_architecture), with numbers prefixed using `i` symbol ("complex dimension").

## Verticals for LNP/BP proposals:

Name | Description | Examples
---- | ----------- | --------
Cryptographic primitives | Basic cryptographic functions applied at the level of transactions or client-validated data | Commitment schemes, zero knownledge
Consensus layer | Standards critical for consensus in distributed systems | Data encoding, validation rules
[Internet2](https://github.com/internet2-org) | Standards for end-to-end encrypted censorship-resistant networking communications (Internet2) | Network encryption, decentralized naming systems, network data serialization
Bitcoin protocol | Changes at the level of bitcoin protocol | Commitments in bitcoin transactions, single-use-seals applications to bitcoin, layer 1 enhancements
Lightning network protocol | Changes to lighting-network related standards and state channel mechanics | New types of state channels, new lightning network message types, changes in channel transaction structure
Smart contracts | Distributed smart contract execution environment and VMs | Bitcoin scripts, scriptless scripts, RGB, Simplicity language
Game theory | Game-theoretical setups for trustless protocols | Incentive schemes with bitcoin transactions & RGB smart contracts
