# Legion Quantum

> **Quantum computing consulting and applied research.**
>
> Part of [Legion](https://legioncloud.dev) — *Forging the Intelligence Infrastructure*.

---

## Mission

Turn quantum computing from academic curiosity into engineering advantage. We help companies explore, design, and deploy quantum applications with the rigor of production engineering.

## What we do

- **Discovery Workshops** — assess where quantum computing actually helps your business.
- **Proof of Concept** — honest quantum vs classical benchmarks, reproducible.
- **Production Integration** — hybrid quantum-classical systems, deployed.
- **Post-Quantum Cryptography** — migration to NIST-approved algorithms (Kyber, Dilithium).
- **Corporate Training** — structured programs for CTOs and engineering teams.
- **Applied Research** — co-funded research with IP sharing.

Detailed methodology in [`.claude/strategy.md`](./.claude/strategy.md).

## Principles

1. **No hype.** If a problem doesn't benefit from quantum, we say so.
2. **Reproducible benchmarks.** Every performance claim comes with code and data.
3. **Engineering discipline.** Notebooks run, deps are explicit, seeds are fixed.
4. **Honest about hardware today.** NISQ is real; we design within its limits.

## Stack we work with

- **SDKs:** Qiskit, PennyLane, Cirq, Braket SDK
- **Hardware:** IBM Quantum, AWS Braket, Azure Quantum, IonQ, Quantinuum
- **Simulation:** Qiskit Aer, cuQuantum, PennyLane Lightning
- **QML:** PennyLane + PyTorch / JAX
- **Post-quantum:** liboqs, Open Quantum Safe, NIST reference implementations

## Status

`concept` — division bootstrapped 2026-04-22. First primers and benchmarks coming.

## Structure

```
quantum/
├── .claude/          — internal docs: strategy, working lines, conventions
├── primers/          — public educational material (coming)
├── research/         — applied research notebooks and preprints (coming)
├── playbooks/        — consulting guides (coming)
├── benchmarks/       — reproducible benchmarks (coming)
└── blog/             — technical thought leadership (coming)
```

## Getting started with quantum (external resources)

While our own primers are being written:

- [Qiskit Textbook](https://learn.qiskit.org/)
- [PennyLane tutorials](https://pennylane.ai/qml/)
- [NIST Post-Quantum Cryptography](https://csrc.nist.gov/projects/post-quantum-cryptography)

## Contact

- Website: https://legioncloud.dev
- Inquiries: open an issue or reach out via the website.
