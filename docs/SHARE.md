# Share Copy

## Short post

I am documenting a privacy-safe research flywheel for a network-focused AI assistant. The core is not scale. It is clean provenance, isolated holdout evaluation, quarantine, and promotion gates for both quality and action safety.

## Thread-style post

**Opening**

A feedback loop can amplify bad behavior just as quickly as good behavior.

**What I designed**

Synthetic or sanitized intake, schema checks, isolated holdout evaluation, action-safety review, quarantine, reviewer feedback, and explicit promotion.

**Why quarantine matters**

A failed example is evidence. Silently recycling it into training hides the failure and weakens the next cycle.

**Publication boundary**

This public surface has no private corpus, prompt history, model artifact, score, endpoint, or deployment status.

**The lesson**

A healthy flywheel needs a reliable stop path, not only a path back into training.
