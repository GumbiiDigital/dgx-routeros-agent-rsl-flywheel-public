# Case Study: Quarantine Before Promotion

## Context

Iterative training systems improve only when feedback is trustworthy. A plausible answer can still be unsafe, unsupported, or privacy-sensitive.

## Problem

A naive flywheel feeds every correction back into the next training set. That can blur the holdout boundary, repeat private details, and reward behavior that acts without sufficient evidence.

## What I built

The public design uses distinct destinations for evaluated items:

- promote_candidate for items that satisfy quality, privacy, and action-safety gates;
- quarantine for items with a known defect or unresolved risk; and
- reject for items that should not re-enter the loop.

Holdout evaluation remains isolated from training input. Reviewer feedback changes the item record, not the historical result.

## Engineering decisions

- Sanitization happens before an item becomes eligible for training.
- Provenance class is mandatory even when the source text is synthetic.
- Privacy and action safety are independent gates.
- Aggregate scale is described qualitatively in public.
- A promotion decision includes reasons, not just a score.
- Quarantine is durable until a targeted review clears it.

## Representative artifact

The synthetic evaluation record shows a fictional holdout item, gate results, a quarantine path, and the evidence required for later promotion. It contains no private corpus text or operational metric.

## Evidence available here

- The evaluation record parses as JSON.
- The record clearly identifies synthetic provenance.
- Promotion gates and quarantine reasons are explicit.
- The repository checker rejects common private-data patterns.
- CI runs the same publication gate.

## Lessons

A flywheel is safer when it can stop. The promotion gate should protect the next training cycle from both low-quality behavior and privacy leakage.

## Limitations

No model, corpus, private score, or training result is published here. The case study documents methodology only.
