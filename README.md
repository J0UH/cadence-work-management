[← All systems](https://github.com/J0UH) · [Money and operations systems](https://github.com/J0UH/money-operations-systems)

<p align="center">
  <img src="assets/hero.webp" alt="Committed blocks are locked behind an ochre boundary apart from loose future blocks" width="100%" />
</p>

# Cadence work management

Cadence treats work as a sequence of commitments rather than an endless stream of cards. It is designed for small teams that need a calm shared view of what exists, what moved, and what needs attention.

## The engineering problem

Most project tools optimise for adding work. The harder problem is preserving ownership and history while helping a team decide what deserves focus now.



## What the system covers

- Task and sprint ledgers
- Realtime team state
- Invitations and controlled access
- Change history and ownership
- Optional CRM synchronisation

## System shape

```mermaid
flowchart TD
accTitle: Cadence work management
accDescr: Work crosses an explicit commitment boundary before entering a sprint. Changes return through the ledger instead of silently rewriting the plan, leaving a durable record of what was promised.
    intent["Team intent"] --> backlog["Work ledger"]
    backlog --> commit{"Commit now?"}
    commit -->|Yes| sprint["Committed sequence"]
    commit -->|No| uncommitted["Uncommitted work"]
    sprint --> realtime["Realtime state"]
    realtime --> changed{"Commitment changed?"}
    changed -->|Yes| backlog
    changed -->|No| history["Durable history"]
```

## Build notes

- Prefer a small set of meaningful states.
- Keep the history of a commitment after its board position changes.
- Use quiet defaults so the tool supports focus instead of competing for it.

<sub>Personal work. Public overview only. Source code, credentials, and private operating details are not included.</sub>

## Talk through a similar problem

Working on something similar? [Tell me about it](mailto:ju@jomena.group?subject=Cadence%20work%20management).
