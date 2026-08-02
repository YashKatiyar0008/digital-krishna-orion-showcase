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
| Understanding | 4.55/5 | 4.30/5 | Automated rubric | Complete; human review pending |
| Empathy | Not separately scored | Not separately scored | Human blind rubric | Pending |
| Actionability | 2.26/5 | 1.60/5 | Automated rubric | Complete; human review pending |
| Cultural relevance | 1.05/5 | 1.00/5 | Keyword-based proxy | Complete; weak result |
| Hindi/Hinglish quality | 1.13/5 | 2.71/5 | Four supplemental prompts | Complete; native review pending |
| Instruction following | 3.29/5 | 3.59/5 | Automated rubric | Complete; human review pending |
| Safety boundary | 2.95/5 | 1.65/5 | One supplemental crisis prompt | Complete; remediation required |
| Unsupported quotation rate | 0% detected | 0% detected | Pattern check in this sample | Complete; source audit pending |
| Response latency | 2.975 seconds | 2.253 seconds | Mean local generation time | Complete for this run |
| Automated preference | 29.4% | 17.6% | Identity-blinded deterministic scores | Complete; 52.9% ties |

The run used 12 deterministically selected private held-out English prompts, four supplemental Hindi/Hinglish prompts, and one supplemental safety prompt. Generation used the same public neutral instruction, temperature 0, and 220-token limit. Automated scoring did not use model identity. It measured observable proxies and must not be described as human evaluation. Prompt hashes and per-case score metadata are public; raw held-out prompts and unedited outputs remain private to protect dataset integrity.

The SFT adapter did not outperform the base overall in this small run. It improved multilingual matching, instruction following, and latency, while performing worse on automated understanding, actionability, cultural relevance, and the dedicated safety prompt. This is a useful failure signal and makes adapter remediation plus human review the next step.

## Verified pipeline test

On 18 July 2026, a deterministic 30-scenario safety/retrieval suite passed 30/30. It included English, Hindi, Hinglish, prompt injection, fabricated-verse handling, self-harm boundaries, and empty-input validation. The suite checked exact matches against a 25-record verified scripture corpus and the structured response contract. It used mock/evaluation mode without a live generation model, so it is not evidence that SFT outperforms the base model.

## Required failure cases

- Weak SFT response: observed in actionability and the dedicated safety prompt; raw case restricted to judge review
- Base/SFT tie: 9 of 17 automated comparisons were ties
- Language failure: base model scored poorly on the four Hindi/Hinglish proxy cases; native review remains pending
- Overused cultural reference: not observed by the conservative keyword proxy; human review remains pending
- Case requiring verified retrieval: exact scripture quotation remains routed to verified retrieval rather than trusted to SFT memory
