<!-- markdownlint-disable -->

# Hardening Report: matrix-org--netlify-pr-preview/v2

> This file was generated automatically by the hardening agent.

**Policy SHA:** `d636be7e43ef829af6e853da6b3c7566db9f72fe`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `2`

Action **matrix-org--netlify-pr-preview/v2** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### unpinned-uses (severity: high)

A composite step in action.yml points to a mutable tag instead of a full 40-character commit SHA: `uses: matrix-org/pr-details-action@v1.3`. Whoever controls that tag can move it to different code. The other uses: references (bobheadxi/deployments and nwtgck/actions-netlify) are pinned to SHAs.

Locations:

- `action.yml:73`

## Iteration Notes

### Iteration 1

**Fixes applied:** unpinned-uses

**Notes:**

Pinned matrix-org/pr-details-action@v1.3 to 15bde5285d7850ba276cc3bd8a03733e3f24622a # v1.3 in action.yml.

