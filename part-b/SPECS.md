# IRCTC Feature Specifications — Part B

## Feature Spec 1: Tatkal Virtual Queue

### Problem Statement

Tatkal traffic spikes create booking failures and uncertainty.

### Current State

Users reach booking but do not know if requests are queued or failed.

### Proposed Solution

Introduce a live queue with estimated wait time and booking window.

### Proposed User Flow

1. User enters Tatkal page
2. User joins queue
3. Queue position shown
4. Countdown displayed
5. Booking unlocked
6. Payment completed

### Technical Implementation Plan

System components:

* Frontend
* Queue service
* Booking API

New data:

* queuePosition
* estimatedWait
* sessionExpiry

API:

* POST /queue/join
* GET /queue/status

Frontend:

* Queue card
* Countdown timer

Third-party:

* Redis

### Success Metrics

* Booking completion +20%
* Server failures −30%

### Edge Cases

* Queue timeout
* Refresh recovery

---

## Feature Spec 2: Persistent Search Filters

### Problem Statement

Filters reset and show inconsistent train results.

### Proposed Solution

Persist filters in session storage and backend.

### Technical Plan

Frontend + API + cache updates.

### Metrics

Reduce re-filter attempts.

---

## Feature Spec 3: Reliable Seat Lock

### Problem Statement

Seat selection disappears.

### Proposed Solution

Temporary seat reservation.

### Technical Plan

Seat-lock table + timeout.

### Metrics

Reduce seat reset complaints.

---

## Feature Spec 4: Payment Status Tracker

### Problem Statement

Users cannot determine payment state.

### Proposed Solution

Show payment stages.

### Technical Plan

Payment polling + webhook.

### Metrics

Reduce duplicate payment attempts.

---

## Feature Spec 5: Simplified PNR Dashboard

### Problem Statement

PNR terms difficult to understand.

### Proposed Solution

Status cards + explanations.

### Metrics

Reduce support requests.

---

## Feature Spec 6: Mobile Booking Flow

### Problem Statement

Booking screens are crowded.

### Proposed Solution

Stepper-based booking flow.

### Metrics

Improve mobile completion.
