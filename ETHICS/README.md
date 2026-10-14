# Ethics — NEOVIM_PRIOR_DOCS

**Project:** NEOVIM_PRIOR_DOCS  
**Category:** SOFTWARE_DEVELOPMENT  
**Upstream:** https://github.com/neovim/neovim  
**Pinned commit:** `09e4491a5351e37cea4ed83b163de315fedc2eaa`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `c4add498a2211df5c92d82dfdf9636346cdeca59d32aeb40519e6d7e85e94966`  
**Date:** October 2026

## Position

NEOVIM_PRIOR_DOCS is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
