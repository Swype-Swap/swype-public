# Reliability And Recovery

SWYPE is designed to keep routes observable and recoverable through normalized tracking, expiry handling, and reconciliation.

## Public Recovery Model

After a route is created, SWYPE keeps a transaction record and a stable SWYPE tracking identifier.

SWYPE may continue to:

- synchronize external transaction state
- normalize provider or network statuses
- expire stale waiting flows
- update the public status view
- move a route into recovery, failure, refund, or completion states as more information becomes available

## Public Failure Scenarios

- Provider fails before deposit
  SWYPE returns an error or a fresh route path instead of leaving a live payment instruction active.

- Provider fails after deposit but before completion
  SWYPE keeps the route observable and continues reconciliation or recovery tracking.

- Funds appear delayed or stuck
  SWYPE continues synchronization against provider and network state and keeps the route visible through the public status model.

- Cross-chain delivery fails after an upstream stage succeeds
  SWYPE records the intermediate state and continues recovery or reconciliation instead of dropping the route silently.

- Expiry reached before valid completion
  The route transitions into an expired state.

## Guarantees And Limits

SWYPE publicly guarantees:

- a stable SWYPE tracking identifier
- normalized status tracking
- expiry handling
- non-custodial design

SWYPE does not publicly guarantee:

- that every route always succeeds
- that every provider supports refunds automatically
- that provider and network issues resolve instantly
- that protected private routes guarantee anonymity
