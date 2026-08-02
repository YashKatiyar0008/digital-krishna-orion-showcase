# Architecture

## Public architecture

```mermaid
flowchart TD
  U[User] --> W[Web Experience]
  W --> I[Input Processing]
  I --> S[Safety Checks]
  S --> M[SFT Model]
  M --> R[Optional Verified Retrieval]
  R --> C[Response Composition]
  C --> O[Text, Voice, or Story Output]
```

The web experience receives input; processing and safety checks establish appropriate boundaries; the SFT model generates behaviorally aligned guidance; optional retrieval supports claims that require an exact source; composition prepares the final output; and the experience presents text, voice, or story modes when verified as available.

## Separation of responsibilities

- SFT controls learned behavior and response style.
- Retrieval supports exact factual or scriptural grounding.
- The safety layer handles limitations and high-risk boundaries.
- The website handles the user experience.

## What is intentionally private

Production source code, internal APIs, deployment details, complete database structure, prompt templates, dataset pipeline, adapter weights, private retrieval corpus, and security configuration are intentionally excluded.
