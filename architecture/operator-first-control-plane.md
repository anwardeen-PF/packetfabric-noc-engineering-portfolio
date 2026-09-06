# Operator-First Control Plane

## Goal

Provide one human-facing operational surface while keeping production execution, credentials, and platform-specific engines behind explicit boundaries.

```text
OPERATOR
   |
   v
LOCAL CONTROL PLANE
   |
   +--> read-only incident adapters
   +--> evidence normalization
   +--> human-first renderer
   +--> workflow / recovery state
   |
   v
EXPLICIT REMOTE ACTION
   |
   v
PLATFORM-SPECIFIC RUNTIME
```

## Design properties

### Local startup is safe

Starting the operator console should not automatically:

- open a production session;
- change a device;
- acknowledge an incident;
- modify a ticket;
- restart a service.

### Remote actions are explicit

The operator should know:

- target;
- action;
- read/write classification;
- whether approval is required;
- expected effect.

### Machine output stays behind the renderer

Raw data remains available, but the default surface is optimized for decision-making:

```text
CATEGORY
  Label        Result
```

### Recovery is part of the architecture

The console, helper files, installer, and drift checks are source-controlled so the operating environment can be rebuilt consistently.

## Principle

The control plane should reduce cognitive load without reducing operator control.
