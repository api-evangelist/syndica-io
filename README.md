# Syndica (syndica)

Syndica is a Solana-only infrastructure company building developer infrastructure for Web3. Its production platform provides fault-tolerant, load-balanced Solana JSON-RPC over HTTP and WebSocket from four global regions (Northern Virginia, Oregon, London, Singapore), plus **ChainStream** — a real-time JSON-RPC streaming API that consolidates transaction, slot, and block updates from multiple validators using a "fastest wins" strategy with optional cross-validator verification. Syndica also operates a 0%-commission Solana staking validator running Jito-Solana for MEV optimization, publishes Solana protocol research, and develops **Sig**, an open-source Solana validator client written in Zig.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/syndica-io/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Solana, Blockchain, Web3, RPC, Streaming, Infrastructure, Validator, Staking

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Syndica Solana RPC (HTTP) API
High-performance Solana JSON-RPC HTTP endpoints served from a fault-tolerant elastic-node architecture across four global regions. Supports the full standard Solana RPC method surface (`getAccountInfo`, `getBalance`, `getTransaction`, `sendTransaction`, `getProgramAccounts`, `getSignaturesForAddress`, etc.) with credential-level rate limits, per-method routing rules, and detailed observability.

**Base URL:** `https://solana-mainnet.api.syndica.io/api-key/<API_KEY>`

