# Legion Quantum — Contexto del repo

> Consultoría e investigación en computación cuántica. **Objetivo:** ser los mejores consultores cuánticos de la región.
>
> Parte de [Legion](../../CLAUDE.md) — holding de divisiones especializadas. **Núcleo de la empresa.**

---

## 1. Qué es esta división

Legion Quantum combina **consultoría** y **R&D** en computación cuántica. No somos una empresa académica — somos una consultora técnica especializada con capacidad de investigación aplicada.

**Visibilidad:** Public. Este repo es la vitrina pública más importante de Legion.

**Rol en Legion:** división **núcleo**. Si una sola división debe brillar, es esta.

## 2. Referencias obligatorias

- [`../../CLAUDE.md`](../../CLAUDE.md) — contexto maestro de Legion
- [`../../team/git-workflow.md`](../../team/git-workflow.md) — convenciones Git
- [`../../team/claude-usage.md`](../../team/claude-usage.md) — cómo usar Claude Code
- [`./strategy.md`](./strategy.md) — estrategia de la división
- [`./lineas-de-trabajo.md`](./lineas-de-trabajo.md) — líneas activas

## 3. Stack técnico (por competencia)

```
SDKs cuánticos:    Qiskit, PennyLane, Cirq, Braket SDK
Simulación:        Qiskit Aer, cuQuantum, PennyLane Lightning
Hardware acceso:   IBM Quantum, AWS Braket, Azure Quantum, IonQ, Quantinuum
Lenguajes:         Python 3.12 (principal)
ML / QML:          PennyLane + PyTorch / JAX, TensorFlow Quantum
Optimización:      QAOA, VQE, D-Wave Ocean (annealing), Gurobi (baseline clásico)
Post-quantum:      liboqs, OpenQuantumSafe, implementaciones NIST (Kyber, Dilithium)
Visualización:     Bloch sphere plots, circuitos, papers-grade figures (matplotlib, plotly)
```

## 4. Estructura del repo (propuesta)

```
quantum/
├── .claude/
├── primers/              ← material educativo público (QC 101, QML 101...)
├── research/             ← notebooks y papers de research aplicada
├── playbooks/            ← guías de consultoría (QAOA en producción, etc.)
├── benchmarks/           ← benchmarks reproducibles (clásico vs cuántico)
├── blog/                 ← thought leadership
├── case-studies/         ← casos públicos (con permiso)
├── README.md
└── .gitignore
```

## 5. Convenciones locales

**Repo público = vitrina.** Cuidamos la calidad por encima de la cantidad.

- **Notebooks:** ejecutables, con outputs guardados, reproducibles (seed fija, deps explícitas).
- **Papers / research:** referencias citadas correctamente (BibTeX). Preferir preprints en arXiv.
- **Benchmarks:** código + datos + metodología clara. Nunca claims vacíos ("10x speedup") sin reproducibilidad.
- **Primers y tutoriales:** nivel alto pero accesible. Audiencia objetivo: ingenieros senior que no saben QC.

## 6. Co-authorship de Claude

Repo **public** → co-author Claude **permitido y recomendado**.

## 7. Contactos y responsables

- **Lead:** por definir (idealmente físico/a con PhD en QC)
- **Equipo:** por formar

## 8. Estado actual

Repo recién creado. Scaffold en curso. Líneas de investigación y consultoría por definir con equipo.
