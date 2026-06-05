# IRCTC Problem Discovery — Part A

## Summary

* Total problems documented: 6 (3 given + 3 self-discovered)
* Platform explored: irctc.co.in
* Devices used: Desktop Chrome + Mobile Chrome
* Goal: Identify friction points and prepare solution planning for Part B

---

# Problem 1: Tatkal Booking Crashes at 10:00 AM [Given]

## What is broken

The Tatkal booking flow becomes unresponsive at peak opening time. Users lose session state, experience freezes, and receive unclear feedback.

## Affected users

Tatkal users during the booking window, especially time-sensitive travelers.

## Frequency

Daily during Tatkal release hours.

## Current flow — step by step

1. User logs into IRCTC.
2. Searches train and date.
3. Selects Tatkal quota.
4. Enters passenger details.
5. Clicks Book.
6. Loading screen persists.
7. Session resets or booking fails.

## Where exactly it breaks

Steps 5–7 due to high concurrent load and lack of feedback.

---

# Problem 2: Search Filters Do Not Work Reliably [Given]

## What is broken

Train filters sometimes reset or display inconsistent results.

## Affected users

Users searching trains with class and availability constraints.

## Frequency

Intermittent, more visible during peak usage.

## Current flow — step by step

1. Search route.
2. Results appear.
3. Apply class filter.
4. Apply availability filter.
5. Results refresh.
6. Filters disappear.

## Where exactly it breaks

Steps 4–6 due to inconsistent filter persistence.

---

# Problem 3: Seat Selection Resets Randomly [Given]

## What is broken

Selected seat preferences do not consistently persist.

## Affected users

Families, elderly travelers, accessibility users.

## Frequency

Occasional; more noticeable on mobile.

## Current flow — step by step

1. Select train.
2. Open seat map.
3. Select berth.
4. Continue booking.
5. Preference changes.
6. User rechecks selection.

## Where exactly it breaks

Between selection and passenger detail sync.

---

# Problem 4: Payment Status Has Poor Feedback [Self-Discovered]

## How I found it

Observed payment options and reviewed confirmation flow.

## Screenshot/Description

Payment page shows waiting state with limited progress visibility.

## What is broken

Users cannot determine whether payment is processing or failed.

## Affected users

Users paying via UPI and net banking.

## Frequency

Occurs under slower network conditions.

## Current flow — step by step

1. Complete passenger details.
2. Open payment page.
3. Choose payment method.
4. Confirm payment.
5. Processing spinner appears.
6. No clear state update.
7. User refreshes.

## Where exactly it breaks

Steps 5–7 due to missing status communication.

---

# Problem 5: PNR Status Information Is Hard To Interpret [Self-Discovered]

## How I found it

Explored PNR inquiry flow.

## Screenshot/Description

Information hierarchy is difficult for first-time users.

## What is broken

Status terms are difficult to understand.

## Affected users

Occasional travelers and older users.

## Frequency

Common.

## Current flow — step by step

1. Open PNR page.
2. Enter PNR.
3. Submit.
4. Results display.
5. User reads codes.
6. User searches externally.

## Where exactly it breaks

Step 5 because status explanation is insufficient.

---

# Problem 6: Mobile Booking Experience Feels Cluttered [Self-Discovered]

## How I found it

Opened IRCTC on mobile browser.

## Screenshot/Description

Multiple stacked sections require scrolling.

## What is broken

Users lose context during booking.

## Affected users

Mobile users.

## Frequency

Consistent.

## Current flow — step by step

1. Open mobile site.
2. Search train.
3. Open results.
4. Continue booking.
5. Scroll repeatedly.
6. Miss actions.

## Where exactly it breaks

Steps 4–6 due to layout density.

---
