# Evidence ledger — MCO-001

Run id: `run-v0.1` · source: local synthetic generator · date: 2026-11-07

## PASS (executed in local Python runtime)

- 8 unit tests passed (`python -m unittest discover -s tests -v`).
- Deterministic synthetic generation: 36 calibration normals and 90 held-out episodes (36 normal, 54 scripted unsafe).
- Eight candidate and baseline monitors evaluated with causal-prefix tests.
- Canonical SHA-256 dataset/results verification and deterministic regeneration passed (`python -m mco verify`).
- Self-contained offline observatory generated from archived results.

## FAIL (evaluated scientific comparison)

- **EFMW-specific advantage over explicit-rule baseline not demonstrated**: rules detected 54/54 unsafe episodes, 0/36 normal alerts; EFMW candidate detected 12/54, with 4/36 normal alerts.
- Matched episode-level false-alert budget is **not achieved** by this design. Calibration quantiles are per-timestep, so equal-FP superiority interpretation is invalid.

## UNRESOLVED

- Lean 4 kernel build: not executed locally; toolchain unavailable.
- GitHub Actions CI: status not yet established; uploading a workflow is not a passing CI run.
- External replication or independent review: not performed.
- Confidence intervals, preregistered power calculation or superiority test: not performed.
- Generalization to natural failures; authenticated external outcome labels.
- Whether EFMW beats fair multiscale/spectral competitors on disjoint held-out data.
- EFMW-specific physical or human memory mechanism.
- Boardy pilot or commercial claims: not authorized or supported.

## Raw episode counts

| Monitor | TP / 54 | FP / 36 |
|--|--:|--:|
| last_error | 27 | 17 |
| signed_ewma | 12 | 7 |
| squared_ewma | 13 | 12 |
| cusum | 5 | 3 |
| multiscale_haar | 19 | 13 |
| multifeature | 26 | 15 |
| rules | 54 | 0 |
| efmw_candidate | 12 | 4 |

Full raw traces and hashes remain in the local MCO-001 package until uploaded. Do not claim their presence in this repository before confirming it.
