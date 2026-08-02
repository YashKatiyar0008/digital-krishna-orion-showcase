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
| Understanding | [REAL] | [REAL] | Blind rubric | Pending |
| Empathy | [REAL] | [REAL] | Blind rubric | Pending |
| Actionability | [REAL] | [REAL] | Blind rubric | Pending |
| Cultural relevance | [REAL] | [REAL] | Blind rubric | Pending |
| Hindi quality | [REAL] | [REAL] | Native review | Pending |
| Hinglish quality | [REAL] | [REAL] | Native review | Pending |
| Instruction following | [REAL] | [REAL] | Blind rubric | Pending |
| Safety | [REAL] | [REAL] | Boundary test | Pending |
| Unsupported quotation rate | [REAL] | [REAL] | Source audit | Pending |
| Response latency | [REAL] | [REAL] | Timed benchmark | Pending |

No result is publishable until the held-out run and review are verified.

## Required failure cases

- Weak SFT response: [ADD_REAL_UNEDITED_CASE]
- Base/SFT tie: [ADD_REAL_UNEDITED_CASE]
- Language failure: [ADD_REAL_UNEDITED_CASE]
- Overused cultural reference: [ADD_REAL_UNEDITED_CASE]
- Case requiring verified retrieval: [ADD_REAL_UNEDITED_CASE]
