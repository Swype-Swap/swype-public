# Architecture Overview

SWYPE is best understood as a layered non-custodial payments and routing platform.

## Public System Layers

1. Product and presentation layer
   - website
   - swap surface
   - Swype Me request flows
   - creator tipping
   - Telegram Mini App
   - embeds and widgets
   - partner-facing docs and portal

2. Application layer
   - request validation
   - access control
   - session handling
   - tracking responses
   - user-facing status delivery

3. Routing and orchestration layer
   - public route planning
   - protected private route planning
   - payout resolution
   - transaction record creation
   - route-state normalization

4. Data and trust layer
   - sessions
   - payout preferences
   - request records
   - swap and tip records
   - analytics
   - sensitive-field protection

5. Execution layer
   - supported execution providers
   - supported blockchain networks
   - hosted checkout or fiat-connected providers where supported

## Public Responsibility Boundary

SWYPE owns the user experience, request logic, routing orchestration, tracking model, and trust controls.

Supported execution providers and supported blockchain networks handle execution and settlement.

SWYPE does not take custody of user funds and does not ask users for private keys or recovery phrases.

## What Is Intentionally Not Published

This public documentation does not publish:

- provider-ranking logic
- fallback ordering
- pricing heuristics
- private-route decomposition
- operational playbooks
- internal recovery procedures beyond public-safe lifecycle explanations
