# Educators — NEOVIM_PRIOR_DOCS

**Project:** NEOVIM_PRIOR_DOCS  
**Category:** SOFTWARE_DEVELOPMENT  
**Upstream:** https://github.com/neovim/neovim  
**Pinned commit:** `09e4491a5351e37cea4ed83b163de315fedc2eaa`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `c4add498a2211df5c92d82dfdf9636346cdeca59d32aeb40519e6d7e85e94966`  
**Date:** October 2026

## Teaching with NEOVIM_PRIOR_DOCS

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `c4add498a2211df5c92d82dfdf9636346cdeca59d32aeb40519e6d7e85e94966` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
