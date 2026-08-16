# FlowHE-IoT Reproducibility Supplement v1.1

Reviewer-facing reproducibility supplement for the frozen FlowHE-IoT experimental chain used by the CSDE 2026 manuscript.

## Final frozen design

- Classifier: Linear SVM
- C = 30
- CKKS: R_N8192_S40
- N = 8192
- scale = 2^40
- coefficient-modulus chain = [60, 40, 60]
- Safe runtime states:
  - S0: S40 row B1
  - S1: S40 SIMD B32
  - S2: S40 SIMD B64
  - S3: S40 SIMD B128
- S30 is excluded from the final policy after boundary-near correctness testing.

## Reviewer quick verification

1. Open `CLAIM_EVIDENCE_MATRIX.csv`.
2. Find the claim of interest and its manuscript section.
3. Follow `evidence_source` to the frozen CSV/JSON under `evidence/`.
4. Use `MANUSCRIPT_TABLE_MAP.csv` and `MANUSCRIPT_FIGURE_MAP.csv` for the final Table I-VI and Fig. 1-5 mappings.
5. Inspect the corresponding source notebook under `code/notebooks/` if implementation detail is needed.
6. Verify package integrity using `CHECKSUMS.sha256`.

## Important scope notes

- Raw Edge-IIoTset and IoT-23 datasets are not redistributed.
- Historical/superseded results are retained for provenance but are explicitly separated by `docs/SUPERSEDED_RESULTS.md`.
- Final manuscript claims must follow `CLAIM_EVIDENCE_MATRIX.csv` and `docs/CLAIM_BOUNDARIES.md`.
- S30 is not an operational profile; S40 is the only admitted CKKS profile.
- IoT-23 CKKS evidence covers the stated 320-case subset, not all 381,645 sampled rows.

## v1.1 packaging fixes

- Corrected all claim-evidence paths to their actual `evidence/...` locations.
- Finalized manuscript section mappings for the 36 authoritative claims.
- Replaced generic figure/table inventories with exact manuscript Fig. 1-5 and Table I-VI maps.
- Added the final manuscript figure assets, including the corrected Fig. 1 architecture.
- Removed unfinished citation/license placeholders from the reviewer package.
- Regenerated the file manifest and SHA-256 checksums.
