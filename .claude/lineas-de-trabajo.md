# Líneas de trabajo — Legion Quantum

> Áreas concretas con **referencias contrastables** (papers, frameworks, libros, actores) como punto de partida del equipo.
>
> Ver definición de estados en `../../templates/lineas-de-trabajo.md.template`.

---

## Líneas activas

(Ninguna todavía — división arranca en 2026-04.)

---

## Líneas en exploración / diseño

### Quantum Machine Learning (QML)

- **Estado:** `exploring`
- **Objetivo:** consultoría + research en QML aplicado: clasificadores variacionales, quantum kernels, redes neuronales híbridas cuánticas-clásicas.
- **Motivación:** área de mayor tracción actual con clientes que ya entienden ML clásico. Buen on-ramp comercial.
- **Siguiente paso:** primer notebook público con benchmark QML vs ML clásico en dataset conocido (UCI / MNIST reducido).

**Referencias:**

*Papers seminales / reviews:*
- Schuld & Killoran, *Quantum Machine Learning in Feature Hilbert Spaces* — [arXiv:1803.07128](https://arxiv.org/abs/1803.07128). Fundacional para quantum kernels.
- Havlíček et al., *Supervised learning with quantum-enhanced feature spaces*, **Nature 567, 209 (2019)** — [link](https://www.nature.com/articles/s41586-019-0980-2). QSVM experimental en hardware IBM.
- Cerezo et al., *Variational Quantum Algorithms*, **Nature Reviews Physics 3, 625 (2021)** — [link](https://www.nature.com/articles/s42254-021-00348-9). Review de referencia sobre VQAs; incluye QML.
- Biamonte et al., *Quantum machine learning*, **Nature 549, 195 (2017)** — arXiv:1611.09347. Review original QML.

*Frameworks:*
- **PennyLane** (Apache 2.0) — [pennylane.ai](https://pennylane.ai). Diferenciable, integración PyTorch/JAX/TF. **Primera elección** para QML en Legion.
- **Qiskit Machine Learning** (Apache 2.0) — [qiskit-community.github.io/qiskit-machine-learning](https://qiskit-community.github.io/qiskit-machine-learning).
- **TensorFlow Quantum** — [tensorflow.org/quantum](https://www.tensorflow.org/quantum).
- **torchquantum** (MIT) — [github.com/mit-han-lab/torchquantum](https://github.com/mit-han-lab/torchquantum).

*Debate "quantum advantage" en ML (lectura crítica):*
- Schuld, *Is quantum advantage the right goal for quantum machine learning?* (arXiv:2203.01340, 2022) — ensayo honesto.

*Por dónde empezar:*
- [PennyLane QML codebook](https://pennylane.ai/codebook/) — gratuito, interactivo, cubre VQE, QAOA, QML, quantum chemistry.
- [Qiskit Textbook: Machine Learning](https://learn.qiskit.org/course/machine-learning/).

---

### Optimización cuántica

- **Estado:** `exploring`
- **Objetivo:** consultoría aplicada en QAOA, VQE, quantum annealing para problemas de optimización industrial (logística, finanzas, grids, scheduling).
- **Motivación:** verticales claras; enunciados QUBO bien definidos en industria.
- **Siguiente paso:** caso reproducible público (ej. portfolio optimization con QAOA, TSP pequeño con annealing) como carta de presentación.

**Referencias:**

*Papers seminales:*
- Farhi, Goldstone, Gutmann, *A Quantum Approximate Optimization Algorithm* — [arXiv:1411.4028](https://arxiv.org/abs/1411.4028). QAOA original.
- Peruzzo et al., *A variational eigenvalue solver on a photonic quantum processor*, **Nat. Commun. 5, 4213 (2014)** — [link](https://www.nature.com/articles/ncomms5213). VQE original.
- Lucas, *Ising formulations of many NP problems* (arXiv:1302.5843, 2014) — bible de QUBO para problemas clásicos.
- Harrigan et al., *Quantum approximate optimization of non-planar graph problems on a planar superconducting processor*, Nat. Phys. 17, 332 (2021) — QAOA en hardware real.

*Frameworks:*
- **D-Wave Ocean SDK** (Apache 2.0) — [docs.ocean.dwavesys.com](https://docs.ocean.dwavesys.com). Annealing.
- **PennyLane / Qiskit QAOA** — implementaciones didácticas y de producción.
- **OpenJij** — solver QUBO abierto alternativo a D-Wave.

*Empresas referencia:*
- **D-Wave Systems** (annealing).
- **QC Ware** — servicios de optimización para finanzas.
- **Multiverse Computing** — finanzas y optimización industrial.
- **Pasqal** (neutral atoms, optimización).

*Benchmarks honestos (lectura obligatoria para no sobrevender):*
- Blekos et al., *A review on Quantum Approximate Optimization Algorithm and its variants* (Physics Reports, 2024) — state-of-play actualizado.

*Por dónde empezar:*
- [PennyLane QAOA tutorial](https://pennylane.ai/qml/demos/tutorial_qaoa_intro/).
- [D-Wave Getting Started](https://docs.dwavesys.com/docs/latest/doc_getting_started.html).

---

### Post-Quantum Cryptography (PQC)

- **Estado:** `designing`
- **Objetivo:** consultoría de migración cripto clásica → algoritmos post-cuánticos (NIST-approved).
- **Motivación:** **deadline regulatorio real** — NSA CNSA 2.0 exige migración antes de 2030 para sistemas nacionales; tendencia global paralela (EU, UK). Alta demanda esperada 2025-2028.
- **Siguiente paso:** playbook de migración con decisiones arquitectónicas típicas (hybrid cripto, crypto agility, inventario de dependencias).

**Referencias:**

*Estándares (primero a leer):*
- [NIST FIPS 203 — ML-KEM (Kyber)](https://csrc.nist.gov/pubs/fips/203/final) — encapsulamiento de claves post-cuántico. **Standard final.**
- [NIST FIPS 204 — ML-DSA (Dilithium)](https://csrc.nist.gov/pubs/fips/204/final) — firma digital.
- [NIST FIPS 205 — SLH-DSA (SPHINCS+)](https://csrc.nist.gov/pubs/fips/205/final) — firma hash-based.
- [NIST PQC Standardization program](https://csrc.nist.gov/projects/post-quantum-cryptography/post-quantum-cryptography-standardization) — estado histórico + rounds 4, HQC.
- [NSA CNSA 2.0 Algorithms PDF](https://media.defense.gov/2025/May/30/2003728741/-1/-1/0/CSA_CNSA_2.0_ALGORITHMS.PDF) — cronograma obligatorio US gov.

*Librerías / implementaciones:*
- **liboqs** (MIT) — [openquantumsafe.org/liboqs](https://openquantumsafe.org/liboqs); [github.com/open-quantum-safe/liboqs](https://github.com/open-quantum-safe/liboqs). Implementaciones C de los algoritmos NIST.
- **oqs-provider (OpenSSL 3)** — integra liboqs como provider OpenSSL — punto de entrada para migración real de TLS.
- **PQCrypto libraries** (referencia NIST) — implementaciones de referencia de los autores.

*Papers referencia:*
- Ducas et al., *CRYSTALS-Kyber* (original submission) — pqcrystals.org.
- Lyubashevsky et al., *CRYSTALS-Dilithium* — pqcrystals.org.
- Bernstein & Lange, *Post-quantum cryptography: an introduction* — cr.yp.to/papers.html.

*Guías gubernamentales:*
- CISA "Post-Quantum Cryptography Initiative" — cisa.gov/post-quantum-cryptography-initiative.
- UK NCSC guidance on PQC migration.

*Empresas / actores:*
- Cloudflare (blog técnico con implementaciones early en TLS).
- Google (Chrome con Kyber híbrido desde 2023).
- PQShield, evolutionQ, Quantinuum.

*Por dónde empezar:*
- [liboqs tutorial](https://github.com/open-quantum-safe/liboqs/wiki) — install, run kems/signatures, integrar en OpenSSL.
- Leer FIPS 203 (cap 1-3) para vocabulario común.

---

### Simulación cuántica aplicada

- **Estado:** `exploring`
- **Objetivo:** research aplicada en química computacional cuántica y simulación de materiales. VQE para moléculas, algoritmos de simulación de Hamiltonianos.
- **Motivación:** industrias farma, materiales, química energética tienen interés creciente. Ticket de consultoría alto (research + aplicación).
- **Siguiente paso:** decidir si es vertical que perseguimos en 2026 o exploración pasiva. Identificar partner académico/universidad si sí.

**Referencias:**

*Papers / reviews:*
- McArdle, Endo, Aspuru-Guzik, Benjamin, Yuan, *Quantum computational chemistry*, **Rev. Mod. Phys. 92, 015003 (2020)** — [link](https://link.aps.org/doi/10.1103/RevModPhys.92.015003). **Review canónico**.
- Cao et al., *Quantum chemistry in the age of quantum computing*, **Chem. Rev. 119, 19 (2019)** — otra review foundational.
- Google experiments: Arute et al., *Hartree-Fock on a superconducting qubit quantum computer* (Science 369, 2020).

*Frameworks:*
- **OpenFermion** (Apache 2.0) — [github.com/quantumlib/OpenFermion](https://github.com/quantumlib/OpenFermion). Translator de química a operadores cuánticos.
- **PennyLane Quantum Chemistry** — [docs.pennylane.ai/en/stable/introduction/chemistry.html](https://docs.pennylane.ai/en/stable/introduction/chemistry.html). VQE y otros algoritmos de química.
- **Qiskit Nature** (Apache 2.0) — química y materiales.
- **PySCF** — driver clásico para generar Hamiltonianos que se pasan a los SDKs cuánticos.

*Actores / iniciativas:*
- **Google Quantum AI** — líder en experimentos química.
- **IBM Quantum** — herramientas de química.
- **Quantinuum (ex-Honeywell + Cambridge Quantum)** — servicios en química.
- **Zapata Computing** (ahora parte de otros) — research aplicada.
- **Classiq** — herramientas de síntesis de circuitos.

*Por dónde empezar:*
- [PennyLane quantum chemistry demos](https://pennylane.ai/qml/demos_quantum_chemistry/).
- McArdle et al. review (cap 1-3).

---

### Formación corporativa

- **Estado:** `designing`
- **Objetivo:** programas de 1-2 semanas para equipos técnicos corporativos. Audiencias: CTOs, ingenieros ML, CISOs.
- **Motivación:** on-ramp de bajo compromiso para prospects; genera ingresos mientras consultoría seria arranca.
- **Siguiente paso:** sillabus + primeros materiales abiertos en `primers/`. Definir 3 programas: "QC para líderes técnicos", "QML para ingenieros ML", "PQC para CISOs".

**Referencias:**

*Libros canónicos:*
- Nielsen & Chuang, *Quantum Computation and Quantum Information* (Cambridge, 10th anniversary ed. 2010). **Biblia del área.**
- Schuld & Petruccione, *Machine Learning with Quantum Computers* (Springer, 2021). QML systematic.
- Wittek, *Quantum Machine Learning: What Quantum Computing Means to Data Mining* (Academic Press, 2014). Histórico pero útil para contexto.
- Hidary, *Quantum Computing: An Applied Approach* (Springer, 2021). Orientado a ingenieros.
- Bernhardt, *Quantum Computing for Everyone* (MIT Press, 2019). Para perfiles no-técnicos.

*Cursos / materiales gratis:*
- [IBM Qiskit Textbook](https://learn.qiskit.org/) — gratis, interactivo, múltiples cursos (core, ML, chemistry).
- [PennyLane Codebook](https://pennylane.ai/codebook/) — gratis, interactivo.
- [IBM Quantum Challenges](https://quantum-computing.ibm.com/challenges) — retos prácticos anuales.
- MIT OCW "Quantum Computation" (Aram Harrow).

*Certificaciones / sandboxes:*
- **IBM Quantum** (acceso gratuito a hardware pequeño).
- **AWS Braket** — acceso pay-per-shot a IonQ, Rigetti, Oxford Quantum Circuits, IQM.
- **Azure Quantum** — IonQ, Quantinuum, Rigetti.

*Por dónde empezar:*
- Nielsen & Chuang cap 1-4 para vocabulario mínimo.
- Qiskit Textbook core para práctica hands-on.

---

### Research publicable

- **Estado:** `exploring`
- **Objetivo:** producir mínimo 1 paper / preprint anual de calidad. Participar en conferencias relevantes.
- **Motivación:** credibilidad no se compra; se construye con publicación.
- **Siguiente paso:** identificar tema inicial que combine research original + aplicación práctica (evitar teórico puro).

**Referencias:**

*Venues / conferencias:*
- **QIP** (Quantum Information Processing) — anual, venue #1 teórica.
- **TQC** (Theory of Quantum Computation) — anual.
- **Q2B** (Quantum 2 Business) — anual, bridge industria-academia.
- **IEEE QCE** (Quantum Week) — IEEE conference.
- **NeurIPS / ICML** — tracks de quantum ML.

*Revistas:*
- **Nature Quantum Information** (npj Quantum Information) — [nature.com/npjqi](https://www.nature.com/npjqi). Open-access, alta visibilidad.
- **Quantum** (quantum-journal.org) — [quantum-journal.org](https://quantum-journal.org). Open-access, revisión rigurosa, gratuita para autores.
- **Physical Review X Quantum** (PRX Quantum).
- **IEEE Transactions on Quantum Engineering**.

*Preprint server:*
- **arXiv quant-ph** — [arxiv.org/list/quant-ph/recent](https://arxiv.org/list/quant-ph/recent). Obligatorio monitorear.
- Categoría secundaria útil: cs.ET (emerging technologies).

*Por dónde empezar:*
- Seguir arXiv quant-ph diario (feed RSS).
- Asistir (virtualmente si es caro) a QIP 2026 / TQC 2026.

---

## Líneas archivadas

(Vacío.)

---

**Última actualización:** 2026-04-22
