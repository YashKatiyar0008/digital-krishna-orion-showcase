# SFT Evidence

## 1. Base-model identity

`[REPLACE_WITH_EXACT_MODEL_ID]`

Revision: `[REPLACE_WITH_EXACT_REVISION]`

## 2. Dataset evidence

Document verified total example count, language and category distributions, train/validation/test split, data-review process, privacy controls, duplicate removal, and source verification. Public proof should use aggregates and sanitized samples only.

| Evidence | Verified value |
|---|---|
| Total examples | [REPLACE_WITH_REAL_VALUE] |
| Language distribution | [REPLACE_WITH_REAL_VALUE] |
| Category distribution | [REPLACE_WITH_REAL_VALUE] |
| Train/validation/test split | [REPLACE_WITH_REAL_VALUE] |

## 3. Training evidence

| Field | Verified value |
|---|---|
| Method | [REPLACE_WITH_REAL_VALUE] |
| Epochs | [REPLACE_WITH_REAL_VALUE] |
| Learning rate | [REPLACE_WITH_REAL_VALUE] |
| Maximum sequence length | [REPLACE_WITH_REAL_VALUE] |
| Hardware | [REPLACE_WITH_REAL_VALUE] |
| Run date | [REPLACE_WITH_REAL_VALUE] |
| Duration | [REPLACE_WITH_REAL_VALUE] |
| Final training loss | [REPLACE_WITH_REAL_VALUE] |
| Final validation loss | [REPLACE_WITH_REAL_VALUE] |
| Adapter directory screenshot | [ADD_REAL_SCREENSHOT] |
| Terminal screenshot | [ADD_REAL_SCREENSHOT] |
| Loss graph | [ADD_REAL_SCREENSHOT] |

## 4. Adapter evidence

The trained adapter remains private. Authorized judges may be shown proof of adapter files, a reviewed configuration summary, the model version, and a successful adapter-loading demonstration. Weights are not published.

## 5. Evaluation evidence

A fair comparison uses the same base model, user prompts, neutral system instruction, generation settings, and held-out test set. Outputs must be unedited and blindly scored as A versus B.

## 6. Evidence checklist

- [ ] Exact base-model ID and revision verified
- [ ] Dataset aggregates verified
- [ ] Split integrity and duplicate checks documented
- [ ] Training terminal screenshot redacted and added
- [ ] Loss graph verified and added
- [ ] Adapter existence and version verified
- [ ] Held-out outputs captured without editing
- [ ] Blind evaluation completed
- [ ] Public evidence reviewed for sensitive data
