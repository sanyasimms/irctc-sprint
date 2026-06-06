# AI Feature Specification: Waitlist Prediction

## Problem It Solves

Users cannot estimate waitlist confirmation.

## Proposed Feature

Show chance of confirmation.

## Model Choice

XGBoost classifier

## Input Data

* Historical waitlist data
* Route
* Season
* Cancellation history

## Output

"Estimated confirmation probability: 82%"

## Fallback

Show standard waitlist.

## Success Metrics

* Lower cancellations
* Higher booking confidence

## Risks

Prediction uncertainty.
