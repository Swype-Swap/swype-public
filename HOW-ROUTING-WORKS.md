# How Routing Works

SWYPE routes payment and swap flows through a non-custodial orchestration model.

## High-Level Flow

1. The user chooses a product flow such as tipping, Swype Me, public swap, protected private swap, or a fiat-connected route.
2. SWYPE validates the request and resolves the destination or payout preference.
3. SWYPE selects the safest and cheapest supported path available for the requested flow while considering:
   - route validity
   - destination compatibility
   - provider availability
   - estimated cost
   - operational reliability
4. SWYPE creates instructions and a stable SWYPE tracking identifier.
5. SWYPE keeps the route observable through normalized status updates while supported providers and networks handle execution and settlement.

## Tipping And Swype Me

Tipping and Swype Me use the same request, routing, and tracking model as swaps, but begin from a payment or request experience instead of a trading intent.

In these flows:

- the recipient controls the destination or payout preference
- the payer gets a guided flow
- SWYPE handles request logic, payout resolution, and status tracking
- SWYPE remains non-custodial

## Public And Private Routes

Public routes optimize for direct execution.

Protected private routes optimize for route confidentiality and expose a public-safe tracker model instead of full internal route detail.

SWYPE does not publish confidential route-planning internals in this repository.
