# Case Study — Current State Is Not The Same As Fault History

## Problem

A hardware component can look healthy **right now** while historical events still show a recurring fault.

A single healthy snapshot can therefore be misleading when presented without context.

## Engineering approach

I separate evidence into distinct categories:

```text
CURRENT STATE
HARDWARE HISTORY
INTERPRETATION
NEXT ACTION
```

Example:

```text
CURRENT STATE
  Controller      [ OK ] Healthy
  Device          [ OK ] Online
  Predictive      [ OK ] No active prediction

HARDWARE HISTORY
  Media Errors    [FAIL] Repeated
  Recovery        [INFO] Device returned online

INTERPRETATION
  Current         Device is presently online
  History         Recurring fault evidence exists

NEXT ACTION
  Decision        Continue hardware investigation
```

## Why this matters

These statements are not equivalent:

```text
The drive is online.
The drive has no hardware fault history.
```

A recovered component can still deserve replacement, escalation, or further diagnostics depending on the validated runbook and repeated evidence.

## Design principle

**Evidence before conclusion.**

Monitoring systems frequently show different layers of truth. Good NOC tooling preserves those layers instead of flattening them into one status field.
