# Coherence-Lab — MCO-001

**Monolithic Coherence Observatory** is a reproducible synthetic benchmark for comparing an EFMW-inspired candidate monitor with conventional anomaly monitors and explicit safety rules in AI introduction-workflow histories.

**Research status:** exploratory synthetic prototype, not validation of EFMW physics, human memory mechanisms, production AI assurance, or commercial effectiveness.

## MCO-001 v0.1 results

| Monitor | Unsafe episodes detected (of 54) | Normal episodes alerted (of 36) |
|---|---:|---:|
| Explicit rules | 54 | 0 |
| Last error | 27 | 17 |
| Multifeature | 26 | 15 |
| Multiscale Haar | 19 | 13 |
| Squared EWMA | 13 | 12 |
| Signed EWMA | 12 | 7 |
| EFMW candidate | 12 | 4 |
| CUSUM | 5 | 3 |

All values originate from a locally executed synthetic run. The explicit-rule monitor has direct access to scripted safety flags and is not information-matched to residual-only monitors. Calibration targets **per-timestep** alerts, not equal episode-level false-alarm budgets. No EFMW-specific superiority is established.

## Verification boundaries

- **PASS (local):** Eight Python unit tests, deterministic synthetic generation and verification, offline snapshot generation.
- **FAIL (comparison):** EFMW candidate did not outperform explicit rules; matched episode-level false-alert comparisons are not achieved.
- **UNRESOLVED:** Lean kernel build, independent replication, real data, external review, human/physical mechanism, and commercial validity.

## Publication scope

This repository is being populated from the MCO-001 local research package. **Do not treat missing source/data files as verified online artifacts.** The frozen protocol and evidence ledger are included as separate records. Original full ZIP is available from the project author.

**Next experiment:** MCO-002 — equal information access, matched episode-level false-alarm budgets, independent holdouts and broader multiscale competing models.
