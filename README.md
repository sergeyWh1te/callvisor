# callvisor

**Callvisor** is an application-level proxy for Ethereum JSON-RPC, designed to bring observability, introspection, and traffic control to Web3 infrastructure — just like **Envoy** or **Linkerd**, but for smart contract interactions.

Built in Go and designed for performance, it transparently proxies `eth_call`, `eth_subscribe`, and `eth_sendRawTransaction` over WebSocket or HTTP, while decoding calldata using ABI definitions and enriching every interaction with semantic context.

---

## 🌐 Why Callvisor?

Web3 lacks foundational tools like service meshes, API gateways, and observability layers that are common in modern cloud-native infrastructure.

**Callvisor aims to close that gap**, providing:

- Transparent proxying of Ethereum RPC traffic
- Deep awareness of contract method calls and event logs
- Real-time decoding of function arguments and log topics
- Support for upstream node pools (e.g. Infura, Erigon, Besu, Geth)
- Metrics, tracing, and structured logging for smart contract activity

---

## 🧩 Core Features

- 🔌 **Transparent WebSocket proxy** (full-duplex)
- 🔍 **ABI-aware decoding** of all JSON-RPC interactions
- 📊 **Semantic observability layer** over smart contract calls and logs
- 🧠 **Function signature resolution** (via ABI or selector registries)
- 📈 **Metrics export** (Prometheus ready, coming soon)
- ⛔ **Traffic filtering** and routing based on method, contract, chain
- 🔐 Ready for integration in multi-tenant or L2 infrastructure

---

## 🚀 Quickstart

```bash
go run ./cmd/server
