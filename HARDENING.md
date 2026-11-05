<!-- markdownlint-disable -->

# Hardening Report: matrix-org--netlify-pr-preview/v3

> This file was generated automatically by the hardening agent.

**Policy SHA:** `d636be7e43ef829af6e853da6b3c7566db9f72fe`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `2`

Action **matrix-org--netlify-pr-preview/v3** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### unpinned-uses (severity: high)

action.yml refers to an action by a version tag instead of a full 40-character commit SHA: `uses: matrix-org/pr-details-action@v1.3`. A tag can be moved to point at different code, which is a supply-chain risk. Pin it to the commit SHA, with the tag as a trailing comment.

Locations:

- `action.yml:73`

## Iteration Notes

### Iteration 1

**Fixes applied:** unpinned-uses

**Notes:**

Pinned matrix-org/pr-details-action@v1.3 to 15bde5285d7850ba276cc3bd8a03733e3f24622a (# v1.3) in action.yml. Other uses were already SHA-pinned.

