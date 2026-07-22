# DGX RouterOS Agent RSL Flywheel

I built this as the public record for a research flywheel around a network-focused agent. The private source preserves sanitized corpora, holdouts, retrieval manifests, reports, training runs, and promotion gates. This branch records the evidence discipline without publishing raw corpus text or operational identity.

## What I built

1. Versioned corpus and retrieval layouts with manifests and source references.
2. Separate train, validation, and holdout material.
3. Privacy and action-safety checks before promotion.
4. Evaluation reports that retain failure modes instead of hiding them in one score.
5. Quarantine and promotion decisions with explicit reasons.
6. Reproducible build, refresh, evaluation, and receipt-verification scripts.

## Recorded results

| Observation | Source evidence | Status |
|---|---|---|
| V1/V2/V3 corpus generations are recorded | source manifests and README | Historical |
| V3 contains 2,383 sanitized source-grounded public/synthetic examples | source README | Historical |
| V3 adapters were quarantined after holdout regression | source README/reports | Historical decision |
| v1 restart uses 500/100/100 train/validation/holdout | source corpus | Historical |
| v2 uses 3,500/350 plus a frozen 500-case holdout and was rejected | source corpus/README | Historical decision |

## Why it matters

A flywheel amplifies useful behavior and mistakes. Holdout contamination, private strings, unsafe actions, or unresolved failures should stop promotion.

## Engineering approach

Corpus items carry provenance and sanitization state. Evaluation separates quality, privacy, and action safety. Quarantine is durable until targeted review clears it.

## Sanitized architecture boundary

See [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md).

## Repository map

- [docs/CASE-STUDY.md](docs/CASE-STUDY.md)
- [docs/RSL-EVALUATION-RECORD.md](docs/RSL-EVALUATION-RECORD.md)
- [docs/PUBLICATION-SAFETY.md](docs/PUBLICATION-SAFETY.md)
- [examples/synthetic-evaluation-record.json](examples/synthetic-evaluation-record.json)

## Evidence rules and limits

Readings are historical private-source evidence. This is a public project interface, not an operational training repository; it contains no raw private corpus, model weights, addresses, accounts, or deployment claims.
