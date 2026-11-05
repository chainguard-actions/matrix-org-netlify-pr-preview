<!-- markdownlint-disable -->

# Hardening Report: matrix-org--netlify-pr-preview/v1

> This file was generated automatically by the hardening agent.

**Policy SHA:** `d636be7e43ef829af6e853da6b3c7566db9f72fe`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `2`

Action **matrix-org--netlify-pr-preview/v1** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### unpinned-uses (severity: high)

action.yml references a third-party action by a version tag instead of a full 40-character commit hash: `uses: matrix-org/pr-details-action@v1.1`. Whoever controls that repository can move the tag to different code, and the next run would use it.

Locations:

- `action.yml:73`

## Iteration Notes

### Iteration 1

**Fixes applied:** unpinned-uses

**Notes:**

Pinned matrix-org/pr-details-action@v1.1 to c1e95d2ae187aa89460a5149e63daadc12f69974 (# v1.1) in action.yml. The other uses: references were already pinned.

