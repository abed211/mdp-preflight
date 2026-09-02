# Sample MDP Preflight Report

This fictional example demonstrates the expected evidence level. It is not a claim about a real product.

```text
MDP PREFLIGHT REPORT

Repository: Northstar Delivery Demo
Observed maturity: PROTOTYPE
Audit scope: customer web app, courier app, operations portal, API package,
database schema, auth middleware, build scripts, and existing test commands.
Critical journey: customer creates order → operations assigns courier → courier accepts
→ status update returns to customer.

SCORECARD
A Project/execution       3/5  All apps have run commands; environment contract is incomplete.
B Requirements/rules      2/5  Happy-path statuses exist; cancellation and reassignment are undefined.
C Feature completeness    2/5  Order screens persist data; notifications and recovery are placeholders.
D Data integrity          1/5  No idempotency key or unique guard prevents duplicate order submission.
E Auth/authz               1/5  Courier ownership is hidden in UI but not enforced on the API mutation.
F Multi-system contracts  2/5  Apps share an API, but each declares different status strings locally.
G Executable testing      2/5  Unit tests run; no contract or cross-app journey test exists.
H Security/privacy        1/5  Confirmed order-object authorization gap; sensitive error body returned.
I Release/operations      1/5  Build passes; rollback, monitoring, and post-release checks are undefined.
J Context/memory          0/5  No canonical requirements, contracts, decisions, or verified state record.

Total: 15/50

CRITICAL JOURNEY TRACE
ENTRY              PROVEN   Customer form submits to POST /orders.
UI STATES          PARTIAL  Loading exists; duplicate click remains enabled.
VALIDATION         PARTIAL  Address required client-side; server accepts invalid service area.
AUTHORIZATION      MISSING  Courier can mutate an order assigned to another courier by changing ID.
DOMAIN RULE        PARTIAL  Status order exists in one service; cancellation/reassignment absent.
API/EVENT          PARTIAL  REST mutations exist; app status enums disagree.
DATA               PARTIAL  Order persists; duplicate/idempotency and concurrent assignment unhandled.
SIDE EFFECT        MISSING  Notification adapter is a production-path stub.
FAILURE/RECOVERY   MISSING  Assignment timeout and offline courier recovery are undefined.
TEST               MISSING  No test crosses customer, operations, courier, and persisted state.

RELEASE BLOCKERS
- HIGH: Server does not verify that the authenticated courier owns the assignment.
- HIGH: Duplicate order submission can create multiple persisted orders.
- Critical delivery journey has no executable cross-system proof.

TOP THREE ACTIONS
1. Add server-side assignment ownership authorization and denial tests.
2. Define one canonical order state contract and idempotent creation/assignment behavior.
3. Add one persisted end-to-end journey covering create, assign, accept, update, and denial.

NOT VERIFIED
- Production deployment, secrets store, backup restore, and external notification provider:
  credentials/infrastructure were unavailable and no production action was authorized.
```

The score is intentionally subordinate to evidence. A project with 40/50 still fails release if a confirmed high-severity authorization gap remains.

