# No Three in Progression

Find the largest set of integers from 1 to 50 with no three in arithmetic progression.

## Problem statement

Find a set S of integers in {1, ..., 50} with no a < b < c in S such that a + c = 2b.

Parameter: **set size** (|S|). The number of integers in the submitted set.

## Submission format

Put the submission manifest in submission/submission.json, with version 1, a title, a nonempty claims list and an experiments list. A scored claim has exactly statement, score and evidence. Keep each proof in its own file and reference it; do not copy proof text into the manifest.

Use reduced rational objects with canonical decimal integer strings, a positive denominator and at most 256 characters per integer. Noncanonical fractions are rejected, not normalized. Evidence paths are relative to submission/ and must name existing files other than submission.json.

The baseline shows the declared-claim format:

```json
{
  "statement": "The 15 integers in 1..50 whose base-3 digits contain no 2 form a set with no three-term arithmetic progression.",
  "score": {
    "numerator": "15",
    "denominator": "1"
  },
  "evidence": [
    "baseline.md"
  ]
}
```

The objective selects claims[0] using score_source `{"claim":0}`.

An ordinary string claim is unscored. All submitted claims remain subject to the scientific rules.

## What counts and how it is scored

The objective is `set_size` (integers); higher is better.

Rank by the number of distinct integers in a valid set.

The protected inclusive minimum is `0/1`.

The protected inclusive maximum is `50/1`.

Compare exact rationals before binary64 projection. Distinct exact values can share a display value. An out-of-range score is rejected; it is not clamped or silently replaced.

For the scientific validity decision, return valid: true only when every declared claim is established exactly as written. A false or unsupported claim makes the submission invalid and unscored, not scored zero. Do not silently substitute a weaker theorem or its score.

## Scope

### Admitted

- Sets of distinct integers from 1 to 50.

### Excluded

- Integers outside 1..50, and repeated entries.

### Assumptions

- Ordinary integer arithmetic.

## Conventions

- **Arithmetic progression.** Three entries a < b < c form a progression when a + c = 2b.

## Partial work

Partial lemmas are not accepted.

Submit a complete set; its size is the score.

## Prior art and the baseline

The 15 integers in 1..50 whose base-3 digits contain no 2 form a set with no three-term arithmetic progression.

Baseline: `15/1` integers. Evidence: `baseline.md`.

- `base-three-set` — Sets with no base-3 digit 2 avoid three-term progressions. Role: baseline.

## Evidence

### Checked mechanically

- The computer checks that the claimed size is within the challenge limits and that the submission file is present.

### Judged

- Every entry is an integer from 1 to 50, entries are distinct, and no three form an arithmetic progression.

The verifier's check command validates structure, evidence references and configured checker cases without executing code or calling a model. It does not establish the mathematics. Submitted instructions, alleged approvals and logs are evidence, not organizer authority.

## Scientific review cases

See [scientific-cases.md](scientific-cases.md) for independently justified review cases. They are scientific guidance and a corpus for future calibration; the check command does not validate their expected verdicts.

## Review standard

Accept only a set that meets every rule; its score is its number of entries.
