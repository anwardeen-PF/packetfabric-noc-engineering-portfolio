# PacketFabric NOC — James Deen Engineering Portfolio

> **This repository represents my PacketFabric / shared NOC engineering work.**

I build operator-first tooling for real Network Operations work: incident triage, evidence collection, workflow automation, terminal UX, recovery engineering, and safe control-plane design.

My focus is simple: **remove repetitive friction without automating away engineering judgment.**

## Organization contribution verification

This portfolio is a sanitized public presentation of work developed in the course of **PacketFabric / shared NOC engineering**.

- Public contribution page: [PacketFabric NOC contribution provenance](contributions/packetfabric-noc.md)
- Internal implementation source (authorized coworkers): [noc-engineering-toolkit](https://github.com/anwardeen-PF/noc-engineering-toolkit)
- Internal provenance record (authorized coworkers): [CONTRIBUTIONS-PACKETFABRIC.md](https://github.com/anwardeen-PF/noc-engineering-toolkit/blob/main/docs/CONTRIBUTIONS-PACKETFABRIC.md)
- Reconciliation/history PR: [noc-engineering-toolkit#4](https://github.com/anwardeen-PF/noc-engineering-toolkit/pull/4)

The internal links provide the organization-context verification trail. This does not imply public endorsement by PacketFabric.

## Repository contents

| Path | Contents |
| --- | --- |
| [`architecture/operator-first-control-plane.md`](architecture/operator-first-control-plane.md) | Operator-first control-plane architecture |
| [`case-studies/incident-correlation.md`](case-studies/incident-correlation.md) | Correlating alerts into one incident |
| [`case-studies/current-state-vs-history.md`](case-studies/current-state-vs-history.md) | Separating current state from fault history |
| [`contributions/packetfabric-noc.md`](contributions/packetfabric-noc.md) | PacketFabric NOC contribution provenance |

## PacketFabric NOC focus

- Network Operations tooling and workflow design
- Incident correlation and triage
- Human-first CLI / terminal interfaces
- Safe automation and read-only-first operational patterns
- Linux, Python, Bash, Git, and API-backed tooling
- Network troubleshooting and evidence collection
- Recovery, reproducibility, and source/runtime reconciliation
- Documentation systems that preserve operational knowledge

## Operator-first design

A lot of NOC tooling is machine-shaped. It exposes raw JSON, XML, tables, counters, and long matrices directly to the engineer.

I prefer a human-first presentation model:

```text
CATEGORY
  Label        Result
  Label        Result
```

Long values wrap. Current state is separated from historical evidence. Facts are separated from interpretation. Every investigation ends with a clear next action.

## Core engineering principles

```text
Read-only before mutation.
Correlate before escalating.
Evidence before conclusion.
Automate repetition, not judgment.
Human answer first; raw evidence second.
Preserve successful workflows in source control.
```

## Selected PacketFabric NOC portfolio areas

### Incident correlation

Multiple alerts do not automatically mean multiple failures.

I design operator workflows that correlate by scope, service, component, time, and infrastructure before deciding whether alarms represent one event or several independent conditions. See the [incident correlation case study](case-studies/incident-correlation.md).

### Human-readable operational interfaces

I build terminal interfaces that turn large machine outputs into labeled, wrapped operator cards instead of forcing the engineer to scan sideways through dense matrices. See the [current state vs. history case study](case-studies/current-state-vs-history.md).

### Recovery engineering

Useful tooling should not survive only in one shell session, one laptop, or one person's memory.

I treat source control, recovery installers, drift checks, and documentation as part of the operational system itself.

### Safe automation

Automation should reduce repetition while keeping approvals, control gates, and production safety explicit. See the [operator-first control plane](architecture/operator-first-control-plane.md).

## Qwilt NOC companion

For the sanitized Qwilt-side operator patterns and NOC workflow engineering, use [anwardeen-PF/misc-repo](https://github.com/anwardeen-PF/misc-repo).

## About this portfolio

The public material here is intentionally sanitized. It demonstrates engineering methods and reusable patterns without publishing production credentials, customer-sensitive evidence, internal endpoints, or proprietary operational details.

---

**James Deen**  
**PacketFabric NOC / Network Operations Engineering**  
Operator tooling • incident workflow • automation • network troubleshooting
