# SFT Evidence

## 1. Base-model identity

Primary showcase run: `mlx-community/Qwen3-1.7B-4bit`

Public adapter label: `digital-krishna-qwen3-1.7b-lora`. The exact upstream revision was not preserved in the reviewed configuration and is therefore not claimed.

## 2. Dataset evidence

Document verified total example count, language and category distributions, train/validation/test split, data-review process, privacy controls, duplicate removal, and source verification. Public proof should use aggregates and sanitized samples only.

| Evidence | Verified value |
|---|---|
| Total examples | 1,760 conversations |
| Language distribution | English, Hindi, and Hinglish are present; exact audited percentages pending |
| Category distribution | Broad modern-life, cultural-guidance, and safety categories; exact audited percentages pending |
| Train/validation/test split | 1,586 / 77 / 97, assigned deterministically by SHA-256 of canonical identifier |

## 3. Training evidence

| Field | Verified value |
|---|---|
| Method | MLX LoRA over a 4-bit Qwen3 base; rank 8, scale 20, dropout 0, 8 adapted layers |
| Schedule | 400 optimization iterations, batch size 1, gradient accumulation 8 |
| Learning rate | 0.00001 |
| Maximum sequence length | 1,024 tokens |
| Hardware | MacBook Air with Apple M4 and 16 GB unified memory |
| Run date | Not preserved in reviewed artifacts |
| Duration | Not preserved in reviewed artifacts |
| Final training loss | Not preserved in reviewed Qwen3 artifacts |
| Final validation loss | Not preserved in reviewed Qwen3 artifacts |
| Adapter directory screenshot | Not yet added; local artifact existence verified |
| Terminal screenshot | Not yet added |
| Loss graph | Not available for the reviewed Qwen3 run |

## 4. Adapter evidence

The trained adapter remains private. Authorized judges may be shown proof of adapter files, a reviewed configuration summary, the model version, and a successful adapter-loading demonstration. Weights are not published.

Local review verified the final adapter plus checkpoints at iterations 100, 200, 300, and 400. An earlier proof run on `Qwen/Qwen2.5-0.5B-Instruct` completed one epoch using 776 training and 38 validation conversations. That run recorded training loss 1.015 and validation loss 0.849. It is disclosed separately so its results are not misattributed to Qwen3.

## 5. Evaluation evidence

A fair comparison uses the same base model, user prompts, neutral system instruction, generation settings, and held-out test set. Outputs must be unedited and blindly scored as A versus B.

## 6. Evidence checklist

- [x] Base-model ID verified from adapter configuration
- [ ] Exact upstream revision recovered
- [x] Dataset totals and split counts verified
- [ ] Split integrity and duplicate checks documented
- [ ] Training terminal screenshot redacted and added
- [ ] Loss graph verified and added
- [x] Adapter existence and version verified locally
- [ ] Held-out outputs captured without editing
- [ ] Blind evaluation completed
- [ ] Public evidence reviewed for sensitive data
