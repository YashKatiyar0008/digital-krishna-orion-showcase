# Evaluation

## Evaluation goals

Measure understanding, empathy, actionability, cultural relevance, Hindi quality, Hinglish quality, instruction following, clarification behavior, safety boundaries, unsupported quotation rate, and response latency.

## Test-set rules

Use unseen prompts with no training overlap, multiple categories, multilingual coverage, ambiguous and multi-turn prompts, and safety-boundary prompts. Record versioned test-set hashes privately without exposing private data.

## Fair base-versus-SFT comparison

Keep the prompt, neutral system message, generation settings, token limits, model family, and test set the same. Save complete, unedited outputs.

## Blind review

Randomize outputs as Response A and Response B so reviewers do not know which system produced each. Define a scoring rubric before review, record ties and disagreements, and reveal identities only after scores are locked.

## Results

| Metric | Base model | Digital Krishna SFT | Method | Status |
|---|---:|---:|---|---|
| Understanding | Not measured | Not measured | Blind rubric | Pending |
| Empathy | Not measured | Not measured | Blind rubric | Pending |
| Actionability | Not measured | Not measured | Blind rubric | Pending |
| Cultural relevance | Not measured | Not measured | Blind rubric | Pending |
| Hindi quality | Not measured | Not measured | Native review | Pending |
| Hinglish quality | Not measured | Not measured | Native review | Pending |
| Instruction following | Not measured | Not measured | Blind rubric | Pending |
| Safety | Not measured in A/B | Not measured in A/B | Boundary test | Pending |
| Unsupported quotation rate | Not measured | Not measured | Source audit | Pending |
| Response latency | Not measured | Not measured | Timed benchmark | Pending |

No result is publishable until the held-out run and review are verified.

## Verified pipeline test

On 18 July 2026, a deterministic 30-scenario safety/retrieval suite passed 30/30. It included English, Hindi, Hinglish, prompt injection, fabricated-verse handling, self-harm boundaries, and empty-input validation. The suite checked exact matches against a 25-record verified scripture corpus and the structured response contract. It used mock/evaluation mode without a live generation model, so it is not evidence that SFT outperforms the base model.

## Required failure cases

- Weak SFT response: pending held-out review
- Base/SFT tie: pending blind comparison
- Language failure: pending native-speaker review
- Overused cultural reference: pending held-out review
- Case requiring verified retrieval: exact scripture quotation; evaluation example pending
