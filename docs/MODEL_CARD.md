# Model Card

| Field | Value |
|---|---|
| Project | Digital Krishna |
| Base model | `mlx-community/Qwen3-1.7B-4bit` |
| Adapter method | MLX LoRA, rank 8 over 8 layers |
| Version | `digital-krishna-qwen3-1.7b-lora` |
| Languages | English, Hindi, Hinglish |
| Completion status | Adapter trained; blind quality and human safety evaluation still in progress |

## Intended uses

General reflective guidance, structured next steps, multilingual interaction, and culturally grounded educational experiences within documented safety boundaries.

## Out-of-scope uses

Medical diagnosis or treatment, emergency response, therapy replacement, legal or financial advice, divine authority, guaranteed predictions, surveillance, or high-stakes automated decisions.

## Training summary

The primary adapter was trained for 400 optimization iterations on 1,586 conversations, with 77 validation and 97 held-out test conversations. Configuration: learning rate 0.00001, maximum sequence length 1,024, batch size 1, gradient accumulation 8, and seed 42. Training ran locally on an Apple M4 MacBook Air with 16 GB unified memory. Final Qwen3 loss values were not found in the retained reviewed artifacts and are not claimed.

## Evaluation summary

Blind base-versus-SFT scoring has not yet been completed. A separate deterministic safety/retrieval suite passed 30 of 30 scenarios on 18 July 2026, covering English, Hindi, Hinglish, prompt injection, fabricated-verse handling, high-risk boundaries, and empty-input validation. That result validates the tested pipeline behavior, not general model quality.

## Safety boundaries

The model should disclose limitations, avoid unsupported exact quotations, express uncertainty, protect privacy, and encourage qualified or emergency support where appropriate.

## Known limitations and ethical considerations

Possible hallucination, multilingual quality variation, cultural overgeneralization, retrieval errors, and inconsistent safety behavior require ongoing evaluation. The project must avoid religious impersonation, exclusionary claims, and over-reliance by vulnerable users.

## Licensing status

The base checkpoint remains subject to its upstream license. Public adapter licensing has not been finalized; weights are not distributed here.

## Model-access policy

The adapter is private. Proof of existence and a controlled loading demonstration may be provided to authorized judges. No weights are included here.
