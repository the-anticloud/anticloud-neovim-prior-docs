# Students — NEOVIM_PRIOR_DOCS

**Project:** NEOVIM_PRIOR_DOCS  
**Category:** SOFTWARE_DEVELOPMENT  
**Upstream:** https://github.com/neovim/neovim  
**Pinned commit:** `09e4491a5351e37cea4ed83b163de315fedc2eaa`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `c4add498a2211df5c92d82dfdf9636346cdeca59d32aeb40519e6d7e85e94966`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `09e4491a5351e37cea4ed83b163de315fedc2eaa`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `c4add498a2211df5c92d82dfdf9636346cdeca59d32aeb40519e6d7e85e94966`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
