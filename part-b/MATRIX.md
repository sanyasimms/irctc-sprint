# Impact vs Effort Matrix

|             | Low Effort                          | High Effort             |
| ----------- | ----------------------------------- | ----------------------- |
| High Impact | Filter Persistence, Payment Tracker | Tatkal Queue, Seat Lock |
| Low Impact  | PNR Dashboard                       | AI Waitlist             |

## Placement Justifications

Tatkal Queue — Major Project
High user impact. Requires backend changes.

Filter Persistence — Quick Win
Frontend-heavy and improves search.

Seat Lock — Major Project
Touches booking infrastructure.

Payment Tracker — Quick Win
Reduces uncertainty.

PNR Dashboard — Fill-In
UX improvement.

AI Predictor — Time Sink
Useful but requires data maturity.

## Recommended Order

1. Filter Persistence
2. Payment Tracker
3. Seat Lock
4. Tatkal Queue
5. PNR Dashboard
6. AI Predictor
