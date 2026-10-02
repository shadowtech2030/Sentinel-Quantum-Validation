# Sentinel Quantum — Security & Authority Boundaries

## Purpose

Sentinel Quantum is the **cryptographic trust engine** of the Sentinel ecosystem.

It decides whether an identity, key, certificate, attestation, cryptographic operation or cryptographic trust relationship is acceptable under the currently valid policy.

## Quantum may

Sentinel Quantum may:

- validate identities and attestations;
- authorize or deny cryptographic operations;
- reject invalid or untrusted credentials;
- detect and block replayed or downgraded cryptographic exchanges;
- rotate or revoke cryptographic material when policy permits;
- apply fail-closed cryptographic guardrails;
- preserve and verify evidence integrity;
- continue in safe-local mode using the last valid policy when Central is temporarily unavailable.

## Quantum may not

Sentinel Quantum does **not** independently:

- stop or start a PLC;
- close or open a valve;
- change industrial process logic;
- modify a machine recipe;
- change a production setpoint;
- make business or process-control decisions;
- replace the human operator for significant OT remediation.

## Human-in-the-loop

Important operational remediation remains under human authority through the Sentinel HUB.

Quantum can protect the **trust boundary**. It does not take ownership of the **industrial process boundary**.

## Fail-closed principle

When cryptographic trust cannot be established, Quantum may deny the sensitive cryptographic operation rather than silently downgrade trust.

This fail-closed behavior is intentionally limited to the security and cryptographic boundary. It must not be represented as autonomous OT process control.
