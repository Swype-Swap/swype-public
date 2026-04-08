# Public Status Model

SWYPE exposes a normalized public status model so developers, users, and support flows can inspect route progress without seeing confidential routing internals.

## Top-Level Statuses

- `quote_pending`
- `quoted`
- `awaiting_deposit`
- `deposit_detected`
- `confirming`
- `routing`
- `delivering`
- `completed`
- `expired`
- `failed`
- `refunded`
- `recovery_in_progress`

## Why This Exists

Different providers and networks may use different transaction-state language.

SWYPE normalizes those external signals into a stable public lifecycle model so:

- users get clearer status updates
- developers can integrate against a stable contract
- support flows can reason about route progression consistently

## Protected Routes

For protected private routes, SWYPE may expose a tracker or stage model without publishing the full internal route decomposition.
