# Reseal log

Each entry records one authorized change to a sealed document and the reseal that
followed it. This file sits outside the seal: `MANIFEST.sha256` lists the seven
corpus documents only, so a new entry here never changes a sealed digest.

## 2026-10-04: README name change

- Authorized change: the README footer now names Zain Dana Harper in place of the
  retired Zentropy Labs name. Commit 33dab32, PR #5.
- Approval: the author approved this reseal in chat on 2026-10-04.
- Files whose digests changed: `README.md` only.
  - before: `71b4041eed8bf3e92af272f34dc7fb8292504ce631caefc583e264972042ccb0`
  - after: `c4ef6c251dc020267b888a9f5370c5c82bfc566d9447673cbe932b966dcf434b`
- The other six digests are unchanged.
- `MANIFEST.sha256` before: `dfb35d29120a5eeeae186a58d67425c5cb2ea296ef4df8511ef65e63f15ca0c4`
- `MANIFEST.sha256` after: `6ac30dc76624162b9b4af64b4818a08ebfd68bbf14dcb82a687e7027fd7c1419`
- Method: the new digest is SHA-256 over the committed LF blob of `README.md`, the
  same procedure as the 2026-09-03 reseal in PR #4. `python verify_manifest.py`
  prints `MATCH` after the reseal.
