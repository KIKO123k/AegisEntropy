# Memory

> Chronological action log. Hooks and AI append to this file automatically.
> Old sessions are consolidated by the daemon weekly.

| 22:55 | Project health check: found unresolved merge conflicts in all 5 src scripts (repo mid-merge), missing data/ dir, logged bug-001/bug-002 | src/*.py, .wolf/buglog.json, .wolf/cerebrum.md | check complete, fixes not applied (report-only) | ~9k |
| 23:01 | Created data/ dir, downloaded CICIDS2017 PortScan CSV (73MB) from HF mirror c01dsnap/CIC-IDS2017, verified 286,467 rows + all 9 FEATURES present; added data/README.md; resolves bug-002 | data/*.csv, data/README.md, .wolf/anatomy.md | verified with pandas smoke test (py -3.14) | ~3k |
