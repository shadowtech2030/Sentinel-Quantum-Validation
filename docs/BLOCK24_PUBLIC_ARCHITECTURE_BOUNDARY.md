# Sentinel Quantum — Block 24 Public Architecture Boundary

```mermaid
flowchart TB
    Human["Human operator"]
    Central["Sentinel Central<br/>HUB supervision & decision support"]
    Quantum["Sentinel Quantum<br/>Cryptographic trust engine"]
    Edge["Sentinel Edge / local Sentinel engines"]
    OT["OT / IT environment"]
    HSM["Optional hardware custody"]
    QKD["Optional QKD input"]

    Human <--> Central
    Central <-->|"Defined trust/security contracts"| Quantum
    Central <--> Edge
    Edge --- OT
    HSM -. "key custody / opaque handles" .-> Quantum
    QKD -. "optional key-material input" .-> Quantum
    Quantum -. "trust state / guardrails / evidence" .-> Central
```

## Public boundary

- Central provides supervision and decision support.
- Quantum provides cryptographic trust.
- Edge / local engines retain field context.
- Human operators retain authority over meaningful OT actions.

Quantum may deny a cryptographic operation when trust cannot be established.

Quantum does not directly control industrial processes.

SAFE_LOCAL preserves cryptographic guardrails when Central is unavailable.