**Human URL:** [https://docs.syndica.io/platform/solana-rpc/overview](https://docs.syndica.io/platform/solana-rpc/overview)

- [Documentation](https://docs.syndica.io/platform/solana-rpc/overview)
- [Quickstart — Make Your First RPC Call](https://docs.syndica.io/platform/getting-started/make-your-first-rpc-call)
- [Authentication — API Keys](https://docs.syndica.io/platform/concepts/api-keys)
- [Rate Limits — Credential Rate Limits](https://blog.syndica.io/credential-rate-limits-manage-and-secure-your-solana-rpc-endpoints-using-custom-rules/)
- [Sample Code — `Syndica/solana-rpc-demo`](https://github.com/Syndica/solana-rpc-demo)

### Syndica Solana RPC (WebSocket) API
Standard Solana RPC PubSub WebSocket service — `accountSubscribe`, `programSubscribe`, `signatureSubscribe`, `slotSubscribe`, `blockSubscribe`, `logsSubscribe`, `rootSubscribe`. A drop-in replacement for `wss://api.mainnet-beta.solana.com` with Syndica's edge routing, validator consolidation, and per-credential rate limits.

**Base URL:** `wss://solana-mainnet.api.syndica.io/api-key/<API_KEY>`

**Human URL:** [https://docs.syndica.io/platform/getting-started/subscribe-to-websocket-events](https://docs.syndica.io/platform/getting-started/subscribe-to-websocket-events)

- [Documentation](https://docs.syndica.io/platform/getting-started/subscribe-to-websocket-events)
- [API Reference — `blockSubscribe`](https://docs.syndica.io/platform/solana-rpc/websocket/blockSubscribe)
- [Authentication — API Keys](https://docs.syndica.io/platform/concepts/api-keys)

### Syndica ChainStream API
ChainStream is Syndica's real-time Solana data streaming API. It consolidates updates from multiple validators using a **"fastest wins"** strategy so the subscriber benefits from the lowest-latency notification across the validator set, and offers an optional `verified` parameter that delivers only transactions confirmed by multiple validators at `processed` commitment. Uses JSON-RPC 2.0 over WebSocket. Supports `transactionsSubscribe`, `slotsSubscribe`, and encoded `blocksSubscribe` against `solana-mainnet` (devnet coming). Production users have cut limit-order time-to-fill from 10s to 300ms with ChainStream.

**Base URL:** `wss://chainstream.api.syndica.io/api-key/<API_KEY>`

**Human URL:** [https://docs.syndica.io/platform/chainstream-api/](https://docs.syndica.io/platform/chainstream-api/)

- [Documentation](https://docs.syndica.io/platform/chainstream-api/)
- [API Reference — Slot Subscriptions](https://docs.syndica.io/platform/chainstream-api/slot-subscriptions)
- [Authentication — API Keys](https://docs.syndica.io/platform/concepts/api-keys)
- [Product Page — ChainStream](https://syndica.io/infrastructure/chainstream)
- [Blog — Solana Data Streaming](https://blog.syndica.io/solana-data-streaming-how-to-power-your-dapp-with-real-time-data/)

### Syndica Sig Validator RPC API
Sig is Syndica's open-source Solana validator client implemented in **Zig**, built for performance, modular RPC, and read-optimized operation. The project exposes a Solana-compatible RPC surface and is developed in the open under the Apache-2.0 license alongside companion libraries `rocksdb-zig`, `lsquic`, `boringssl-zig`, `zstd.zig`, and `base58-zig`.

**Human URL:** [https://github.com/Syndica/sig](https://github.com/Syndica/sig)

- [GitHub — `Syndica/sig`](https://github.com/Syndica/sig)
- [Sig Documentation — sig.fun](https://sig.fun/)
- [Product Page — Sig](https://syndica.io/open-source/sig)
- [Blog — Sig tag](https://blog.syndica.io/tag/sig/)
- [Blog — A Solana Validator Client Explained](https://blog.syndica.io/a-solana-validator-client-explained-everything-you-need-to-know/)

## Common Properties

- [Portal — syndica.io](https://syndica.io)
- [Portal — Enterprise](https://syndica.io/enterprise)
- [Documentation — docs.syndica.io](https://docs.syndica.io)
- [Documentation — Stake Docs](https://docs.syndica.io/platform/staking/overview)
- [FAQ](https://docs.syndica.io/platform/faq)
- [Support](https://docs.syndica.io/platform/support)
- [StatusPage — status.syndica.io](https://status.syndica.io)
- [Blog — blog.syndica.io](https://blog.syndica.io/)
- [Research Library](https://syndica.io/research?n=library)
- [About Us](https://syndica.io/company/about-us)
- [Contact Us](https://syndica.io/company/contact-us)
- [Careers](https://syndica.io/company/careers)
- [SignUp — Contact Sales](https://syndica.io/enterprise)
- [Pricing — Cost Estimator](https://syndica.io/enterprise/calculator)
- [Stake With Syndica](https://syndica.io/stake)
- [Open Source — Sig](https://syndica.io/open-source/sig)
- [Documentation — Sig Docs](https://sig.fun/)
- [GitHubOrganization — github.com/Syndica](https://github.com/Syndica)
- [GitHubRepository — Sig](https://github.com/Syndica/sig)
- [GitHubRepository — solana-rpc-demo](https://github.com/Syndica/solana-rpc-demo)
- [GitHubRepository — rocksdb-zig](https://github.com/Syndica/rocksdb-zig)
- [LinkedIn](https://www.linkedin.com/company/syndica-io)
- [X / Twitter — @Syndica_io](https://twitter.com/Syndica_io)
- [Support — support@syndica.io](mailto:support@syndica.io)

## Features

- Solana JSON-RPC over HTTP — fault-tolerant, load-balanced elastic-node architecture
- Solana JSON-RPC PubSub over WebSocket — full standard subscription set
- ChainStream real-time streaming API at `wss://chainstream.api.syndica.io`
- "Fastest wins" multi-validator consolidation for lower latency and no-miss delivery
- `verified` parameter for cross-validator confirmation at `processed` commitment
- Edge gateway routing across four global regions (Northern Virginia, Oregon, London, Singapore)
- Per-credential custom rate-limit rules (per-method, per-IP, per-credential)
- Detailed observability — RPC call logging, performance metrics, usage insights, analytics dashboard
- 99.99% uptime SLA on production endpoints; billions of RPC requests served monthly
- 10M free RPC requests per month entry tier; enterprise pricing via Cost Estimator
- Open-source Sig validator client written in Zig (Apache-2.0)
- Solana staking validator with 0% commission, Jito-Solana, MEV optimization
- Research arm publishing Solana protocol and consensus research

## Use Cases

- **High-frequency Solana trading** — On-chain trading bots, market makers, and liquidation engines; production users cut limit-order time-to-fill from 10s to 300ms.
- **DEX and DeFi backends** — Stream account, program, and signature updates for AMMs, perps, and lending protocols.
- **Wallet and explorer infrastructure** — High-volume `getAccountInfo`, `getTransaction`, and `getSignaturesForAddress` over the load-balanced HTTP RPC fleet.
- **Indexers and data warehouses** — Continuously ingest transactions, slots, and blocks via ChainStream into ClickHouse, BigQuery, or Postgres.
- **NFT mint and marketplace tooling** — Subscribe to program-derived account changes for real-time mint/list/sale detection.
- **Solana staking** — Delegate SOL to the Syndica validator (0% commission, Jito-Solana, MEV optimization).
- **Solana protocol R&D** — Build on or contribute to Sig and its companion Zig libraries.

## Integrations

- **Solana mainnet-beta** — drop-in for `api.mainnet-beta.solana.com`
- **`@solana/web3.js`** — `Connection` URL replacement
- **`solana-cli`** — `solana config set --url https://solana-mainnet.api.syndica.io/api-key/<KEY>`
- **Anchor framework** — Solana program development
- **Jito-Solana** — MEV-aware validator client
- **GitHub** — open-source Sig validator and companion Zig libraries

## Solutions

- **Solana RPC (Shared)** — multi-tenant HTTP/WebSocket with 10M free monthly requests
- **ChainStream** — premium real-time Solana streaming
- **Enterprise / Dedicated** — custom RPC capacity, dedicated nodes, SLA
- **Staking** — 0% commission Solana validator with Jito-Solana
- **Sig (Open Source)** — Apache-2.0 Zig validator client
- **Research** — public Solana protocol and consensus research

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
