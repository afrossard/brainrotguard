# Fork maintenance: merge-based ports from upstream

This repo is a personal fork of GHJJ123/brainrotguard, run on a home Kubernetes cluster; contributing back upstream is occasional at most.
Upstream changes are ported by an agent reviewing `main..upstream/main` and recording the result as a merge commit, keeping the fork's side for anything unwanted, so git itself tracks which upstream commits have been reviewed.
Cherry-picking was rejected because git cannot tell a skipped commit from an unreviewed one, so it would need a hand-kept ledger.

## Consequences

- Which project is upstream (GHJJ123/brainrotguard, or SirTerrific/tubetamer, which shares no git history with it) depends on the outcome of issue #1.
- The fork adopts the `container-base` conventions (Renovate, Conventional Commits, generated releases and changelog) and publishes its own image to GHCR only once it actually diverges with features of its own; until then it runs upstream as-is.
- Once those conventions are adopted, upstream's `CHANGELOG.md` and `version.py` changes are always dropped on port.
- Kubernetes manifests live in the cluster's GitOps repo, not here.
