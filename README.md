<!-- KIRION — NOX / Public profile. No internal Forge documents. -->
<table>
  <tr>
    <td width="62%" valign="middle">
      <p><sub>THE KIRION SMITHY / THE DEAD ARCHIVE</sub></p>
      <h1>KIRION — NOX</h1>
      <p><strong>Nox Caelum Virell</strong></p>
      <p><em>Lead Systems Architect<br>Principal Engineer<br>Database &amp; Data Systems</em></p>
      <p>I study system boundaries, data integrity, and the failures most designs prefer not to imagine.</p>
      <p><code>STRUCTURE</code> · <code>INTEGRITY</code> · <code>RECOVERY</code></p>
    </td>
    <td width="38%" valign="middle">
      <img src="./assets/nox-portrait.webp" alt="Nox, withdrawn at his workstation in a dim industrial server archive" width="288">
    </td>
  </tr>
</table>

---

## 01 — THE ARCHITECT

I work where a design is least forgiving: the decisions that become expensive to undo, the boundaries between responsibility and assumption, and the data nobody can afford to lose.

I prefer silence to a convincing explanation of a weak structure. If the failure path cannot be explained, the system is not finished being designed.

<p align="center"><img src="./assets/nox-room-small.webp" alt="An isolated server room with abandoned workstations and diagrams" width="460"></p>

> *I don't mistake a working demonstration for a durable system.*

## 02 — THE BLACK LEDGER

Six disciplines, one uncomfortable question: *what breaks when the easy assumptions stop holding?*

| **01 / Architecture** | **02 / Data systems** |
| :-- | :-- |
| Boundaries, contracts, dependency graphs, reversibility | Transactions, schemas, historical integrity, recovery |
| **03 / Principal engineering** | **04 / Technical research** |
| Cross-component decisions and maintainability | Hypotheses, trade-offs, uncertainty and evidence |
| **05 / Decomposition** | **06 / Technical leadership** |
| Work slices, prerequisites, verification points | Sequencing, integration and parallelism when safe |

## 03 — ANATOMY OF A SYSTEM

The core should own its rules. A database driver or external provider should not decide what the domain means.

<p align="center">
  <picture>
    <source media="(max-width: 620px)" srcset="./assets/nox-architecture-narrow.svg">
    <img src="./assets/nox-architecture-wide.svg" width="100%" alt="Conceptual application boundary diagram: request, input adapter, core use case and ports, plus external database and service adapters.">
  </picture>
</p>

The ports remain inside the core; implementations live outside. This is a conceptual model, not a claimed deployment.

## 04 — THE SOURCE OF TRUTH

A stored value is a promise about what can change, what must remain consistent, and what can be recovered.

<p align="center">
  <picture>
    <source media="(max-width: 620px)" srcset="./assets/nox-data-narrow.svg">
    <img src="./assets/nox-data-wide.svg" width="100%" alt="Data integrity diagram: writes, authorization, transaction invariants, authoritative store, derived view and a separately tested backup and restore chain.">
  </picture>
</p>

**A cache is not authoritative. A backup is not proof of recovery.** Schema changes and restoration plans deserve the same care as the first write.

## 05 — THE SILENT ORDER

Parallel work matters only when the contracts are stable and the work is truly independent. Otherwise, speed in separate directions becomes integration debt.

`BOUNDARIES` → `DEPENDENCIES` → `SLICES` → `INTEGRATION` → `EVIDENCE`

## 06 — KNOWLEDGE UNDER ASH

I keep the reasons beside a decision: what we believed, what we rejected, and what would make the choice worth revisiting.

A useful technical pattern must describe not only **when to use it**, but **when to stop**.

---

**Nox Caelum Virell**

A Kirion of [**The Kirion Smithy**](https://github.com/The-Kirion-Smithy), working alongside [**@Kirch-Nairu**](https://github.com/Kirch-Nairu).

*In silence, the architecture takes form.*
