# Case study: quarantine before promotion

## Actual problem

Multiple corpus generations and evaluation paths made it possible for a naive flywheel to contaminate holdouts, repeat privacy defects, or reward unsafe action behavior.

## Source-backed sequence

1. V1 and V2 evolved into sanitized source-grounded V3 material.
2. Retrieval manifests and evaluation reports stayed beside build scripts.
3. V3 full and guarded adapters were quarantined after holdout regression.
4. A v1 restart was bounded at 500 train, 100 validation, and 100 holdout rows.
5. V2 expanded to 3,500 train, 350 validation, and a frozen 500-case holdout; its run was rejected.

## Failed hypotheses

- Bigger training material automatically improves behavior: unsupported.
- Private-safe is automatically action-safe: false.
- One aggregate score is enough for promotion: false.

## Bounded tests and acceptance gates

Source scripts provide manifest checks, retrieval checks, privacy lint, holdout evaluation, action-safety review, and receipt verification. Promotion requires provenance, schema, privacy, holdout quality, and action-safety gates with no unresolved quarantine reason.

## Result

The concrete result is a refusal and quarantine path. The public branch keeps that decision visible and does not claim a promoted adapter.
