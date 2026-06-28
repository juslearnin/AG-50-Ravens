# Smart-Trace (AG-50 Ravens)

Smart-Trace is an enterprise-grade, high-performance asset serialization and cryptographic tracking system designed for absolute supply chain transparency and regulatory compliance. Built on the MERN stack (MongoDB, Express.js, React, Node.js), the platform specializes in the rapid generation, hierarchical aggregation, and cryptographic verification of GS1-compliant identification structures.

---

## 🔥 Key System Capabilities

* **High-Throughput Tracking Engines:** Generates, signs, and hashes over 10,000+ structurally unique, GS1-compliant identifiers (SSCCs) in under 5 seconds with an active, scan-and-verify operations dashboard.
* **Dual-State Failover Architecture:** Features an automated local memory fallback wrapper (`memoryStore`). If a remote database connection drops, the application seamlessly redirects runtime operations into its local simulation state to prevent runtime crashes.
* **Immutable Parent-Child Aggregation:** Enforces topological validation rules across product packing lines (Primary Units ➔ Secondary Cases ➔ Tertiary Pallets), enabling full upstream lineage lookups.
* **Decommissioning State Guards:** Strict state-machine routing instantly flags and drops validation checks on any decommissioned or blacklisted identifier strings across the supply chain network.

---

## 🏗️ Repository Architecture & Directories

```text
AG-50_Ravens/
├── backend/               # Express.js Server & Core Verification Logic
│   ├── controllers/       # Batch generation, hierarchy mapping, and admin stats engines
│   ├── models/            # Document structures for Serial schemas and Aggregation logs
│   ├── utils/             # Luhn validation, memory fallback matrices, SSCC generators
│   └── app.js             # API route mounts, server middleware, and lifecycle setups
├── frontend/              # Create React App Dashboard Portal
│   ├── src/
│   │   ├── components/    # Serial scanners, generation sheets, and data streams
│   │   └── api/           # Centralized Axios interceptors and endpoints
└── .gitignore             # Root security barrier (keeps hidden variables local)
