# DGX RouterOS Agent RSL Flywheel Public

I built this repository as a public research interface for privacy-safe training, evaluation, and feedback-loop methods for a network-focused AI assistant. The emphasis is not dataset volume. It is evidence quality, quarantine, holdout integrity, and promotion safety.

## What I built

The design covers:

- synthetic and sanitized corpus intake;
- schema and privacy validation;
- training-candidate preparation;
- isolated holdout evaluation;
- action-safety scoring;
- failure quarantine;
- reviewer feedback; and
- promotion gates that require both quality and privacy evidence.

## Why it matters

A flywheel can amplify mistakes as easily as it amplifies useful behavior. If failed examples, private details, or unsafe actions re-enter training without control, the loop becomes less trustworthy over time.

I treat quarantine and promotion as first-class engineering components.

## Engineering approach

Corpus items carry provenance class, sanitization state, task type, expected evidence, and allowed action level. Holdout material stays separate from training material. Evaluation results are grouped by behavior rather than presented as a single score.

Promotion requires:

- privacy scan pass;
- schema pass;
- holdout quality pass;
- action-safety pass;
- no unresolved quarantine reason; and
- human review for boundary changes.

Scale is described broadly because operational corpus metrics are not part of this public surface.

## Synthetic public-safe architecture

The diagram shows a fictional research pipeline and does not reproduce a private corpus or deployment.

See [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md).

## Representative work and artifacts

- [Case study](docs/CASE-STUDY.md) - how quarantine protects a feedback loop.
- [Synthetic evaluation record](examples/synthetic-evaluation-record.json) - promotion and refusal evidence in JSON.
- [Publication safety](docs/PUBLICATION-SAFETY.md) - corpus and reporting boundary.
- [Share copy](docs/SHARE.md) - public explanation in my voice.
- [Safety checker](scripts/check_publication_safety.py) - repository privacy gate.

## Evidence and lessons

This repository proves only the public structure: an original evaluation schema, a synthetic architecture, explicit promotion gates, valid JSON, and automated privacy checks. It does not publish private metrics or claim a trained model has passed these gates.

The central lesson is that quarantined failures are valuable evidence. They should be inspected and classified, not silently recycled.

## Repository map

| Path | Purpose |
|---|---|
| README.md | Research interface and limits |
| docs/CASE-STUDY.md | Quarantine and promotion case study |
| docs/ARCHITECTURE.md | Synthetic Mermaid flywheel |
| docs/PUBLICATION-SAFETY.md | Corpus publication rules |
| docs/SHARE.md | Share-ready copy |
| examples/ | Synthetic JSON evaluation |
| scripts/check_publication_safety.py | Privacy and structure checker |
| .github/workflows/publication-safety.yml | CI gate |

## Publication boundary

This is a public project interface, not an operational training repository. I exclude live addresses, hostnames, hardware identities, accounts, local paths, credentials, raw telemetry, private corpora, service inventories, private topology, equipment maps, controller identities, and operational commands. Examples are synthetic and do not reproduce a live environment.

## Limitations

This repository does not disclose corpus size, model state, private evaluation metrics, deployment status, or promotion results. The example record is illustrative and is not evidence of a completed training run.
